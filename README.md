# PyGoodVibes
**détection non supervisée de sons anormaux**
Réalisé par Chrisophe Gauffre et Aurélien Nanette

contact linkedin: [/christophegauffre](https://www.linkedin.com/in/christophegauffre)  [/a-nanette](https://www.linkedin.com/in/a-nanette)


# A propos
Ce projet vous propose l'exécution d'un app streamlit, vous permettant de comprendre comment traiter des données audio, et détecter des anomalies dans des sons de machine.
Les données sont issues de [Kaggle](https://www.kaggle.com/daisukelab/dc2020task2).

![image](https://user-images.githubusercontent.com/53881073/135213653-a90129a9-79cf-4717-8982-e143bfda212e.png)

Tous les détails ne sont pas forcément décrits dans l'appli, mais vous pourrez saisir la philosophie du traitement de données effectué:
1. **transformation des sons** audio en représentation temps-fréquence (spectrogrammes)
![image](https://user-images.githubusercontent.com/53881073/135142159-bee72160-e159-488a-aea6-484ce0f8ca0b.png)
1. **encodage des spectrogrammes**: _embedding_, et _ACP_ pour générer de beaux nuages de points de sons normaux.
![image](https://user-images.githubusercontent.com/53881073/135142090-7497b3ad-4b5a-423d-8cba-a5564c11a375.png)
1. **détection d'anomalies** dans les nuages de points comportant des sons normaux et des sons anormaux par _One Class SVM_ et _Local Outlier Factor_
![reglage-gamma-OSVM3](https://user-images.githubusercontent.com/53881073/135214068-33794be5-c10a-49c1-886b-df8a369df08f.png)

# Utilisation
Pour que ce notebook soit pleinement opérationnel, une utilisation avec colab et google drive est vivement conseillée.
- à la racine de votre drive, créez un dossier Kaggle dans lequel vous déposez votre fichier json de crédential Kaggle (rdv dans votre compte kaggle pour le générer). Ceci permettra de télécharger facilement le dataset depuis Kaggle grâce à l'API Kaggle
- téléchargez tous les fichiers et dossiers de ce git dans un dossier de votre drive
- ouvrez le notebook **pyGoodVibes-streamlit-final.ipynb** dans google colab
- exécuter chaque cellule, **_sauf  la dernière!_** (elle kilel le tunnel ngrok du streamlit, et rendra le streamlit inopérationnel! ) 

# Résultats
Selon les types de machine, les résultats varient de très bons (quasi 100% sans faux positifs) à très mauvais (quasi du hasard on dirait..), selon le seuil de sensibilité réglé sur l'app. es résultats sont sensiblement les mêmes entre le OcSVM ou le LOF

![image](https://user-images.githubusercontent.com/53881073/135142241-8f6305d4-080c-41ee-9784-19846fde7378.png)

**Lancez le streamlit, cela vous donnera un bon aperçu de ce qu'il est possible de faire!**
