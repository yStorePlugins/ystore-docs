# yPlayerShop
<secondary-label ref="management"/>

### Descrição
Dê adeus as lojinhas de baús e entre na era moderna dos menus!

### Versões
<secondary-label ref="1.8"/>
<secondary-label ref="1.9"/>
<secondary-label ref="1.10"/>
<secondary-label ref="1.11"/>
<secondary-label ref="1.12"/>
<secondary-label ref="1.13"/>
<secondary-label ref="1.14"/>
<secondary-label ref="1.15"/>
<secondary-label ref="1.16"/>
<secondary-label ref="1.17"/>
<secondary-label ref="1.18"/>
<secondary-label ref="1.19"/>
<secondary-label ref="1.20"/>

### Demonstração
<video src="//www.youtube.com/watch?v=2r37JGfQFj8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/playershop&nbsp;- Abre o menu principal
/playershop [player]&nbsp;- Abre o menu da loja do player
/playershop favoritas&nbsp;- Abre o menu de lojas favoritas
/playershop help&nbsp;- Envia a mensagem de ajuda
/playershop&nbsp;giveslot&nbsp;- Dá slots para um jogador
/playershop&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yplayershop.use - Permissão para o /playershop
yplayershop.favorites - Permissão para o /playershop favoritas
yplayershop.help - Permissão para o /playershop help
yplayershop.look - Permissão para o /playershop [player]
yplayershop.giveslot - Permissão para o /playershop giveslot
yplayershop.admin.reload - Permissão para o /playershop reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPlayerShop/
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="commands.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     ___                                          _
#    / __\___  _ __ ___  _ __ ___   __ _ _ __   __| |___
#   / /  / _ \| '_ ` _ \| '_ ` _ \ / _` | '_ \ / _` / __|
#  / /__| (_) | | | | | | | | | | | (_| | | | | (_| \__ \
#  \____/\___/|_| |_| |_|_| |_| |_|\__,_|_| |_|\__,_|___/
#
# Lista de comandos do plugin.

# Utilize "comando|comando" para criar aliases.
# Por exemplo: "gm|gamemode"
# Você pode criar quantas aliases quiser.
commands:
  playershop: 'playershop|playerloja|shopplayer|lojaplayer'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        ____  _                       ____  _
#  _   _|  _ \| | __ _ _   _  ___ _ __/ ___|| |__   ___  _ __
# | | | | |_) | |/ _` | | | |/ _ \ '__\___ \| '_ \ / _ \| '_ \
# | |_| |  __/| | (_| | |_| |  __/ |   ___) | | | | (_) | |_) |
#  \__, |_|   |_|\__,_|\__, |\___|_|  |____/|_| |_|\___/| .__/
#  |___/               |___/                            |_|
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

# Modo de depuração para correção de problemas no plugin.
debug-mode: false

#      ___      _        _
#     /   \__ _| |_ __ _| |__   __ _ ___  ___
#    / /\ / _` | __/ _` | '_ \ / _` / __|/ _ \
#   / /_// (_| | || (_| | |_) | (_| \__ \  __/
#  /___,' \__,_|\__\__,_|_.__/ \__,_|___/\___|
#
# Configurações do banco de dados.

database:
  # Determina o tipo de banco de dados. Valores válidos: [SQLITE, MYSQL, HIKARI (recomendado)]
  storage-type: SQLITE

  # Dados para conexão ao banco de dados MYSQL.
  data:
    # Endereço de conexão do banco de dados. [EX: 127.0.0.1]
    host: localhost
    # Porta de conexão do banco de dados. [EX: 3306]
    port: 3306
    # Nome do banco de dados a ser conectado. [EX: minecraft]
    database: ''
    # Usuário de conexão. [EX: root]
    username: ''
    # Senha do usuário de conexão: [EX: 123]
    password: ''

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

slots:
  # Quantia padrão de slots que o jogador irá ter
  default: 1
  # Quantia máxima de slots que o jogador poderá ter
  max: 20
  # Item do slot que será ativável
  item:
    material: 'HOPPER'
    name: '&bSlots'
    lore:
      - ''
      - '&fQuantia: &a{amount}'
      - ''
      - '&7Clique com botão direito para ativar.'

categories:
  # Quantia máxima de categorias que o jogador poderá ter
  max: 5

# Configuração da barra de avaliação
rating:
  symbol-full: '&e★'
  symbol-empty: '&f☆'
]]>
</code-block>
</chapter>

