# Aula 04 — .gitignore e arquivos gerados

Objetivos
- Usar `.gitignore` para evitar versionar build, dependências e segredos.
- Aplicar `.gitignore` a arquivos já rastreados (untrack).

Imagens
- ![Gitignore](../assets/gitignore.svg)
- ![Padrões de Gitignore](../assets/gitignore-patterns.svg)

Teoria rápida
- `.gitignore` evita que arquivos apareçam em `git status` como não rastreados.
- Padrões:
  - `pasta/` ignora pasta inteira
  - `*.log` ignora logs
  - `!arquivo.txt` nega o ignore (força incluir)

Prática guiada
```bash
# criar e popular .gitignore
cat > .gitignore <<'EOF'
node_modules/
dist/
build/
.env
*.log
.DS_Store
EOF

git add .gitignore
git commit -m "chore: adiciona .gitignore padrão"

# se já tinham arquivos rastreados, remover do index (manter no disco)
git rm -r --cached node_modules/ dist/ build/ 2>/dev/null || true
git commit -m "chore: remove arquivos gerados do versionamento"
```

Exercícios
1) Crie um `.env` com `API_KEY=123` e confirme que não aparece em `git status`.
2) Crie um `error.log` e confirme que é ignorado.

Dica
- Modelos por linguagem: https://github.com/github/gitignore

Checklist de saída
- Você sabe criar e ajustar um `.gitignore` e “desversionar” arquivos gerados.