# O Paradoxo do Erro: Por Que Iniciantes Falham ao Programar com LLMs

## Contexto e Pergunta Científica

Estudos anteriores mostram que estudantes iniciantes têm dificuldade em usar
LLMs para gerar código. A explicação mais comum, citada por alunos e
professores, é a falta de vocabulário técnico para escrever bons prompts. Isso
leva à pergunta central: **o iniciante falha por falar "errado" (estilo) ou por
não saber o que dizer (substância)?** Para responder, analisamos **Lucchetti et
al. (2025)** (_Substance Beats Style: Why Beginning Students Fail to Code with
LLMs_), publicado na NAACL 2025.

## **Natureza da fonte:** análise secundária do conjunto de dados StudentEval, com prompts escritos por **80 estudantes** que haviam cursado apenas **uma disciplina de programação**. O conjunto reúne **1.749 prompts** sobre **48 tarefas de CS1**, cada aluno resolvendo 8 problemas. Os prompts originais foram escritos para o modelo _code-davinci-002_, hoje defasado.

## 1. Hipótese 1: O Problema é o Estilo (Vocabulário)

Os autores testaram a hipótese com um experimento causal: trocaram termos
técnicos dos prompts por sinônimos usados pelos próprios alunos (ex.: "integer"
por "whole number") e mediram a taxa de acerto do código gerado.

- **Escala do teste:** 12 conceitos técnicos, **65 substituições** e geração de
  código com Llama 3.1 (8B e 70B).
- **Efeitos fracos:** para 4 dos 14 conceitos analisados não houve diferença
  estatisticamente confiável, e as diferenças encontradas tendem a ser pequenas.
- **Corrigir o vocabulário não resolve:** trocar termos não padronizados por
  termos técnicos precisos **não trouxe ganhos confiáveis** em nenhuma
  categoria. A relação entre vocabulário e falha é **correlacional**, não
  causal.
- **Exceção:** termos que _enganam_ o modelo prejudicam o resultado (ex.: pedir
  para "print" ou "display" quando a função deveria "return").

---

## 2. Hipótese 2: O Problema é a Substância (Informação)

Os autores anotaram **303 trajetórias de prompts** (sequências de tentativas de
um aluno em uma tarefa) com as "pistas" (_clues_): informações sobre o
comportamento esperado do código, como arredondar o resultado ou descrever a
estrutura da lista de entrada.

- **Pistas completas:** quando o prompt final continha todas as pistas, a chance
  de sucesso foi de **86%**.
- **Falta de uma pista:** com **uma única pista ausente**, a chance caiu para
  **40%**.
- **Reescrever não adianta:** em prompts com menos da metade das pistas, mexer
  apenas nos detalhes das pistas existentes levou ao sucesso em **apenas 11%**
  dos casos.

---

## 3. O Ciclo da Frustração

O estudo identificou que muitos alunos ficam "presos" em ciclos de tentativas
que repetem o mesmo erro.

- **Efeito do ciclo:** trajetórias com ciclo tiveram **30%** de sucesso, contra
  **72%** sem ciclo. Em ciclos com mais de três arestas, o sucesso caiu para
  **14%**.
- **Causa dos ciclos:** em **90%** das edições dentro de ciclos havia pistas
  faltando, e **75%** eram apenas reescritas; dessas, **54%** não alteravam o
  nível de detalhe de nenhuma pista.
- **Como escapar:** das 44 trajetórias que saíram de um ciclo, só **7** o
  fizeram com edições triviais. A maioria **adicionou uma pista nova (13)** ou
  **mais detalhe a pistas existentes (20)**.

---

## 4. Síntese do Posicionamento

- O iniciante não falha por "falar errado" com a máquina, e sim por **não saber
  que informação a máquina precisa**. A substância vence o estilo.
- A dificuldade está em decidir o que o modelo consegue inferir sozinho e o que
  precisa ser dito. Isso exige entender o problema e o que o código deve fazer,
  ou seja, **fundamentos**.
- Ensinar "palavras certas" para o prompt tem pouco efeito. É mais promissor
  ensinar a **identificar a informação que falta**.

## **Limites do estudo:** amostra de iniciantes com uma só disciplina de programação, de instituições selecionadas dos EUA, e prompts escritos para um modelo mais antigo. Os resultados podem não se generalizar a programadores mais experientes.

## Referências

- LUCCHETTI, F.; WU, Z.; GUHA, A.; FELDMAN, M. Q.; ANDERSON, C. J. **Substance
  Beats Style: Why Beginning Students Fail to Code with LLMs**. In: _Annual
  Conference of the Nations of the Americas Chapter of the ACL (NAACL)_, 2025.
  Disponível em:
  [aclanthology.org/2025.naacl-long.433](https://aclanthology.org/2025.naacl-long.433/)
  e [arxiv.org/abs/2410.19792](https://arxiv.org/abs/2410.19792).
