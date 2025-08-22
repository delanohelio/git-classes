# Aula 15 — Reflog e recuperação

Objetivos
- Usar `git reflog` para encontrar referências “perdidas”.
- Recuperar um commit criando uma branch a partir do reflog.

Imagens
- ![Reflog](../assets/reflog.svg)
- ![Fluxo de recuperação](../assets/recovery-flow.svg)

Teoria rápida
- Reflog registra movimentos de HEAD/branches localmente (não é compartilhado).
- Útil para desfazer resets ou achar commits “órfãos”.

Prática guiada
```bash
git reflog
# pegue um hash mostrado no reflog e crie uma branch de resgate
git checkout -b rescue/<data> <hash>
git log --oneline --decorate
```

Exercícios
1) Faça um `reset --hard`, identifique o commit no `reflog` e recupere numa nova branch.
2) Use `git cherry-pick <hash>` para trazer apenas um commit desejado para a `main`.

Checklist de saída
- Você consegue recuperar trabalho usando o reflog.