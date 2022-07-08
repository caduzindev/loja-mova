# Loja Mova
O objetivo deste projeto é construir uma api de loja virtual simples. Onde o cliente pode logar, selecionar produtos para comprar, adicionar itens no carrinho, fazer pedidos e etc.

## **Nota**
- O inventario de produtos pode estar pre-cadastrado em um banco de dados, em memoria... onde você achar melhor.
- A autenticação deve ser feita usando JWT

## **Requisitos**
- [ ] O Usuario deve poder logar com uma conta na loja
- [ ] Se não exisir a conta do usuario, ele poderá se cadastrar
- [ ] Deve haver uma rota `/products` que traz todos os produtos da loja (usuario não precisa estar logado)
- [ ] Deve haver uma rota `/products/{id}` que traz as informações especificas de um produto (usuario não precisa estar logado)
- [ ] Deve haver uma rota `/cart` que traz os itens do carrinho daquele `Usuario`, contendo os produtos anteriormente adicionados com informações como ID do produto,nome,preço e quantidade daquele produto selecionada anteriormente pelo `Usuario` (Usuario precisa estar logado)
- [ ] Deve haver uma rota `/cart/add` onde o `Usuario` adiciona os produtos de seu interesse no carrinho (Usuario precisa estar logado)
- [ ] Deve haver uma rota `/cart/product/{id}/?quantity={quantidade}` onde o usuario poderá ajusta a quantidade pedida para qualquer produto no carrinho (Usuario precisa estar logado)
- [ ] Deve haver uma rota `/cart/delete/product/{id}` onde o usuario deleta um produto do carrinho (usuario precisa estar logado)