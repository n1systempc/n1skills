# N1 Skills

Coleção de skills para agentes de IA, com foco em copywriting pelo método N1 System.

Cada skill reúne instruções em um arquivo `SKILL.md` e pode incluir referências, scripts e recursos auxiliares para orientar o agente em tarefas específicas.

## Skills disponíveis

| Skill | Finalidade | Instruções |
| --- | --- | --- |
| **Neuromarketing** | Criar e revisar textos persuasivos com o método N1 System, incluindo a estrutura BRAZIL, headlines, anúncios, landing pages, emails e roteiros de vendas. | [SKILL.md](.agents/skills/neuromarketing/SKILL.md) |

A skill de neuromarketing inclui referências sobre [leis do poder aplicadas à copy](.agents/skills/neuromarketing/references/leis-do-poder.md) e [humanização de textos](.agents/skills/neuromarketing/references/humanizer.md).

## Instalar no VS Code

A skill é usada pelo agente de IA dentro do editor. O passo a passo abaixo considera o **GitHub Copilot no VS Code**.

### Instalação pelo terminal

Tenha o VS Code atualizado, o GitHub Copilot configurado com sua conta, o Git e o Node.js com npm disponíveis.

1. Abra no VS Code a pasta do projeto em que deseja usar a skill.
2. Acesse **Terminal → Novo Terminal** e confira se o terminal está na raiz desse projeto.
3. Execute:

   ```sh
   npx skills add n1systempc/n1skills --skill neuromarketing --agent github-copilot
   ```

4. Siga as opções do instalador para concluir. O comando seleciona apenas a skill `neuromarketing` e usa o escopo do projeto.

Para disponibilizá-la em todos os seus projetos, use a instalação pessoal:

```sh
npx skills add n1systempc/n1skills --skill neuromarketing --agent github-copilot --global
```

Confira a instalação com `npx skills list` ou, no caso pessoal, `npx skills list --global`. Os parâmetros de instalação estão documentados no [CLI Skills](https://github.com/vercel-labs/skills).

### Instalação manual, sem Node.js

Baixe ou clone este repositório e copie a pasta inteira `.agents/skills/neuromarketing`, incluindo `references/`, para a mesma localização no projeto de destino:

```text
seu-projeto/
└── .agents/
    └── skills/
        └── neuromarketing/
            ├── SKILL.md
            └── references/
```

Se você já abriu o próprio repositório N1 Skills no VS Code, os arquivos estão no lugar certo.

### Ativar e conferir no chat

Abra uma nova conversa no Copilot e digite `/` para selecionar `neuromarketing`. Por exemplo:

```text
/neuromarketing Crie três headlines para um curso de fotografia para iniciantes.
```

Se a skill não aparecer, confira o caminho `.agents/skills/neuromarketing/SKILL.md` e use `/skills` para consultar as skills disponíveis. Confirme também que a pasta aberta no editor é a raiz do projeto.

O Copilot reconhece skills em `.agents/skills/` e permite invocá-las pelo chat. Consulte a [documentação oficial de Agent Skills no VS Code](https://code.visualstudio.com/docs/agent-customization/agent-skills).

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
