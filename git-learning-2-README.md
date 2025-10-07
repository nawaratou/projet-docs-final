# Git Learning 2
Exercice 2 – Branching & Merging
Objectifs :

Créer une nouvelle branche
Effectuer des modifications sur cette branche
Créer une Pull Request (PR) vers main
Fusionner la PR
Étapes détaillées :

Créer et cloner le dépôt git-learning-2 :
gh repo create git-learning-2 --public --clone
cd git-learning-2
Créer une branche myself :

git checkout -b myself
Créer un fichier about.txt avec tes infos :

echo "Nom: Ousseini, Prénom: Hama, Lieu de naissance: Niamey" > about.txt
Ajouter et committer le fichier :

git add about.txt
git commit -m "Ajout du fichier about.txt sur la branche myself"
Pousser la branche sur GitHub :
git push -u origin myself
Créer une Pull Request (PR) vers main :

gh pr create --title "Ajout about.txt" --body "Pull request de myself vers main" --base main --head myself
Fusionner la PR sur GitHub ou via CLI :
gh pr merge --merge

Résultat attendu :
Le fichier about.txt est maintenant sur la branche main
Historique de commits reflétant la création de la branche, les changements et la fusion
