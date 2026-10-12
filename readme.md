# N1 Skills

Coleção de skills para agentes de IA, com foco em copywriting pelo método N1 System. Atualmente, a única skill disponível é `neuromarketing`.

Cada skill reúne instruções em um arquivo `SKILL.md` e pode incluir referências, scripts e outros materiais de apoio para orientar o agente em tarefas específicas.

## Skills disponíveis

| Skill | Finalidade | Instruções |
| --- | --- | --- |
| `neuromarketing` | Orientar a criação e revisão de anúncios, headlines, páginas de vendas, emails e roteiros com o método N1 System e a estrutura BRAZIL. | [SKILL.md](.agents/skills/neuromarketing/SKILL.md) |

A skill de neuromarketing inclui referências sobre [leis do poder aplicadas à copy](.agents/skills/neuromarketing/references/leis-do-poder.md) e [humanização da escrita](.agents/skills/neuromarketing/references/humanizer.md).

## Estrutura da skill disponível

```text
n1skills/
├── .agents/
│   └── skills/
│       └── neuromarketing/
│           ├── SKILL.md
│           └── references/
│               ├── leis-do-poder.md
│               └── humanizer.md
└── readme.md
```

Os arquivos da skill ficam em `.agents/skills/neuromarketing/`.

## Como usar

1. Abra a pasta do projeto no seu agente de IA.
2. Consulte o `SKILL.md` de neuromarketing e seus materiais de apoio.
3. Peça ao agente para aplicar a skill e forneça o contexto da tarefa. Caso ela não seja carregada automaticamente, indique o caminho do arquivo no pedido.

Exemplo de pedido:

```text
Leia .agents/skills/neuromarketing/SKILL.md e aplique suas instruções
para criar três anúncios para meu curso de fotografia.
Público: iniciantes que fotografam com celular.
Objetivo: inscrições em uma aula gratuita.
Tom: direto e acessível.
```

Para tarefas de copywriting, informe produto, público, objetivo, canal, tom de voz e evidências disponíveis para sustentar as afirmações.

## Adicionar ou atualizar uma skill

Crie uma pasta em `.agents/skills/<nome-da-skill>/` com um arquivo `SKILL.md`. Comece pelos campos `name` e `description`, seguidos das instruções:

```markdown
---
name: minha-skill
description: Descreva o que a skill faz e quando deve ser utilizada.
---

# Minha Skill

Explique o fluxo de trabalho, os dados necessários e o resultado esperado.
```

Use `references/` para documentação complementar, `scripts/` para automações e `assets/` para modelos ou arquivos utilizados nas entregas. Ao atualizar uma skill, revise também suas referências e os exemplos deste README.

## Licença

O repositório ainda não possui um arquivo de licença geral.
