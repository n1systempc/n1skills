# N1 Skills

Coleção de skills para agentes de IA, com foco em copywriting pelo método N1 System e na criação e melhoria de novas skills.

Cada skill reúne instruções em um arquivo `SKILL.md` e pode incluir referências, scripts e outros materiais de apoio para orientar o agente em tarefas específicas.

## Skills disponíveis

| Skill | Finalidade | Instruções |
| --- | --- | --- |
| `neuromarketing` | Orientar a criação e revisão de anúncios, headlines, páginas de vendas, emails e roteiros com o método N1 System e a estrutura BRAZIL. | [SKILL.md](.agents/skills/neuromarketing/SKILL.md) |
| `skill-creator` | Criar, revisar e avaliar skills, incluindo testes de acionamento, benchmarks e revisão de resultados. | [SKILL.md](.agents/skills/skill-creator/SKILL.md) |

A skill de neuromarketing inclui referências sobre [leis do poder aplicadas à copy](.agents/skills/neuromarketing/references/leis-do-poder.md) e [humanização da escrita](.agents/skills/neuromarketing/references/humanizer.md).

## Estrutura

```text
n1skills/
├── .agents/
│   └── skills/
│       ├── neuromarketing/
│       │   ├── SKILL.md
│       │   └── references/
│       └── skill-creator/
│           ├── SKILL.md
│           ├── LICENSE.txt
│           ├── agents/
│           ├── assets/
│           ├── eval-viewer/
│           ├── references/
│           └── scripts/
├── .aider-desk/skills/skill-creator → ../../.agents/skills/skill-creator
├── .claude/skills/skill-creator → ../../.agents/skills/skill-creator
├── skills-lock.json
└── readme.md
```

Os arquivos das skills ficam em `.agents/skills/`. As pastas `.claude/skills/` e `.aider-desk/skills/` contêm links simbólicos para `skill-creator`, compartilhando a mesma versão das instruções.

O arquivo [`skills-lock.json`](skills-lock.json) registra a origem e o hash da skill `skill-creator`, proveniente de `anthropics/skills`.

## Como usar

1. Abra a pasta do projeto no seu agente de IA.
2. Consulte o `SKILL.md` da skill desejada e seus materiais de apoio.
3. Peça ao agente para aplicar a skill e forneça o contexto da tarefa. Caso ela não seja carregada automaticamente, indique o caminho do arquivo no pedido.

Exemplos de pedidos:

```text
Leia .agents/skills/neuromarketing/SKILL.md e aplique suas instruções
para criar três anúncios para meu curso de fotografia.
Público: iniciantes que fotografam com celular.
Objetivo: inscrições em uma aula gratuita.
Tom: direto e acessível.
```

```text
Use a skill skill-creator para criar uma skill de revisão de artigos.
Ela deve verificar clareza, organização e consistência do texto,
entregando sugestões acompanhadas de exemplos de reescrita.
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

A skill `skill-creator` inclui um validador básico de estrutura e metadados. Com Python 3 e PyYAML disponíveis, execute a partir da raiz do projeto:

```bash
python3 .agents/skills/skill-creator/scripts/quick_validate.py .agents/skills/minha-skill
```

Substitua `minha-skill` pela pasta que deseja validar. Os demais scripts podem exigir dependências adicionais; os testes de acionamento em `run_eval.py` utilizam a CLI do Claude.

## Licença

A skill `skill-creator` inclui sua própria [licença](.agents/skills/skill-creator/LICENSE.txt). O repositório ainda não possui um arquivo de licença geral para os demais conteúdos.
