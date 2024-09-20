# Binance - Blockchain Developer with Solidity

Este projeto foi desenvolvido durante um bootcamp na plataforma Digital Innovation One (DIO), com o objetivo de implementar um token ERC20 na blockchain Ethereum usando Solidity.

## Descrição

O projeto consiste na criação de um contrato inteligente para o token `DIOToken`, que segue o padrão ERC20, amplamente utilizado na blockchain Ethereum. O contrato inclui funcionalidades básicas para operações com tokens, como transferências, aprovações e consultas de saldo.

## Funcionalidades

- **SafeMath**: Uma biblioteca interna para realizar operações matemáticas com segurança, evitando problemas como overflow e underflow.
- **ERC20 Interface**: Define as funções padrão para um token ERC20, como `totalSupply`, `balanceOf`, `transfer`, `approve`, `transferFrom`, `allowance`, além dos eventos `Transfer` e `Approval`.
- **DIOToken**: Implementa o contrato do token com as seguintes características:
  - Símbolo: `DIO`
  - Nome: `DIO Token`
  - Decimais: 2
  - Suprimento Total: 100.000 tokens
  - Os tokens iniciais são alocados para o endereço `0x5ab5a63E3928c1E86dE83aed75e6BadF3a494e43`.

## Funções Principais

- `totalSupply()`: Retorna o total de tokens em circulação, excluindo os que foram destruídos.
- `balanceOf(address tokenOwner)`: Retorna o saldo de tokens de um determinado endereço.
- `transfer(address to, uint tokens)`: Transfere uma quantidade específica de tokens do remetente para o destinatário.
- `approve(address spender, uint tokens)`: Aprova um endereço para gastar uma quantidade específica de tokens em nome do remetente.
- `transferFrom(address from, address to, uint tokens)`: Transfere tokens de um endereço para outro usando a aprovação prévia.
- `allowance(address tokenOwner, address spender)`: Retorna a quantidade de tokens que um `spender` pode gastar em nome do `tokenOwner`.
- `approveAndCall(address spender, uint tokens, bytes data)`: Aprova tokens para um `spender` e notifica o contrato receptor.

## Como Usar

1. Clone o repositório e instale as dependências necessárias para compilar e testar o contrato Solidity.
2. Compile o contrato utilizando um compilador Solidity compatível (versão 0.4.24).
3. Faça o deploy do contrato na rede Ethereum usando ferramentas como Remix, Truffle, ou Hardhat.
4. Interaja com o contrato através de um cliente web3 ou usando a interface do Remix para executar as funções disponíveis.

## Requisitos

- Solidity 0.4.24
- Node.js e npm (para ferramentas de desenvolvimento, como Truffle ou Hardhat)
- MetaMask ou outro provedor web3 para interagir com o contrato na blockchain

## Instalação

1. Clone o repositório:

    ```bash
    git clone https://github.com/alyssonzanchi/DIO-Token.git
    ```

2. Compile o contrato:

    ```bash
    truffle compile
    ```

3. Faça o deploy na rede desejada:

    ```bash
    truffle migrate
    ```

## Licença

Este projeto é licenciado sob a licença MIT. Isso significa que você pode usar, copiar, modificar, fundir, publicar, distribuir, sublicenciar e/ou vender cópias do software, desde que a atribuição apropriada seja dada ao autor original. Para mais detalhes, consulte o arquivo [LICENSE](LICENSE).

## Contato

Para quaisquer dúvidas, sugestões ou feedback, entre em contato através:

- LinkedIn: [linkedin.com/in/alyssonzanchi](https://www.linkedin.com/in/alyssonzanchi/)
- GitHub: [github.com/alyssonzanchi](https://github.com/alyssonzanchi)

Se precisar de suporte ou tiver alguma dúvida específica sobre o código, sinta-se à vontade para abrir uma issue no repositório.

## Agradecimentos

Este projeto foi desenvolvido durante o bootcamp "Binance - Blockchain Developer with Solidity" na [Digital Innovation One](https://web.dio.me/). Agradecimentos especiais aos instrutores e à comunidade DIO pelo suporte e aprendizado contínuo.

---

© 2024 [Alysson Zanchi]. Todos os direitos reservados.
