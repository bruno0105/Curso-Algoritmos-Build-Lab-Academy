### Aula 01 — O que é um Algoritmo
**Data:** 2026-05-07
**Link:** https://www.youtube.com/watch?v=M5ka2z5molg&list=PLWA6aa2tQjEFdsgi34pUC1e2IyzwXLhwr&index=2
**Instrutor:** Ellon
**Status:** ✅ Concluída

---

#### O que foi abordado

Primeira aula técnica do curso. O instrutor introduziu os conceitos fundamentais
que sustentam toda a lógica de programação: o que é um algoritmo, como ele pode
ser representado, em qual paradigma este curso se baseia e como o computador
executa um algoritmo na prática.

---

#### 1. Algoritmo *(0:46)*

Um algoritmo é uma **sequência lógica e ordenada de passos** com o objetivo de
realizar uma tarefa ou resolver um problema. Três características são essenciais:

- **Sequencial** — os passos têm ordem. Trocar a ordem muda o resultado.
- **Lógico** — cada passo deve fazer sentido dentro do contexto do problema.
- **Finito** — deve ter início, meio e fim definidos.

**Exemplo prático usado na aula — Trocar uma lâmpada *(2:40 – 5:15)*:**

O instrutor usou esse exemplo para mostrar que um algoritmo do cotidiano segue
a mesma lógica de um algoritmo computacional. A ordem dos passos é crítica:
pegar a escada antes de subir, desligar a energia antes de tocar na lâmpada.
Inverter qualquer passo quebra o algoritmo.

Esse raciocínio se aplica diretamente ao código: uma variável precisa ser
declarada antes de ser usada, uma condição precisa ser avaliada antes de executar
um bloco, um loop precisa ter critério de parada definido antes de rodar.

---

#### 2. Formas de Representação *(1:08)*

Algoritmos podem ser representados de diferentes formas:

| Representação | Descrição |
|---------------|-----------|
| Linguagem natural | Texto descritivo em português ou outro idioma |
| Lista numerada | Passos sequenciais em formato de lista |
| Pseudocódigo | Estrutura similar ao código, mas em linguagem humana |
| Fluxograma | Representação visual com símbolos padronizados |

O foco deste curso será em **fluxogramas**. A vantagem do fluxograma é tornar
o raciocínio visual — é possível enxergar o fluxo de decisões e repetições antes
de escrever uma linha de código.

> 💡 **Conexão com LP I (C):** No Code::Blocks, antes de escrever qualquer
> função, o fluxograma ajuda a mapear quais variáveis serão necessárias, quais
> condições existem e quantas iterações um loop precisa executar. É uma etapa
> de projeto, não de implementação.

---

#### 3. Paradigmas de Programação *(1:41)*

Um paradigma é o **modelo mental e estrutural** usado para criar sistemas. Define
como o programador organiza o raciocínio e a solução do problema.

O curso adota o paradigma **estruturado e sequencial *(2:17)***, que é
caracterizado por:

- Execução linha a linha, de cima para baixo
- Uso de três estruturas de controle: sequência, decisão e repetição
- Ausência de objetos, classes ou estados globais compartilhados

Esse é exatamente o paradigma da linguagem C — e o motivo pelo qual C é ensinada
no início de cursos de computação. Ela força o programador a pensar de forma
estruturada e explícita, sem abstrações que escondam o que está acontecendo na
memória.

> 💡 **Conexão com TADS:** No 3º semestre, com Orientação a Objetos em Java, o
> paradigma muda para o orientado a objetos. Compreender bem o paradigma
> estruturado agora torna a transição mais consciente — você entenderá o que o
> OO resolve que o estruturado não resolve facilmente.

---

#### 4. Funcionamento de um Sistema *(5:16)*

O instrutor explicou a relação entre três componentes fundamentais: