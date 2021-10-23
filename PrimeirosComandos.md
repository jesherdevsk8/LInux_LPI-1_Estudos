# Primeiros Comandos
___
### Comando para saber o SHELL - ($ <- visualiza a variável)
```
echo $SHELL
saída: /bin/bash
```

### Para saber se o comando é interno ou externo do SHELL
```
type echo
 echo é um comando interno do shell

type tar
 tar é /usr/bin/tar         <- comando externo
```

### Variável para saber locais onde estão os programas executáveis
```
echo $PATH
saída-> /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/home/boyah/.dotnet/tools

OBS: No meu caso apareceu .dotnet/tolls pois instalei o .NET core para Linux
```

### Comando para pesquisar aonde um comando está instalado
```
whereis clear
 saída-> clear: /usr/bin/clear /usr/share/man/man1/clear.1.gz
``` 	

### Variável Local e Global
```
Síntaxe: NUMERO=10
echo $NUMERO
 '10'   <-- obs: Abrindo outro bash a variável não irá funcionar, para isso vc tem q transforma-la em global, executando
export NUMERO   <- sendo assim se abrir outro bash, ela funcionará
```

- Exportar variável
```
export NUMERO
echo $NUMERO
 '10'
```

### Comando para visualizar somente as variáveis globais
```
env
```

### Comando para ver histórico dos comandos
- listar o histórico
```
history
```

- limpar histórico
```
history -c

echo $HISTFILE
 /home/boyah/.bash_history

```
### Variáveis importantes que caem na prova 101 da LPI-1
```
echo $SHELL
echo $HOME
echo $PWD
echo $PATH
echo $HISTFILE
echo $HISTSIZE
```

### Comando para mostrar todas variáveis do sistemas - globais e locais
* Como a saída na tela é bem grande, vamos paginar com comando |(pipe) less
```
set | less

 less = é comando de paginação
```

### Comandos básicos
- comandos de navegação
```
ls = listar

cd = change directory - mudar diretório

clear = limpa a tela

pwd = mostra o local onde estou

cd .. = volta um diretório
```
* mostrar data
```
date = mostra data - sex 22 out 2021 19:21:38 -03
```

- Apelidar um comando
```
alias cls="clear"
```

### Comandos de ajuda
```
man ping

bzip2 --help

whatis tar

apropos git
```
### Comandos em modo sequencial

- => ; ele executa o comando mesmo se o primeiro não funcionar
```
cd Downloads/;clear;ls -l
```
* => && se o primeiro comando não funcionar ele não executa o próximo 
```
sudo apt update && sudo apt upgrade
```
- => || se o primeiro comando estiver certo e o segundo comando errado, ele não executa o próximo
```
date || jrm  <- comando errado
```