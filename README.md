# marketing.office.place — Gamer Store


## Funcionalidades
- Catálogo carregado de forma dinâmica pela API pública DummyJSON.
- Categorias: notebooks, smartphones e acessórios.
- Busca por nome/descrição, filtro por categoria e ordenação.
- Carrinho com quantidade, remoção de itens e total.
- Carrinho salvo no `localStorage` do navegador.
- Layout responsivo para celular, tablet e computador.


## Como a API funciona
- A constante `API_URLS` em `script.js` guarda os endereços dos endpoints.
- `fetch()` faz as requisições para a API.
- `Promise.all()` aguarda as respostas.
- `response.json()` converte cada resposta para objetos JavaScript.
- `renderProducts()` monta os cards no HTML.
- Os filtros atualizam a lista sem precisar recarregar a página.

API usada: https://dummyjson.com/docs/products

## Observações importantes
- A API fornece dados de demonstração e não é um fornecedor real de produtos gamer.
- Os preços retornados pela API são usados em uma conversão ilustrativa para reais (fator 5,2 definido no JavaScript). Altere `DOLAR_PARA_REAL_DEMO` se quiser modificar a simulação.
- O checkout apenas demonstra o fluxo. Não coleta dados bancários e não processa pagamentos.
- Para uma loja real, será necessário backend, banco de dados, autenticação, estoque próprio e integração segura com um gateway de pagamento.