<chapter title="economies.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#  _____                                  _
# | ____| ___  ___  _ __   ___  _ __ ___ (_) ___  ___
# |  _|  / __|/ _ \| '_ \ / _ \| '_ ` _ \| |/ _ \/ __|
# | |___| (__| (_) | | | | (_) | | | | | | |  __/\__ \
# |_____|\___|\___/|_| |_|\___/|_| |_| |_|_|\___||___/

# Providers disponíveis:
#
#   AtlasEconomiaSecundaria, AtlasMinas, AtlasMinasV2,
#   JH_Shop, LegendaryEconomy, NextCash, PlayerPoints,
#   StormEconomiaSecundaria, StormMinas, TGCash,
#   yAlmas, yPoints, yRankup,
#   Vault
#

# Economia padrão que irá vir na placa
# Deixe '' (vazio) para não usar
default: 'money'

economies:
  money:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'Money'
    # Formato inteiro
    display: 'Dinheiro'
    # Formato abreviado
    abbreviated: 'coins'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yplayershop.provider.money'
    # ‘Item’ que aparecerá no menu
    item:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ''
        - ' &f* Valor de compra: &a{buy}&f.'
        - ' &f* Valor de venda: &a{sell}&f.'
        - ''
        - '&aBotão &fESQUERDO&a para alterar o valor de compra'
        - '&aBotão &fDIREITO&a para alterar o valor de venda'
        - '&aBotão &fQ&a para excluir essa economia'
]]>
</code-block>
</chapter>

<chapter title="menus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___ _ __  _   _ ___
#   /    \ / _ \ '_ \| | | / __|
#  / /\/\ \  __/ | | | |_| \__ \
#  \/    \/\___|_| |_|\__,_|___/
#
# Sistema de menus.

# Setas dos menus.
arrows:
  back:
    material: 'ARROW:0'
    name: '&cVoltar'
    lore: ['&7Clique para voltar ao menu anterior.']
  previous:
    material: 'ARROW:0'
    name: '&cAnterior'
    lore: ['&7Clique para ir à página anterior.']
  next:
    material: 'ARROW:0'
    name: '&aPróximo'
    lore: ['&7Clique para ir à próxima página.']

# Menu principal
main:
  name: '&8Loja'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  empty-slot: 22
  my-shop-slot: 39
  favorites-slot: 41
  items:
    empty:
      material: 'WEB'
      name: '&eVazio...'
      lore: [ '&7Nenhuma loja aberta', '&7no momento.' ]
    my-shop:
      material: '182d36b973e57e4c0fe28c371a7f11fc04a2a342a88a7e5e5d83edbcab61770e'
      name: '&aMinha Loja'
      lore: [ '', ' &fSlots ocupados: &c{slots_used}&7/&a{slots_total}', ' &fEstoque atual: &b{stock} itens', ' &fAvaliação: &e{rating} &7({rating_raw}/5.0) {rating_amount}', '', '&aClique para gerenciar sua loja' ]
    shop:
      material: '{player}'
      name: '&eLoja de {player}'
      lore: [ '', ' &fAvaliação: &e{rating} &7({rating_raw}/5.0) {rating_amount}', '', '&aClique para visualizar' ]
    favorites:
      material: 'd4a1d6d0a62e1e46e76fec45a5dd2ffbe4bf0b35b7f4c75f6d23f676f77992fd'
      name: '&eFavoritas'
      lore: [ '', ' &fLojas favoritadas: &b{amount}', '', '&aClique para visualizar' ]

# Menu de lojas favoritas
favorites:
  name: '&8Loja'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  back-slot: 38
  previous-slot: 41
  next-slot: 42
  items:
    shop:
      material: '{player}'
      name: '&eLoja de {player}'
      lore: [ '', ' &fAvaliação: &e{rating} &7({rating_raw}/5.0) {rating_amount}', '', '&aClique para visualizar' ]
  facing:
    e1:
      slot: 11
      material: 'STAINED_GLASS_PANE:14'
    e2:
      slot: 12
      material: 'STAINED_GLASS_PANE:14'
    e3:
      slot: 13
      material: 'STAINED_GLASS_PANE:14'
    e4:
      slot: 14
      material: 'STAINED_GLASS_PANE:14'
    e5:
      slot: 15
      material: 'STAINED_GLASS_PANE:14'
    e6:
      slot: 20
      material: 'STAINED_GLASS_PANE:14'
    e7:
      slot: 21
      material: 'STAINED_GLASS_PANE:14'
    e8:
      slot: 22
      material: 'STAINED_GLASS_PANE:14'
    e9:
      slot: 23
      material: 'STAINED_GLASS_PANE:14'
    e10:
      slot: 24
      material: 'STAINED_GLASS_PANE:14'

