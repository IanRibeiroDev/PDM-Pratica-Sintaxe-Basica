# Prática Sintaxe Básica

Iremos revisar e fixar melhor alguns assuntos de sintaxe básica 
de Kotlin durante essa prática.

Nela temos o código de um sistema simples de uma livraria, onde
podemos cadastrar, excluir, editar e buscar livros. Contudo,
partes do código estão incorretas ou faltando. É aí que você
entra ;). Use seus conhecimentos da sintaxe básica do Kotlin 
para consertar o sistema.

## Passos

**1 - Implementar a função listar:** o sistema vem com 4 livros
cadastrados, porém, a função para exibi-los está vazia! Implemente a 
função, cuja assinatura já está presente na linha 53, de modo que 
ela imprima no console cada livro presente no repositório. Utilize
o laço de repetição **for** para percorrer cada índice do repositório 
de livros e imprimí-los no console. Lembre-se que a sintaxe para
acessar um valor de uma lista em Kotlin é "nomeDaLista[índice]".

Após implementar o método, rode o programa e chame a opção 5 para
testar seu código, caso esteja funcionando, 4 livros devem aparecer
no console.

Um desses livros, o "Livro dos Livros", está imprimindo seu preço
incorretamente, 1000000.0 ao invés de 999999.99. Isso ocorre devido
ao atributo preço ser do tipo **float**, que não tem precisão 
suficiente para guardar números com mais de 7 dígitos. Vamos
consertar isso no próximo passo.


**2 - De Float para Double:** para resolver nosso problema, vamos
alterar o atributo preço da classe Livro de Float para Double. Também
precisamos alterar a função inputPreco() para que a mesma retorne 
Double ao invés de Float. Por último, na função main(), remova os
"f" após os números onde os livros estão sendo cadastrados.

Feito isso, vamos agora cadastrar um livro. Execute o programa e
escolha a primeira opção. Quando for pedido o preço, informe um 
valor negativo. Agora escolha a opção 5 para listar os livros.
Perceba que o sistema permitiu o cadastro de um livro com preço
negativo, o que nunca deveria acontecer. Vamos consertar isso!

**3 - Validando o preço:** adicione à função inputPreco() uma
validação para que o preço nunca possa ser negativo. Lembre-se
de alterar a variável preco de "val" para "var", para que o valor da
mesma possa ser alterado novamente, caso o primeiro número informado
seja inválido.

Feito isso, vamos agora remover um livro. Escolha a segunda opção
e digite "Livro dos Livros". Ao listar os livros novamente, podemos
confirmar que o mesmo foi deletado. Agora vamos tentar excluir um 
livro novamente, mas dessa vez, quando a aplicação pedir para 
digitar o título, apenas pressione "enter". Perceba que a mensagem
de exclusão foi a mesma, apesar de livro nenhum ter sido excluído.

**4 - Validando remoção:** o método remove, utilizado em excluirLivro(),
retorna true, caso a remoção tenha ocorrido, ou false, caso não.
Sabendo disso, use a **instrução condicional** apropriada para 
imprimir uma mensagem personalizada caso nenhuma remoção tenha ocorrido.

**5 - Implementando editarLivro():** agora, utilizando tudo que você
aprendeu, implemente a função editarLivro(), onde o usuário deve escolher
se gostaria de alterar o título ou preço do livro, informar o novo
valor, e o sistema salvará essa alteração no repositório. Faça as
adaptações que julgar necessárias, inclusive na própria classe Livro.
Por fim, descomente o item 4 do when na função main() adicionando a
chamada a função editarLivro() ao mesmo.

Parabéns, você concluiu a prática :)




