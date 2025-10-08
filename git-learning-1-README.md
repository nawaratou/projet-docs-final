# Git Learning 1
Exercice 1 – First Repo & Simple Commit

**Objectifs :**  
- Créer un dépôt GitHub  
- Cloner le dépôt localement  
- Ajouter des fichiers, les committer et les pousser sur GitHub  
- Vérifier l’historique des commits

**Étapes détaillées :**  

1. **Créer le dépôt sur GitHub et le cloner :

gh repo create git-learning-1 --public --clone

Se déplacer dans le dossier cloné :
cd git-learning-1
Créer le fichier README.md et y écrire du texte :
echo "Mon premier projet Git" > README.md
Ajouter une ligne avec ton nom et numéro de Mac :
echo "Nom : Nawaratou, Mac : 17" >> README.md
Ajouter le fichier à l’index de Git :
git add README.md
Créer un commit pour enregistrer les modifications :
git commit -m "Ajout du README avec nom et Mac"
Envoyer les changements sur GitHub :
git push origin main
Résultat attendu :
Fichier README.md sur GitHub avec texte et informations personnelles
Historique de commits reflétant chaque étape
