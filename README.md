# PesquisaJava
Como toda linguagem de programação existem diversos tipos de estruturas. Dentre elas, estruturas condicionais, estruturas de looping, além de mudar a sintaxe dos tipos de dados.
<p>No presente trabalho serão abordadas as estruturas e tipos de dados na linguagem Java.</p>


## Dados
 
 Nome: Marcos Vinícius Barros Freire; </p>
 Nome: Maria Clara Souza de Lima; </p>
 Turma: 2°A - DS; </p>
 Orientador: Prof° Aline; </p>
 
 
 ## Índice
 
 * <a href="#t1"> Tipos de Dados </a>
 * <a href="#t2"> Estruturas Condionais </a>
 * <a href="#t3"> Estruturas de Looping </a>
 * <a href="#t4"> Elementos (Views) </a>
 * <a href="t5"> Referências </a>

<h2 id="t1"> Tipos de dados </h2>

### Primitivos

Dados primitivos são aqueles que armazenam apenas um valor do seu tipo declarado por vez (seus valores não podem ser mudados), caso outro número seja colocado na variável seu valor inicial será alterado:


#### Byte: 

Armazena números inteiro, abrange números entre -128 a 127 (porém seu valor por padrão é 0). Seu tamanho é de 8 bits ( economizando muito espaço por ser quatro vezes menor que o tipo int).
Exemplo de sintaxe: byte tipoByte = 127;

#### Short: 

Armazena números inteiros, abrange números entre -32.768 a 32.767 (porém seu valor por padrão é 0). Seu tamanho é de 16 bits ( economizando muito espaço por ser duas vezes menor que o tipo int).
Exemplo de sintaxe: short tipoShort = 32767;

#### Int: 

Armazena números inteiros, abrange números entre -2.147.483.648 a 2.147.483.647(porém seu valor por padrão é 0). Seu tamanho é de 32 bits 
Exemplo de sintaxe:  int tipoInt = 2147483647;

#### Long:

O tipo de dado long faz parte dos inteiros, por isso é similar ao short e o int, ou seja, armazena números negativos e positivos, porém possui o dobro da capacidade de armazenamento do int, logo possui 64 bits.

#### Float e Double: 

São tipos de dados que fazem parte npumeros dos reais, ou seja, armazena casas decimais. A diferença entre eles é o armazenamento, enquanto o Float armazena 4 bytes, o Double armazena 8 bytes.

#### Boolean:

Armazena valores: verdadeiro (true) e falso (false). Seu tamanho é de 1 bit.
Exemplo de sintaxe: boolean tipoBooleano = true;

#### Char: 

Esse tipo de dado utiliza a tabela UNICODE e é utilizado para armazenar apenas um caractere, ou seja, 16 bits. Para resolver esse problema se utiliza de umas das classes invólucras, a string. Isso permite que se armazenem vários caracteres, ocupando 1 byte por caractere.

Existem várias outras classes invólucras, como se observa na imagem abaixo:

<center><img src="https://user-images.githubusercontent.com/128001916/228694287-5137ebf4-3e89-430e-8639-474a26a36d6a.png"></center>

### Por referência 

Dados por referência armazenam as localizações de objetos na memória do computador. Esses objetos podem conter diversas variáveis de instância (um valor diferente para cada objeto membro da classe) e métodos (procedimentos em outras linguagens de programação) dentro do objeto apontado. As variáveis de referência tem seu valor inicial nulo (null): 

**Arrays:** são utilizadas para definir os valores do mesmo tipo em alocações de memória contínuas.  
Exemplo de sintaxe: int [ ] idade = new int [10] (neste exemplo o array do tipo int começa no 0 e termina no 9) 

**String** [ ] nomes = {"Maria","Joao","Leonardo"}; (neste exemplo o array do tipo string possui 3 elementos) 
*String não é um tipo de dado primitivo pois seu valor pode ser modificado sendo um referencial* 


<h2 id="t2"> Estruras de Condicionais </h2>

A linguagem de programação Java, se assemelha ao C# em diversos aspectos, tendo poucas diferenças de sintaxe.
Adendo: as estruturas de condicionais ficam dentro da classe main. 
Ex:
```
public static void main(String[] args) {
	estruturas de condicionais
}
```

### Condional Simples

**Sintaxe:**

```
[tipo de dado] [nome das variáveis];

if (condição) {
	instruções;
}
```

**Exemplo:**

```
float media, nota1, nota2;

media = (nota1 + nota2) / 2

  if (media >= 7) {
		System.out.println(“Você foi aprovado com média de: ” + media);
}
```

### Condicional Composta

**Sintaxe:** 

```
[tipo de dado] [nome das variáveis];

if (condição) {
	instruções;
}
else{
	instruções;
}
```

**Exemplo:** 

```
float media, nota1, nota2;

media = (nota1 + nota2) / 2

	if (media>=7) {
		System.out.println(“Você foi aprovado com média de: “ + media);
   }
	else{
		System.out.println(“Você foi reprovado com média de: “ + media);
  }
```

### Condicional Encadeada

**Sintaxe:** 

```
[tipo de dado] [nome das variáveis];

if (condição) {
  instruções;
}
else if (condição) {
  instruções;
}
else{
  instruções;
}
```

**Exemplo:**

