# marketing.office.place — Gamer Store

Projeto de loja virtual demonstrativa baseado na estrutura do ZIP TucanStore. O tema foi adaptado para produtos de tecnologia e público gamer, com visual escuro, verde neon e azul ciano.

## Funcionalidades
- Catálogo carregado de forma dinâmica pela API pública DummyJSON.
- Categorias: notebooks, smartphones e acessórios.
- Busca por nome/descrição, filtro por categoria e ordenação.
- Carrinho com quantidade, remoção de itens e total.
- Carrinho salvo no `localStorage` do navegador.
- Layout responsivo para celular, tablet e computador.

## Passo a passo para executar
1. Extraia o arquivo ZIP em uma pasta do computador.
2. Abra a pasta `marketing-office-place` no Visual Studio Code.
3. Confira se existem `index.html`, `style.css`, `script.js` e `README.md`.
4. Abra o `index.html` no navegador. Recomendado: usar a extensão **Live Server** no VS Code e clicar em **Go Live**.
5. Verifique o status “API conectada” na área de produtos. É necessário ter internet para consultar a API.
6. Digite no campo de busca, selecione uma categoria ou altere a ordenação.
7. Clique em “Adicionar ao carrinho”, abra o carrinho e teste a remoção e o total.

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
