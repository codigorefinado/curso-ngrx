# Imutabilidade

Um objeto imutável é um objeto no qual seu estado não pode ser modificado após ser criado. Invocar qualquer função dele, esperando que o mesmo te devolva um objeto, implica na criação de um novo objeto, mesmo que o propósito do método alterar o valor de algum atributo do mesmo.

No Angular imutabilidade ajuda a melhorar a performance, pois otimiza o sistema de detecção de mudanças.

Em todas as linguagem, ajuda a criar código mais limpo devido ao fato de dispensar a necessidade de controlar se a informação mudou através de verificações dos atributos, em outras palavras, podemos detectar se um objeto mudou apenas olhando se a referência de memória é diferente, sem precisar olhar seus atributos.

Permite desfazer alterações, devido a possibilidade de termos a informação atual e a anterior.

Torna o sistema previsível. Pois não haverá alterações inadvertidas comuns quando se trabalha com ponteiros, onde se quer alterar a informação em um local, e acaba alterando em vários outros erroneamente.

Facilita o processo de depuração (debug)

Simplifica a programação concorrente, objetos imutáveis podem ser compartilhadas com segurança em diversas threads. Permite escrever código praticamente sem sincronização ou bloqueios, diminuindo a complexidade do código concorrente e os erros.

Um objeto por ser imutável, pode ser compartilhada em qualquer parte da aplicação, servindo como cache e economizando memória.




### Recomedação de leitura:

https://pt.stackoverflow.com/questions/103460/o-uso-de-imutabilidade

https://medium.com/opensanca/imutabilidade-eis-a-quest%C3%A3o-507fde8c6686

https://desenvolvedor.expert/por-que-imutabilidade-eh-importante-fd0ba22f103e

https://www.devmedia.com.br/o-reflexo-da-imutabilidade-no-codigo-limpo/30697

http://www.arquiteturajava.com.br/livro/favoreca-imutabilidade-e-simplicidade.pdf

http://www.javapractices.com/topic/TopicAction.do?Id=29