# Menu de configuração da loja
my-shop:
  name: '&8Loja'
  size: 54
  slots: [ 12, 13, 14, 15, 16, 21, 22, 23, 24, 25 ]
  back-slot: 37
  previous-slot: 42
  next-slot: 43
  items:
    info-slot: 10
    categories-slot: 19
    settings-slot: 39
    preview-slot: 40
    add-cancel-slot: 41
    item:
      lore:
        - ''
        - '&fEstoque: &b{amount}'
        - '&fCategoria: &b{category}'
        - ''
        - '&aBotão &fESQUERDO &apara configurar'
        - '&aBotão &fQ &apara deletar'
    info:
      material: '182d36b973e57e4c0fe28c371a7f11fc04a2a342a88a7e5e5d83edbcab61770e'
      name: '&aInformações'
      lore:
        - ''
        - ' &fSlots ocupados: &c{slots_used}&7/&a{slots_total}'
        - ' &fEstoque atual: &b{stock} itens'
        - ' &fAvaliação: &e{rating} &7({rating_raw}/5.0) {rating_amount}'
        - ''
        - ' &fLoja aberta: {status}'
        - ''
        - '&aClique para abrir ou fechar a loja'
    categories:
      material: BOOK
      name: '&aCategorias'
      lore:
        - ''
        - ' &fCategorias criadas: &e{amount}'
        - ''
        - '&aClique para gerenciar'
    settings:
      material: HOPPER
      name: '&aConfigurações do Menu'
      lore:
        - '&7Configure o tamanho, slots'
        - '&7setas e botões diversos.'
        - ''
        - '&aClique para gerenciar'
    preview:
      material: EYE_OF_ENDER
      name: '&aPre-visualização'
      lore:
        - '&7Veja como irá ficar a sua'
        - '&7loja para os outros jogadores.'
        - ''
        - '&aClique para ver'
    add:
      material: '32332b770a4874698862855da5b3fe47f19ab291df766b6083b5f9a0c3c6847e'
      name: '&aAdicionar Item'
      lore:
        - '&7Adicione mais um item no'
        - '&7catálogo de sua loja.'
        - ''
        - '&f * Ao ativar o modo seleção'
        - '&f clique em um item no seu inventário'
        - ''
        - '&aClique para ativar o modo'
    cancel:
      material: '32cbdc9d4c590eac285a4544f2b1e068bd27fd52173ac8d7679013823cbab95a'
      name: '&aCancelar Seleção'
      lore:
        - '&7Saia do modo de seleção de itens'
        - '&7para o catálogo de sua loja.'
        - ''
        - '&f * Clique em um item no seu inventário'
        - ''
        - '&aClique para desativar o modo'
    slot-empty:
      material: 'STAINED_GLASS_PANE:5'
      name: '&aSlot Livre'
    slot-need:
      material: 'STAINED_GLASS_PANE:14'
      name: '&cSlot Bloqueado'

# Menu de opções da loja
my-shop-options:
  name: '&8Loja'
  size: 27
  back-slot: 22
  items:
    size-slot: 10
    back-slot-slot: 12
    previous-slot-slot: 13
    next-slot-slot: 14
    review-slot-slot: 15
    favorite-slot-slot: 16
    size:
      material: CHEST
      name: '&aTamanho'
      lore:
        - '&7Tamanho do menu da'
        - '&7sua loja.'
        - ''
        - '&f Atual: &a{size}'
        - ''
        - '&aClique para alternar o tamanho'
    back-slot:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aBack-Slot'
      lore:
        - '&7Slot que a seta de voltar irá ficar'
        - '&7no menu principal da loja.'
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aClique para alterar'
    previous-slot:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aPrevious-Slot'
      lore:
        - '&7Slot que a seta da página anterior irá'
        - '&7ficar no menu principal da loja.'
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aClique para alterar'
    next-slot:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aNext-Slot'
      lore:
        - '&7Slot que a seta da página seguinte irá'
        - '&7ficar no menu principal da loja.'
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aClique para alterar'
    review-slot:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aReview-Slot'
      lore:
        - '&7Slot que o ícone de avaliar irá'
        - '&7ficar no menu principal da loja.'
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aClique para alterar'
    favorite-slot:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aFavorite-Slot'
      lore:
        - '&7Slot que o ícone de favoritar irá'
        - '&7ficar no menu principal da loja.'
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aClique para alterar'

