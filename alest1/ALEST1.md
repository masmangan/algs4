# Instalação

Este repositório contém o código Java que acompanha o livro *Algorithms, 4th Edition*, de Robert Sedgewick e Kevin Wayne. O código e os dados são mantidos separadamente. Para as instruções de obtenção dos dados e o contexto do repositório, consulte [ALEST2.md](/alest2/ALEST2.md).

O código e os dados de exemplo foram obtidos a partir da página do livro de Sedgewick e Wayne em: https://algs4.cs.princeton.edu/code/.

Os dados não são versionados no repositório e devem ser obtidos em: https://algs4.cs.princeton.edu/code/algs4-data.zip.

Para obter e descompactar o arquivo de dados:

```
wget https://algs4.cs.princeton.edu/code/algs4-data.zip
unzip algs4-data.zip
```

# Compilação

Utilize o Maven para compilar as classes.

```
mvn package
```

Os arquivos compilados devem estar na pasta `target`. Os exemplos abaixo usam `target/algs4-1.0.0.0.jar`.

# Modelos

O repositório oferece implementações de tipos elementares, coleções lineares, pesquisa, ordenação e union-find. A documentação de cada classe aponta para as seções correspondentes do material de [Sedgewick e Wayne](https://algs4.cs.princeton.edu/code/).

TODO: o repositório não contém um diagrama de modelos dedicado aos tipos e estruturas de ALEST I. Avaliar a criação de um diagrama quando houver uma fonte didática para ele.

# Exemplos

Os comandos abaixo adaptam os exemplos presentes nos comentários das classes para a organização deste repositório. Os arquivos de dados referenciados precisam estar disponíveis em `algs4-data`.

# UNIDADE 02: Estruturas lineares

## 2.1. Estruturas contíguas X Estruturas encadeadas

As versões por vetor redimensionável e por lista encadeada presentes no repositório permitem contrastar as duas representações. Consulte [LinkedBag.java](/src/main/java/edu/princeton/cs/algs4/LinkedBag.java), [ResizingArrayBag.java](/src/main/java/edu/princeton/cs/algs4/ResizingArrayBag.java), [LinkedStack.java](/src/main/java/edu/princeton/cs/algs4/LinkedStack.java), [ResizingArrayStack.java](/src/main/java/edu/princeton/cs/algs4/ResizingArrayStack.java), [LinkedQueue.java](/src/main/java/edu/princeton/cs/algs4/LinkedQueue.java) e [ResizingArrayQueue.java](/src/main/java/edu/princeton/cs/algs4/ResizingArrayQueue.java).

## 2.2. Coleções e suas operações de acesso

### 2.2.1. Listas

TODO: o repositório não inclui uma implementação denominada `List`. Usar as coleções encadeadas e com vetor redimensionável como ponto de partida, conforme a ementa da disciplina.

### 2.2.2. Pilhas

#### Stack

Pilha genérica LIFO implementada com lista simplesmente encadeada: [Stack.java](/src/main/java/edu/princeton/cs/algs4/Stack.java). Há ainda [LinkedStack.java](/src/main/java/edu/princeton/cs/algs4/LinkedStack.java) e [ResizingArrayStack.java](/src/main/java/edu/princeton/cs/algs4/ResizingArrayStack.java). Consulte a [Seção 1.3](https://algs4.cs.princeton.edu/13stacks/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Stack < algs4-data/tobe.txt
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.LinkedStack < algs4-data/tobe.txt
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.ResizingArrayStack < algs4-data/tobe.txt
```

### 2.2.3. Filas

#### Queue

Fila genérica FIFO implementada com lista encadeada: [Queue.java](/src/main/java/edu/princeton/cs/algs4/Queue.java). As alternativas presentes são [LinkedQueue.java](/src/main/java/edu/princeton/cs/algs4/LinkedQueue.java) e [ResizingArrayQueue.java](/src/main/java/edu/princeton/cs/algs4/ResizingArrayQueue.java). Consulte a [Seção 1.3](https://algs4.cs.princeton.edu/13stacks/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Queue < algs4-data/tobe.txt
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.LinkedQueue < algs4-data/tobe.txt
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.ResizingArrayQueue < algs4-data/tobe.txt
```

# UNIDADE 03: Classificação e pesquisa

## 3.1. Pesquisa sequencial X pesquisa binária

### SequentialSearchST

Tabela de símbolos com pesquisa sequencial em uma lista encadeada não ordenada: [SequentialSearchST.java](/src/main/java/edu/princeton/cs/algs4/SequentialSearchST.java). Consulte a [Seção 3.1](https://algs4.cs.princeton.edu/31elementary/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.SequentialSearchST < algs4-data/tinyST.txt
```

### BinarySearch

#### BinarySearch

Pesquisa binária em um vetor ordenado de inteiros. Os dados de exemplo estão na [Seção 1.1](https://algs4.cs.princeton.edu/11model/) do livro e a implementação está em [BinarySearch.java](/src/main/java/edu/princeton/cs/algs4/BinarySearch.java).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.BinarySearch algs4-data/tinyAllowlist.txt < algs4-data/tinyText.txt
```

#### StaticSETofInts

Conjunto estático de inteiros mantido em vetor ordenado e consultado por pesquisa binária. Consulte [StaticSETofInts.java](/src/main/java/edu/princeton/cs/algs4/StaticSETofInts.java) e a [Seção 1.2](https://algs4.cs.princeton.edu/12oop/).

TODO: a classe não fornece um cliente `main()`; incluir um exemplo executável apenas se houver um cliente correspondente no material da disciplina.

## 3.2. Classificação de dados

As implementações de classificação existentes no repositório estão listadas abaixo. Os comentários das classes indicam a forma de execução e, quando aplicável, os dados de exemplo.

### 3.2.1. Bubble Sort

TODO: não há uma implementação de Bubble Sort no repositório.

### 3.2.2. Insertion Sort

#### Insertion

[Insertion.java](/src/main/java/edu/princeton/cs/algs4/Insertion.java) — [Seção 2.1](https://algs4.cs.princeton.edu/21elementary/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Insertion < algs4-data/tiny.txt
```

### 3.2.3. Mergesort

#### Merge e MergeBU

[Merge.java](/src/main/java/edu/princeton/cs/algs4/Merge.java) e [MergeBU.java](/src/main/java/edu/princeton/cs/algs4/MergeBU.java) — [Seção 2.2](https://algs4.cs.princeton.edu/22mergesort/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Merge < algs4-data/tiny.txt
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.MergeBU < algs4-data/tiny.txt
```

### 3.2.4. Quicksort

#### Quick e Quick3way

[Quick.java](/src/main/java/edu/princeton/cs/algs4/Quick.java) e [Quick3way.java](/src/main/java/edu/princeton/cs/algs4/Quick3way.java) — [Seção 2.3](https://algs4.cs.princeton.edu/23quicksort/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Quick < algs4-data/tiny.txt
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Quick3way < algs4-data/tiny.txt
```

# UNIDADE 04: Árvores

## 4.1. Definições e representação

TODO: não há no repositório um material introdutório ou diagrama específico para as definições e representações de árvores.

## 4.2. Árvores genéricas

TODO: não há uma implementação de árvore genérica identificada no repositório.

## 4.3. Árvores binárias de pesquisa

### BST

[BST.java](/src/main/java/edu/princeton/cs/algs4/BST.java) implementa uma tabela de símbolos ordenada em uma árvore binária de pesquisa. Consulte a [Seção 3.2](https://algs4.cs.princeton.edu/32bst/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.BST < algs4-data/tinyST.txt
```

## 4.4. Operações: caminhamento, pesquisa, inserção, remoção

As operações disponíveis em [BST.java](/src/main/java/edu/princeton/cs/algs4/BST.java) incluem `get`, `put`, `delete`, `min`, `max`, `floor`, `ceiling`, `rank`, `select` e iteração das chaves. O cliente `main()` da classe imprime as chaves em ordem crescente.

TODO: confirmar quais caminhamentos devem receber exemplos explícitos; o repositório não oferece um cliente separado para os caminhamentos da árvore binária de pesquisa.

## 4.5. Árvores balanceadas e sua eficiência

### RedBlackBST

[RedBlackBST.java](/src/main/java/edu/princeton/cs/algs4/RedBlackBST.java) implementa uma tabela de símbolos ordenada como árvore rubro-negra. Consulte a [Seção 3.3](https://algs4.cs.princeton.edu/33balanced/).

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.RedBlackBST < algs4-data/tinyST.txt
```
