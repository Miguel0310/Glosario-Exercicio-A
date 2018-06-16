# Glosario Exercicio A

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
