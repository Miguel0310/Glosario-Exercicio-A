# Glosario Exercicio A

## 1. Construtor
O construtor é uma subrutina que tem como objetivo inicializar uma clase 
```JAVA
public Persona() {} //CONSTRUTOR SEM PARÁMETROS
```
Em java, é criado quando se cria uma clase. Posee o mesmo nome da classe e NÃO pode devolver ninhum valor nem sequer especificar a palabra <code>void</code>

## 2. Instanciação
Uma Instanciação é o processo na qual se realiza uma cópia do objeto (clase) existente
```JAVA
public class Pessoa
        {
            public char sexo;
            public string nome;
            public int idade;
        }

public class Funcionario
        {
            static void Main()
            {
                //Faço a declaração da minha classe e a instancio, tudo na mesma linha
                
                Pessoa objPessoa = new Pessoa();
               //Defino o valor dos campos criados na classe Pessoa
               
                objPessoa.sexo = 'm';
                objPessoa.nome = "Wellington";
                objPessoa.idade = 21;

                //Leio o valor do campo nome

                Console.WriteLine(objPessoa.nome);
            }          
        }
  ```
 
## 3. Palavra reservada *new*
A palavra reservada <code>new</code> é usada únicamente para instanciar objetos

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

## 6. Palavra reservada this
