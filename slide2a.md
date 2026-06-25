## Ma recommandation

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

## Et dans mon IDE ?

- **VS Code** via git-lens, depuis [décembre 2025](https://github.com/gitkraken/vscode-gitlens/issues/2387)
- **IntelliJ** depuis [août 2025](https://www.jetbrains.com/help/idea/2025.2/apply-changes-from-one-branch-to-another.html#rebase-branch)