# Menu de opções do item
item-options:
  name: '&8Loja'
  size: 27
  back-slot: 10
  items:
    stock-add-slot: 12
    stock-remove-slot: 13
    category-slot: 14
    type-slot: 15
    economies-slot: 16
    stock-add:
      material: '32332b770a4874698862855da5b3fe47f19ab291df766b6083b5f9a0c3c6847e'
      name: '&a+ Estoque'
      lore:
        - '&7Adicione mais itens ao'
        - '&7estoque da sua loja.'
        - ''
        - ' &f Atual: &a{amount}'
        - ''
        - '&aBotão &fESQUERDO&a para adicionar 64'
        - '&aBotão &fDIREITO&a para adicionar 1'
        - '&aBotão &fQ&a para adicionar TUDO'
    stock-remove:
      material: '32cbdc9d4c590eac285a4544f2b1e068bd27fd52173ac8d7679013823cbab95a'
      name: '&c- Estoque'
      lore:
        - '&7Remova alguns itens do'
        - '&7estoque da sua loja.'
        - ''
        - ' &f Atual: &a{amount}'
        - ''
        - '&aBotão &fESQUERDO&a para remover 64'
        - '&aBotão &fDIREITO&a para remover 1'
        - '&aBotão &fQ&a para remover TUDO'
    category:
      material: 'BOOK'
      name: '&eCategoria'
      lore:
        - '&7Defina a categoria que este'
        - '&7item irá ficar na loja.'
        - ''
        - ' &f Atual: &a{category}'
        - ''
        - '&aClique para alterar'
    type-buy:
      material: '7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      name: '&aTipo da loja'
      lore:
        - '&7Tipo da sua loja:'
        - ''
        - ' &f• &aComprar item &8(Jogadores vendem a você)'
        - ' &f• &7Vender item &8(Jogadores compram de você)'
        - ' &f• &7Comprar e vender item'
        - ''
        - '&aClique para alterar'
    type-sell:
      material: '7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      name: '&aTipo da loja'
      lore:
        - '&7Tipo da sua loja:'
        - ''
        - ' &f• &7Comprar item &8(Jogadores vendem a você)'
        - ' &f• &aVender item &8(Jogadores compram de você)'
        - ' &f• &7Comprar e vender item'
        - ''
        - '&aClique para alterar'
    type-buy-sell:
      material: '7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      name: '&aTipo da loja'
      lore:
        - '&7Tipo da sua loja:'
        - ''
        - ' &f• &7Comprar item &8(Jogadores vendem a você)'
        - ' &f• &7Vender item &8(Jogadores compram de você)'
        - ' &f• &aComprar e vender item'
        - ''
        - '&aClique para alterar'
    economies:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomias'
      lore:
        - '&7Configure os preços de compra'
        - '&7e venda que este item terá.'
        - ''
        - '&aClique para alterar'

# Menu de seleção de economias
providers:
  name: '&8Selecionar economia'
  size: 27
  previous: 9
  next: 17
  back: 18
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]

# Menu da loja do player
player-shop:
  name: '&8Loja de: &7{player}'
  item:
    buy: '&2C &r{price_buy} &7({provider_abbreviated})'
    sell: '&cV &r{price_sell} &7({provider_abbreviated})'
    buy-sell: '&2C &r{price_buy} | &cV &r{price_sell} &7({provider_abbreviated})'
    none: '&cNenhuma economia configurada.'
    lore:
      - ''
      - '&fEstoque: &b{amount}'
      - '&fCategoria: &b{category}'
      - ''
      - '{formats}'
      - ''
      - '&aClique para comercializar'
    category-lore:
      - '&aClique para desselecionar'
  items:
    slot-empty:
      material: 'STAINED_GLASS_PANE:5'
      name: '&aSlot Livre'
    slot-need:
      material: 'STAINED_GLASS_PANE:14'
      name: '&cSlot Bloqueado'
    favorite:
      material: 'd4a1d6d0a62e1e46e76fec45a5dd2ffbe4bf0b35b7f4c75f6d23f676f77992fd'
      name: '&eFavoritar'
      lore: [ '&7Coloque esta loja na', '&7sua lista de lojas favoritas.', '', ' &fFavorita: &r{status}&f.', '', '&aClique para alternar' ]
    review:
      material: 'GLASS_BOTTLE'
      name: '&eAvaliar'
      lore: [ '&7Avalie essa loja com uma', '&7nota de 0 a 5.', '', ' &cVocê ainda não avaliou', '' ]
    review-already:
      material: 'EXP_BOTTLE'
      name: '&eAvaliar'
      lore: [ '&7Avalie essa loja com uma', '&7nota de 0 a 5.', '', ' &fSua avaliação: &e{rating} &7({rating_raw}/5.0) {rating_amount}', '' ]

