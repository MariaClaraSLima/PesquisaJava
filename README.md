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

<div align="center">
	<img src="https://user-images.githubusercontent.com/128001916/228694287-5137ebf4-3e89-430e-8639-474a26a36d6a.png" width="500px" height="300px"/>
</div>

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

**Button:**

O *button* é um elemento no qual o usuário pode clicar para executar uma ação.

*Sintaxe:*

```
<Button
     android:id="@+id/button_id"
     android:layout_height="wrap_content"
     android:layout_width="wrap_content"
     android:text="@string/self_destruct" />
```
**Image Button:**

Possui características muito similares ao *button*, porém ao invés de exibir um texto no botão, será exibido uma imagem.

*Sintaxe:*

```
<?xml version="1.0" encoding="utf-8"?>
 <selector xmlns:android="http://schemas.android.com/apk/res/android">
     <item android:state_pressed="true"
           android:drawable="@drawable/button_pressed" /> <!-- pressed -->
     <item android:state_focused="true"
           android:drawable="@drawable/button_focused" /> <!-- focused -->
     <item android:drawable="@drawable/button_normal" /> <!-- default -->
 </selector>
```

**Chips:**

São elementos compactados que representam entidades, atributos, ação ou texto. Este tipo de elemento é utilizado para inserir informações, filtrar conteúdo, acionar uma ação ou até mesmo filtrar conteúdo.

*Atributos básicos*

```
android:checkable //Muda de acordo com a condição (true ou false)
android:text //Coloca o texto do chip.
app:chipIcone app:chipIconEnabled  //Coloca um ícone no chip
app:checkedIcone app:checkedIconEnabled //Coloca ícone personalizado (depois de selecionado).
app:closeIcone app:closeIconEnabled //Coloca um ícone personalizado no qual o usuário pode clicar para fechar. 
```

*Sintaxe:*
```
public Chip (Context context, 
                AttributeSet attrs, 
                int defStyleAttr)
```

**GroupChips:**

Como o nome sugere, este elemento armazena grupos de chips, ou seja, vários chips. Por padrão esses chips serão organizados em várias linhas, porém pode-se utilizar a propriedade `app:singleLine` para colocar apenas em uma linha horizontal. Dependendo da quantidade de chips pode-se utilizar a propriedade `HorizontalScrollView`, isso fará com que habilite um scroll de rolagem horizontal.

*Sintaxe:*
```
public ChipGroup (Context context, 
                AttributeSet attrs, 
                int defStyleAttr)
```

**CheckBox:**

Esse elemento é um tipo de botão, porém com uma característica de poder ser marcado ou desmarcado conforme a necessidade do usuário.

*Sintaxe:*

```
public CheckBox (Context context, 
                AttributeSet attrs, 
                int defStyleAttr, 
                int defStyleRes)
```

**RadioGroup:**

Este elemento é uma classe utilizada para desmarcar qualquer outro botão que esteja dentro do grupo (RadioButtons), ou seja, ao marcar este botão o restante é desmarcado e apesar alguns de opção específica não possam ser desmarcados, podem ser limpos para remover a marcação, garantindo assim que apenas uma opção será marcada. 

*Sintaxe:*

```
<RadioGroup xmlns:android="Url de referência a objeto"
       Botões da classe
</RadioGroup>
```

**RadioButton:** 

Este elemento é um botão de rádio que pode ter dois estados, marcado ou desmarcado, porém o usuário não pode desmarcá - lo uma vez que marcou, por isso é utilizado dentro da classe RadioGroup. 

<div align="center">
	<img src="https://user-images.githubusercontent.com/128001916/230232684-176417e3-8540-458a-b32e-228b68954582.png" width="400px"/>
</div>

*Sintaxe:* 
```
<RadioGroup xmlns:android="Url de referência a objeto"
```

```
<RadioButton android:id="@+id/radio_pirates"
	android:layout_width="wrap_content"
	android:layout_height="wrap_content"
	android:text="@string/pirates"
	android:onClick="onRadioButtonClicked"/>

<RadioButton android:id="@+id/radio_pirates"
	android:layout_width="wrap_content"
	android:layout_height="wrap_content"
	android:text="@string/pirates"
	android:onClick="onRadioButtonClicked"/>
 </RadioGroup>
```
**ToggleButton:**

Este elemento exibe dois estados, marcado ou desmarcado, com o botão com um indicador colorido e acompanhado com o texto on ou off  

*Sintaxe:*
```
<TextView
        android:id="@+id/toggle_button_label"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toStartOf="@id/toggle"
        app:layout_constraintHorizontal_chainStyle="packed"
        app:layout_constraintBaseline_toBaselineOf="@id/toggle"
        android:text="@string/toggle_button" />
```

