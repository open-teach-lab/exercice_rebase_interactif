# Exercice Rebase Interactif

L'objectif est d'utiliser la commande `rebase` de manière interactive pour nettoyer l'historique de ce dépôt.

## Instructions

- Cloner le projet
- Utiliser la commande `git rebase -i --root` pour démarrer un rebase interactif depuis le premier commit
- Utiliser les commandes interactives et changer l'ordre des lignes pour atteindre le résultat attendu.

Vous pouvez effectuer plusieurs rebase si nécéssaire.

## Résultat attendu

Chaque commit ne doit porter que sur un seul fichier (à vérifier avec `git show cac51b8` où `cac51b8` serait le hash du commit).

L'ordre et les messages de commit sont importants.

L'historique final doit ressembler à :

```
6c2563c feat: voiture.yaml
45a1738 feat: societe.yaml
cdf3be4 feat: contact.yaml
deb8555 chore: .gitkeep logs
314cc6d chore: .gitignore
ed53fa5 feat: enoncé de l'exercice
61f4adb chore: commit initial
```

## Aide

- Pour split un commit en plusieurs commits pendant le rebase: arrêtez-vous en mode édition dessus, puis utilisez `git reset HEAD~1` afin de l'annuler. Les modifications étant maintenant dans votre copie de travail, vous pouvez les commiter séparément, puis reprendre le rebase.
