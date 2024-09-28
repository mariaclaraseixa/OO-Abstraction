# OO-Abstraction



De acordo com as Notas Digitais de Programação Orientada a Objetos (B.Tech, 1º Ano – 2º Sem, 2018-19, Departamento de CSE & IT) do Malla Reddy College of Engineering & Technology (2018), os principais princípios da programação orientada a objetos incluem encapsulamento, abstração de dados, polimorfismo, herança, ligação dinâmica e passagem de mensagens. Esses princípios formam a base da POO, permitindo o desenvolvimento de código modular e eficiente, promovendo a reutilização e flexibilidade dos objetos. A abstração refere-se ao ato de representar características essenciais sem incluir os detalhes ou explicações de fundo. As classes utilizam o conceito de abstração e são definidas como uma lista de atributos, como tamanho, peso, custo e funções para operar sobre esses atributos. Elas encapsulam todas as propriedades essenciais do objeto que será criado. Os atributos são chamados de membros de dados, pois armazenam informações, e as funções que operam nesses dados são chamadas de funções-membro. As classes utilizam o conceito de abstração de dados, por isso são chamadas de tipo abstrato de dados (TAD) (Malla Reddy College of Engineering & Technology, 2018), ou seja, os princípios destacados neste texto são:

1. Encapsulation
2. Data abstraction
3. Polymorphism
4. Inheritance
5. Dynamic binding
6. Message passing

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


# References

Malla Reddy College of Engineering & Technology. Object Oriented Programming: Digital Notes (B.Tech, I Year – II Sem, 2018-19, Department of CSE & IT). Autonomous Institution – UGC, Govt. of India. Maisammaguda, Dhulapally, Secunderabad, Telangana State, India, 2018. Available at: https://mrcet.com/downloads/digital_notes/HS/OOP_10122018.pdf.