# Menu de avaliar a loja
review:
  name: '&8Loja de: &7{player}'
  size: 27
  back-slot: 10
  items:
    one-slot: 12
    two-slot: 13
    three-slot: 14
    four-slot: 15
    five-slot: 16
    one:
      material: 'd55fc2c1bae8e08d3e426c17c455d2ff9342286dffa3c7c23f4bd365e0c3fe'
      name: '&e+1'
      lore:
        - '&7Avalie esta loja com'
        - '&7apenas 1 estrela.'
        - ''
        - '&aClique para avaliar'
    two:
      material: 'dc61b04e12a879767b3b72d69627f29a83bdeb6220f5dc7bea2eb2529d5b097'
      name: '&e+2'
      lore:
        - '&7Avalie esta loja com'
        - '&7apenas 2 estrelas.'
        - ''
        - '&aClique para avaliar'
    three:
      material: '6823f77558ca6060b6dc6a4d4b1d86c1a5bee7081677bbc336ccb92fbd3ee'
      name: '&e+3'
      lore:
        - '&7Avalie esta loja com'
        - '&73 estrelas.'
        - ''
        - '&aClique para avaliar'
    four:
      material: '91b9c4d6f7208b1424f8595bfc1b85ccaaee2c5b9b41e0f564d4e0aca959'
      name: '&e+4'
      lore:
        - '&7Avalie esta loja com'
        - '&74 estrelas.'
        - ''
        - '&aClique para avaliar'
    five:
      material: 'bc1415973b42f8286f948e2140992b9a29d80965593b14553d644f4feafb7'
      name: '&e+5'
      lore:
        - '&7Avalie esta loja com'
        - '&75 estrelas.'
        - ''
        - '&aClique para avaliar'

# Menu de compra e venda
buy-sell:
  name: '&8Loja de: &7{player}'
  size: 27
  back-slot: 9
  item:
    buy: '&2C &r{price_buy} &7({provider_abbreviated}) a cada &f{amount}'
    sell: '&cV &r{price_sell} &7({provider_abbreviated}) a cada &f{amount}'
    buy-sell: '&2C &r{price_buy} | &cV &r{price_sell} &7({provider_abbreviated}) a cada &f{amount}'
    lore:
      - ''
      - '&fEstoque: &b{amount}'
      - '&fCategoria: &b{category}'
      - ''
      - '{formats}'
      - ''
  items:
    display-slot: 11
    buy-slot: 13
    sell-slot: 14
    amount-slot: 16
    buy:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aComprar'
      lore:
        - '&7Comprar o item à venda'
        - ''
        - '{formats}'
        - ''
        - ' &7Estoque atual: &f{stock}'
        - ''
        - '&aBotão &fESQUERDO&a para comprar &f{amount}'
    sell:
      material: 'c532576b8bc9a876419a39ae4498c456fe9ee5bdc7ba91fd3b2f1b0a7eb91'
      name: '&aVender'
      lore:
        - '&7Vender seus itens à loja'
        - ''
        - '{formats}'
        - ''
        - '&aBotão &fESQUERDO&a para vender &f{amount}'
    amount:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&aQuantia'
      lore:
        - '&7Configure a quantia que gostaria'
        - '&7de comercializar nessa loja.'
        - ''
        - ' &fAtual: &b{amount}'
        - ''
        - '&aClique para alterar'

# Menu de configuração da loja (categorias)
categories:
  name: '&8Loja'
  size: 45
  slots: [ 12, 13, 14, 15, 16 ]
  back-slot: 28
  previous-slot: 33
  next-slot: 34
  items:
    add-slot: 10
    add:
      material: '924757bc9a3171f9d0fdfbd209ac42e15f7744eb5f2db31920ff8af8d94567c6'
      name: '&aAdicionar categoria'
      lore:
        - ''
        - ' &fCategorias criadas: &e{amount}'
        - ''
        - '&aClique para adicionar &f+1'
    slot-empty:
      material: 'STAINED_GLASS_PANE:5'
      name: '&aSlot Livre'
    # Configuração do item da categoria
    categories:
      name: '&e{name}'
      lore:
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aBotão &fESQUERDO &apara configurar'
        - '&aBotão &fQ &apara deletar'

