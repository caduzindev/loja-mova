# Loja Mova
O objetivo deste projeto é construir uma api de loja virtual simples. Onde o cliente pode logar, selecionar produtos para comprar, adicionar itens no carrinho, fazer pedidos

## **Nota**
- O inventario de produtos deve estar pre-cadastrado no banco de dados.
- A autenticação deve ser feita usando JWT
- E **Obrigatorio** ter uma documentação que mostre como rodar seu projeto localmente, para facilitar a avaliação
- E **Obrigatorio** documentar as rotas... pode documentar elas da forma que você quiser

## **Requisitos**
- [ ] O Usuario deve poder logar com uma conta na loja
- [ ] Se não exisir a conta do `Usuario`, ele poderá se cadastrar
- [ ] Deve haver uma rota `/products` que traz todos os produtos da loja (`Usuario` não precisa estar logado)
- [ ] Deve haver uma rota `/products/{id}` que traz as informações especificas de um produto (`Usuario` não precisa estar logado)
- [ ] Deve haver uma rota `/cart` que traz os itens do carrinho daquele `Usuario`, contendo os produtos anteriormente adicionados com informações como ID do produto,nome,preço e quantidade daquele produto selecionada anteriormente pelo `Usuario` (Usuario precisa estar logado)
- [ ] Deve haver uma rota `/cart/add?product_id={id}` onde o `Usuario` adiciona os produtos de seu interesse no carrinho (Usuario precisa estar logado)
- [ ] Deve haver uma rota `/cart/product/{id}?quantity={quantidade}` onde o `Usuario` poderá ajustar a quantidade pedida para qualquer produto no carrinho (Usuario precisa estar logado)
- [ ] Deve haver uma rota `/cart/delete/product/{id}` onde o `Usuario` deleta um produto do carrinho (`Usuario` precisa estar logado)
- [ ] Deve haver uma rota `/cart/amount` que deve retornar o calculo das somas das quantidades multiplicada pelo preço unitário de cada produto solicitado (`Usuario` precisa estar logado)
- [ ] Deve haver uma rota `/orders/sendOrder` que irá pegar as informações do carrinho do `Usuario` e criará um pedido com valor total da compra,produtos selecionados e informações do `Usuario` (`Usuario` precisa estar logado)
- [ ] Deve haver uma rota `/orders` onde irá listar todos os pedidos do `Usuario` (`Usuario` precisa estar logado)
- [ ] Deve haver uma rota `/orders/delete/{id}` onde o `Usuario` poderá deletar um pedido (`Usuario` precisa estar logado)
- [ ] Deve haver uma rota `/orders/show/{id}` que exibe as informações de um pedido especifico (`Usuario` precisa estar logado)

## **Requisitos BONUS!!!!!**
Não é obrigatorio fazer estas features abaixo mas se você conseguir, ganhará pontos extras
- [ ] Se o `Usuario` pedir um quantidade que exceda a quantidade "disponível" do produto, deve ser retornar uma resposta de erro
- [ ] O `Usuario` pode especificar um endereço de cobrança e envio quando o pedido for feito
- [ ] O `Usuario` pode ver as taxas de envio adicionadas ao valor total da compra
## **Obrigatório ter**
- PHP
- Docker
- Pelo menos 1 teste unitario
- Mysql como banco de dados
## **Será um diferencial** (ganhará pontos extras)
- Slim 4
- Testes de Integração
- Conventional Commits
- Seguir alguns principios do SOLID
- Documentar rotas com swagger

## **Links de referência**
- Lib de JWT -> [php-jwt](https://github.com/firebase/php-jwt)
- Tutorial de autenticação JWT -> [tutorial](https://www.youtube.com/watch?v=B-7e-ZpIWAs)