```
float media, nota1, nota2;

media = (nota1 + nota2) / 2

	if (media >= 7) {
		System.out.println(“Você foi aprovado com média: “ + media);
	}
	else if (media >= 4 && <6){
		System.out.println(“Você está de recuperação!”);
	}
	else {
		System.out.println(“Você foi reprovado com média: “ + media);
	}
 ```
 
 ### Condicional Witch/Case
 
<p>É uma alternativa para quando se possui múltiplos if ou else de forma encadeada.</p>
<p>O switch/case verifica o valor contido em uma variável, realizando comparações com cada instrução. Cada instrução é determinada por case.</p>
<p>Caso aconteça da variável não corresponder com nenhum dos casos, se executa o último bloco, nomeado de default.</p>

 
 **Sintaxe:**
 
 ```
switch (expressão) {
	
  case valor1: 
	  instruções;
	  break;

  case valor2: 
	  instruções;
	  break;

  case valorN: 
	  instruções;
	  break;

  default: 
    instruções;
    break; 
}
 ```
 
 **Exemplo:**
 
 ```
int dia;

dia = 7;

switch {
	
	case 1:
		System.out.println(“Hoje é Domingo!”);
		break;

	case 2:
		System.out.println(“Hoje é Segunda-Feira!”);
		break;

	case 3:
		System.out.println(“Hoje é Terça-Feira!”);
		break;

	case 4:
		System.out.println(“Hoje é Quarta-Feira!”);
		break;

	case 5:
		System.out.println(“Hoje é Quinta-Feira!”);
		break;

	case 6:
		System.out.println(“Hoje é Sexta-Feira!”);
		break;

	case 7:
		System.out.println(“Hoje é Sábado!”);
		break;

	default:
		System.out.println(“Dia inválido”);
		break;
}
```

<h2 id="t3"> Estruturas de Looping </h2>

Estruturas de repetição são utilizadas para repetição de partes de programas. 

### For 

For (para) é uma declaração de fluxo de controle que repete parte do programa diversas vezes. Entre as estruturas o “For” é a mais utilizada. Quando o número de  repetição é fixo se recomenda sua utilização
O for possui três formas: 

#### For simples 

Inicia a variável, checa sua condição, incrementa ou decrementa o valor. 

**Sintaxe:**

```
for(inicialização da variável; condição; alteração da variável) {  
       [comando]
}
```
 
#### For-each 

Conta os loops que serão usados durante a operação, você declara o tipo da variável seguido do nome do array utilizado durante a execução da aplicação. (A quantidade do array será a quantidade do loop). 

**Sintaxe:**

```
for (tipo da variável: array) 
{ 
    comandos usando a variável;
}
```

#### For marcado 

Reserva um nome para ser usado para cada um dos loops do programa. Facilita sua utilização várias vezes sem a necessidade de reescrevê-lo. 

**Sintaxe:**

```
nomedoLoop:  
for(inicialização; condição; alteração da variável) {  
	//comando
}
```

### While

While (enquanto) é uma declaração de fluxo de controle que executa parte do programa repetitivamente dependendo da condição dada a ela (repete até a condição ser falsa). Quando o número de repetição não for fixo se recomenda sua utilização

**Sintaxe:**

```
while (condição) {
	// código a ser executado
}
```


### Do while 

Do while (faça enquanto) é uma declaração de fluxo de controle que executa parte do programa pelo menos uma vez, e passa a executar repetitivamente dependendo da condição dada a ela (se a condição for falsa na sua primeira, não será repetido) . 
Quando o número de repetição não for fixo, mas precisa ser repetido pelo menos uma vez,  se recomenda sua utilização. 

**Sintaxe:**

```
do{
	// código a ser executado
} while (condição);
```

<h2 id="t4"> Elementos (Views) </h2>

### Buttons

### Text

### Widgets


<h2 id="t5"> Referências </h2>

https://www.javatpoint.com/pt/loops-em-java
https://blog.betrybe.com/for-java/#1
https://www.treinaweb.com.br/blog/estruturas-condicionais-e-estruturas-de-repeticao-em-java
https://www.jdevtreinamento.com.br/estruturas-de-repeticao-em-java/
https://productoversee.com/java-estruturas-de-repeticao/
http://excript.com/java/estrutura-repeticao-for-java.html 
http://tdsa2014.blogspot.com/2014/05/tipos-de-dados-primitivos-e-de.html 
https://www.devmedia.com.br/tipos-de-dados-por-valor-e-por-referencia-em-java/25293
https://www.academicotech.com/post/tipos-de-dados-em-java 
https://blog.grancursosonline.com.br/os-tipos-primitivos-da-linguagem-java/ 
https://www.javatpoint.com/pt/tipo-de-dado-em-java#:~:text=Existem%20dois%20tipos%20de%20dados,Incluem%20classes%2C%20interfaces%20e%20arrays. 
https://www.treinaweb.com.br/blog/estruturas-condicionais-e-estruturas-de-repeticao-em-java
https://blog.betrybe.com/java/switch-case-java/#3
https://www.computersciencemaster.com.br/estruturas-condicionais-if-else-lacos-de-repeticao-while-for-em-java/
https://www.youtube.com/watch?v=Y22RVgmE3PE
https://www.youtube.com/watch?v=JEAQeT7YGs4
https://rockcontent.com/br/talent-blog/estruturas-condicionais-2/#:~:text=As%20condicionais%20simples%20s%C3%A3o%20aquelas,a%20condi%C3%A7%C3%A3o%20definida%20seja%20satisfeita.

