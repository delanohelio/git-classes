# Aula 07 — Branches: criar e navegar

Objetivos
- Entender branches como ponteiros para commits.
- Criar, listar e alternar entre branches.

Imagens
- ![Branches básico](../assets/branch-basics.svg)
- ![HEAD e ponteiros](../assets/head-and-pointers.svg)

Teoria rápida
- Branch é um nome apontando para um commit. HEAD aponta para sua branch atual.
- Criar branches permite desenvolver recursos isoladamente.

Prática guiada
```bash
git branch                    # lista branches
git switch -c feature/cabecalho
echo "<header>Site</header>" >> index.html
git add index.html
git commit -m "feat: cabeçalho inicial"

git switch main
git branch --all
git log --oneline --graph --decorate --all
```

Exercícios
1) Crie uma branch `feature/menu` e acrescente um menu simples em `index.html`.
2) Volte para `main` e confirme que as mudanças da branch não aparecem na `main`.

Checklist de saída
- Você consegue criar uma branch e voltar para a `main`.