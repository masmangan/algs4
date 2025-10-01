
# Introdução

Código e dados foram obtidos a partir da página do livro de Sedgewick e Wayne em: https://algs4.cs.princeton.edu/code/.
Este repositório foi criado como uma conveniência para alunos de disciplinas que adotam o livro, por exemplo, Algoritmos e Estruturas de Dados II.

O código foi obtido por meio de uma bifurcação do repositório original em https://github.com/kevin-wayne/algs4/ e os dados foram obtidos por um arquivo compactado em: https://algs4.cs.princeton.edu/code/algs4-data.zip. 

Para obter e descompactar o arquivo de dados:

```
wget https://algs4.cs.princeton.edu/code/algs4-data.zip
unzip algs4-data.zip
```

Os arquivos de dados ocupam aproximadamente 1 GB. Os maiores arquivos são dados de exemplos de grafos.

Todos os códigos e dados do livro foram instalados, embora apenas alguns códigos e arquivos sejam discutidos na disciplina.

# Compilação

Utilize o Maven para compilar as classes. 

```
mvn package
```

Desative a extensão do VS Code para Gradle, caso utilize o Maven.

Os arquivos compilados devem estar na pasta /target, junto com um arquivo algs4-1.0.0.0.jar.

Os arquivos de dados indicados no material e comentários estão na pasta /input.

# Exemplos

Para executar um dos exemplos apresentados em aula:


## Graph.java
Exemplos indicados nos comentários de Graph.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph tinyG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph mediumG.txt
```

O jshell (https://docs.oracle.com/en/java/javase/21/docs/specs/man/jshell.html) pode ser utilizado para executar os exemplos.

Para ler o tinyG.txt e apresentar a saída:

Ative o jshell:

```
jshell --class-path target/algs4-1.0.0.0.jar
```

No jshell, execute o método main() da classe Graph:

```
edu.princeton.cs.algs4.Graph.main(new String[]{"algs4-data/tinyG.txt"});
/exit
```

Para executar um método qualquer, basta utilizar os mesmos comandos de um programa Java, adaptando para a sintaxe do jshell.

Por exemplo, para obter uma imagem com o desenho do grafo, por meio do método toDot() da classe Graph:

Ative o jshell:

```
jshell --class-path target/algs4-1.0.0.0.jar
```

No jshell, apresente a saída do método toDot() da classe Graph:

```
import edu.princeton.cs.algs4.Graph;
import edu.princeton.cs.algs4.In;
import static java.lang.System.out;

In in = new In("algs4-data/tinyG.txt");
Graph G = new Graph(in);
System.out.println(G.toDot());
/exit
```

Copie a saída do método toDot() e utilize uma aplicação para desenhar o grafo, por exemplo, https://dreampuf.github.io/GraphvizOnline/.
Copie e cole a saída no editor da esquerda.

<img width="1349" height="801" alt="image" src="https://github.com/user-attachments/assets/e52b5845-5cdd-4822-ae0f-b86592853d17" />


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

## CC.java (Connected Components)

Exemplos indicados nos comentários de CC.java:

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.CC algs4-data/tinyG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.CC algs4-data/mediumG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.CC -Xss50m algs4-data/largeG.txt
```