**Switch:**

Este elemento é um botão de alternância de dois estados (tendo sua versão mais antiga o *SwitchCompat*). O usuário pode arrastar o botão "polegar" para frente e para trás para selecionar uma das duas opções ou simplesmente tocar no botão para alternar entre as opções. 

<div align="center">
	<img src="https://user-images.githubusercontent.com/128001916/230237251-ffc6ed11-7e92-4f57-83c4-bcf53ab7d8d0.png" width="300px" height="200px"/>
</div>

*Sintaxe:*
```
fun SwitchComposable(modifier: Modifier = Modifier) {
    Switch(
        checked = false,
        modifier = modifier,
        onCheckedChange = { isChecked ->
            if (isChecked) {
                // The switch is checked.
            } else {
                // The switch isn't checked.
            }
        }
    )
} 
```


**FloatingActionButton:**

Este elemento é um botão de ação flutuante, é utilizado para um tipo especial de ação promovida. Eles são distinguidos por um ícone circular flutuando acima da interface do usuário e possuem comportamentos de movimento especiais relacionados a metamorfose, lançamento e ponto de ancoragem de transferência.

<div align="center">
	<img src="https://user-images.githubusercontent.com/128001916/230237092-5d1d8cd1-8171-422f-b9a4-04863ca42e0c.png" width="300px" height="300px"/>
</div>

*Sintaxe:*
```
<com.google.android.material.floatingactionbutton.FloatingActionButton
        android:id="@+id/fab"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="end|bottom"
        android:src="@drawable/ic_my_icon"
        android:contentDescription="@string/submit"
        android:layout_margin="16dp" />
```


### Text

**MultiAutoCompleteTextView:** 

Este elemento é uma exibição de texto editável, que pode mostrar sugestões de conclusão para a substring do texto em que o usuário está digitando, em vez de necessariamente para a coisa toda.

*Sintaxe:*
```
public class CountriesActivity extends Activity {
     protected void onCreate(Bundle savedInstanceState) {
         super.onCreate(savedInstanceState);
         setContentView(R.layout.autocomplete_7);

         ArrayAdapter<String> adapter = new ArrayAdapter<String>(this,
                 android.R.layout.simple_dropdown_item_1line, COUNTRIES);
         MultiAutoCompleteTextView textView = findViewById(R.id.edit);
         textView.setAdapter(adapter);
         textView.setTokenizer(new MultiAutoCompleteTextView.CommaTokenizer());
     }

     private static final String[] COUNTRIES = new String[] {
         "Belgium", "France", "Italy", "Germany", "Spain"
     };
 }
```

**CheckedTextView:** 

Este elemento é uma extensão para TextView (elemento que mostra o texto para o usuário) que suporta o Checkable (Define uma extensão para visualizações que as tornam verificáveis)  interface e aos monitores.

*Sintaxe:*
```
<CheckedTextView
android:id="@+id/simpleCheckedTextView"
android:layout_width="fill_parent"
android:layout_height="wrap_content"
android:checked="true"
android:gravity="center"
android:checkMark="@drawable/checked"
android:text="Checked Text View" />
```

**TextInputLayout:** 

Este elemento mostra um rótulo flutuante quando a dica está oculta enquanto o usuário insere o texto.

*Sintaxe:*
```
<com.google.android.material.textfield.TextInputLayout
         android:layout_width="match_parent"
         android:layout_height="wrap_content"
         android:hint="@string/form_username">
```


### Widgets

**SeekBar:** 

Este elemento é uma extensão da ProgressBar que adiciona um polegar (“linha”) arrastável para que o usuário possa levá-la para direita ou esquerda para definir o progresso atual. 

*Sintaxe:*
```
 <SeekBar
        android:id="@+id/seekbar"
        android:layout_marginTop="400dp"
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:max="150"/>
```
 
**SeekBar (Discrete):** O SeekBar Discrete realiza a mesma função do SeekBar porém para números discretos.

*Sintaxe:* 
```
<org.adw.library.widgets.discreteseekbar.DiscreteSeekBar
        android:id="@+id/seekBar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        app:dsb_indicatorColor="@color/purple_200"
        app:dsb_max="100"
        app:dsb_min="0"
        app:dsb_progressColor="@color/purple_200"
        app:dsb_rippleColor="@color/purple_200"
        app:dsb_trackColor="@color/purple_200" />
```

**RatingBar:** 

Este elemento é uma extensão do ProgressBar e SeekBar que mostra a classificação em estrelas. 
 
*Sintaxe:* 
```
 <RatingBar
            android:id="@+id/rtb"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:numStars="5"
            android:progressTint="#FFC107"
            android:secondaryProgressTint="#FFEB3B"
            android:stepSize="0.1"/>
```

