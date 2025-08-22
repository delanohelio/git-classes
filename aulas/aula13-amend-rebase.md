# Aula 13 — Amend e rebase básico

Objetivos
- Corrigir o último commit com `--amend`.
- Usar rebase interativo para limpar o histórico local.
- Entender riscos de reescrever histórico já publicado.

Imagens
- ![Rebase vs Merge](../assets/rebase-vs-merge.svg)
- ![Fluxo de amend](../assets/amend-flow.svg)

Teoria rápida
- `git commit --amend` altera a mensagem e/ou conteúdo do último commit.
- `git rebase -i` permite reordenar, unir (squash), renomear (reword) commits.
- Evite reescrever histórico já pushado para branches compartilhadas.

Prática guiada
```bash
# corrigir último commit
echo "<meta name=\"viewport\" content=\"width=device-width\">" >> index.html
git add index.html
git commit --amend -m "feat: adiciona meta viewport à home"

# rebase interativo nos últimos 3 commits
git rebase -i HEAD~3
# na tela interativa: use pick/squash/reword conforme desejado
git log --oneline
```

Exercícios
1) Crie 3 commits pequenos e use `rebase -i` para condensar em 1.
2) Altere a mensagem do commit final com `reword`.

Checklist de saída
- Você sabe ajustar o último commit e organizar histórico local.