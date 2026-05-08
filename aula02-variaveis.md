# Aula 02 · Variáveis

> 🔗 [Assistir no YouTube](https://www.youtube.com/watch?v=M5ka2z5molg&list=PLWA6aa2tQjEFdsgi34pUC1e2IyzwXLhwr&index=3)
> 📅 Data: 2026-05-07 · ✅ Concluída

Aula focada no conceito de variáveis — um dos pilares fundamentais de qualquer
algoritmo. O instrutor apresentou o que são variáveis, quais os
tipos básicos existentes em fluxogramas e as regras que devem ser seguidas para
nomeá-las corretamente.

---

## 1 · O que é uma Variável

Uma variável é um **espaço reservado na memória do computador** utilizado para
armazenar um valor temporariamente durante a execução de um programa. Esse valor
pode mudar ao longo da execução — daí o nome "variável".

Pense em uma variável como uma **caixa etiquetada**:

- A **etiqueta** é o nome da variável
- O **conteúdo** da caixa é o valor armazenado
- O **tamanho** da caixa é o tipo de dado

Quando o programa termina, todas as variáveis são destruídas — os valores não
persistem entre execuções. Para guardar dados de forma permanente, é necessário
usar arquivos ou bancos de dados (conteúdo de semestres futuros).

> 💡 Em C, toda variável precisa ser declarada antes de ser usada, informando
> obrigatoriamente o seu tipo: `int idade = 21;` — tipo `int`, nome `idade`, valor `21`.

---

## 2 · Tipos de Variáveis

O instrutor apresentou os quatro tipos básicos usados em fluxogramas, que
correspondem diretamente aos tipos primitivos das linguagens de programação:

| Tipo no Fluxograma | Descrição | Exemplos | Equivalente em C |
|--------------------|-----------|----------|-----------------|
| **Inteiro** | Números sem parte decimal | `1`, `42`, `-7`, `0` | `int` |
| **Real** | Números com parte decimal | `3.14`, `-0.5`, `9.99` | `float` / `double` |
| **Caracter** | Letras, símbolos e alfanuméricos | `'A'`, `"Bruno"`, `"abc123"` | `char` / `char[]` |
| **Lógico** | Apenas dois valores possíveis | `verdadeiro` / `falso` | `int` (0 ou 1) em C |

O instrutor mencionou ainda a existência de **estruturas de dados mais complexas**,
como vetores e matrizes, que armazenam múltiplos valores do mesmo tipo — conteúdo
abordado nos módulos seguintes.

### Por que o tipo importa?

O tipo define quanto espaço será reservado na memória e quais operações são válidas
sobre aquela variável. Não faz sentido somar dois caracteres ou comparar um número
com verdadeiro/falso sem uma conversão explícita.

Em C, esse controle é rígido e obrigatório — o compilador rejeita operações
incompatíveis com o tipo declarado. Isso é uma característica do paradigma
estruturado: o programador tem controle e responsabilidade total sobre os dados.

> ⚠️ Em C não existe tipo `bool` nativo no padrão C89/C90 — valores lógicos são
> representados por `int`, onde `0` equivale a falso e qualquer valor diferente
> de zero equivale a verdadeiro. O tipo `bool` passa a existir com `#include <stdbool.h>`
> no padrão C99 em diante.

---

## 3 · Regras de Nomenclatura

Nomear variáveis corretamente é uma questão tanto de **sintaxe** (o compilador
rejeita nomes inválidos) quanto de **boas práticas** (nomes ruins tornam o código
ilegível).

### Regras obrigatórias

**Não começar com número ou underline**

O nome de uma variável deve começar com uma letra. Começar com número causa erro
de compilação porque o compilador interpreta o caractere inicial como parte de um
valor numérico, não como um identificador.

```
✅ idade
✅ nota1
❌ 1nota      ← inválido: começa com número
❌ _valor     ← evitar: underline no início é reservado para identificadores do sistema
```

**Não usar espaços**

Espaço delimita tokens na linguagem. Um nome com espaço seria interpretado como
dois identificadores separados, causando erro de sintaxe.

```
✅ nomeCompleto
✅ nome_completo
❌ nome completo    ← inválido: interpretado como duas palavras separadas
```

**Evitar acentuação**

Caracteres acentuados (`á`, `ã`, `ç`, `é`) não fazem parte do conjunto de
caracteres ASCII padrão. Dependendo do compilador e do sistema operacional,
podem causar erros de compilação ou comportamento inesperado.

```
✅ situacao
✅ idade
❌ situação     ← evitar: caracter não ASCII
❌ médio        ← evitar: acento pode causar problema
```

**Não usar palavras reservadas**

Palavras reservadas são termos que a linguagem já usa para definir sua própria
estrutura — tipos, comandos e estruturas de controle. Usá-las como nome de
variável causa conflito de interpretação.

Exemplos de palavras reservadas em C:

| | | | |
|-|-|-|-|
| `int` | `float` | `char` | `double` |
| `if` | `else` | `while` | `for` |
| `return` | `void` | `struct` | `switch` |

```
✅ contador
✅ totalItens
❌ int      ← inválido: palavra reservada
❌ float    ← inválido: palavra reservada
❌ for      ← inválido: palavra reservada
```

**Garantir que cada nome seja único**

Dentro do mesmo escopo, duas variáveis não podem ter o mesmo nome. Redeclarar
uma variável já existente causa erro de compilação.

```c
int idade = 21;
int idade = 25;   // ❌ erro: redeclaração de variável no mesmo escopo
```

### Boas práticas além das regras

Além das regras obrigatórias, existem convenções amplamente adotadas no mercado
que tornam o código mais legível e profissional:

| Convenção | Estilo | Exemplo |
|-----------|--------|---------|
| camelCase | primeira palavra minúscula, demais com maiúscula | `nomeCompleto`, `totalVendas` |
| snake_case | palavras separadas por underline | `nome_completo`, `total_vendas` |
| Nomes descritivos | o nome deve revelar a intenção | `idade` em vez de `x`, `totalAlunos` em vez de `t` |

> 💡 Em C, a convenção mais comum é `snake_case` para variáveis e funções.
> Independente do estilo adotado, o mais importante é a consistência —
> não misturar convenções no mesmo projeto.

---

## 4 · Exercício Prático da Aula

O instrutor realizou um exercício ao final para testar a compreensão das regras.
O objetivo era identificar quais nomes de variáveis são válidos ou inválidos:

| Nome | Válido? | Motivo |
|------|---------|--------|
| `nomeAluno` | ✅ | Começa com letra, sem espaço, sem acento |
| `1nota` | ❌ | Começa com número |
| `nota final` | ❌ | Contém espaço |
| `situação` | ❌ | Contém acento |
| `int` | ❌ | Palavra reservada |
| `total_vendas` | ✅ | Snake case válido |
| `_interno` | ⚠️ | Tecnicamente válido, mas reservado por convenção para o sistema |

---

## 5 · Conexão com C e LP I

Tudo que foi visto nesta aula se aplica diretamente à linguagem C:

```c
#include <stdio.h>

int main() {
    // Declaração de variáveis com tipo explícito
    int    idade       = 21;
    float  altura      = 1.75;
    char   inicial     = 'B';

    // Uso das variáveis
    printf("Idade: %d\n", idade);
    printf("Altura: %.2f\n", altura);
    printf("Inicial: %c\n", inicial);

    return 0;
}
```

Cada tipo declarado reserva uma quantidade específica de memória:

| Tipo | Tamanho típico | Faixa de valores |
|------|---------------|------------------|
| `char` | 1 byte | -128 a 127 |
| `int` | 4 bytes | -2.147.483.648 a 2.147.483.647 |
| `float` | 4 bytes | ~6 casas decimais de precisão |
| `double` | 8 bytes | ~15 casas decimais de precisão |

---

## Checklist de Revisão

- [ ] Variável é um espaço nomeado na memória para armazenar um valor temporário
- [ ] Os quatro tipos básicos são: inteiro, real, caracter e lógico
- [ ] Nome de variável não pode começar com número ou underline
- [ ] Nome de variável não pode conter espaços
- [ ] Evitar acentuação para garantir compatibilidade
- [ ] Não usar palavras reservadas como nome de variável
- [ ] Cada variável deve ter um nome único dentro do mesmo escopo
- [ ] Em C, o tipo é obrigatório na declaração

---