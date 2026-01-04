## Conclusion

Utilisation systématique de (presque) toutes les options en même temps :

```ini
[alias]
r = rebase --interactive --update-refs --autosquash
```

ou

```ini
[rebase]
updateRefs = true
autoSquash = true
```

Il faut rebaser tout le temps, quel que soit le protocole retenu !

- minimisation des conflits
- résolution au plus tôt
