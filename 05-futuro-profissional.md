# O Futuro do Profissional: O Que Sobra para o Humano

## Contexto e Pergunta Científica

Se as ferramentas de IA passam a escrever boa parte do código, a discussão sobre habilidades e formação chega a uma questão bem importante: se a máquina escreve o código, o que sobra para o humano saber?

Para responder a essa pergunta, foi analisado o relatório **The Future of Software Engineering Retreat Findings and Strategic Insights** (THOUGHTWORKS, 2026), que registra as conclusões de um encontro de profissionais seniores de engenharia de software realizado em Park City, Utah, de 1 a 3 de fevereiro de 2026, por ocasião dos 25 anos do Manifesto Ágil.

**Natureza da fonte:** o relatório não é um estudo experimental. Ele reúne a opinião de praticantes, registrada sob a Chatham House Rule (as falas não são atribuídas a pessoas ou empresas), e apresenta poucos dados quantitativos. Por isso é usado aqui como posicionamento da indústria, e não como uma medição quantitaviva.

## 1. O Rigor Não Desaparece, Muda de Lugar

A pergunta que organiza o relatório é para onde vai a engenharia quando a IA cuida do código. A resposta dos participantes é que o rigor antes aplicado à escrita e à leitura de cada linha se desloca para cinco principais pontos:

* **Especificação:** a revisão passa a acontecer antes do código, sobre o plano que a IA vai seguir. Histórias de usuário vagas deixam de ser suficientes.
* **Testes:** escrever os testes antes (TDD) funciona como validação determinística de uma geração que não é determinística, e evita que o agente escreva testes que confirmam um comportamento errado.
* **Tipos e restrições:** sistemas de tipos e limites de contexto são usados para tornar o código incorreto impossível de representar e para reduzir o alcance de um erro.
* **Mapeamento de risco:** a verificação passa a ser proporcional ao dano que o código pode causar se estiver errado, e não igual para todo o código.
* **Compreensão contínua:** como o código muda mais rápido do que se consegue revisar, as equipes precisam de outros meios para manter o entendimento do sistema, como programação em par e retrospectivas de arquitetura.

## 2. As Habilidades do "Middle Loop"

Também é descrito no relatório uma nova categoria de trabalho, situada entre o ciclo interno do desenvolvedor (escrever, testar, depurar) e o ciclo externo (integração, entrega e operação): a engenharia de supervisão, chamada de middle loop.

* **Decomposição:** dividir um problema em pacotes de trabalho do tamanho adequado para um agente.
* **Calibração de confiança:** saber quanto confiar no que o agente entrega e reconhecer resultados plausíveis, porém incorretos.
* **Coerência arquitetural:** manter um modelo mental do sistema e a consistência entre frentes de trabalho paralelas.
* **Avaliação de qualidade:** julgar o resultado sem depender da leitura de cada linha.

Segundo o relatório, o trabalho de apenas traduzir tarefas já detalhadas em código é o que tende a desaparecer. As quatro habilidades acima dependem de fundamentos de computação e de clareza ao especificar, o que converge com o artigo-âncora do tema (THORGEIRSSON; WEIDMANN; SU, 2026), que associa a proficiência em vibe coding ao desempenho em ciência da computação e à habilidade de escrita.

## 3. A Formação do Profissional Experiente

* **Juniores:** o relatório contraria a ideia de que o iniciante perdeu espaço. Os participantes defendem que a IA encurta a fase inicial em que o júnior ainda custa mais do que produz, e que ele representa uma aposta na produtividade futura da equipe.
* **Nível pleno:** a preocupação maior recai sobre profissionais de nível intermediário que entraram no mercado durante a fase de contratações em massa e podem não ter consolidado os fundamentos exigidos pelo trabalho de supervisão.
* **Modelo de formação:** o exemplo citado é o programa cooperativo da Universidade de Waterloo, que combina base teórica com 2,5 anos de estágio na indústria, em seis períodos de quatro meses (THOUGHTWORKS, 2026).
* **Revisão de código como aprendizado:** a revisão sempre serviu também para ensinar e para espalhar o conhecimento do sistema. Se ela diminui sem que outra prática ocupe esse papel, abre-se uma lacuna de compreensão.

## 4. Dívida Cognitiva em Escala de Equipe

O relatório afirma que a dívida técnica está se tornando **dívida cognitiva**: a distância entre a complexidade do sistema e o entendimento que as pessoas têm dele. A forma de medir o custo dessa dívida aparece entre as questões que o encontro deixou em aberto.

Kosmyna et al. (2025) usam o mesmo termo para o efeito sobre o indivíduo que delega o raciocínio à ferramenta. O relatório descreve o problema na escala da equipe: um sistema que cresce mais rápido do que a capacidade do time de compreendê-lo.

## 5. Síntese do Posicionamento

* A IA assume a escrita do código, mas não a responsabilidade por ele. O que sobra para o humano é especificar, verificar e compreender o sistema.
* Essas habilidades dependem de fundamentos. A formação continua necessária, e as tarefas de iniciante precisam ser substituídas por outras formas de aprendizado, e não apenas eliminadas.
* O risco central trazido pelo relatório não é a máquina escrever o código, e sim as equipes deixarem de entender o que foi escrito.

## Referências

* THOUGHTWORKS. **The Future of Software Engineering Retreat Findings and Strategic Insights**. 2026. Disponível em: [thoughtworks.com](https://www.thoughtworks.com/content/dam/thoughtworks/documents/report/tw_future%20_of_software_development_retreat_%20key_takeaways.pdf).
* THOUGHTWORKS. **Thoughtworks marks 25th anniversary of Agile Manifesto with Future of Software Development Retreat**. 2 fev. 2026. Disponível em: [thoughtworks.com](https://www.thoughtworks.com/en-us/about-us/news/2026/future-of-software-development-retreat).
* THORGEIRSSON, S.; WEIDMANN, T.; SU, Z. **Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency**. In: *Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems (CHI '26)*, 2026. DOI: [10.1145/3772318.3791666](https://doi.org/10.1145/3772318.3791666).
* KOSMYNA, N. et al. **Your Brain on ChatGPT: Accumulation of Cognitive Debt when Using an AI Assistant for Essay Writing Task**. 2025. Disponível em: [arxiv.org/abs/2506.08872](https://arxiv.org/abs/2506.08872).
