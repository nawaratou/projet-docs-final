# Git Learning 3

 Exercice 3 – Gestion des conflits durant le merging
Objectifs :
Créer une branche de test pour simuler un conflit
Modifier un fichier depuis main et depuis la branche de test
Résoudre le conflit manuellement

Étapes détaillées :
Créer et cloner le dépôt git-learning-3 :

gh repo create git-learning-3 --public --clone
cd git-learning-3
Ajouter le remote vue que le depot est déjà créer :
git remote add origin https://github.com/nawaratou/git-learning-3.git
Créer le fichier notes.txt sur main :

echo "Ligne écrite depuis la branche main" > notes.txt
git add notes.txt
git commit -m "Ajout du fichier notes.txt sur la branche main"
git push -u origin main
Créer une branche conflict-test et modifier notes.txt :
git checkout -b conflict-test
echo "Ligne écrite depuis la branche conflict-test" >> notes.txt
git commit -am "Modification de notes.txt depuis conflict-test"
git push -u origin conflict-test
Retour sur main et modifier notes.txt différemment :

git checkout main
echo "Ligne écrite depuis la branche main pour la seconde fois" >> notes.txt
git commit -am "Modification de notes.txt depuis main"
git push
Tenter de merger conflict-test dans main (conflit attendu) :

git merge conflict-test
Résoudre le conflit manuellement dans notes.txt, puis :
git add notes.txt
git commit -m "Résolution du conflit, conservation des deux lignes"
git push
Résultat attendu :

notes.txt contient les deux lignes issues des branches main et conflict-test
Historique reflète le conflit et sa résolution.
