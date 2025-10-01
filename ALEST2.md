
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

Se o projeto

Os arquivos compilados devem estar na pasta /target, junto com um arquivo algs4-1.0.0.0.jar.

Os arquivos de dados indicados no material e comentários estão na pasta /input.

# Exemplos

Para executar um dos exemplos apresentados em aula:


## BreadthFirstPaths

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph algs4-data/tinyCG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.BreadthFirstPaths algs4-data/tinyCG.txt 0

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.BreadthFirstPaths algs4-data/largeG.txt 0
```

## DepthFirstPaths

```
java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.Graph algs4-data/tinyCG.txt

java -cp target/algs4-1.0.0.0.jar edu.princeton.cs.algs4.DepthFirstPaths algs4-data/tinyCG.txt 0
```

