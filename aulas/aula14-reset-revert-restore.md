# Aula 14 — Reset vs Revert vs Restore

Objetivos
- Diferenciar `reset`, `revert` e `restore`.
- Escolher a ferramenta certa para cada cenário.

Imagens
- ![Reset e Revert](../assets/reset-revert.svg)
- ![Modos de reset](../assets/reset-modes.svg)

Teoria rápida
- `restore`: desfaz working dir ou staging (sem mexer em commits).
- `reset`: move ponteiros (HEAD/branch) para outro commit.
  - `--soft` mantém stage e working
  - `--mixed` limpa stage; mantém working (padrão)
  - `--hard` descarta tudo até aquele commit
- `revert`: cria um novo commit que desfaz outro (seguro para histórico público).

Prática guiada
```bash
# simule um commit "ruim"
echo "<div>Quebra layout</div>" >> index.html
git add index.html && git commit -m "feat: mexe no layout (ruim)"

# revert seguro
git revert HEAD                      # abre editor para mensagem
git log --oneline

# reset local (antes do push)
git reset --soft HEAD~1              # volta um commit, mantendo no stage
git reset --mixed HEAD~1             # volta e limpa stage
# CUIDADO:
# git reset --hard HEAD~1            # descarta de vez
```

Exercícios
1) Faça `revert` de um commit específico pelo hash.
2) Teste `reset --mixed` e reavalie o status.

Checklist de saída
- Você sabe quando usar `revert` vs `reset` vs `restore`.