# Menu de opções da categoria
categories-options:
  name: '&8Loja'
  size: 27
  back-slot: 22
  items:
    icon-slot: 11
    slot-slot: 13
    name-slot: 15
    icon:
      name: '&aÍcone'
      lore:
        - '&aClique para alterar o ícone'
    slot:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aSlot'
      lore:
        - '&7Slot que a categoria irá ficar'
        - '&7no menu principal da loja.'
        - ''
        - '&fSlot: &b{slot}'
        - ''
        - '&aClique para alterar'
    name:
      material: 'e4d49bae95c790c3b1ff5b2f01052a714d6185481d5b1c85930b3f99d2321674'
      name: '&aNome'
      lore:
        - '&7Nome que irá mostrar no ícone'
        - '&7da categoria na loja.'
        - ''
        - '&fAtual: &7{name}&f.'
        - ''
        - '&aClique para alterar o nome'

# Menu de configuração da loja (categorias)
categories-icon:
  name: '&8Loja'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 37, 38, 39 ]
  back-slot: 45
  previous-slot: 41
  next-slot: 43
  items:
    add-slot: 42
    add:
      material: '62d90ad63dd826df02994abdcc6c2306163e1072d1b9e63ad4e7d7d1cf87cdf9'
      name: '&eDefinir Item'
      lore:
      - '&7Clique para definir um'
      - '&7item customizado no baú.'
      - '&7(custom-skull ou item específico)'
]]>
</code-block>
</chapter>

<chapter title="messages.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___  ___ ___  __ _  __ _  ___  ___
#   /    \ / _ \/ __/ __|/ _` |/ _` |/ _ \/ __|
#  / /\/\ \  __/\__ \__ \ (_| | (_| |  __/\__ \
#  \/    \/\___||___/___/\__,_|\__, |\___||___/
#                              |___/
#
# Plugin messages

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &aShop comandos:

    &a> /playershop
    &a> /playershop favoritas
    &a> /playershop <player>
    &a> /playershop giveslot <player> <quantia>

  yourself: '&cVocê não pode executar esse comando em sí mesmo.'
  slots-need: '&cVocê precisa de mais slots livres.'
  slot-activated: '&aVocê ativou &e{amount} &ade slots.'
  slot-max: '&cVocê já chegou no máximo.'
  slot-give: '&aVocê deu &e{amount} &ade slots para o jogador &e{player}&a.'
  category-digit-icon: |
    &aDigite o item que você deseja
    &7para cancelar digite &ncancelar&7
  category-digit-slot: |
    &aDigite o slot que você deseja
    &7para cancelar digite &ncancelar&7
  category-digit-name: |
    &aDigite o nome que você deseja
    &7para cancelar digite &ncancelar&7
  category-change-icon: '&aVocê mudou o ícone da categoria com sucesso.'
  category-change-slot: '&aVocê mudou o slot da categoria para {slot}.'
  category-change-name: '&aVocê mudou o nome da categoria para {name}.'
  reviewed: '&aVocê avaliou a loja de &f{player}&a com &f{amount} estrelas&a.'
  digit-slot: |
    &aDigite o slot que você deseja
    &7para cancelar digite &ncancelar&7
  digit-amount: |
    &aDigite o valor que você deseja
    &7para cancelar digite &ncancelar&7
  change-slot: '&aVocê mudou o slot para {slot}.'
  change-amount: '&aVocê mudou o valor para {amount}.'
  inv-full: '&cSeu inventário está cheio. É necessário no mínimo um slot vazio.'
  stock-add: '&aVocê adicionou &f{amount}x &aitens no estoque.'
  stock-remove: '&aVocê removeu &f{amount}x &aitens do estoque.'
  cant-buy: '&cEste item não foi completamente configurado.'
  stock-has: '&cEsta loja possui apenas {amount}x itens em estoque.'
  owner-offline: '&cEsta loja possui uma economia que não permite que o dono esteja offline e o dono desta loja está offline.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  no-balance-owner: '&cO jogador {player} não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  inv-amount-empty: '&cVocê precisa de {amount}x slots vazios.'
  bought: '&aVocê comprou &f{amount}x&a itens na loja de &f{player}&a.'
  sell: '&aVocê vendeu &f{amount}x&a itens na loja de &f{player}&a.'
  inv-has: '&cVocê possui apenas {amount}x itens no inventário.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/142-yPlayerShop">Site do plugin yPlayerShop</a>
    </category>
</seealso>