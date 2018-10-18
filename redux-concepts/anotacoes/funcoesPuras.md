## [Funções puras, oque é?](https://pt.stackoverflow.com/questions/255557/o-que-%C3%A9-uma-fun%C3%A7%C3%A3o-pura)
Uma função pura é aquela que não provoca efeitos colaterais, ou seja, ela não muda qualquer estado na aplicação. Mas não é só isto, ela precisa sempre gerar o mesmo resultado com os mesmos argumentos, ou seja, ela precisa ser completamente determinística.

Quando a função só gera um resultado determinístico e não muda estado fica mais entender o seu funcionamento, o fluxo de operações é mais previsível, é mais fácil depurar e testar o código, é preciso depurar menos código já que tende a ter menos erros, é muito mais fácil lidar com concorrência e paralelização, e é mais fácil fazer coisas complexas dada a simplicidade dela, o que inclusive permite otimizações agressivas.

Ao contrário do que muita gente pensa não é o algoritmo que é difícil de lidar é a estrutura de dados. É ela que sempre dá problema. Não é o comportamento e sim o estado. A não ser que o algoritmo seja muito complexo e mal feito.

Uma função que acesse algo externo à aplicação não pode ser pura. Qualquer entrada de dados (ler teclado, acessar armazenamento, receber pacote de rede, acessar outra aplicação, pedir algo para o sistema operacional como o relógio, etc.) ou qualquer cálculo que depende do estado de alguma coisa que a aplicação não controle e não possa garantir que o estado é sempre o mesmo (geração randômica verdadeira é o maior exemplo de algo que deve dar um resultado que depende de um estado não determinístico, tem função randômica que é determinística, embora precisa ser usada de forma específica para ser pura). Para ajudar lidar com isto a linguagens funcionais possuem monads.

Funções matemáticas de forma geral são puras. O que trabalha com tipos por valor passadas por valor costuma ser puro, o que trabalha em algo por referência que seja um objeto imutável costuma ser puro.
Academicamente costuma-se atribuir estas características para uma função pura:
 - são idempotentes
 - possuem transparência referencial
 - permitem memoização
 - adotam avaliação tardia
