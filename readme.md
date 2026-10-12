# N1 Skills

Coleção de skills para agentes de IA, com foco em copywriting pelo método N1 System.

Cada skill reúne instruções em um arquivo `SKILL.md` e pode incluir referências, scripts e recursos auxiliares para orientar o agente em tarefas específicas.

## Skills disponíveis

| Skill | Finalidade | Instruções |
| --- | --- | --- |
| **Neuromarketing** | Criar e revisar textos persuasivos com o método N1 System, incluindo a estrutura BRAZIL, headlines, anúncios, landing pages, emails e roteiros de vendas. | [SKILL.md](.agents/skills/neuromarketing/SKILL.md) |

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

As instruções e referências podem ser lidas diretamente, sem instalação de dependências.

## Estrutura da skill de neuromarketing

```text
.
├── .agents/
│   └── skills/
│       └── neuromarketing/
│           ├── SKILL.md
│           └── references/
│               ├── humanizer.md
│               └── leis-do-poder.md
└── README.md
```

O conteúdo das skills fica em `.agents/skills/`.

## Adicionar uma skill

Crie uma pasta em `.agents/skills/<nome-da-skill>/` com um arquivo `SKILL.md`. No início do arquivo, defina os campos `name` e `description` em YAML; em seguida, documente as instruções, as entradas necessárias e o resultado esperado. Coloque referências e scripts em subpastas quando necessário.
