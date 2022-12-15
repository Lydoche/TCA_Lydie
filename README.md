# TCA_Lydie

Step 1:

1(TCA)_load_data.ipynb file :

> Load phenotypes and brain CT, SA, VOL 

> Merge AN and Autism datasets

> Filter on magnetic field strenght and age

>> Export 'df_tsa_tca.csv' file

Step 2:

3(V)_run_BLR-VOL.ipynb

> / ! \ Use 'df_tsa_tca_NM.csv' issued by Step 1

> Defines model to run normative modelling

> Run BLR

> Predict Z-Scores on AN/ASD/TD

>> Export file with Z-Scores


Analyses:

* CLUSTERING : 7_Clustering.ipynb

> Load file with Z-Scores issued in Step 2

> Perform clustering on Autism Z-Scores

> Analyse clinical scores across clusters

> Compute correlation with AN Z-Scores

* Prediction : 9_SVM.ipynb

> Perform Multiclass prediction (leave-one-out)

> Perform Binary classification

* Shuffle labels in AN / TD to assess ENIGMA correlation : Bootstrap_cor_enigma.ipynb

> Load ENIGMA beta values and 'df_tsa_tca.csv' issued in Step 1

> Shuffle labels 500x

> Plot correlation distribution

