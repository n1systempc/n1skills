# N1 Skills

Repositório de skills para orientar assistentes de IA em tarefas específicas. Cada skill reúne instruções, métodos e referências em um arquivo `SKILL.md`.

## Neuromarketing — N1 System

A [skill de neuromarketing](.agents/skills/neuromarketing/SKILL.md) apresenta um framework de copywriting persuasivo baseado no método **N1 System**. Ela orienta a criação e a revisão de textos a partir do público, da oferta e da ação desejada, do primeiro gancho à chamada final.

O método combina pesquisa de público, princípios de persuasão, quebra de padrão e técnicas de humanização da escrita para construir uma comunicação clara, relevante e com personalidade.

### Quando usar

- Anúncios e criativos para tráfego pago.
- Headlines, ganchos e chamadas para ação.
- Landing pages, páginas de vendas e páginas de captura.
- Roteiros de vídeo de vendas e VSLs.
- Emails de venda e sequências de email marketing.
- Revisão de copies que precisam de mais clareza, diferenciação ou conexão com o público.

### Como o método funciona

O processo começa pela identificação do público e de suas motivações. Em seguida, define um ângulo de comunicação, organiza os argumentos e revisa a linguagem para evitar textos genéricos ou artificiais.

A estrutura **BRAZIL** organiza a copy em seis etapas:

| Etapa | Função |
| --- | --- |
| **B — Gancho** | Chamar a atenção com uma quebra de padrão. |
| **R — Exposição** | Apresentar a situação e o problema do público. |
| **A — Realidade** | Mostrar um caminho simples para lidar com o problema. |
| **Z — A verdade** | Desenvolver a perspectiva que sustenta a proposta. |
| **I — Solução** | Apresentar o produto, seu diferencial e responder a objeções. |
| **L — Chamada** | Indicar a próxima ação e ajudar o leitor a visualizar o resultado. |

A skill também inclui orientações sobre curiosidade e continuidade da leitura, quatro categorias de motivação de compra usadas pelo método — necessidade, status, metafísico e tribalismo — e uma revisão final de sentimento, conexão e confiança.

### Como usar

Em um assistente com suporte a skills, disponibilize a pasta [neuromarketing](.agents/skills/neuromarketing) conforme o mecanismo de carregamento da ferramenta. As instruções principais estão no `SKILL.md`, acompanhadas dos materiais de referência.

Ao fazer um pedido, mencione a skill e informe:

- **Produto ou serviço:** o que você oferece e qual é o diferencial.
- **Público:** para quem é a mensagem, suas necessidades e objeções.
- **Formato e canal:** onde o texto será publicado.
- **Objetivo:** qual ação o leitor deve realizar.
- **Tom e contexto:** estilo de linguagem, detalhes da oferta e provas disponíveis.

Exemplo de criação:

```text
Use a skill de neuromarketing para criar 3 versões de um anúncio.

Produto: curso de fotografia com celular.
Público: pequenos empreendedores que fotografam os próprios produtos.
Diferencial: aulas práticas com exercícios usando os produtos do aluno.
Canal: Instagram.
Objetivo: levar o leitor à página de apresentação do curso.
Tom: direto, próximo e sem promessas exageradas.

Aplique a estrutura BRAZIL e varie o gancho de cada versão.
```

Exemplo de revisão:

```text
Use a skill de neuromarketing para revisar a copy abaixo.
Identifique trechos genéricos, melhore a sequência dos argumentos
e deixe a chamada para ação mais clara. Preserve os fatos da oferta
e explique brevemente as principais alterações.

[Cole a copy aqui]
```

### Arquivos da skill

- [SKILL.md](.agents/skills/neuromarketing/SKILL.md): princípios, estrutura BRAZIL, processo de criação e checklist de revisão.
- [Leis do Poder](.agents/skills/neuromarketing/references/leis-do-poder.md): adaptações das 48 Leis do Poder para posicionamento, autoridade e diferenciação na copy.
- [Humanizer](.agents/skills/neuromarketing/references/humanizer.md): guia para identificar padrões de escrita artificial e tornar o texto mais natural.