**SearchView:** 

Este elemento é utilizado para mostrar para o usuário uma um local para inserir uma pesquisa e enviar uma solicitação a um provedor de pesquisa, mostrando uma lista de sugestões ou resultados de consulta disponíveis para o usuário escolher uma opção. 

*Sintaxe:*
```
<?xml version="1.0" encoding="utf-8"?>
    <menu xmlns:android="http://schemas.android.com/apk/res/android">
        <item android:id="@+id/search"
              android:title="@string/search_title"
              android:icon="@drawable/ic_search"
              android:showAsAction="collapseActionView|ifRoom"
              android:actionViewClass="android.widget.SearchView" />
    </menu>
 ```
**TextureView:** 

Este elemento é utilizado para exibir um fluxo de conteúdo, como o proveniente de uma visualização de câmera, um vídeo ou uma cena OpenGL. O fluxo de conteúdo pode vir do processo do aplicativo, bem como de um processo remoto.

*Sintaxe:*
```
public class MyActivity extends Activity implements TextureView.SurfaceTextureListener {
      private MediaPlayer mMediaPlayer;
      private TextureView mTextureView;

      protected void onCreate(Bundle savedInstanceState) {
          super.onCreate(savedInstanceState);

          mMediaPlayer = new MediaPlayer();

          mTextureView = new TextureView(this);
          mTextureView.setSurfaceTextureListener(this);
          setContentView(mTextureView);
      }
```
**SurfaceView:**

Este elemento fornece uma superfície de desenho dedicada incorporada dentro de uma hierarquia de exibição. Você pode controlar o formato desta superfície e, se quiser, seu tamanho; o SurfaceView cuida de colocar a superfície no local correto na tela.

*Sintaxe:*
```
SurfaceView(
    context: Context!,
    attrs: AttributeSet!,
    defStyleAttr: Int,
    defStyleRes: Int)
```
**Horizontal Divider:** 

Este elemento que cria uma linha horizontal dividindo os elementos 

*Sintaxe:*
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
   android:layout_width="match_parent"
   android:layout_height="match_parent"
   android:paddingLeft="16dp"
   android:paddingRight="16dp"
   android:orientation="horizontal"
   android:gravity="center">
 </LinearLayout>
```

**Vertical Divider:** 

Este elemento que cria uma linha vertical dividinho os elementos

*Sintaxe:*
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
   android:layout_width="match_parent"
   android:layout_height="match_parent"
   android:paddingLeft="16dp"
   android:paddingRight="16dp"
   android:orientation="vertical"
   android:gravity="center">
 </LinearLayout>
```

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
https://developer.android.com/guide/topics/ui/controls/radiobutton?hl=pt-br#java 
https://developer.android.com/reference/android/widget/RadioGroup.html 
https://developer.android.com/reference/android/widget/RadioGroup.html 
https://developer.android.com/reference/android/widget/RadioButton.html 
https://developer.android.com/develop/ui/views/components/togglebutton 
https://developer.android.com/reference/android/widget/ToggleButton 
https://developer.android.com/reference/androidx/appcompat/widget/SwitchCompat 
https://developer.android.com/reference/com/google/android/material/floatingactionbutton/FloatingActionButton 
https://developer.android.com/develop/ui/views/components/floating-action-button 
https://developer.android.com/reference/android/widget/MultiAutoCompleteTextView 
https://developer.android.com/reference/android/widget/TextView 
https://developer.android.com/reference/android/widget/Checkable 
https://developer.android.com/reference/android/widget/CheckedTextView 
https://abhiandroid.com/ui/checkedtextview 
https://developer.android.com/reference/android/widget/SeekBar.html 
https://acervolima.com/android-criando-uma-seekbar/ 
https://acervolima.com/seekbar-discreto-no-android-usando-biblioteca/ 
https://developer.android.com/reference/android/widget/RatingBar 
https://uware.com.br/como-usar-ratingbar-no-android-studio/ 
https://developer.android.com/reference/android/widget/SearchView  
https://developer.android.com/training/search/setup?hl=pt-br 
https://developer.android.com/reference/android/view/TextureView 
https://developer.android.com/reference/android/view/TextureView 
https://developer.android.com/reference/kotlin/android/view/SurfaceView 
https://developer.android.com/reference/android/view/SurfaceView 
https://developer.android.com/reference/android/view/View.html 
https://developer.android.com/reference/android/widget/LinearLayout 
https://developer.android.com/reference/android/widget/ImageButton
https://developer.android.com/reference/android/widget/Button.html
https://developer.android.com/reference/com/google/android/material/chip/ChipGroup
https://developer.android.com/reference/com/google/android/material/chip/Chip.html
https://developer.android.com/reference/android/widget/CheckBox.html

