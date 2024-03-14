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
