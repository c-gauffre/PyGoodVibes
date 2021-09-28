# PyGoodVibes
détection non supervisée de sons anormaux

# A propos
Ce projet vous propose l'exécution d'un app streamlit, vous permettant de comprendre comment traiter des données audio, et détecter des anomalies dans des sons de machine.
Les données sont issues de [Kaggle](https://www.kaggle.com/daisukelab/dc2020task2).

Tous les détails ne sont pas mentionnés, mais vous pourrez saisir la philosophie du traitement de données effectué:
- transformation des sons audio en représentation temps-fréquence (spectrogrammes)
- encodage des spectrogrammes: _embedding_, et _ACP_ pour générer de beaux nuages de points de sons normaux.
- recherche d'anomalies dans les nuages de points comportant des sons normaux et des sons anormaux par _One Class SVM_ et _Local Outlier Factor_

# Utilisation
Pour que ce notebook soit pleinement opérationnel, une utilisation avec colab et google drive est vivement conseillée.
- à la racine de votre drive, créez un dossier Kaggle dans lequel vous déposez votre fichier json de crédential Kaggle (rdv dans votre compte kaggle pour le générer). Ceci permettra de télécharger le dataset depuis Kaggle grâce à l'API Kaggle
- téléchargez tous les fichiers et dossiers de ce git dans un dossier de votre drive
- ouvrez le notebook ** ** dans google colab
- exécuter chaque cellule, _sauf  la dernière!_ (elle kill le tunnel et rendra le streamlit inopérationnel! ) 

# Résultats
Selon les types de machine, les résultats varient de très bons (quasi 100% sans faux positifs) à très mauvais (quasi du hasard on dirait..)

**Lancez le streamlit, cela vous donnera un bon aperçu de ce qu'il est possible de faire!**
