## Mises à jour difficiles

- synchronisation des branches multiples avec la branche de référence
- intégration de fix aux premières branches

                          `subfeature2`
                                ▲
           `subfeature1` ───────┘
                 ▲
`develop` ───────┘

=> Comment éviter de rebaser chaque branche 1 à 1 ?

Nouveauté [git 2.38](https://github.blog/open-source/git/highlights-from-git-2-38/#rebase-dependent-branches-with-update-refs) (octobre 2022) : option `--update-refs`
