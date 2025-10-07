
# Instalação

Este repositório foi criado como uma conveniência para aulas de disciplinas que adotam o livro de Sedgewick e Wayne, por exemplo, Algoritmos e Estruturas de Dados II. O objetivo desse procedimento é evitar modificar o repositório original, para poder acompanhar correções eventuais por parte dos autores originais.

Note que código e dados estão em pastas separadas, por isso, os comandos para executar os exemplos devem ser adaptados. A seguir, são indicadas as adaptações necessárias para cada apresentado usado em aula.

Código e dados foram obtidos a partir da página do livro de Sedgewick e Wayne em: https://algs4.cs.princeton.edu/code/. 

O código foi obtido por meio de uma bifurcação do repositório original em https://github.com/kevin-wayne/algs4/.

Para utilizar o repositório, faça uma bifucação (botão Fork) e instale os arquivos de dados do livro localmente ou usando o CodeSpaces.

Os dados não são versionados no repositório e devem ser obtidos em: https://algs4.cs.princeton.edu/code/algs4-data.zip. 
Os arquivos de dados ocupam aproximadamente 1 GB. Os maiores arquivos são dados de exemplos de grafos.

Para obter e descompactar o arquivo de dados:

```
wget https://algs4.cs.princeton.edu/code/algs4-data.zip
unzip algs4-data.zip
```

Após esse procedimento, todos os códigos e dados do livro foram instalados, embora apenas alguns códigos e arquivos sejam discutidos na disciplina.


# Compilação

Utilize o Maven para compilar as classes. 

```
mvn package
```

Desative a extensão do VS Code para Gradle, caso utilize o Maven.

Os arquivos compilados devem estar na pasta `target`. Utilizaremos o `arquivo algs4-1.0.0.0.jar`.

Os arquivos de dados indicados no material e comentários estão na pasta `algs4-data`.

# Exemplos

Para executar um dos exemplos apresentados em aula:


## Graph.java
Exemplos indicados nos comentários de `Graph.java`:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph algs4-data/tinyG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph algs4-data/mediumG.txt
```

O `jshell` (https://docs.oracle.com/en/java/javase/21/docs/specs/man/jshell.html) pode ser utilizado para executar os exemplos.
Neste caso, as classes e exemplos podem ser executados sem a necessidade de criar novos programas.

Por exemplo, para ler os dados do arquivo `tinyG.txt` e executar o método `main()`, basta utilizar os comandos a seguir no terminal.

Ative o `jshell`:

```
jshell --class-path target/algs4-1.0.0.0.jar
```

No jshell, execute o método main() da classe Graph. O comando `/exit` encerra a execução do jshell e retorna ao terminal.

```
edu.princeton.cs.algs4.Graph.main(new String[]{"algs4-data/tinyG.txt"});

/exit
```

Para executar um método qualquer, basta utilizar os mesmos comandos que seriam usados em um programa Java, adaptados para a sintaxe do jshell.

Por exemplo, para obter uma imagem com o desenho do grafo, por meio do método toDot() da classe Graph:

Ative o jshell:

```
jshell --class-path target/algs4-1.0.0.0.jar

import edu.princeton.cs.algs4.Graph;
import edu.princeton.cs.algs4.In;
import static java.lang.System.out;

In in = new In("algs4-data/tinyG.txt");
Graph G = new Graph(in);
System.out.println(G.toDot());

/exit
```

Para aproveitar a saída do programa, copie a saída do método toDot() no jshell e utilize uma aplicação para desenhar o grafo, por exemplo, https://dreampuf.github.io/GraphvizOnline/. Copie e cole a saída no editor da esquerda.

O resultado será uma imagem com base nos dados do grafo:

<img width="1349" height="801" alt="image" src="https://github.com/user-attachments/assets/e52b5845-5cdd-4822-ae0f-b86592853d17" />

As adaptações dos comandos apresentados no livros e nos comentários das classes são apresentadas a seguir.

## BreadthFirstPaths

Exemplos indicados nos comentários de BreadthFirstPaths.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph algs4-data/tinyCG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.BreadthFirstPaths algs4-data/tinyCG.txt 0

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.BreadthFirstPaths algs4-data/largeG.txt 0
```

## DepthFirstPaths

Exemplos indicados nos comentários de DepthFirstPaths.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph algs4-data/tinyCG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.DepthFirstPaths algs4-data/tinyCG.txt 0
```

## Cycle

Exemplos indicados nos comentários de Cycle.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Cycle algs4-data/tinyG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Cycle algs4-data/mediumG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Cycle algs4-data/largeG.txt

```


## CC (Connected Components)

Exemplos indicados nos comentários de CC.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.CC algs4-data/tinyG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.CC algs4-data/mediumG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.CC -Xss50m algs4-data/largeG.txt
```


# Digraph

# Topological
Exemplos indicados nos comentários de Topological.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Topological algs4-data/jobs.txt /
```