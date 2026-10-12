# N1 Skills

Coleção de skills para agentes de IA, com foco em copywriting pelo método N1 System e na criação e melhoria de novas skills.

Cada skill reúne instruções em um arquivo `SKILL.md` e pode incluir referências, scripts e recursos auxiliares para orientar o agente em tarefas específicas.

## Skills disponíveis

| Skill | Finalidade | Instruções |
| --- | --- | --- |
| **Neuromarketing** | Criar e revisar textos persuasivos com o método N1 System, incluindo a estrutura BRAZIL, headlines, anúncios, landing pages, emails e roteiros de vendas. | [SKILL.md](.agents/skills/neuromarketing/SKILL.md) |
| **Skill Creator** | Criar, revisar e avaliar skills, com recursos para testes, comparação de resultados e melhoria das descrições de ativação. | [SKILL.md](.agents/skills/skill-creator/SKILL.md) |

A skill de neuromarketing inclui referências sobre [leis do poder aplicadas à copy](.agents/skills/neuromarketing/references/leis-do-poder.md) e [humanização de textos](.agents/skills/neuromarketing/references/humanizer.md).

## Como usar

1. Abra este repositório no ambiente do seu agente de IA.
2. Escolha uma skill e indique o caminho do respectivo `SKILL.md` no pedido. Se o ambiente oferecer descoberta automática de skills, confirme que ela está disponível.
3. Descreva a tarefa, o contexto e o resultado esperado.

Exemplo para copywriting:

```text
Use a skill em .agents/skills/neuromarketing/SKILL.md para criar
três variações de anúncio para meu curso de fotografia para iniciantes.
O público usa o celular para fotografar e quer melhorar suas fotos de viagem.
Use um tom direto e finalize com uma chamada para conhecer o curso.
```

Exemplo para criação de skills:

```text
Use a skill em .agents/skills/skill-creator/SKILL.md para criar
uma skill de revisão de artigos de blog, com critérios de clareza,
estrutura e consistência de tom. Inclua exemplos para avaliar os resultados.
```

As instruções e referências podem ser lidas diretamente, sem instalação de dependências. Os scripts auxiliares da `skill-creator` têm requisitos próprios; consulte seus arquivos antes de executá-los.

## Estrutura do projeto

```text
.
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
├── .aider-desk/skills/
├── .claude/skills/
├── skills-lock.json
└── README.md
```

O conteúdo das skills fica em `.agents/skills/`. As pastas `.aider-desk/skills/` e `.claude/skills/` contêm links para a `skill-creator`. O arquivo `skills-lock.json` registra a origem e o hash dessa skill externa.

## Adicionar uma skill

Crie uma pasta em `.agents/skills/<nome-da-skill>/` com um arquivo `SKILL.md`. No início do arquivo, defina os campos `name` e `description` em YAML; em seguida, documente as instruções, as entradas necessárias e o resultado esperado. Coloque referências e scripts em subpastas quando necessário.

## Créditos e licença

A `skill-creator` tem origem no repositório `anthropics/skills`, conforme registrado em [skills-lock.json](skills-lock.json), e inclui uma [licença Apache 2.0](.agents/skills/skill-creator/LICENSE.txt). Essa licença acompanha o componente; o repositório não possui um arquivo de licença geral na raiz.
