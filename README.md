# Abstracao 

## Visao geral 
### Abstração Explicada com Emojis

Imagine que você está tentando explicar a ideia de um **carro** para alguém que nunca viu um. Em vez de mostrar todas as partes complexas do motor, da eletrônica e dos detalhes técnicos, você simplesmente desenha isso: 🚗. Esse emoji é uma **abstração** do carro, uma simplificação visual que representa o conceito de um carro sem entrar nos detalhes complicados.

Em programação orientada a objetos, **abstração** funciona da mesma maneira. A abstração é como criar uma **imagem mental** ou uma **representação** simplificada de algo da vida real. Por exemplo, se estivermos programando sobre um carro, não precisamos lidar diretamente com todos os componentes internos do motor ou as especificidades do tipo de combustível. Em vez disso, focamos em aspectos mais simples e úteis, como o ato de "dirigir", "frear" ou "acelerar".

Aqui está como os emojis podem nos ajudar a entender os conceitos de abstração:

- 🚗 - O emoji de um carro **não mostra** como o carro realmente funciona, mas nos dá uma ideia clara de que estamos falando de um carro.
- 💻 - O emoji de um laptop **não nos diz** como o processador ou a memória funcionam, mas simboliza um computador.
- 🍎 - O emoji de uma maçã **não inclui** informações sobre seu sabor, peso ou variedade, mas nos faz pensar em uma maçã.

Na programação, uma **classe** é como o emoji 🚗. Ela representa um conceito (como "Carro"), mas esconde os detalhes complexos de como o carro realmente funciona. Ao invés de ver cada detalhe, nós interagimos apenas com as partes que são importantes para o que queremos fazer.

Então, quando dizemos que a abstração é uma **representação** ou **simplificação**, estamos criando algo que captura as partes essenciais da realidade, deixando de fora os detalhes desnecessários para a tarefa em questão. Da mesma forma que o emoji 🚗 é uma abstração de um carro, uma classe em programação é uma abstração de um conceito da vida real.

**Resumo:** A abstração é como pegar a essência de algo e transformá-la em uma versão mais simples, mais fácil de entender e trabalhar. É a forma que usamos para focar no que é importante, ignorando o que não precisamos saber no momento.

## Relação com OO

Relação entre Abstração e Classe em C++
Em C++, uma classe é a forma que usamos para abstrair objetos do mundo real, capturando apenas os aspectos essenciais que precisamos. Vamos considerar o exemplo de um carro novamente:

Realidade Complexa:
Na vida real, um carro tem várias partes complexas: o motor, a transmissão, o sistema elétrico, os freios, etc. Se você fosse representar cada detalhe em um programa, o código seria muito complicado e difícil de lidar.

Abstração com Classe:
Em C++, em vez de modelar todos esses detalhes, criamos uma classe que abstrai os elementos que são mais importantes para o nosso propósito. Podemos criar uma classe Carro que simplifica a ideia de um carro, contendo apenas os atributos e funções mais relevantes.


# Abstracao

## MALLA - Notas Digitais de Programação Orientada a Objetos
De acordo com as Notas Digitais de Programação Orientada a Objetos (B.Tech, 1º Ano – 2º Sem, 2018-19, Departamento de CSE & IT) do Malla Reddy College of Engineering & Technology (2018), os principais princípios da programação orientada a objetos incluem encapsulamento, abstração de dados, polimorfismo, herança, ligação dinâmica e passagem de mensagens. Esses princípios formam a base da POO, permitindo o desenvolvimento de código modular e eficiente, promovendo a reutilização e flexibilidade dos objetos. A abstração refere-se ao ato de representar características essenciais sem incluir os detalhes ou explicações de fundo. As classes utilizam o conceito de abstração e são definidas como uma lista de atributos, como tamanho, peso, custo e funções para operar sobre esses atributos. Elas encapsulam todas as propriedades essenciais do objeto que será criado. Os atributos são chamados de membros de dados, pois armazenam informações, e as funções que operam nesses dados são chamadas de funções-membro. As classes utilizam o conceito de abstração de dados, por isso são chamadas de tipo abstrato de dados (TAD) (Malla Reddy College of Engineering & Technology, 2018), ou seja, os princípios destacados neste texto são:

