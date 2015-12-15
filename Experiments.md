# Esperimenti #

Sono stati effettuati alcuni esperimenti per testare il funzionamento dei vari classificatori in diverse condizioni.

**Test dei classificatori con rimozione dei termini utilizzati una sola volta, selezione di soli 150 termini ed utilizzo delle emoticons**

**Naive Bayes:**
```
Correctly Classified Instances         133               72.6776 %
Incorrectly Classified Instances        50               27.3224 %
Kappa statistic                          0.4305
Mean absolute error                      0.3156
Root mean squared error                  0.4154
Relative absolute error                 63.1123 %
Root relative squared error             83.0785 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 48 27 |  a = 0
 23 85 |  b = 4
```

**J48:**
```
Correctly Classified Instances         117               63.9344 %
Incorrectly Classified Instances        66               36.0656 %
Kappa statistic                          0.3132
Mean absolute error                      0.3758
Root mean squared error                  0.4941
Relative absolute error                 75.1541 %
Root relative squared error             98.8168 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 63 12 |  a = 0
 54 54 |  b = 4
```

**`MultiLayerPerceptron:`**
```
Correctly Classified Instances         112               61.2022 %
Incorrectly Classified Instances        71               38.7978 %
Kappa statistic                          0.2814
Mean absolute error                      0.3495
Root mean squared error                  0.49  
Relative absolute error                 69.9098 %
Root relative squared error             98.0052 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 68  7 |  a = 0
 64 44 |  b = 4
```

**WLSVM:**
```
Correctly Classified Instances         122               66.6667 %
Incorrectly Classified Instances        61               33.3333 %
Kappa statistic                          0.3392
Mean absolute error                      0.3333
Root mean squared error                  0.5774
Relative absolute error                 66.6667 %
Root relative squared error            115.4701 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 55 20 |  a = 0
 41 67 |  b = 4
```

**`VotedPerceptron:`**
```
Correctly Classified Instances         125               68.306  %
Incorrectly Classified Instances        58               31.694  %
Kappa statistic                          0.3604
Mean absolute error                      0.3169
Root mean squared error                  0.563 
Relative absolute error                 63.388  %
Root relative squared error            112.5948 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 52 23 |  a = 0
 35 73 |  b = 4
```

**Test dei classificatori con rimozione dei termini utilizzati una sola volta, selezione di soli 200 termini ed utilizzo delle emoticons**

**Naive Bayes:**
```
Correctly Classified Instances         143               78.1421 %
Incorrectly Classified Instances        40               21.8579 %
Kappa statistic                          0.5444
Mean absolute error                      0.3002
Root mean squared error                  0.4043
Relative absolute error                 60.0435 %
Root relative squared error             80.8534 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 53 22 |  a = 0
 18 90 |  b = 4
```

**J48:**
```
Correctly Classified Instances         122               66.6667 %
Incorrectly Classified Instances        61               33.3333 %
Kappa statistic                          0.3095
Mean absolute error                      0.3605
Root mean squared error                  0.4929
Relative absolute error                 72.1024 %
Root relative squared error             98.581  %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 44 31 |  a = 0
 30 78 |  b = 4
```

**`MultiLayerPerceptron:`**
```
Correctly Classified Instances         105               57.377  %
Incorrectly Classified Instances        78               42.623  %
Kappa statistic                          0.2343
Mean absolute error                      0.4293
Root mean squared error                  0.6458
Relative absolute error                 85.8515 %
Root relative squared error            129.1657 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 73  2 |  a = 0
 76 32 |  b = 4
```

**WLSVM:**
```
Correctly Classified Instances         123               67.2131 %
Incorrectly Classified Instances        60               32.7869 %
Kappa statistic                          0.3436
Mean absolute error                      0.3279
Root mean squared error                  0.5726
Relative absolute error                 65.5738 %
Root relative squared error            114.5197 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 53 22 |  a = 0
 38 70 |  b = 4
```

