# Bandit 7
#### O objetivo do nível é ler um arquivo e achar a flag que está do lado da palavra "millionth"
```
$ ssh bandit7@bandit.labs.overthewire.org -p 2220
```
A senha é a flag do nível anterior.

Esse nível é bem direto em seu objetivo. Por ter que procurar uma palavra no arquivo, o comando *grep* é o mais indicado pois ele printa linhas que seguem o padrão passado como parâmetro. Para usá-lo, vamos utilizar o pipe (|), que envia a saída de um comando como entrada para o próximo comando.
O comando que resultará na flag será:
```
$ cat data.txt | grep "millionth"
```
Isso significa que o comando *grep* está sendo aplicado à saída do comando *cat*, que é o conteúdo no arquivo data.txt, e procura nesse conteído pelo padrão que passamos como parâmetro, que é a palavra "millionth".

