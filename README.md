# Glosario Exercicio A

1. [Construtor](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#1-construtor)
2. [Instanciação](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#2-instancia%C3%A7%C3%A3o)
3. [Palavra reservada new](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#3-palavra-reservada-new)
4. [Palavra reservada instanciof](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#4-palavra-reservada-instanciof)
5. [Encapsulamento](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#5-encapsulamento)
6. [Palavra reservada this](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#6-palavra-reservada-this)
7. [Getters/Setters](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#7-getterssetters)
8. [Palavra reservada public/private](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#8-palavra-reservada-publicprivate)
9. [Assinatura de método](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#9-assinatura-de-m%C3%A9todo)
10. [Sobrecarga de método](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#10-sobrecarga-de-m%C3%A9todo)
11. [Escopo de classe](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#11-escopo-de-classe)
12. [Escopo de objeto](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#12-escopo-de-objeto)
13. [Palavra reservada final](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#13-palavra-reservada-final)
14. [Relacionamento de dependência](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#14-relacionamento-de-depend%C3%AAncia)
15. [Relacinamento de Agregação](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#15-relacinamento-de-agrega%C3%A7%C3%A3o)
16. [Relacionamento de Composição](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#16-relacionamento-de-composi%C3%A7%C3%A3o)
17. [REFERÊNCIAS](https://github.com/Miguel0310/Glosario-Exercicio-A/blob/master/README.md#17-refer%C3%8Ancias)

## 1. Construtor
O construtor é uma subrutina que tem como objetivo inicializar uma clase 
```JAVA
public Persona() {} //CONSTRUTOR SEM PARÁMETROS
```
Em java, é criado quando se cria uma clase. Posee o mesmo nome da classe e NÃO pode devolver nenhum valor nem sequer especificar a palabra <code>void</code>.

## 2. Instanciação
Uma Instanciação é o processo na qual se realiza uma cópia do objeto (clase) existente
```JAVA
//
Pessoa objPessoa = new Pessoa(); //Declaramos a Classe Pessoa objPessoa
  ```
 
## 3. Palavra reservada *new*
A palavra reservada <code>new</code> é usada para instanciar e criar objetos ou invocar construtores.
```JAVA
//
int i = new int(); 
```

## 4. Palavra reservada *instanciof*
Determina se um objeto é a instancia de uma classe, superclasse ou interface. O objetivo do operador é conhecer se um objeto é de um determinado tipo. Por tipo define-se como classe ou interface.
```JAVA
class Animal {
class Perro extends Animal {
   public static void main (String[] args){
     Perro toby = new Perro();
     if (toby instanceof Animal)
       System.out.println("toby es un perro y también un animal");
   }
}
}
```
## 5. Encapsulamento
Encapsulamento em POO é definido como um *ocultamiento* do estado, sirve para que só possa modificar-se mediante operações definidas para ese objeto

* Predeterminado
* +Public: Pode ser acessado por afora da classe e qualquer parte do programa.
* #Protected: Só pode ser acessado pela classe e por suas herenças.
* -Private: Só pode-se acessar pela mesma classe.
```JAVA
class Exemplo{
        public String nome;
        private int CPF;
}   
```
## 6. Palavra reservada this
A palavra reservada **this** foi criada para evitar conflitos entre uma variable local e uma global
```JAVA
      public class Mercado {
             private int valor
        public Mercado(int valor){
              //assigno na variable local o valor da global
              this.valor=valor
          } 
      }
```
Neste exemplo existe uma variable global chamada <code>valor</code> e uma local com o mesmo nome. Esta técnica de POO é usada para diferençar e que o compilador consiga entender a diferença.
Outra maneira é trocando o nome de umas das variables.
```JAVA
      public class Mercado {
             private int valor
        public Mercado(int _valor){
              valor = _valor
          } 
      }
```
## 7. Getters/Setters
Os métodos Getters/Setters sao usados para indicar um valor de acesso; eles sempre estao serám públicos e tem duas funcoes:
* Setters: Do ingles **set** que significa "estabelecer" tem como funcao agregar um valor inicial de maneira explicita.
* Getters: Do ingles **get** que significa "obtener", ele serve para obter um valor asignado a um atributo.
Exemplo:
```JAVA
      public class Aluno {
             private String Nome;
             private String Sobrenome;
             private String correio;
             
        public String getNombre()
        {
                return nombre;
        }
        public void setNombre(String nombre)
        {
                this.nombre = nombre;
        }

        public String getApellido()
        {
                return apellido;
        }
        public void setApellido(String apellido)
        {
                this.apellido = apellido;
        }

        public String getCorreo()
        {
                return correo;
        }
        public void setCorreo(String correo)
        {
                this.correo = correo;
        }
}
```
E no __main__ será implementado suas respetivas entrada e retorno de valores.

## 8. Palavra reservada public/private
Sao modificadores de acesso que permitem a visibilidade das **classes, métodos e atributos**.
Como segurança e boa prática de programação, nas declaraçoes de variáveis é usada o **private** para garantir a modificação accidental sendo só acessivel através do método.

## 9. Assinatura de método
A assinatura de métodos é a maneira de identificar um método de forma única; em um programa aonde pode-se ter os métodos com o mesmo nome, voce precissa de ter uma maneira de diferenciarlos com as siguientes informaçoes.
* Modificadores: Podem ser **public**, **private**; que indicam a visibilidade do método.
* Tipo de Retorno: Um método pode ou nao retornar um valor.
* Nome do método: Nome que identifica-lo.
* Lista de parâmetro: Os parâmetros que logos sao chamados.

## 10. Sobrecarga de método
A sobrecarga de métodos permite têr dois ou mais métodos com o mesmo nome com a diferença que realizam diferentes açoes.
```JAVA
SOMA(int X, int Y);
SOMA(String X, String Y);
SOMA(int X, int Y, int Z);
```
## 11. Escopo de classe
O escopo de uma classe é coinciderada como os límites para uma variavel aonde ela é declarada.
Se ela é declarada dentro dos métodos, só pode ser usada dentro de aquel método.

## 12. Escopo de objeto
Refere-se aos límites que uma variavel pode ser usada; ela pode ser categoridaza de distintas maneiras.
* **Variavel Global:** Existe durante toda a execuçao do programa e pode ser utilizada em cualquer funçao.
* **Variavel Local:** Só pode ser utilizada dentro de uma funçao e a mesma é declarada nese momento. Ao finalizar aquela tarefa da funçao, a será destruida e nao poderá ser re-utilizada de novo.
* **Variavel com Parâmetros:** Inicializadas no momentos que sao llamadas as funcoes. Embora sejam utilizadas como inicialização da função, elas podem ser utilizadas normalmente como uma variável local dentro do bloco de função onde estão.

## 13. Palavra reservada final
A palavra reservada final em um método tem a funcao que nao poderá ser sobrescrito; em uma variavel, ela nao poderá trocar de valor, sendo uma constante.

## 14. Relacionamento de dependência
Uma dependência indica a ocorrência de um relacionamento semântico entre dois ou mais elementos do modelo, onde uma classe cliente é dependente de alguns serviços da classe fornecedora, mas não tem uma dependência estrutural interna com esse fornecedor

![img1](http://www.linhadecodigo.com.br/artigos/img_artigos/admilson_nogueira/uml_dependencia.jpg)

## 15. Relacinamento de Agregação
É uma forma especializada na qual os relacionamentos é coinciderado com um todo com suas partes.
![img2](http://www.linhadecodigo.com.br/artigos/img_artigos/admilson_nogueira/uml_agregacao_1.jpg)

## 16. Relacionamento de Composição
Pode ser definida como uma parte de um todo. Se a classe aonde a classe de agregacao está é destruido, ambos serao destruidos.
![img3](http://www.linhadecodigo.com.br/artigos/img_artigos/admilson_nogueira/uml_composicao_1.jpg)

## 17. REFERÊNCIAS
* https://conceitospoo.wordpress.com/2013/07/01/escopo-de-variavel/

* https://www.devmedia.com.br/forum/uso-da-palavra-reservada-final/565425

* http://www.linhadecodigo.com.br/artigo/943/uml-unified-modeling-language-generalizacao-agregacao-composicao-e-dependencia.aspx

* https://desenvolvimentoaberto.org/2014/02/14/classes-escopos-java-c-e-c/

* https://pooperrotti.wikispaces.com/Assinatura+de+métodos
