# Aula 04 — Branches e merges básicos (30min)

![Branches e merge](../assets/branch-merge.svg)

## Objetivos
- Criar e alternar entre branches.
- Fazer merges (fast-forward e com merge commit).

## Plano (30min)
- 0–5m: Motivação: trabalhar em paralelo sem quebrar a main.
- 5–12m: Conceitos: ponteiros, HEAD, fast-forward.
- 12–20m: Demo: `branch`, `checkout -b`, `merge`.
- 20–27m: Prática guiada.
- 27–30m: Checagem.

## Comandos
```bash
git branch
git checkout -b feature/cabecalho
# edite algo e faça commit
git checkout main
git merge feature/cabecalho
git log --oneline --graph --decorate
```

## Atividade guiada
- Crie uma branch de feature, faça 1–2 commits, faça merge na main.

## Desafio extra
- Faça um segundo merge que exija um commit de merge (sem fast-forward).

## Recursos
- Imagem: `assets/branch-merge.svg`