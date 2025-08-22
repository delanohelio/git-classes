# Aula 03 — Histórico e inspeção: log, diff, restore (30min)

![Árvore de commits](../assets/commit-tree.svg)

## Objetivos
- Ler o histórico com diferentes formatos.
- Ver diferenças entre commits e restaurar arquivos.

## Plano (30min)
- 0–4m: Revisão.
- 4–12m: Teoria: commits, pais, HEAD, hash.
- 12–20m: Demo: `log`, `show`, `diff`, `restore`.
- 20–27m: Prática guiada.
- 27–30m: Checagem.

## Comandos
```bash
git log --oneline --decorate --graph --all
git show HEAD
git diff HEAD~1 HEAD
git restore --staged <arquivo>
git restore <arquivo>
```

## Atividade guiada
- Faça um commit que introduz um erro.
- Use `git diff` para localizar a mudança e `git restore` para desfazer no working dir.

## Desafio extra
- Use `git show <hash>` para inspecionar um commit específico.

## Recursos
- Imagem: `assets/commit-tree.svg`