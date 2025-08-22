# Git Classes — Introdução a Git

Material para um minicurso de Git voltado a adolescentes do Ensino Médio Integrado de Programação para Internet. Curso prático, com exercícios guiados, imagens e desafios.

## Objetivos de aprendizagem
- Entender o que é controle de versão e por que usar Git.
- Praticar o ciclo: working directory → staging area → repositório (commit).
- Navegar e inspecionar histórico (log, show, diff).
- Criar branches, fazer merge, rebase e resolver conflitos.
- Conectar a repositórios remotos (GitHub) e colaborar via Pull Requests.
- Aplicar boas práticas de mensagens, tags, fluxo de trabalho e proteção de branches.
- Recuperar trabalhos perdidos com reflog, reset, restore e revert.

## Pré-requisitos
- Git instalado (Windows/macOS/Linux)
- Conta no GitHub
- Editor de código (VS Code recomendado)
- Terminal (PowerShell, Terminal do macOS, ou Bash no Linux)

## Instalação rápida
- Windows: https://git-scm.com/download/win
- macOS: `brew install git`
- Linux (Debian/Ubuntu): `sudo apt-get install git`
- Configuração inicial:
```bash
git --version
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
git config --global core.editor "code --wait"  # opcional
```

## Estrutura do repositório
- `aulas/` — 20 aulas em Markdown (10 por tarde), com teoria breve, prática guiada, exercícios e desafios.
- `assets/` — Imagens SVG usadas nas aulas (diagramas e fluxos).
- `README.md` — Esta página.

## Como usar este material
1. Abra cada aula na pasta `aulas/` em ordem.
2. Siga os passos “Prática guiada” e execute os comandos no seu terminal.
3. Conclua os “Exercícios” e os “Desafios”.
4. Consulte as imagens em `assets/` conforme os links dentro das aulas.

## Sumário (Tarde 1: Aulas 01–10)
1. [Aula 01 — Introdução ao Git](aulas/aula01-introducao.md)
2. [Aula 02 — Instalação e Configuração](aulas/aula02-instalacao-config.md)
3. [Aula 03 — Repositório local: init, status, add, commit](aulas/aula03-init-status-add-commit.md)
4. [Aula 04 — .gitignore e arquivos gerados](aulas/aula04-gitignore.md)
5. [Aula 05 — Histórico: log, show, diff](aulas/aula05-historico.md)
6. [Aula 06 — Restaurando mudanças: restore](aulas/aula06-restore.md)
7. [Aula 07 — Branches: criar e navegar](aulas/aula07-branches-basico.md)
8. [Aula 08 — Merge básico](aulas/aula08-merge-basico.md)
9. [Aula 09 — Remotos: origin, push, pull](aulas/aula09-remotos-basico.md)
10. [Aula 10 — Clonar e fork básico](aulas/aula10-clone-fork.md)

## Sumário (Tarde 2: Aulas 11–20)
11. [Aula 11 — Pull Requests no GitHub](aulas/aula11-pull-requests.md)
12. [Aula 12 — Conflitos e resolução](aulas/aula12-conflitos.md)
13. [Aula 13 — Amend e rebase básico](aulas/aula13-amend-rebase.md)
14. [Aula 14 — Reset vs Revert vs Restore](aulas/aula14-reset-revert-restore.md)
15. [Aula 15 — Reflog e recuperação](aulas/aula15-reflog-recuperacao.md)
16. [Aula 16 — Tags e versões](aulas/aula16-tags-versoes.md)
17. [Aula 17 — Workflows e Conventional Commits](aulas/aula17-workflows-convcommits.md)
18. [Aula 18 — Stash: guardando trabalho](aulas/aula18-stash.md)
19. [Aula 19 — Submódulos (introdução)](aulas/aula19-submodulos.md)
20. [Aula 20 — Boas práticas e proteções](aulas/aula20-boas-praticas-protecoes.md)

## Cheatsheet rápido
```bash
git status
git add <arquivo>
git commit -m "mensagem curta e clara"
git log --oneline --graph --decorate --all
git switch -c minha-branch
git merge <branch>
git remote add origin <url>
git push -u origin main
git pull --ff-only
```

## Como subir este material ao GitHub (opção local)
```bash
git clone https://github.com/delanohelio/git-classes.git
cd git-classes
# Copie os arquivos desta pasta para aqui
git add .
git commit -m "feat: adiciona curso completo (20 aulas + assets)"
git push -u origin main
```