## Oque é o estado de uma aplicação?
- Dados de resposta de uma requisição
- Informações do usuário
- Entrada de dados
- Estado da tela (UI)
- Rota ou localização da sua página atual


## Dados que mudam


## Imutabilidade
  Um objeto imutável é um objeto no qual seu estado não pode ser modificado após ser criado. Invocar qualquer função dele, esperando que o mesmo te devolva um objeto, implica na criação de um novo objeto, mesmo que o propósito do método alterar o valor de algum atributo do mesmo.


## Oque é o Flux?
  - Single Direction Data Flow
  - Se propoe a resolver o problema de compartilhamento de estado partes diferentes de sua aplicação. De maneira que, ao alterar o estado em uma parte da tela, a outra parte é alterada com o mesma informação sem a necessidade de ficar criando, atualizando, clonando outros objetos objetos.
  - [Saiba mais sobre flux no blog](https://medium.com/codigorefinado/flux-o-que-%C3%A9-isso-f90071c54cf8)


### Quais são os príncipais conceitos do Flux?
  - Single state (padrão de projetos Singleton)
  - Actions
  - Reducers
  - Store
  - One-way dataflow
  

## Três princípios do Redux
- Única fonte da verdade
  - Unica arvore armazenando o estado no **Store**
  - Previsibilidade e manutenibilidade
  - Server Side Rendering (SSR) - Angular Universal
  - Facilita o teste e depuração (debug)
  
  Para viabilizar a fonte única da verdade, pense nele como o Padrão de projetos Singleton que controla o estado.

  
- Estado é somente leitura
  - Deriva propriedades do estado
  - Despacha, Executa ações para mudar o estado
  - Padrão imutável - *Immutable*
  
- Funções puras modificam o estado
  - Funções pura são **Reducers**
  - **Reducers** responde para tipos de ações (**Action**)
  - **Reducers** retornam um novo estado


###  

###

###



Você pode ler sobre o Vuex, a implementação o Redux para VueJS [aqui](https://medium.com/codigorefinado/gerenciando-estado-com-vuex-2accf11e9849)
