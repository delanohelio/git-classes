# Aula 06 — Restaurando mudanças: restore

Objetivos
- Desfazer mudanças no working directory e tirar arquivo do stage.
- Entender quando usar `restore` em vez de `reset`.

Imagens
- ![Restore](../assets/restore.svg)
- ![Matriz de desfazer](../assets/undo-matrix.svg)

Teoria rápida
- `git restore arquivo` descarta alterações não commitadas do working dir.
- `git restore --staged arquivo` retira do stage, mantendo alterações no working dir.

Prática guiada
```bash
# sujar arquivo
echo "<footer>2025</footer>" >> index.html
git status

# descartar alterações do working dir
git restore index.html

# simular adição ao stage e remoção do stage
echo "<footer>2025</footer>" >> index.html
git add index.html
git restore --staged index.html      # sai do stage, mas mantém mudanças
git status

# versão antiga do comando (ainda funciona)
git checkout -- index.html
```

Exercícios
1) Crie alterações em `styles.css`, adicione ao stage e depois remova do stage.
2) Descarte completamente as alterações feitas em `styles.css` (sem commit).

Checklist de saída
- Você diferencia descartar mudanças e apenas retirar do stage.