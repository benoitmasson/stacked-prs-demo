# Pull Requests incrémentales – _a.k.a. Stacked Pull Requests_

[Benoît Masson](linkedin) - OVHcloud (Noms de domaines)

## Introduction

**Principe** : découper les PRs trop longues

**Avantages** :

- relecture par morceaux
- potentiellement dans le désordre

**Comment faire** :

- utiliser des branches distinctes pour chaque sous-fonctionnalité atomique

**Difficulté** :

- synchronisation des branches multiples avec la branche de référence

=> Comment éviter de rebaser chaque branche 1 à 1 ?

Nouveauté [git 2.38](https://github.blog/open-source/git/highlights-from-git-2-38/#rebase-dependent-branches-with-update-refs) (octobre 2022) : option `--update-refs`
