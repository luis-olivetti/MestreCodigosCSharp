# Perguntas teóricas de introdução

> 1 - Em quais linguagens o C# foi inspirado?

A linguagem C#, criada a partir de 1999 através de um convite da Microsoft para Anders Hejlsberg e sua equipe.
Essa linguagem foi baseada em C, C++ e Java.

> 2 - Inicialmente o C# foi criado para qual finalidade?

Buscava uma linguagem simples, moderna, de uso geral e orientada a objetos.
Sua finalidade foi de possibilitar a criação de soluções executáveis sobre a plataforma .NET Framework.
Com isso, o programador não cria uma solução para um dispositivo eletrônico específico, e sim para uma plataforma .NET Framework.

> 3 - Quais os principais motivos para a Microsoft ter migrado para o Core?

Ser multiplataforma, além da questão da portabilidade e nuvem.

> 4 - Cite as principais diferenças entre .Net Full Framework e .Net Core.

O .NET Framework é utilizado para desenvolver aplicações Windows, com Windows Forms, WPF e aplicações WEB com ASP. NET MVC.
.NET Core possui código livre e multiplataforma. Suporta UWP para criar aplicações Windows e as bibliotecas ASP. NET Core para aplicações Web multiplataformas.

# Utilizando POO

> O que é POO?

POO significa Programação Orientada a Objetos

> O que é polimorfismo?

Polimorfismo se trata de que um objeto pode se comportar como se fosse outro objeto. Por exemplo:
Um objeto `Peixe` é um `Animal`, herda todas as propriedades e métodos da classe base, mas o objeto `Animal` não pode ser tratado como `Peixe`, pois ele não possui todas as características de `Peixe`.

Além disso, através de classes abstratas ou interfaces podemos manipular classes/interfaces derivadas sem se importar com suas especificidades.

> O que é abstração?

Abstração é uma forma de gerenciar a complexidade através de classificações hierárquicas, ignorando coisas que não são importantes para determinado contexto, lidando com algo complexo de forma simples, ou muitas vezes lidando com várias coisas diferentes como se fossem iguais.

Podemos criar camadas semânticas de sistemas complexos subdividindo-os em unidades menores.

A abstração serve como uma base para outras classes que queiram ser do mesmo grupo de objetos.

> O que é encapsulamento?

Para falar sobre o encapsulamento, vou demonstrar o seguinte exemplo:

Uma superclasse `Animal` que possui um método `Mover`.

Uma classe `Humano: Animal` que também possui um método `Mover` (Implementa o seu jeito de se mover, caminhando)

E a classe `Peixe: Animal` com o método `Mover` (Implementa o seu jeito de se mover, nadando)

Nesse caso, ao criar essas classes `Humano` e `Peixe` e executar o método `Mover`, conhecemos o método `Mover`, utilizado para movimentar o animal, mas não precisamos conhecer o que o método faz internamente, pois eles estão encapsulados.
Se o animal se movimenta rastejando, pulando ou andando, isso não importa para nós, pois sabemos que existe o método que movimenta o animal.

> Quando usar uma classe abstrata e quando devo usar uma interface?

Classes abstratas e interfaces podem ser utilizadas em situações que várias classes possuem métodos em comum, mas que também possuem suas particularidades. Então elas poderiam herdar de uma classes abstrata ou de interfaces.

A principal diferença entre classes abstratas e interfaces é que uma classe poderia implementar diversas interfaces, já com a abstração, ela poderia ser implementada somente de uma.

Além disso, interfaces só definem contratos, não comportamentos.
Já com uma classe abstrata podemos definir os comportamentos em comum das classes derivadas.

> O que faz as interfaces IDisposable, IComparable, ICloneable e IEnumerable?

* IDisposable destina-se principalmente a liberar recursos não gerenciados utilizados em nosso código, tais como conexões com banco de dados, arquivos e hardwares externos. Estes devem ser liberados manualmente.

* IComparable é usado para fornecer uma ordem de classificação padrão para seus objetos.

* ICloneable dá suporte à clonagem, que cria uma nova instância de uma classe com o mesmo valor de uma instância existente.

* IEnumerable permite iterarmos por uma coleção.

> Existe herança múltipla (de classes) em C#?

Não, pois poderia ocasionar um problema chamado herança diamante onde uma classe B e C poderiam herdar da classe A que possui o método Correr, mas B e C sobreescrever esse método Correr e executam suas particularidades.

Se implementarmos uma classe D, com herança múltipla de B e C, qual método iria ser executado se chamarmos o método Correr?
Nesse caso, podemos utilizar Interfaces.

# Trabalhando com testes

> Quais os principais frameworks que podemos usar no desenvolvimento de testes?

MSTest: Framework padrão do Visual Studio.

NUnit: Framework mais utilizado entre os Devs .NET.

XUnit: Framework mais recente, nascido para simplificar e modernizar a forma de escrever testes unitários.

Referências:

https://www.eduardopires.net.br/2017/07/ferramentas-para-escrever-testes-de-unidade-mais-eficientes/

https://xunit.github.io/docs/comparisons.html

https://www.devmedia.com.br/a-evolucao-da-linguagem-de-programacao-csharp/28639
