# Introduzione #
In questo progetto viene presentata un'applicazione che permette di effettuare sentiment analysis su Twitter utilizzando tecniche di machine learning. Sono stati utilizzati classificatori presenti nella libreria Weka.
L'applicazione può essere utilizzata tramite linea di comando o tramite API consultabili attraverso la documentazione Javadoc.

# Utilizzo tramite linea di comando #

Lista di comandi e loro significato:

**prepareTrain:**
Costruisce le strutture dati necessarie per l'addestramento del classificatore tra cui un file contenente i termini utilizzati suddivisi per tweet. E' possibile inoltre inserire due parametri opzionali:
"-sf": elimina i termini utilizzati una sola volta
"-re": elimina le emoticons non considerandole quindi durante l'addestramento del classificatore.

**construct `<nome-classificatore>`:**
costruisce e addestra il classificatore Weka specificato nel parametro.
E' possibile inserire un ulteriore parametro opzionale indicante il numero di termini totali da selezionare per l'addestramento.
Il nome del classificatore da inserire deve coincidere con il nome della classe che lo rappresenta nella libreria Weka (per il classificatore Naive Bayes ad esempio il nome sarà `weka.classifiers.bayes.NaiveBayes`).
Il classificatore costruito viene memorizzato su disco.

**weightedMajority `<nomi-classificatori>`:**
costruisce un classificatore weighted majority utilizzando i classificatori specificati come parametri. Permette inoltre di inserire dei tweet da classificare in modo interattivo.

**evaluateWm:**
Valuta il classificatore weighted majority tramite un insieme di tweets di test.

# Utilizzo tramite API #

**Esempio di costruzione ed uso di un classificatore:**
Gli oggetti principali da utilizzare sono `"ClassifierBuilder"` e `"Options"`. Il primo si occupa della costruzione e dell'addestramento del classificatore mentre il secondo è responsabile della gestione delle varie opzioni del classificatore. Quest'ultimo è rappresentato da un'oggetto `"WekaClassifier"`.

```
ClassifierBuilder clb = new ClassifierBuilder();
Options opt = new Options();
clb.setOpt(opt);
//seleziona solo i termini utilizzati più di una volta
opt.setSelectedFeaturesByFrequency(true);
//seleziona solamente 150 termini
opt.setNumFeatures(150);
//rimuove le emoticons
opt.setRemoveEmoticons(true);
//prepara le strutture dati per il train e il test
clb.prepareTrain();
clb.prepareTest();
//classificatore Weka
NaiveBayes nb = new NaiveBayes();
//costruzione e memorizzazione su disco del classificatore
WekaClassifier wc = clb.constructClassifier(nb);
//classificazione di un tweet
wc.classify("i am very sad");
```

**Esempio di costruzione ed utilizzo di un classificatore weighted majority a partire da classificatori già costruiti:**
Per costruire un classificatore weighted majority  è necessario creare un oggetto `"WeightedMajority"`, costruito attraverso una lista di classificatori già addestrati. Un oggetto `"Item"` rappresenta un tweet; esso memorizza sia la sua classificazione reale, sia quella datagli dal classificatore.
```
List<IClassifier> classifiers = new LinkedList<IClassifier>();
ClassifierBuilder cb = new ClassifierBuilder();
//prende tre classificatori già costruiti
WekaClassifier wc1 = cb.retrieveClassifier("weka.classifiers.bayes.NaiveBayes");
WekaClassifier wc2 = cb.retrieveClassifier("weka.classifiers.trees.J48");
WekaClassifier wc3 = cb.retrieveClassifier("weka.classifiers.functions.VotedPerceptron");
classifiers.add(wc1);
classifiers.add(wc2);
classifiers.add(wc3);
WeightedMajority wm  = new WeightedMajority(classifiers);
//costruisce e classifica un tweet
Item item = wm.weightedClassify("i am very sad");
//stampa la classificazione data al tweet dal classificatore
System.out.println(item.getPolarity());
//imposta la classificazione reale del tweet
item.setTarget("4");
//comunica al classificatore weighted majority la polarità esatta del tweet
wm.setTarget(item);
System.out.println(wm.get_cl2weight().get(1) + " " + wm.get_cl2weight().get(2) + " " + wm.get_cl2weight().get(3));
```