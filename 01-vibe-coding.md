# 1. Vibe coding: o que é e o que prediz quem é bom nisso

> Integrante 1 · Tema 4 — Habilidades e formação
> Pergunta que esta seção responde: **o que significa ter proficiência em programar com IA hoje?**

## Posicionamento

Programar só conversando com a IA não dispensa saber computação. No estudo-âncora, os
participantes **nem viam o código**, e mesmo assim o conhecimento de Ciência da Computação foi o
preditor que mais pesou: explicou cerca de **2 vezes mais variância** do desempenho do que a
habilidade de escrita (THORGEIRSSON; WEIDMANN; SU, 2026). E usar LLM com mais frequência **não**
esteve associado a desempenho melhor: a correlação foi negativa (r = −0,258).

## 1.1 De onde vem o termo

- **Karpathy (2 fev. 2025)** cunhou "vibe coding" num post no X: um jeito de programar em que você
  se entrega ao modelo e chega a *"forget that the code even exists"*. Aceita as mudanças sem ler o
  diff, cola a mensagem de erro de volta no chat e contorna bug em vez de entender (KARPATHY, 2025).
- **Willison (19 mar. 2025)** reagiu ao uso do termo para *qualquer* programação com IA. Para ele,
  vibe coding é especificamente gerar código **sem revisar nem entender**. Usar LLM revisando,
  testando e sendo capaz de explicar cada linha é outra coisa: programação assistida por IA. A
  regra dele: não fazer commit de código que ele não conseguiria explicar a outra pessoa
  (WILLISON, 2025).

| | Vibe coding (Karpathy) | Programação assistida por IA (Willison) |
|---|---|---|
| Lê o código gerado? | Não | Sim |
| Revisa o diff? | Não, aceita tudo | Sim |
| Testa? | Pelo comportamento visível | Testes de verdade |
| Consegue explicar o que commitou? | Não precisa | É a condição para commitar |

O artigo-âncora estuda a primeira coluna, na forma "pura": o participante não podia ler nem editar
o código.

## 1.2 O estudo-âncora (THORGEIRSSON; WEIDMANN; SU, CHI 2026)

**Desenho**: estudo **pré-registrado** com **100 estudantes** universitários de Zurique
(ETH e Universidade de Zurique), 56 mulheres e 44 homens, idade média de 25,0 anos. Todos tinham
cursado ao menos uma disciplina introdutória de programação e já usavam LLM para programar.

**O que foi medido em cada participante**

| Construto | Instrumento | Tempo |
|---|---|---|
| Conhecimento de CS | SCS1, 12 itens em pseudocódigo (conceitos, rastreio e completar código) | 25 min |
| Escrita | Redação de 300 a 450 palavras explicando um conceito técnico, corrigida por 2 avaliadores com rubrica | 20 min |
| Capacidade cognitiva geral | ICAR16 (raciocínio verbal, matrizes, séries, rotação 3D) | 12 min |
| **Vibe coding** | 3 tarefas de app web: replicar um app, adicionar uma funcionalidade e uma tarefa "descontextualizada" | 3 × 15 min |

O ambiente de vibe coding foi construído pelos autores, com chat à esquerda e preview do app à
direita, usando o modelo **Claude Sonnet 4**. O código gerado aparecia **borrado** na tela: o
participante só podia avaliar o comportamento do app e escrever novos prompts.

**Resultados principais** (escores normalizados de 0 a 1; desempenho médio em vibe coding foi 0,45)

| Correlação com o desempenho em vibe coding | r | p |
|---|---|---|
| Conhecimento de CS | **0,386** | < 0,001 |
| Capacidade cognitiva geral | 0,352 | < 0,001 |
| Escrita | 0,290 | 0,003 |

1. **CS continua valendo depois de controlar inteligência geral.** Com a capacidade cognitiva
   controlada, a correlação parcial de CS cai para 0,281 e continua significativa (p = 0,005). A de
   escrita cai para 0,186 e **deixa de ser significativa** (p = 0,066).
2. **CS pesa cerca de 2 vezes mais que escrita.** Na regressão hierárquica, CS sozinho explica 15,0%
   da variância e escrita sozinha, 8,3%. Os dois juntos explicam 20,8%. Acrescentar CS a um modelo
   que já tem escrita soma 12,5 pontos percentuais; acrescentar escrita a um modelo que já tem CS
   soma 5,9. No modelo final, β = 0,356 para CS e β = 0,244 para escrita, ambos significativos.
3. **Escrita importa por meio do prompt.** A qualidade dos prompts, avaliada por humanos, responde
   por cerca de **52%** da associação entre escrita e desempenho (efeito indireto de 0,152, IC 95%
   de 0,061 a 0,279). Quem escreve melhor escreve prompts melhores, e é isso que ajuda.
4. **Usar mais IA não tornou ninguém melhor nisso.** A frequência de uso de LLM declarada pelo
   participante teve correlação **negativa** com o desempenho em vibe coding (r = −0,258;
   p = 0,010), negativa com escrita (r = −0,282) e nula com CS (r = 0,001).

**Por que isso importa:** se o código estava escondido, CS não ajudou por permitir corrigir código.
Os autores interpretam que ajuda **indiretamente**: o estudante decompõe o problema e tem um modelo
mental de controle de fluxo e de estado, e por isso especifica melhor o que quer.

## 1.3 Limites do estudo (o que ele não prova)

- **É correlacional.** Não mostra que estudar CS *causa* um vibe coding melhor.
- **Os 20,8% explicados deixam cerca de 79% da variância sem explicação** por estes três fatores.
- **A amostra é de estudantes universitários**, não de profissionais nem de pessoas leigas.
- **É vibe coding "puro" e com tempo cronometrado.** Fora do laboratório, as pessoas leem e editam
  o código, e alguns participantes ficaram sem tempo quando estavam perto da solução.
- **O instrumento de escrita foi criado para o estudo** e não tinha sido validado antes.

## 1.4 Resposta à pergunta da seção

Ter proficiência em programar com IA, segundo a evidência disponível, é **saber especificar**: dizer
com precisão o que o programa deve fazer e avaliar se ele faz. Isso depende mais de fundamentos de
computação do que de "saber conversar com a IA". Isso sustenta o restante do trabalho: se o
fundamento é o que mais pesa, a questão passa a ser **como esse fundamento se forma** quando a IA
está disponível desde o primeiro dia (seções 2, 3 e 4).

## Referências

- THORGEIRSSON, S.; WEIDMANN, T. B.; SU, Z. Computer Science Achievement and Writing Skills Predict
  Vibe Coding Proficiency. In: *CHI '26*, Barcelona, 2026.
  [doi.org/10.1145/3772318.3791666](https://doi.org/10.1145/3772318.3791666) ·
  [arxiv.org/abs/2603.14133](https://arxiv.org/abs/2603.14133)
- KARPATHY, A. Publicação que cunhou o termo "vibe coding". X, 2 fev. 2025.
  [x.com/karpathy/status/1886192184808149383](https://x.com/karpathy/status/1886192184808149383)
- WILLISON, S. Not all AI-assisted programming is vibe coding (but vibe coding rocks). 19 mar. 2025.
  [simonwillison.net/2025/Mar/19/vibe-coding/](https://simonwillison.net/2025/Mar/19/vibe-coding/)
