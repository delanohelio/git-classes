# Aula 03 — Repositório local: init, status, add, commit

Objetivos
- Diferenciar working directory, staging area e repositório.
- Executar o ciclo básico: editar → `git add` → `git commit`.
- Escrever mensagens de commit úteis.

Imagens
- ![Ciclo de vida](../assets/working-staging-repo.svg)
- ![Anatomia do commit](../assets/commit-anatomy.svg)

Teoria rápida
- Working directory: seus arquivos “soltos”.
- Staging area: o que será incluído no próximo commit.
- Repositório: histórico oficial (commits).
- Mensagens de commit:
  - Primeira linha curta (<= 72 chars), imperativo: “feat: adiciona…”
  - Corpo opcional com motivação/contexto.

Prática guiada
```bash
# partindo de meu-projeto
echo "<h1>Home</h1>" > index.html
git status

# adiciona ao stage e commita
git add index.html
git commit -m "feat: adiciona página inicial"

# adiciona múltiplos arquivos
echo "body { font-family: system-ui }" > styles.css
echo "console.log('Olá');" > app.js
git add .
git commit -m "chore: adiciona assets iniciais (css/js)"

git log --oneline --decorate --graph
```

Exercícios
1) Altere `app.js` para imprimir seu nome e faça um commit com mensagem clara.
2) Crie um arquivo `about.html`, adicione apenas ele ao stage com `git add about.html` e faça commit.

Desafio
- Crie um commit com corpo multi-linha:
```bash
git commit -m "feat: seção Sobre" -m "Cria pagina about.html com layout mínimo e link no header."
```

Checklist de saída
- Você sabe quando algo está modificado, staged ou commitado.