**`Voted Perceptron:`**
```
Correctly Classified Instances         119               65.0273 %
Incorrectly Classified Instances        64               34.9727 %
Kappa statistic                          0.308 
Mean absolute error                      0.3497
Root mean squared error                  0.5914
Relative absolute error                 69.9454 %
Root relative squared error            118.2754 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 54 21 |  a = 0
 43 65 |  b = 4
```

**Test dei classificatori con rimozione dei termini utilizzati una sola volta, selezione di soli 200 termini senza utilizzo delle emoticons**

**Naive Bayes:**
```
Correctly Classified Instances         131               71.5847 %
Incorrectly Classified Instances        52               28.4153 %
Kappa statistic                          0.4197
Mean absolute error                      0.3578
Root mean squared error                  0.4401
Relative absolute error                 71.5536 %
Root relative squared error             88.0128 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 52 23 |  a = 0
 29 79 |  b = 4
```

**`MultiLayerPerceptron:`**
```
Correctly Classified Instances         134               73.224  %
Incorrectly Classified Instances        49               26.776  %
Kappa statistic                          0.4431
Mean absolute error                      0.3732
Root mean squared error                  0.447 
Relative absolute error                 74.64   %
Root relative squared error             89.402  %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 49 26 |  a = 0
 23 85 |  b = 4
```

**WLSVM:**
```
Correctly Classified Instances         134               73.224  %
Incorrectly Classified Instances        49               26.776  %
Kappa statistic                          0.4338
Mean absolute error                      0.2678
Root mean squared error                  0.5175
Relative absolute error                 53.5519 %
Root relative squared error            103.491  %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 45 30 |  a = 0
 19 89 |  b = 4
```

**`Voted Perceptron:`**
```
Correctly Classified Instances         130               71.0383 %
Incorrectly Classified Instances        53               28.9617 %
Kappa statistic                          0.4049
Mean absolute error                      0.2896
Root mean squared error                  0.5382
Relative absolute error                 57.9235 %
Root relative squared error            107.6322 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 50 25 |  a = 0
 28 80 |  b = 4
```

Il classificatore J48 con questi parametri restituisce un errore di memoria insufficiente.

**Test dei classificatori con rimozione dei termini utilizzati una sola volta, selezione di soli 150 termini con utilizzo delle emoticons**

**Naive Bayes:**
```
Correctly Classified Instances         120               65.5738 %
Incorrectly Classified Instances        63               34.4262 %
Kappa statistic                          0.3039
Mean absolute error                      0.3748
Root mean squared error                  0.4508
Relative absolute error                 74.952  %
Root relative squared error             90.1563 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 49 26 |  a = 0
 37 71 |  b = 4
```

**`MultiLayerPerceptron:`**
```
Correctly Classified Instances         132               72.1311 %
Incorrectly Classified Instances        51               27.8689 %
Kappa statistic                          0.393 
Mean absolute error                      0.3848
Root mean squared error                  0.4425
Relative absolute error                 76.9534 %
Root relative squared error             88.4924 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 37 38 |  a = 0
 13 95 |  b = 4
```

**WLSVM:**
```
Correctly Classified Instances         130               71.0383 %
Incorrectly Classified Instances        53               28.9617 %
Kappa statistic                          0.3824
Mean absolute error                      0.2896
Root mean squared error                  0.5382
Relative absolute error                 57.9235 %
Root relative squared error            107.6322 %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 41 34 |  a = 0
 19 89 |  b = 4
```

**`Voted Perceptron:`**
```
Correctly Classified Instances         126               68.8525 %
Incorrectly Classified Instances        57               31.1475 %
Kappa statistic                          0.36  
Mean absolute error                      0.3115
Root mean squared error                  0.5581
Relative absolute error                 62.2951 %
Root relative squared error            111.62   %
Total Number of Instances              183     

=== Confusion Matrix ===

  a  b   <-- classified as
 48 27 |  a = 0
 30 78 |  b = 4
```

Il classificatore J48 con questi parametri restituisce un errore di memoria insufficiente.