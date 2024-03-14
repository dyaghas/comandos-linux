# comandos-linux
comandos em Linux utilizados na aula de SO.


## man
manual, explica o funcionamento e como usar um comando. Exemplo:
```bash
# Exibe o manual do comando ls
man ls
```
## ls
list, exibe todas as pastas e arquivos no diretório atual. Exemplo:

```bash
ls -l
```
O parâmetro -l é opcional e exibe diversas caracteristicas de cada diretório como quem tem direito a acessar e data de modificação

## cd
Change directory, acessa o diretório especificado: 

```bash
cd Downloads/exemplo
```
Aceita diversos parâmetros como .. por exemplo, movendo para o diretório anterior que é Downloads nesse caso.

## pwd
print working directory, exibe o diretório atual

```bash
pwd

# pode retornar /home/user/Downloads, por exemplo
```

## mkdir e rmdir
mkdir cria um diretório com o nome especificado e rmdir remove um diretório.

```bash
mkdir diretorio/de/destino
rmdir diretorio/de/destino
```
#### Atenção: rmdir não exclui diretórios vazios caso não seja inserido nenhum parâmetro para tal situação

## nano, touch, vi

Os três comandos servem para criar um arquivo. Touch cria um arquivo vazio, nano abre um editor amigável para digitar o conteúdo e vi permite modificações mais avançadas e consequentemente exige mais conhecimento.

```bash
touch arquivo.txt
nano arquivo.txt
vi arquivo.txt
```

#### Importante: o comando touch muda a data de modificação quando utilizado em arquivos já existentes, nada mais. Por outro lado, vi e nano podem ser utilizados para editar arquivos também.

## cat
Concatenate, comando que exibe o conteúdo de um ou mais arquivos juntos. Esse comando não realiza nenhuma modificação no arquivo por si só, apenas exibe o conteúdo concatenado.

```bash
cat arquivo1.txt arquivo2.txt

# pode retornar:
Esse é o conteúdo do arquivo1.txt
Esse é o conteúdo do arquivo2.txt
```

## clear
Limpa o terminal.

##cp e mv
copy e move. Servem para copiar e mover arquivos, a sintaxe é bem semelhante.

```bash
cp arquivo.txt diretorio/de/destino
mv arquivo.txt diretorio/de/destino
```

## wc
Esse comando conta a quantidade de linhas, palavras e bytes em um arquivo ou outro input. Exemplo

```bash
wc arquivo.txt

# pode retornar:
2  33  140  arquivo.txt
```

## exit
Dispensa comentários

## shutdown
Desliga ou reboota o sistema, podendo ser utilizado com diversos parâmetros.

## more e less
Comandos utilizados para exibir conteúdo de texto. Podem ser utilizados em junção com outros comandos como cat. Less possui mais funcionalidades do que more.

```bash
# comando cat e less
cat | less
```

## find
Procura por arquivos no diretório atual e seus filhos, por exemplo:

```bash
# parâmetros para encontrar todos os arquivos com extensão .txt
find -name "*.txt"
```

## chmod
Altera as permissões de um arquivo ou diretório. Há diversas formas de utilizar esse comando como a seguinte:

```bash
chmod 735 arquivo.txt
```

Esse comando dá as permissões rwx-wxr-x, mas como eu sei o que significa esses números? Cada um dos três números representa as permissões de um grupo em binário. 1 significa que aquela permissão foi dada e 0, que não foi dada aquele usuário ou grupo, ou seja:
7 = 111 (rwx) Permissão para read, write e execute
3 = 011 (-wx) Permissão para write e execute
5 = 101 (r-x) Permissão para read e execute
Os grupos são owner, group e others respectivamente.

## history
Exibe os comandos previamente digitados no terminal em ordem cronológica a partir do mais recente. Os comandos são exibidos com um número ao lado que ao ser digitado com uma !, executa tal comando, exemplo:

```bash
# output do comando history
...
72 history
73 ls
74 rmdir

# executa o comando na linha 73
!73
```
## who
Exibe detalhes dos usuários que estão logados atualmente no sistema como nome e horário de login.
