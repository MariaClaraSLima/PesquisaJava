# PesquisaJava
Pesquisa sobre tipos de dados, estruras de condicional e de repetição, na linguagem Java.

<h3> Dados </h3>
  <p> Nome: Marcos Vinícius Barros Freire; </p>
  <p> Nome: Maria Clara Souza de Lima; </p>
  <p> Turma: 2°A - DS; </p>
  <p> Orientador: Prof° Aline; </p>
  

<h2> Tipos de dados </h2>
Primitivos
Dados primitivos são aqueles que armazenam apenas um valor do seu tipo declarado por vez (seus valores não podem ser mudados), caso outro número seja colocado na variável seu valor inicial será alterado:


 Byte: armazena números inteiro, abrange números entre -128 a 127 (porém seu valor por padrão é 0). Seu tamanho é de 8 bits ( economizando muito espaço por ser quatro vezes menor que o tipo int).
Exemplo de sintaxe: byte tipoByte = 127;

short: armazena números inteiros, abrange números entre -32.768 a 32.767 (porém seu valor por padrão é 0). Seu tamanho é de 16 bits ( economizando muito espaço por ser duas vezes menor que o tipo int).
Exemplo de sintaxe: short tipoShort = 32767;

int: armazena números inteiros, abrange números entre -2.147.483.648 a 2.147.483.647(porém seu valor por padrão é 0). Seu tamanho é de 32 bits 
Exemplo de sintaxe:  int tipoInt = 2147483647;

boolean:armazena valores: verdadeiro (true) e falso (false). Seu tamanho é de 1 bit.
Exemplo de sintaxe: boolean tipoBooleano = true;


Por referência 
Dados por referência armazenam as localizações de objetos na memória do computador. Esses objetos podem conter diversas variáveis de instância (um valor diferente para cada objeto membro da classe) e métodos (procedimentos em outras linguagens de programação) dentro do objeto apontado. As variáveis de referência tem seu valor inicial nulo (null): 

Arrays: são utilizadas para definir os valores do mesmo tipo em alocações de memória contínuas.  
Exemplo de sintaxe: int [ ] idade = new int [10] (neste exemplo o array do tipo int começa no 0 e termina no 9) 

String [ ] nomes = {"Maria","Joao","Leonardo"}; (neste exemplo o array do tipo string possui 3 elementos) 
*String não é um tipo de dado primitivo pois seu valor pode ser modificado sendo um referencial* 


Referências:

http://tdsa2014.blogspot.com/2014/05/tipos-de-dados-primitivos-e-de.html 
https://www.devmedia.com.br/tipos-de-dados-por-valor-e-por-referencia-em-java/25293
https://www.academicotech.com/post/tipos-de-dados-em-java 
https://blog.grancursosonline.com.br/os-tipos-primitivos-da-linguagem-java/ 
https://www.javatpoint.com/pt/tipo-de-dado-em-java#:~:text=Existem%20dois%20tipos%20de%20dados,Incluem%20classes%2C%20interfaces%20e%20arrays. 


<h2> Estruras de Condicional </h2>

<h2> Estruturas de Looping </h2>

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
