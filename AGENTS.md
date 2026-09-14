# Padrão Git — leia isto antes de qualquer mudança

Este arquivo vale para **qualquer agente, de qualquer modelo** (Grok, Cursor, Claude, Copilot, etc.).

## Fluxo obrigatório

Toda tarefa — **correção**, **melhoria** ou **função nova**:

1. Abra uma **Issue** (labels: `correção` / `melhoria` / `nova-função`).
2. Crie uma **branch** a partir de `main` (`fix/…`, `improve/…`, `feat/…`, `docs/…`).
3. Commits pequenos, no imperativo: `feat:`, `fix:`, `improve:`, `docs:`, `chore:`.
4. Abra um **Pull Request**.
5. Na descrição do PR, mencione a Issue: `Closes #N`.
6. Só depois faça o merge em `main`.

Não commite direto em `main`. Não pule a Issue. Uma branch = uma Issue.

## Exceção — pinta diária (só este repo)

O heartbeat que pinta o gráfico de contribuições **não** usa Issue nem PR.

Permitido **somente** se todas forem verdade:

- o arquivo é `diario.md`
- a data de hoje (`America/Sao_Paulo`, `YYYY-MM-DD`) ainda não está no arquivo
- **não existe nenhum commit** `author:matheusscherer` nesse dia (qualquer repo)
- a mensagem é `chore(diario): pinta YYYY-MM-DD`
- o commit vai direto em `main`

Trabalho real tem prioridade. Se já houve commit no dia, **não pinte**.

Mudança na automação (workflow, `AGENTS.md`, README, lógica) **não** é exceção — usa Issue + PR.

## Commits

Um commit = uma ideia. Nunca `update`, `wip`, `ajuste`.
Nunca commitar `.env`, senha, CSV de cliente, `.venv`, `node_modules`.

## `main` é sagrado

Sem force-push em `main`. Para desfazer: `git revert`.
