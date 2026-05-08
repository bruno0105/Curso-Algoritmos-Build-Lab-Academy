# Aula 01 · O que é um Algoritmo

> 🔗 [Assistir no YouTube](https://www.youtube.com/watch?v=M5ka2z5molg&list=PLWA6aa2tQjEFdsgi34pUC1e2IyzwXLhwr&index=2)
> 📅 Data: 2026-05-07 · ✅ Concluída

Primeira aula técnica do curso. O instrutor Ellon introduziu o conceito de
algoritmo, as formas de representá-lo, o paradigma adotado no curso e o
funcionamento interno de um sistema computacional.

---

## 1 · O que é um Algoritmo

Um algoritmo é uma **sequência lógica e ordenada de passos** com o objetivo
de realizar uma tarefa ou resolver um problema. Três características essenciais:

- **Sequencial** — os passos têm ordem. Trocar a ordem muda o resultado
- **Lógico** — cada passo deve fazer sentido dentro do contexto do problema
- **Finito** — deve ter início, meio e fim definidos

O instrutor ilustrou com o exemplo de **trocar uma lâmpada**: a ordem é crítica —
desligar a energia antes de tocar na lâmpada, pegar a escada antes de subir.
Inverter qualquer passo quebra o algoritmo.

Esse raciocínio se aplica diretamente ao código: variável declarada antes de
usada, condição avaliada antes de executar o bloco, loop com critério de parada
definido antes de rodar.

---

## 2 · Formas de Representação

Algoritmos podem ser representados de diferentes formas:

| Forma | Descrição |
|-------|-----------|
| Linguagem natural | Texto descritivo em português |
| Lista numerada | Passos sequenciais em formato de lista |
| Pseudocódigo | Estrutura similar ao código, mas em linguagem humana |
| **Fluxograma** | Representação visual com símbolos padronizados ← foco do curso |

> 💡 O fluxograma é ferramenta de projeto, não de implementação.
> Usar antes de abrir o editor para mapear variáveis, condições e iterações.

---

## 3 · Paradigmas de Programação

Um paradigma é o **modelo mental e estrutural** usado para criar sistemas.
O curso adota o paradigma **estruturado e sequencial**, caracterizado por:

- Execução linha a linha, de cima para baixo
- Três estruturas de controle: sequência, decisão e repetição
- Sem objetos, classes ou estados globais compartilhados

Esse é o paradigma da linguagem C — e o motivo pelo qual C é ensinada no início
de cursos de computação. Força o programador a pensar de forma explícita, sem
abstrações que escondam o que acontece na memória.

> 💡 No 3º semestre, com Orientação a Objetos em Java, o paradigma muda.
> Compreender bem o estruturado agora torna essa transição mais consciente.

---

## 4 · Funcionamento de um Sistema

O instrutor explicou a relação entre três componentes fundamentais:

| Componente | Papel |
|------------|-------|
| Algoritmo | Conjunto de instruções — o programa escrito |
| Memória (RAM) | Armazena o algoritmo e os valores das variáveis em execução |
| Processador | Lê e executa cada instrução em sequência |

O computador carrega o algoritmo na memória para que o processador execute
os passos lógicos — exatamente o que acontece quando um programa em C é
compilado e executado no Code::Blocks.

> 💡 Esse modelo é o mesmo estudado em Arquitetura de Computadores.
> A diferença é que lá o foco é no hardware; aqui é em como o software usa esse hardware.

---

## 5 · Processamento de Dados *(prévia da próxima aula)*

O instrutor antecipou o modelo central da próxima aula, comparando o
processamento computacional ao raciocínio humano:

**Entrada → Processamento → Saída**

Em C:

```c
scanf("%d", &valor);       // ENTRADA
resultado = valor * 2;     // PROCESSAMENTO
printf("%d", resultado);   // SAÍDA
```

---

## Checklist de Revisão

- [ ] A ordem dos passos é determinante — inverter gera resultado errado
- [ ] Fluxograma é ferramenta de projeto — usar antes de abrir o editor
- [ ] O paradigma estruturado é a base de C
- [ ] O modelo Entrada → Processamento → Saída aparece em toda aula daqui para frente

---

*Documentado com apoio do Claude · Anthropic*
