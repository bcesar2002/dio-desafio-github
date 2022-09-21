# Descrição do Desafio 1 - Projojeto Conceitual E-Commerce

<p>O esquema deverá ser adicionado a um repositório do Github para futura avaliação do desafio de projeto. Adicione ao Readme a descrição do projeto conceitual para fornecer o contexto sobre seu esquema.</p>

### Objetivo:

<p>Refine o modelo apresentado acrescentando os seguintes pontos:</p>

- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações. 
  + O atributo "tipoCliente" sinaliza se o clente é PF ou PJ; sendo PF, o atributo "CPF" deve ser preenchido e o atributo "CNPJ" será vazio, e vice versa. O mesmo vale para a entidade "Vendedor", através do atributo "tipoVendedor"
- Pagamento – O cliente pode cadastrar mais de uma forma de pagamento.
  + A entidade "FormaPagto" contém as opções de pagamento de cada cliente. Essa entidade tem um atributo "idFormaPagto", que contém o número do cartão de débito/crédito, quando for o caso. Possui uma chave primária composta (identificador do cliente + um sequencial, este último possibilita ter várias formas de pagamento). O identificador do cliente também funciona como chave estrangeira.
- Entrega – Possui status e código de rastreio.
  + Cada pedido possui uma entrega, com previsão de entrega, valor do frete, endereço de entrega e status, além do código de rastreio.

## Levantamento de requisitos/narrativa:

<ol>
  <li> Narrativa do Produto:</li>
    <ul>
      <li> Os produtos são vendidos por uma única plataforma online. Contudo, podem ter vendedores distintos(terceiros)</li>
      <li> Cada produto possui um fornecedor</li>
      <li> Um ou mais produtos podem compor um pedido</li>
    </ul>
  <li> Narrativa do Cliente:</li>
    <ul>
      <li> O cliente pode ser cadastrar no site com seu CPF ou CNPJ</li>
      <li> O endereço do cliente irá determinar o valor do frete</li>
      <li> Um cliente pode comprar mais de um pedido. Este tem um período de carência para devolução do produto</li>
    </ul>
  <li> Narrativa do Pedido:</li>
      <ul>
        <li> Os pedidos são criados por clientes e possuem informações de compra, endereço e status de entrega</li>
        <li> Um produto ou mais compõem o pedido</li>
        <li> O pedido pode ser cancelado</li>
      </ul>
</ol>
