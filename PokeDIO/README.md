# PokeDIO - Pokemon Battle Game with NFTs

Este projeto foi desenvolvido como parte do **Bootcamp Binance - Blockchain Developer with Solidity** na plataforma **DIO**. Trata-se de um minigame de batalha de Pokémon onde os Pokémons são NFTs (Tokens Não Fungíveis). As imagens dos Pokémons são armazenadas no **IPFS**.

## 📜 Descrição
O PokeDIO é um contrato inteligente construído em Solidity que permite a criação, gerenciamento e batalhas entre Pokémons NFTs. Cada Pokémon possui um nome, nível e uma imagem, sendo que seu nível aumenta ao vencer batalhas. O dono de cada Pokémon pode iniciar batalhas com outros jogadores, e o nível dos Pokémons é atualizado com base no resultado da batalha.

### 🛠️ Funcionalidades
- **Criação de Pokémons:** Apenas o dono do contrato pode criar novos Pokémons.
- **Batalha entre Pokémons:** Apenas o dono de um Pokémon pode iniciá-la. O nível dos Pokémons é ajustado de acordo com o resultado da batalha.
- **Pokémons como NFTs:** Cada Pokémon é um NFT único, baseado no padrão **ERC721**, e pode ser transferido entre jogadores.

### 🔗 Tecnologias Utilizadas
- **Solidity**: Linguagem de programação para contratos inteligentes no Ethereum.
- **OpenZeppelin**: Biblioteca utilizada para o padrão **ERC721**.
- **IPFS**: Sistema de armazenamento descentralizado para armazenar as imagens dos Pokémons.

## 🚀 Como Funciona

### 1. Criar um novo Pokémon
Somente o dono do jogo (endereço que implantou o contrato) pode criar novos Pokémons. Ao criar um novo Pokémon, você deve fornecer um nome, o endereço do proprietário e um link para a imagem armazenada no IPFS.

```solidity
function createNewPokemon(string memory _name, address _to, string memory _img) public;
```

### 2. Batalhar com um Pokémon
Somente o dono de um Pokémon pode iniciá-la. Ao iniciar uma batalha, o nível de ambos os Pokémons será ajustado conforme o resultado da luta.

```solidity
function battle(uint _attackingPokemon, uint _defendingPokemon) public;
```

- Se o nível do Pokémon atacante for maior ou igual ao do defensor, ele ganha 2 níveis, e o defensor ganha 1.
- Caso contrário, o atacante ganha 1 nível, e o defensor ganha 2.

### 🖼️ Imagens dos Pokémons
As imagens dos Pokémons são armazenadas no IPFS, e seus links são utilizados no contrato para referenciar visualmente cada NFT.

### 📄 Licença
Este projeto é licenciado sob a licença MIT. Isso significa que você pode usar, copiar, modificar, fundir, publicar, distribuir, sublicenciar e/ou vender cópias do software, desde que a atribuição apropriada seja dada ao autor original. Para mais detalhes, consulte o arquivo [LICENSE](LICENSE).

### Agradecimentos

Este projeto foi desenvolvido durante o bootcamp "Binance - Blockchain Developer with Solidity" na [Digital Innovation One](https://web.dio.me/). Agradecimentos especiais aos instrutores e à comunidade DIO pelo suporte e aprendizado contínuo.

---

© 2024 [Alysson Zanchi]. Todos os direitos reservados.