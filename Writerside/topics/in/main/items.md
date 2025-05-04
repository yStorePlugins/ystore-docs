# Como usar o ItemStack Builder

# Opções Disponíveis no `ConfigurationSection`

Aqui estão os parâmetros que podem ser passados para o `section` e seus respectivos efeitos:

### `id / ID / material / Material`
- **Descrição**: Define o tipo de material do item. Pode ser um nome de material do Minecraft (ex: `STONE`, `IRON_SWORD`) ou o id de um material (ex: `1` para `STONE`).
- **Exemplo**: `"id: 'DIAMOND_SWORD'"`

### `data / Data`
- **Descrição**: Especifica o valor de dados para o item, caso o material possua variações (ex: cor de couro ou tipo de bloco).
- **Exemplo**: `"data: 5"`

### `amount / Amount`
- **Descrição**: Define a quantidade do item. O valor padrão é 1 se não especificado.
- **Exemplo**: `"amount: 5"`

### `name / Name`
- **Descrição**: Define o nome do item. O nome pode ser estilizado com códigos de cor (`&`).
- **Exemplo**: `"name: '&6Espada de Diamante'"`

### `lore / Lore`
- **Descrição**: Define a descrição do item. A descrição pode ser estilizada com códigos de cor (`&`).
- **Exemplo**: `"lore: ['&7A espada mais forte do mundo']"`

### `glow / Glow`
- **Descrição**: Define se o item terá o efeito de brilho. Se `true`, o item brilhará.
- **Exemplo**: `"glow: true"`

### `custom-skull / CustomSkull`
- **Descrição**: Define se o item será uma cabeça personalizada (ex: uma cabeça de jogador ou uma cabeça com textura customizada).
- **Exemplo**: `"custom-skull: true"`
- Caso seja `true`, a URL da cabeça será configurada em `url`.

### `url / URL`
- **Descrição**: URL de uma imagem personalizada usada para itens do tipo "skull" (cabeça). Isso é utilizado quando o item é uma cabeça customizada.
- **Exemplo**: `"url: 'http://textures.minecraft.net/texture/abc123'"`

### `hide-attributes`
- **Descrição**: Se `true`, oculta os atributos do item.
- **Exemplo**: `"hide-attributes: true"`

### `hide-potion-effects`
- **Descrição**: Se `true`, oculta os efeitos da poção.
- **Exemplo**: `"hide-potion-effects: true"`

### `hide-unbreakable`
- **Descrição**: Se `true`, oculta a informação de que o item é inquebrável.
- **Exemplo**: `"hide-unbreakable: true"`

### `hide-destroys`
- **Descrição**: Se `true`, oculta os blocos que o item pode destruir.
- **Exemplo**: `"hide-destroys: true"`

### `hide-placed-on`
- **Descrição**: Se `true`, oculta os blocos onde o item pode ser colocado.
- **Exemplo**: `"hide-placed-on: true"`

### `hide-enchants`
- **Descrição**: Se `true`, oculta os encantamentos do item.
- **Exemplo**: `"hide-enchants: true"`

### `disable-metadata`
- **Descrição**: Se `true`, desativa a adição de metadados NBT no item.
- **Exemplo**: `"disable-metadata: true"`

### `flags`
- **Descrição**: Define as flags do item. As flags alteram o comportamento e a aparência do item.
- **Exemplo**: `"flags: ['HIDE_ENCHANTS', 'HIDE_UNBREAKABLE']"`

### `custom-model-data`
- **Descrição**: Define o ID do modelo customizado para o item, permitindo usar modelos personalizados.
- **Exemplo**: `"custom-model-data: 123"`

### `color`
- **Descrição**: Define a cor do item. Usado principalmente em armaduras de couro.
- **Exemplo**: `"color: '255:0:0'"` (representa a cor vermelha em RGB).

### `nbt-tag / nbt-tag-int / nbt-tag-short / nbt-tag-byte`
- **Descrição**: Define os NBT tags adicionais para o item. São usados para armazenar dados extras no item (ex: etiquetas personalizadas, atributos adicionais).
- **Exemplo**: `"nbt-tag: ['CustomName=>Meu Item']"`

### `effects`
- **Descrição**: Define os efeitos de poção para itens do tipo `POTION`. O formato é `"POTION_TYPE-EXTEND-UPGRADE"`.
- **Exemplo**: `"effects: ['SPEED-true-false']"`
