# Aula 05 — Remotos e GitHub: push, pull, clone (30min)

![Remotos e GitHub](../assets/remote-github.svg)

## Objetivos
- Conectar um repositório local a um remoto no GitHub.
- Fazer `push` e `pull`. Clonar um repositório.

## Plano (30min)
- 0–6m: Criando repo no GitHub.
- 6–15m: Demo: `remote add`, `push -u`, `pull`.
- 15–25m: Prática guiada.
- 25–30m: Checagem.

## Comandos
```bash
git remote add origin https://github.com/<usuario>/<repo>.git
git branch -M main
git push -u origin main
git pull
git clone https://github.com/<usuario>/<repo>.git
```

## Atividade guiada
- Crie um repositório vazio no GitHub e conecte-o ao seu local.
- Faça um novo commit local e `git push`.

## Dica
- Autenticação por token (HTTPS) ou SSH (chaves).

## Recursos
- Imagem: `assets/remote-github.svg`