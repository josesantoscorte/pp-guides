# Winget - Introdução

Como utilizar o winget para instalar e gerir os programas instalados no Windows

## Instalar

### Antes de instalarmos o winget podemos confirmar se ja está insalado no nosso sistema

```ps
winget --version
``` 

Caso o comando winget não exista o winget deve ser instalado

### Instalar o Winget

O winget pode ser facilmente instalado através da microsoft store. Após instalado o comando acima pode ser usado para verificar se foi corretamente instalado.

## Listar os Programas Instalados

Para listar os programas instalados no nosso sistema podemos usar:

```ps
winget list
```

## Instalar um Programa

### Procurar o Pacote
Para instalar um programa primeiro devemos procurar o devido pacote

```ps
winget search <nome do pacote>
```

*Nota: Caso o pacote tenha um nome com espaços podemos usar ' ' ou " " para fazer a procura, por exemplo:*

```ps
winget search 'Windows Notepad'

Name            Id           Version Source
---------------------------------------------
Windows Notepad 9MSMLRH6LZF3 Unknown msstore
```

### Instalar o Pacote
Depois de encontrar-mos o pacote podemos instala-lo usando o seu nome ou id

```ps
winget install --id <id do pacote>
```
ou
```
winget install --name <nome do pacote>
```

## Remover um Pacote
Para remover um pacote podemos utilizar novamento o id ou nome

```ps
winget remove <id do pacote>
```
ou
```ps
winget remove <nome do pacote>
```

## Atualizações
Uma das grandes vantagens de usar um gestor de pacotes é a facilidade com que podemos atualizar as aplicações instaladas no nosso sistema

### Atualizar a lista de pacotes
Antes de atualizarmos as nossas aplicações temos que atualizar a lista de pacotes do winget

Todos os pacotes:

```ps
winget upgrade --all
```

Individualmente:

```ps
winget upgrade --name <nome do pacote>
```
ou
```ps
winget upgrade --id <id do pacote>
```

