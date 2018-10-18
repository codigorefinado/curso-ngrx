# Arquitetura Redux

Acreditamos que o principal contribuinte para complexidade em muitos sitemas é o **gerenciamento de estado** e o fardo que isso acrescenta ao tentar analisar e entender o sistema. Outros contribuintes enstreiamente relacionados são o volume do código e a preocupação com o controle de fluxo do sistema - Bem Mosely & Peter Marks em Out of the Tar Pit: Analysis of software complexity


## Oque é o estado de uma aplicação?
- Dados de resposta de uma requisição
- Informações do usuário
- Entrada de dados
- Estado da tela (UI)
- Rota ou localização da sua página atual
- Objetos mutáveis
- Imutabilidade


## Oque é o Flux? Qual problema ele resolve?
  - Se propoe a resolver o problema de compartilhamento de estado entre partes diferentes da sua aplicação. De maneira que, ao alterar o estado em uma parte da tela, a outra parte é alterada com o mesma informação sem a necessidade de ficar criando, atualizando, clonando outros objetos;
  - Você possui uma View que pode atualizar um Model, e esse Model pode atualizar outro Model, o qual atualiza uma outra View, que poderia atualizar o mesmo Model. Provavelmente, você ficará louco e perderá algumas horas resolvendo problemas deste tipo;
  - Você não sabe oque está acontecendo em sua aplicação;

  - [Saiba mais sobre flux no blog](https://medium.com/codigorefinado/flux-o-que-%C3%A9-isso-f90071c54cf8)

## [Flux](https://facebook.github.io/flux/docs/in-depth-overview.html#content) não é o [Redux](https://redux.js.org/)
  - O Flux é a arquitetura de interfaces que o Facebook utiliza para criar suas aplicações.
  - [Redux](https://cdn-images-1.medium.com/max/800/1*ucOxan56LKUm3gkjaePwRg.png) 
    - É o padrão de mercado
    - [Redux](https://tableless.com.br/bem-vindo-ao-redux/) é uma maneira de pensar o desenvolvimento de aplicações criada pelo [@dan_abramov](https://twitter.com/dan_abramov)  que teve como principio optimizar a ideia do Flux. Ela foi criada para tentar optimizar alguns obstáculos que o Flux começou a enfrentar, e também veio para simplificar a implementação do mesmo. Inspirada em conceitos da linguagem funcional Elm, e de algumas bibliotecas JS como o Immutable.js,  o Baobab, o  RxJs e o próprio Flux, o Redux veio com alguns paradigmas interessantes e um pouco diferenciados do Flux.
 
 
## Qual o ponto negativo?
  - Boilerplate
  - Adiciona complexidade, mas para um sistema grande e complexo, isso pode não ser um problema, pode até simplificar o código existente
  
  
## [Três princípios do Redux](https://redux.js.org/introduction/threeprinciples)
- Única fonte da verdade
  - Previsibilidade e manutenibilidade
  - Server Side Rendering (SSR) - Angular Universal
  - Facilita o teste e depuração (debug)
  - Todo o estado da aplicação é mantido em apenas um único objeto chamado de **Store**
  - Para viabilizar a fonte única da verdade, pense nele como o Padrão de projetos Singleton que controla o estado.

  
- Estado é somente leitura, imutável
  - O estado da aplicação é inalterável, a unica maneira de afeta-lo é emitindo uma Action com a mudança

  
- Funções puras modificam o estado
  - Funções pura são **Reducers**
  - **Reducers** responde para tipos de ações (**Action**)
  - **Reducers** retornam um novo estado


### Oque mais precisamos saber sobre o [Redux](https://www.reddit.com/r/reactjs/comments/6zban0/oversimplified_flow_of_data_through_react_redux/)?
  - One-way dataflow
  - Torna os testes unitários mais fáceis, sem necessidade de mocks, devido a sua divisão/organização e por você estar escrevendo funções puras, na maior parte do tempo.
    - Action Tests
    - Reducers Tests
    - Middleware Tests
    - Components Tests
   - State - É o conjunto de dados
   - Views - É tudo que aparece no navegador, HTML, CSS, Imagens, componentes
   - Actions - São objetos utilizados para transmitir **State** da **View** para **Store**
   - Reducers - responde para Action, são funções puras e retornam o novo estado, obrigatóriamente, possue o **type**, que indica a ação a ser executada;
   - Store -  é responsável por manter, permitir leitura e alterar o **state** através dos **reducers**  

  
**Exemplo de Action**

```
const action = {
  type: 'ADD_TODO',
  payload: {
    label: 'Comer pizza',
    complete: false
  }
};
```


###  

###

###



Você pode ler sobre o Vuex, a implementação o Redux para VueJS [aqui](https://medium.com/codigorefinado/gerenciando-estado-com-vuex-2accf11e9849)
