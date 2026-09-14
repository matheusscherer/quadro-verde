# Quadro verde

Âncora para manter o [gráfico de contribuições](https://github.com/matheusscherer) verde todos os dias.

Uma automação pinta o dia **somente** se ainda não houver nenhum commit do autor. Trabalho real tem prioridade — este arquivo não substitui código de verdade.

Registro: [`diario.md`](./diario.md).

## Git / agentes

Qualquer mudança (exceto a pinta diária) segue [`AGENTS.md`](./AGENTS.md):

```text
Issue → branch → PR (Closes #N) → merge
```

A pinta diária é a única exceção: commit direto em `main` em `diario.md`, e só se o dia ainda estiver vazio.
