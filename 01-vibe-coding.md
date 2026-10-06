# O Fenômeno do Vibe Coding: O Que Prediz Quem Programa Bem com IA

## Contexto e Pergunta Científica

Em fevereiro de 2025, Andrej Karpathy deu nome a um jeito de programar em que a pessoa descreve o que quer, aceita o que o modelo gera e chega a "forget that the code even exists": o *vibe coding*. Com a popularização dessas ferramentas, a discussão sobre habilidades e formação chega a uma questão central: **o que significa ter proficiência em programar com IA hoje? Quem se sai bem é quem sabe computação ou quem sabe escrever bem?**

Para responder a essa pergunta, analisamos o artigo-âncora do tema, **Thorgeirsson, Weidmann e Su (2026)** (*Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency*), publicado na CHI 2026.

**Natureza da fonte:** estudo pré-registrado com **100 estudantes** universitários de Zurique (ETH e Universidade de Zurique), 56 mulheres e 44 homens, idade média de 25,0 anos. Todos tinham cursado ao menos uma disciplina introdutória de programação e já usavam LLM para programar. O desenho é correlacional: mostra associações, não causa.

## 1. Vibe Coding Não É Toda Programação com IA

* **Karpathy (2 fev. 2025):** cunhou o termo num post no X. No vibe coding, a pessoa se entrega ao modelo: aceita as mudanças sem ler o diff, cola a mensagem de erro de volta no chat e contorna o bug em vez de entendê-lo (KARPATHY, 2025).
* **Willison (19 mar. 2025):** reagiu ao uso do termo para *qualquer* programação com IA. Para ele, vibe coding é especificamente gerar código **sem revisar nem entender**. Usar LLM revisando, testando e sendo capaz de explicar cada linha é outra coisa: programação assistida por IA. A regra dele é não fazer commit de código que ele não conseguiria explicar a outra pessoa (WILLISON, 2025).

| | Vibe coding (Karpathy) | Programação assistida por IA (Willison) |
|---|---|---|
| Lê o código gerado? | Não | Sim |
| Revisa o diff? | Não, aceita tudo | Sim |
| Testa? | Pelo comportamento visível | Testes de verdade |
| Consegue explicar o que commitou? | Não precisa | É a condição para commitar |

O artigo-âncora estuda a primeira coluna, na forma "pura": o participante não podia ler nem editar o código.

## 2. O Experimento

Cada participante passou por três testes e depois por três tarefas de vibe coding:

* **Conhecimento de Ciência da Computação (CS):** SCS1, prova validada de programação introdutória em pseudocódigo, com 12 itens (conceitos, rastreio e completar código), em 25 min.
* **Escrita:** redação de 300 a 450 palavras explicando um conceito técnico, corrigida por 2 avaliadores com rubrica, em 20 min.
* **Capacidade cognitiva geral:** ICAR16, teste de raciocínio (verbal, matrizes, séries e rotação 3D), em 12 min.
* **Vibe coding:** 3 tarefas de app web de 15 min cada (replicar um app, adicionar uma funcionalidade e uma tarefa "descontextualizada").

O ambiente foi construído pelos autores, com chat à esquerda e preview do app à direita, usando o modelo **Claude Sonnet 4**. O código gerado aparecia **borrado** na tela: o participante só podia avaliar o comportamento do app e escrever novos prompts.

## 3. Conhecimento de Computação Pesa Mais que a Escrita

Com escores normalizados de 0 a 1, o desempenho médio em vibe coding foi 0,45. As correlações com esse desempenho foram:

| Fator | r | p |
|---|---|---|
| Conhecimento de CS | **0,386** | < 0,001 |
| Capacidade cognitiva geral | 0,352 | < 0,001 |
| Escrita | 0,290 | 0,003 |

* **CS continua valendo depois de controlar a inteligência geral:** com a capacidade cognitiva controlada, a correlação parcial de CS cai para 0,281 e continua significativa (p = 0,005). A de escrita cai para 0,186 e **deixa de ser significativa** (p = 0,066).
* **CS pesa cerca de 2 vezes mais que escrita:** na regressão hierárquica, CS sozinho explica 15,0% da variância e escrita sozinha, 8,3%. Os dois juntos explicam 20,8%. Acrescentar CS a um modelo que já tem escrita soma 12,5 pontos percentuais; acrescentar escrita a um modelo que já tem CS soma 5,9. No modelo final, β = 0,356 para CS e β = 0,244 para escrita, ambos significativos.
* **Escrita importa por meio do prompt:** a qualidade dos prompts, avaliada por humanos, responde por cerca de **52%** da associação entre escrita e desempenho (efeito indireto de 0,152, IC 95% de 0,061 a 0,279). Quem escreve melhor escreve prompts melhores, e é isso que ajuda.
* **Por que CS ajuda sem ver o código:** se o código estava escondido, CS não ajudou por permitir corrigir código. Os autores interpretam que ajuda **indiretamente**: o estudante decompõe o problema e tem um modelo mental de controle de fluxo e de estado, e por isso especifica melhor o que quer.

## 4. Usar Mais IA Não Torna Ninguém Melhor

A frequência de uso de LLM declarada pelo participante teve correlação **negativa** com o desempenho em vibe coding (r = −0,258; p = 0,010), negativa com a escrita (r = −0,282) e nula com o conhecimento de CS (r = 0,001). Familiaridade com a ferramenta não se converteu em proficiência.

## 5. Limites do Estudo

* **É correlacional:** não mostra que estudar CS *causa* um vibe coding melhor.
* **Muita variação sem explicação:** os 20,8% explicados deixam cerca de 79% da variância fora destes fatores.
* **A amostra é de estudantes universitários:** não de profissionais nem de pessoas leigas.
* **É vibe coding "puro" e com tempo cronometrado:** fora do laboratório, as pessoas leem e editam o código, e alguns participantes ficaram sem tempo quando estavam perto da solução.
* **O instrumento de escrita foi criado para o estudo:** não tinha sido validado antes.

## 6. Síntese do Posicionamento

* Ter proficiência em programar com IA, segundo a evidência disponível, é **saber especificar**: dizer com precisão o que o programa deve fazer e avaliar se ele faz.
* Isso depende mais de fundamentos de computação do que de "saber conversar com a IA": mesmo sem ver o código, quem sabia mais CS se saiu melhor, e quem usava mais IA não.
* Se o fundamento é o que mais pesa, a questão passa a ser **como esse fundamento se forma** quando a IA está disponível desde o primeiro dia, que é o que as próximas partes discutem.

## Referências

* THORGEIRSSON, S.; WEIDMANN, T. B.; SU, Z. **Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency**. In: *Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems (CHI '26)*, 2026. DOI: [10.1145/3772318.3791666](https://doi.org/10.1145/3772318.3791666). Disponível também em: [arxiv.org/abs/2603.14133](https://arxiv.org/abs/2603.14133).
* KARPATHY, A. **Publicação que cunhou o termo "vibe coding"**. X, 2 fev. 2025. Disponível em: [x.com/karpathy/status/1886192184808149383](https://x.com/karpathy/status/1886192184808149383).
* WILLISON, S. **Not all AI-assisted programming is vibe coding (but vibe coding rocks)**. 19 mar. 2025. Disponível em: [simonwillison.net/2025/Mar/19/vibe-coding/](https://simonwillison.net/2025/Mar/19/vibe-coding/).