1. Encapsulation
2. Data abstraction
3. Polymorphism
4. Inheritance
5. Dynamic binding
6. Message passing

Com base no que foi dito por esta Autora pensei no seguinte exemplo: 

```cpp
#include <iostream>
#include <string>
using namespace std;

// Definição da classe Carro (usando abstração)
class Carro {
private:
    string marca;
    string modelo;
    int ano;
    float preco;

public:
    // Construtor para inicializar os atributos
    Carro(string m, string mod, int a, float p) : marca(m), modelo(mod), ano(a), preco(p) {}

    // Função para exibir os detalhes do carro
    void exibirDetalhes() {
        cout << "Marca: " << marca << endl;
        cout << "Modelo: " << modelo << endl;
        cout << "Ano: " << ano << endl;
        cout << "Preço: R$" << preco << endl;
    }

    // Função para calcular a depreciação do carro
    void calcularDepreciacao(int anoAtual) {
        int idade = anoAtual - ano;
        float valorDepreciado = preco * (1 - (0.05 * idade));  // Deprecia 5% por ano
        if (valorDepreciado < 0) {
            valorDepreciado = 0;
        }
        cout << "Valor depreciado: R$" << valorDepreciado << endl;
    }
};

int main() {
    // Criação de um objeto da classe Carro
    Carro meuCarro("Toyota", "Corolla", 2015, 75000);

    // Exibir detalhes do carro
    meuCarro.exibirDetalhes();

    // Calcular depreciação
    meuCarro.calcularDepreciacao(2024);

    return 0;
}

A linguagem C++ adiciona ainda de acordo com (2018, Malla) o Conceito de Templates, onde em vez de escrever diferentes funções para diferentes tipos de dados, podemos definir uma função comum. Por exemplo:

```cpp
int max(int a, int b); // Retorna o máximo de dois inteiros
float max(float a, float b); // Retorna o máximo de dois floats
char max(char a, char b); // Retorna o máximo de dois caracteres
```

Este conceito é conhecido como sobrecarga de funções (*function overloading*). No entanto, ao invés de escrever três funções diferentes, como no exemplo acima, o C++ oferece um recurso chamado **Templates**. Com o auxílio dos templates, você pode definir apenas uma função genérica, como a seguinte:

```cpp
T max(T a, T b); // T é chamado de tipo de dado genérico
```

Funções template são uma forma de tornar funções ou classes abstratas, permitindo que o comportamento da função seja definido sem que se saiba previamente qual tipo de dado será manipulado pela função. Isso é conhecido como "funções ou programação genéricas". A função template se concentra mais no pensamento algorítmico do que em um tipo específico de dado.

Por exemplo, você poderia criar uma função de inserção (*push*) de pilha usando templates. Esta função *push* seria capaz de lidar com a operação de inserção em uma pilha para qualquer tipo de dado, ao invés de precisar criar uma função de inserção específica para cada tipo diferente de dado.

#

De acordo com o livro Introduction to Python Programming de Udayan Das, Aubrey Lawson, Chris Mayfield e Narges Norouzi, a abstração é um conceito chave na Programação Orientada a Objetos (POO), no qual o funcionamento interno de uma unidade é ocultado dos usuários e de outras unidades que não precisam conhecer esses detalhes internos. Por exemplo, um motorista geralmente não precisa saber a temperatura exata do motor de seu carro em números. Em vez disso, o carro possui um medidor que exibe se a temperatura do motor está dentro de uma faixa apropriada (Das et al., 2024).

# KUCHERENKO

O conceito de classe abstrata é baseado na ideia de abstração, onde uma classe representa uma ideia geral que não pode ser diretamente instanciada. Um exemplo é a classe "Pessoa", que representa uma noção vaga e genérica. Em contrapartida, classes como "Aluno" ou "Professor" são exemplos concretos dessa generalização e podem ser instanciadas. A classe abstrata, portanto, age como um modelo que define comportamentos e propriedades comuns a suas subclasses, mas não pode ser utilizada para criar objetos diretamente. Isso ajuda a estruturar e organizar o código de forma mais eficiente em aplicações. "Kucherenko exemplifica o conceito de classes abstratas ao explicar que, em um sistema de aplicação, a criação de objetos concretos como 'Aluno' ou 'Professor' faz mais sentido do que a criação de um objeto de uma classe genérica como 'Pessoa'. As classes abstratas, assim, representam ideias gerais que servem de base para classes mais específicas" (Kucherenko, 2018).

# COAD

A visão de abstração de Peter Coad, descrita no livro *"Java Modeling in Color with UML"*, propõe uma abordagem visual e intuitiva para modelagem de sistemas complexos. Essa abordagem organiza as classes em quatro arquétipos básicos, diferenciados por cores, facilitando o entendimento e a construção de modelos de software. Os arquétipos são: *coisas* (verde), *interações* (rosa), *papéis* (amarelo) e *descrições* (azul)【4†source】.

Para exemplificar o uso desses arquétipos, imagine uma situação onde João é proprietário de um carro, atua como motorista e recebe uma multa de trânsito. Cada elemento dessa história pode ser abstraído usando os arquétipos de Coad, ilustrando como essas categorias ajudam a organizar e conectar diferentes partes de um sistema.

No arquétipo **verde** (coisas), identificamos objetos tangíveis no mundo real, como João, representado pela classe "Pessoa", e o "Carro" que ele possui e dirige. Esses são os principais elementos físicos que interagem no sistema.

O arquétipo **rosa** (interações) descreve os eventos que ocorrem entre as *coisas*. Nesse caso, a "Multa de Trânsito" é a interação significativa — João, ao dirigir seu carro, ultrapassa o limite de velocidade e é penalizado. A multa é a interação formal entre João, seu carro, e as autoridades de trânsito.

O arquétipo **amarelo** (papéis) representa as funções ou papéis que os atores desempenham nas interações. João desempenha dois papéis: o de **motorista**, enquanto dirige o carro, e o de **proprietário**, visto que o veículo está registrado em seu nome. Esses papéis são cruciais para compreender como João está relacionado às interações e aos objetos no sistema.

Por fim, o arquétipo **azul** (descrições) detalha atributos das *coisas* e das *interações*. Por exemplo, o "Carro" pode ser descrito com informações como marca, modelo e placa. A "Multa de Trânsito" inclui detalhes como o tipo de infração (excesso de velocidade), a data, hora e valor a ser pago. Além disso, há a "Carteira de Habilitação" de João, que é uma descrição essencial para validar seu papel como motorista.

A abstração proposta por Peter Coad permite, portanto, dividir e organizar os componentes de um sistema em categorias claras, o que facilita tanto o entendimento do domínio quanto a construção de soluções de software. Ao identificar classes e suas relações dentro dessas categorias, a modelagem se torna mais eficiente, com foco nos elementos de negócio relevantes e nas suas interações. Como ele argumenta no livro, essa estruturação ajuda a visualizar melhor o sistema, promovendo maior criatividade e inovação ao explorar "o que poderia ser feito e o que poderia trazer vantagem significativa ao negócio".

# References


**Malla Reddy College of Engineering & Technology.** *Object Oriented Programming: Digital Notes (B.Tech, I Year – II Sem, 2018-19, Department of CSE & IT)*. Autonomous Institution – UGC, Govt. of India. Maisammaguda, Dhulapally, Secunderabad, Telangana State, India, 2018. Disponível em: <https://mrcet.com/downloads/digital_notes/HS/OOP_10122018.pdf>. Acesso em: 28 set. 2024.

**DAS, U.; LAWSON, A.; MAYFIELD, C.; NOROUZI, N.** *Introduction to Python Programming*. OpenStax, Rice University, 2024. Disponível em: <https://openstax.org>. Acesso em: 28 set. 2024. ©2024 Rice University. Texto licenciado sob uma Licença Internacional Creative Commons Atribuição 4.0 (CC BY 4.0).

**KUCHERENKO, Igor.** *Mastering High Performance with Kotlin: Overcome performance difficulties in Kotlin with a range of exciting techniques and solutions*. Birmingham: Packt Publishing Ltd, 2018.

Aqui está a referência no formato ABNT:

**COAD, Peter; DE LUCA, Jeff; LEFEBVRE, Eric.** *Java modeling color with UML: enterprise components and process with Cdrom*. Upper Saddle River: Prentice Hall PTR, 1999.
