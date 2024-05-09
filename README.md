# Objetivo
Demonstrar a paralelização do problema de triplas pitagóricas com openCL.

<h2 align="center">
     <a> Tripla Pitagórica em openCL</a>
</h2>

<p align="center">
    Os códigos deste projeto tem como função encontrar triplas pitagóricas em um intervalo determinado. Fazendo uso da linguagem C o problema é executado em forma serial e também paralela com uso do openCL, e assim é gerado um arquivo .txt contendo as triplas encontradas.
</p>

<h4 align="left">
	🚧   Status: Concluído 🚀 🚧
</h4>


Tabela de conteúdos
=================
<!--ts-->
   * [O que é cada arquivo do projeto](#-o-que-é-cada-arquivo-do-projeto)
   * [Explicação geral do funcionamento dos códigos](#-explicação-geral-do-funcionamento-dos-códigos)
   * [Como executar o projeto](#-como-executar-o-projeto)
   * [Formato e conteúdos dos arquivos de saída](#-Formato-e-conteúdos-dos-arquivos-de-saída)
   * [Autores](#-autores)
<!--te-->


## 💻 O que é cada arquivo do projeto

O arquivo TriplasPitagoricasSerial.c contem o codigo serial para a execução do calculo das triplas na linguagem C. 

O arquivo TriplasPitagoricasParaleloOpenCL.c contem o codigo paralelo para a execução do calculo das triplas na linguagem C com o uso do OpenCL. 


## 💡 Explicação geral do funcionamento dos códigos

O código TriplasPitagoricasSerial.c possui uma função chamada tripla_pitagorica_c. Essa função possui três laços FOR aninhados que através de analise combinatoria realizam o calculo da quantidade de triplas pitagoricas. Além desse calculo, a função também cria o arquivo tripla.txt que irá receber o resultado dos cálculos. 

O código TriplasPitagoricasParaleloOpenCL.c possui no código do KERNEL três laços FOR aninhados que através de analise combinatoria realizam o cálculo da quantidade de triplas pitagoricas em um determinado intervalo. Quando encontradas, as tripla são armazenadas em um array e enviadas para o HOST e a partir dele inseridas em um arquivo triplaParalelo.txt.

## 🚀 Como executar o projeto

#### Pré-requisitos: É necessário possuir um compilador GCC e SKD especifico openCL para a sua máquina.

Para executar o código serial, o arquivo TriplasPitagoricasSerial.c deve ser copiado para o servidor e estando no local onde o arquivo foi salvo, deve ser executado o seguinte comando: 

gcc TriplasPitagoricasSerial.c -o TriplasPitagoricasSerial ./TriplasPitagoricasSerial



Para executar o código paralelo, o arquivo TriplasPitagoricasParaleloOpenCL.c deve ser copiado para o servidor e estando no local onde o arquivo foi salvo, deve ser executado o seguinte comando: 

gcc -L (usasr caso não encontre a biblioteca)  -I (usar caso não encontre o diretório dos headers) TriplasPitagoricasParaleloOpenCL.c -o tripla -lOpenCL



## 📝 Formato e conteúdos dos arquivos de saída

Os arquivos são no formato txt. O conteúdo são as triplas encontradas e quantidade total.


## 🦸 Autores

<a href="https://github.com/osvaldolimeirasantos">
 <img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/91644823?v=4" width="100px;" alt=""/>
 <sub><b>Osvaldo Limeira</b></sub></a> <a href="https://github.com/osvaldolimeirasantos" title="git Osvaldo Limeira">
</a>


<a href="https://github.com/jessicagreig1">
 <img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/34080482?v=4" width="100px;" alt=""/>
 <sub><b>Jessica Cerqueira </b></sub></a> <a href="https://github.com/jessicagreig1" title="git Jéssica Cerqueira">
</a>
 <br />



