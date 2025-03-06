# yMarket
<secondary-label ref="management"/>

### Descrição
Comercialize itens de modo categorizado e com destaque

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
<secondary-label ref="1.21"/>

### Demonstração
<video src="//www.youtube.com/watch?v=bOlhWLRe6A0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mercado - Abre o menu principal.
/mercado vender [player] - Inicia uma venda no mercado.
/mercado pessoal - Abre o menu de vendas pessoais.
/mercado vendas - Abre o menu de vendas próprias.
/mercado ban - Banir um jogador do mercado.
/mercado unban - Desbanir um jogador do mercado.
/mercado setnpc - Setar o NPC.
/mercado delnpc - Deletar o NPC.
/mercado reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymercado.use - Permissão para o /mercadoymercado.sell - Permissão para o /mercado vender [player]ymercado.personal - Permissão para o /mercado pessoalymercado.sells - Permissão para o /mercado vendas
ymarket.announce - Permissão para enviar a mensagem de anúncio no chat ao anunciar
ymarket.sponsor - Permissão para destacar a venda sem custo
ymarket.sell_limit.[numero] - Permissão para ter um limite customizado de vendas simultâneasymercado.ban - Permissão para o /mercado banymercado.unban - Permissão para o /mercado unbanymercado.setnpc - Permissão para o /mercado setnpcymercado.delnpc - Permissão para o /mercado delnpcymercado.admin.reload - Permissão para o /mercado reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMarket/
    ├── categories.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="categories.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
categories:
  weapons:
    # Ordem de verificação da categoria
    order: 1
    # Nome da categoria nas mensagens
    name: '&fArmas'
    # Ícone da categoria nos menus
    icon:
      slot: 20
      material: 'DIAMOND_SWORD'
      name: '&aArmas'
      lore:
        - '&7A categoria de armas permite a'
        - '&7venda de itens de ataque e poções.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    # Itens permitidos na categoria
    items:
      # Permitir todos os DEMAIS itens (que não estiverem na BlackList da config.yml)
      all: false
      nbts: []
      names: []
      types:
        - 'DIAMOND_SWORD'
        - 'GOLD_SWORD'
        - 'IRON_SWORD'
        - 'STONE_SWORD'
        - 'WOOD_SWORD'
        - 'BOW'
        - 'ARROW'
        - 'GLASS_BOTTLE'
        - 'POTION'
  armors:
    order: 2
    name: '&fArmaduras'
    icon:
      slot: 21
      material: 'DIAMOND_CHESTPLATE'
      name: '&aArmaduras'
      lore:
        - '&7A categoria de armaduras permite a'
        - '&7venda de itens de defesa.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: false
      nbts: []
      names: []
      types:
        - 'DIAMOND_HELMET'
        - 'DIAMOND_CHESTPLATE'
        - 'DIAMOND_LEGGINGS'
        - 'DIAMOND_BOOTS'
        - 'GOLD_HELMET'
        - 'GOLD_CHESTPLATE'
        - 'GOLD_LEGGINGS'
        - 'GOLD_BOOTS'
        - 'IRON_HELMET'
        - 'IRON_CHESTPLATE'
        - 'IRON_LEGGINGS'
        - 'IRON_BOOTS'
        - 'LEATHER_HELMET'
        - 'LEATHER_CHESTPLATE'
        - 'LEATHER_LEGGINGS'
        - 'LEATHER_BOOTS'
        - 'CHAINMAIL_HELMET'
        - 'CHAINMAIL_CHESTPLATE'
        - 'CHAINMAIL_LEGGINGS'
        - 'CHAINMAIL_BOOTS'
  tools:
    order: 3
    name: '&fFerramentas'
    icon:
      slot: 22
      material: 'DIAMOND_PICKAXE'
      name: '&aFerramentas'
      lore:
        - '&7A categoria de ferramentas permite a'
        - '&7venda de itens de trabalho.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: false
      nbts: []
      names: []
      types:
        - 'DIAMOND_PICKAXE'
        - 'DIAMOND_AXE'
        - 'DIAMOND_SPADE'
        - 'DIAMOND_HOE'
        - 'IRON_PICKAXE'
        - 'IRON_AXE'
        - 'IRON_SPADE'
        - 'IRON_HOE'
        - 'GOLD_PICKAXE'
        - 'GOLD_AXE'
        - 'GOLD_SPADE'
        - 'GOLD_HOE'
        - 'STONE_PICKAXE'
        - 'STONE_AXE'
        - 'STONE_SPADE'
        - 'STONE_HOE'
        - 'WOOD_PICKAXE'
        - 'WOOD_AXE'
        - 'WOOD_SPADE'
        - 'WOOD_HOE'
  blocks:
    order: 4
    name: '&fBlocos'
    icon:
      slot: 28
      material: 'LOG'
      name: '&aBlocos'
      lore:
        - '&7A categoria de blocos permite a'
        - '&7venda de blocos e decorações.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: false
      nbts: []
      names: []
      types:
        - 'STONE'
        - 'DIRT'
        - 'GRASS'
        - 'GLASS'
        - 'SAND'
        - 'COBBLESTONE'
        - 'WOOD'
        - 'LOG'
        - 'WOOL'
        - 'NETHER_BRICKS'
        - 'SANDSTONE'
        - 'ENDER_STONE'
        - 'END_BRICKS'
        - 'OBSIDIAN'
        - 'LEAVES'
        - 'WOOD_STEP'
        - 'TRAP_DOOR'
        - 'STAINED_GLASS'
        - 'STAINED_GLASS_PANE'
        - 'STAINED_CLAY'
        - 'BOOKSHELF'
        - 'BRICKS'
        - 'STEP'
        - 'CHEST'
        - 'ENDER_CHEST'
        - 'SMOOTH_BRICK'
        - 'WORKBENCH'
        - 'FURNACE'
  books:
    order: 5
    name: '&fLivros'
    icon:
      slot: 29
      material: 'ENCHANTED_BOOK'
      name: '&aLivros'
      lore:
        - '&7A categoria de livros permite a'
        - '&7venda de livros de encantamentos.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: false
      nbts: []
      names: []
      types:
        - 'BOOK'
        - 'ENCHANTED_BOOK'
  spawners:
    order: 6
    name: '&fGeradores'
    icon:
      slot: 30
      material: 'MOB_SPAWNER'
      name: '&aGeradores'
      lore:
        - '&7A categoria de geradores permite a'
        - '&7venda de spawners de mobs.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: false
      nbts: [ 'ySpawnersV2-Item' ]
      names: []
      types: []
  machines:
    order: 7
    name: '&fMáquinas'
    icon:
      slot: 31
      material: 'EMERALD_BLOCK'
      name: '&aMáquinas'
      lore:
        - '&7A categoria de máquinas permite a'
        - '&7venda de geradores de minérios.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: false
      nbts:
        - 'yMaquinas-MaquinaItem'
        - 'yMaquinasVirtuais-Item'
      names: []
      types: []
  others:
    order: 8
    name: '&fOutros'
    icon:
      slot: 32
      material: 'CHEST'
      name: '&aOutros'
      lore:
        - '&7A categoria "outros" permite a'
        - '&7venda de itens em geral.'
        - ''
        - '&f* &7Esta categoria possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para abrir a categoria.'
    items:
      all: true
      nbts: []
      names: []
      types: []
]]>
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
  market: 'market|mercado'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __            _        _
#  _   _|  \/  | __ _ _ __| | _____| |_
# | | | | |\/| |/ _` | '__| |/ / _ \ __|
# | |_| | |  | | (_| | |  |   <  __/ |_
#  \__, |_|  |_|\__,_|_|  |_|\_\___|\__|
#  |___/
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

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Sistemas gerais do plugin
general:
  # Tempo padrão para começar a venda
  default-time: 1800
  # Quantia máxima de vendas simultâneas que o servidor pode ter
  # deixe 0 para ser infinito
  max-sells: 0
  # Quantia máxima de vendas simultâneas que o jogador pode fazer
  # deixe 0 para ser infinito
  player-max-sells: 1
  # Quantia máxima de vendas destacadas que o jogador pode fazer
  # deixe 0 para ser infinito
  player-max-sponsored: 1
  # Tempo mínimo para iniciar uma venda
  # em segundos
  min-time: 900
  # Tempo máximo para iniciar uma venda
  # em segundos
  max-time: 21600
  # Custos para destacar o anúncio
  sponsor-prices:
    price1:
      provider: 'money'
      amount: 100.0

# Sistema de blacklist
black-list:
  # Materiais que estarão na black-list
  materials: [ 'STONE', 'LOG:0' ]
  # NBTTags que estarão na black-list
  nbt-tags: []

# Sistema de npc
npc:
  skin: 'Pitombaa'
  hologram:
    offset: 3.4
    hologram:
      - '&6&lMERCADO'
      - '&7Faça o comércio rápido dos itens!'
      - '[item]EMERALD'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
version: '1.0.0'
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
    permission: 'ymarket.provider.money'
    # ‘Item’ que aparecerá no menu de seleção de economias
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ''
        - '&aClique para alterar'
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

# Ativar o sistema de atualizar o menu principal automaticamente enquanto estiver aberto
menu-updater: true
# Tempo para atualizar o menu automaticamente
# em ticks -> 20 ticks = 1s
menu-updater-time: 200

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
  name: '&8Mercado'
  size: 54
  sponsored-slots: [ 16, 25, 34 ]
  scroller:
    enabled: false
    slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
    previous-slot: 18
    next-slot: 26
  items:
    sponsored-slot: 12
    currencies-slot: 46
    personal-slot: 49
    own-slot: 52
    sponsored:
      material: 'NETHER_STAR'
      name: '&aDestaques!'
      lore:
        - '&7Aqui você pode encontrar os'
        - '&7melhores itens que estão anunciados'
        - '&7no nosso servidor.'
        - ''
        - '&f* &bAtualmente possuímos &f&n{amount}'
        - '&bitens(s) em destaque. :)'
        - ''
        - '&eClique para ver os anúncios.'
    personal:
      material: '{player}'
      name: '&aMercado Pessoal'
      lore:
        - '&7Aqui você pode encontrar os'
        - '&7itens que outros jogadores'
        - '&7anunciaram exclusivamente para você.'
        - ''
        - '&7Você possui &f&n{amount}'
        - '&7anúncio(s) exclusivo(s) no momento. :)'
        - ''
        - '&eClique para ver os anúncios.'
    own:
      material: 'b544a770e894a1fab11e2a2bac15fe3d96946fa52396b531978eb37ac64b8a90'
      name: '&eMeus Anúncios'
      lore:
        - '&7Veja aqui os itens colocados'
        - '&7a venda por você.'
        - ''
        - '&7Você possui &f&n{amount}'
        - '&7itens(s) no momento. :)'
        - ''
        - '&eClique para ver seus anúncios.'
    currencies-none:
      material: 'GOLD_INGOT'
      name: '&cValores'
      lore: [ '&7Você não tem nenhum valor para coletar!' ]
    currencies:
      material: 'GOLD_INGOT'
      name: '&eValores'
      lore:
        - '&r'
        - ' &eValores a receber:'
        - ' {format}'
        - ''
        - '&eClique para coletar os valores.'
  formats:
    currency: ' &7> &f{amount} {provider_abbreviated}'
  lore:
    - '&r'
    - ' &f* &bITEM EM DESTAQUE &f*'
    - ''
    - ' &fVendedor: &7{owner}'
    - ''
    - '&8> &fPreço: &a{amount} {provider_abbreviated}'
    - '&8> &fExpira em: &7{time}'
    - ''
    - '&eClique para adquirir este item.'
  facing:
    e1:
      slot: 16
      material: 'BARRIER'
      name: '&cSlot de Destaque'
    e2:
      slot: 25
      material: 'BARRIER'
      name: '&cSlot de Destaque'
    e3:
      slot: 34
      material: 'BARRIER'
      name: '&cSlot de Destaque'

# Menu de criação
create:
  name: '&8Mercado'
  size: 45
  back-slot: 0
  items:
    item-slot: 13
    confirm-slot: 28
    provider-slot: 30
    price-slot: 31
    duration-slot: 33
    target-slot: 34
    item:
      material: 'BARRIER'
      name: '&eClique em algum item do seu inventário'
      lore:
        - '&7Selecione algum item para leiloar.'
    confirm:
      material: 'STAINED_CLAY:5'
      name: '&aIniciar'
      lore:
        - '&7Esse item será anunciado para'
        - '&7outros jogadores comprarem.'
        - ''
        - '&8> &fItem: &7{item}'
        - '&8> &fDuração: &6{time}'
        - '&8> &fPreço: &6{amount} {provider_abbreviated}'
        - ''
    confirm-cant:
      material: 'STAINED_CLAY:14'
      name: '&cIniciar'
      lore:
        - '&7Selecione um item do seu inventário'
        - '&7para iniciar este anúncio.'
    provider:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aMoeda'
      lore:
        - '&7Moeda que será utilizada no anúncio'
        - '&7deste item.'
        - ''
        - '&7Atual: &fNenhuma'
        - ''
        - '&aClique para alterar a moeda'
    price:
      material: 'GOLD_INGOT'
      name: '&6Preço'
      lore:
        - '&7Defina o valor que o jogador'
        - '&7terá que pagar pelo seu item.'
        - ''
        - '&7Preço: &f{amount} {provider_abbreviated}'
        - ''
        - '&eClique para modificar.'
    duration:
      material: 'WATCH'
      name: '&aDuração customizada'
      lore:
        - '&7Defina um tempo específico'
        - '&7para a duração do seu anúncio.'
        - ''
        - '&fDuração: &6{time}'
        - ''
        - '&eClique para modificar.'
    target:
      material: '{player}'
      name: '&aPessoa alvo'
      lore:
        - '&7Defina quem poderá comprar'
        - '&7este seu anúncio.'
        - ''
        - '&fAlvo: &6{target}'
        - ''
        - '&eBotão &fESQUERDO&e para alterar.'
        - '&eBotão &fDIREITO&e para resetar.'

# Menu de gerenciamento
edit:
  name: '&8Mercado'
  size: 45
  back-slot: 0
  items:
    item-slot: 13
    expire-slot: 28
    provider-slot: 30
    price-slot: 31
    sponsor-slot: 33
    target-slot: 34
    expire:
      material: 'STAINED_CLAY:14'
      name: '&aExpirar'
      lore:
        - '&7Esse anúncio será cancelado'
        - '&7e o item ficará disponível para coleta.'
        - ''
        - '&8> &fItem: &7{item}'
        - '&8> &fDuração: &6{time}'
        - '&8> &fPreço: &6{amount} {provider_abbreviated}'
        - ''
        - '&eClique para cancelar o anúncio.'
    provider:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aMoeda'
      lore:
        - '&7Moeda que será utilizada no anúncio'
        - '&7deste item.'
        - ''
        - '&7Atual: &fNenhuma'
        - ''
        - '&aClique para alterar a moeda'
    price:
      material: 'GOLD_INGOT'
      name: '&6Preço'
      lore:
        - '&7Defina o valor que o jogador'
        - '&7terá que pagar pelo seu item.'
        - ''
        - '&7Preço: &f{amount} {provider_abbreviated}'
        - ''
        - '&eClique para modificar.'
    target:
      material: '{player}'
      name: '&aPessoa alvo'
      lore:
        - '&7Defina quem poderá comprar'
        - '&7este seu anúncio.'
        - ''
        - '&fAlvo: &6{target}'
        - ''
        - '&eBotão &fESQUERDO&e para alterar.'
        - '&eBotão &fDIREITO&e para resetar.'
    sponsor-perm:
      material: 'NETHER_STAR'
      name: '&aDestacar'
      lore:
        - '&7Deixe esse anúncio destacado nas'
        - '&7páginas de venda e em uma'
        - '&7categoria exclusiva.'
        - ''
        - ' &f* &aVocê é VIP e pode destacar seus'
        - ' &a  anúncios gratuitamente.'
        - ''
        - '&eClique para destacar.'
    sponsor-already:
      material: 'NETHER_STAR'
      name: '&aDestacar'
      lore:
        - '&7Deixe esse anúncio destacado nas'
        - '&7páginas de venda e em uma'
        - '&7categoria exclusiva.'
        - ''
        - '&aEste item já está destacado.'
    sponsor:
      material: 'NETHER_STAR'
      name: '&aDestacar'
      lore:
        - '&7Deixe esse anúncio destacado nas'
        - '&7páginas de venda e em uma'
        - '&7categoria exclusiva.'
        - ''
        - ' &f* Preço: &2$ &a{money} coins&f.'
        - ''
        - '&eClique para destacar.'

# Menu de seleção de economias
providers:
  name: '&8Selecionar economia'
  size: 27
  previous: 9
  next: 17
  back: 18
  slots: [ 11, 12, 13, 14, 15 ]

# Menu de seleção de duração
durations:
  name: '&8Selecionar duração'
  size: 36
  previous: 9
  next: 17
  back: 27
  slots: [ 11, 12, 13, 14, 15 ]
  items:
    select-slot: 31
    select:
      material: 'WATCH'
      name: '&aDuração customizada'
      lore:
        - '&7Defina um tempo específico'
        - '&7para a duração do seu leilão.'
        - ''
        - '&eClique para definir.'
    15min:
      material: 'PAPER'
      name: '&a15m'
      nbt-tag: [ 'yMarket-Duration=>900' ]
    30min:
      material: 'PAPER'
      name: '&a30m'
      nbt-tag: [ 'yMarket-Duration=>1800' ]
    1hour:
      material: 'PAPER'
      name: '&a1h'
      nbt-tag: [ 'yMarket-Duration=>3600' ]
    2hour:
      material: 'PAPER'
      name: '&a2h'
      nbt-tag: [ 'yMarket-Duration=>7200' ]
    3hour:
      material: 'PAPER'
      name: '&a3h'
      nbt-tag: [ 'yMarket-Duration=>10800' ]
    4hour:
      material: 'PAPER'
      name: '&a4h'
      nbt-tag: [ 'yMarket-Duration=>14400' ]
    5hour:
      material: 'PAPER'
      name: '&a5h'
      nbt-tag: [ 'yMarket-Duration=>18000' ]
    6hour:
      material: 'PAPER'
      name: '&a6h'
      nbt-tag: [ 'yMarket-Duration=>21600' ]

# Menu de vendas
my-sells:
  name: '&8Mercado'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  previous-slot: 9
  next-slot: 17
  back-slot: 27
  #
  empty-slot: 13
  create-slot: 31
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVazio...'
      lore: [ '&7Você não tem nenhum anúncio ativo!' ]
    create:
      material: '2ddcfe7d91cd80b364cc060160a0699386d096e0e5adf98e8e45e0a198631d8f'
      name: '&aVender um Item'
      lore: [ '&7Faça um anúncio do seu item para', '&7ver quem gostaria de adquirí-lo.', '', '&aClique para iniciar.' ]
  lore:
    - '&f'
    - '&8> &fPreço: &a{amount} {provider_abbreviated}'
    - '&8> &fVender para: &b{target}'
    - ''
    - '&8> &fExpira em: &7{time}'
    - ''
    - '&eClique para gerenciar o anúncio.'
  lore-expired:
    - '&f'
    - '&8> &fPreço: &a{amount} {provider_abbreviated}'
    - ''
    - '&8* Expirado *'
    - ''
    - '&eClique para coletar o item'
    - '&epara o seu inventário.'

# Menu de vendas
sells:
  name: '&8Mercado'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  #
  empty-slot: 22
  filter-slot: 50
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVazio...'
      lore: [ '&7Não há nenhum anúncio ocorrendo!' ]
    filter:
      material: HOPPER
      name: '&aFiltro'
  lore:
    - '&r'
    - ' &fVendedor: &7{owner}'
    - ''
    - '&8> &fPreço: &a{amount} {provider_abbreviated}'
    - '&8> &fExpira em: &7{time}'
    - ''
    - '&eClique para adquirir este item.'
  filter:
    types:
      oldest: 'Menor tempo restante'
      newest: 'Maior tempo restante'
    format:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de confirmação
confirm:
  name: '&8Mercado'
  size: 27
  items:
    item-slot: 13
    confirm-slot: 11
    cancel-slot: 15
    confirm:
      material: 'WOOL:5'
      name: '&aCONFIRMAR'
      lore:
        - '&7Você está prestes a adquirir'
        - '&7um item no nosso mercado.'
        - ''
        - '&aClique para CONFIRMAR a compra.'
    cancel:
      material: 'WOOL:14'
      name: '&cCANCELAR'
      lore:
        - '&7Você está prestes a desistir de'
        - '&7comprar um item no nosso mercado.'
        - ''
        - '&cClique para DESISTIR da compra.'
  lore:
    - '&r'
    - ' &fVendedor: &7{owner}'
    - ''
    - '&8> &fPreço: &a{amount} {provider_abbreviated}'
    - '&8> &fExpira em: &7{time}'
    - ''
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
# Mensagens a serem enviadas pelo plugin.

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/mercado &8- &7Abre o menu principal.
    &a/mercado vender [player] &8- &7Inicia uma venda no mercado.
    &a/mercado pessoal &8- &7Abre o menu de vendas pessoais.
    &a/mercado vendas &8- &7Abre o menu de vendas próprias.
    &a/mercado ban &8- &7Banir um jogador do mercado.
    &a/mercado unban &8- &7Desbanir um jogador do mercado.
    &a/mercado setnpc &8- &7Setar o NPC.
    &a/mercado delnpc &8- &7Deletar o NPC.
    &a/mercado reload &8- &7Recarregar as configurações.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  provider-permission: '&cVocê não tem permissão para leiloar com esta economia.'
  price: '&aPreço alterado para &f{amount}&a.'
  price-digit: |

    &aDigite o preço que você quer anunciar o item.
    &7para cancelar digite &ncancelar&7.

  time-digit: |

    &aDigite o tempo que você deseja.
    &7para cancelar digite &ncancelar&7.

  target-digit: |

    &aDigite o jogador alvo que você deseja.
    &7para cancelar digite &ncancelar&7.

  market-cancelled: |

    &cOPS! Um leilão no qual você participava foi cancelado pelo leiloador, o seu lance foi devolvido.

  market-bought: |

    &aOPA! Você adquiriu um novo item no mercado!

  market-bought-owner: |

    &aOPA! O jogador &f{player}&a adquiriu um item seu no mercado :)

  market-new: |

    &6&l[MERCADO]&e O jogador &f{player}&e adicionou um novo item no mercado.

  market-new-personal: |

    &6&l[MERCADO]&e O jogador &f{player}&e adicionou um novo item no seu mercado pessoal.

  market-expired: |

    &6&l[MERCADO]&e Um item seu que estava a venda expirou.

  max-sells: '&cO mercado já está com seu limite máximo simultâneo ({max}).'
  player-max-sells: '&cVocê já está com seu limite máximo simultâneo ({max}).'
  player-max-sponsoreds: '&cVocê já está com seu limite máximo simultâneo ({max}).'
  start-market: '&aVocê iniciou um novo anúncio no mercado.'
  cancel-market: '&aVocê cancelou o anúncio no mercado.'
  no-balance: '&cVocê não tem {amount} {provider_abbreviated} suficiente para isto. Disponível: {provider_balance}&c.'
  inv-full: '&cO seu inventário está cheio.'
  courier-collected-item: '&aVocê coletou um item do seu correio do mercado.'
  courier-collected-currencies: '&aVocê coletou os valores a receber.'
  cant-market: '&cEste item não pode ser anunciado.'
  currency-found: '&cConfigure a moeda do anúncio.'
  time-found: '&cVocê precisa definir um tempo entre {min} e {max} para iniciar um anúncio.'
  npc-set: '&aNPC setado com sucesso.'
  npc-deleted: '&aNPC removido com sucesso.'
  npc-not-set: '&cNPC não está definido.'
  market-collected: '&aVocê coletou um item do seu mercado para o inventário.'
  target-changed: '&aJogador alvo alterado para &f{target}&a.'
  market-expired-already: '&cEste item já expirou.'
  market-already: '&cEste item já foi vendido.'
  market-sponsored: '&aVocê colocou seu item em destaque no mercado.'
  market-sponsored-already: '&cEste item já está destacado.'
  banned: '&aJogador &f{player}&a banido do mercado com sucesso.'
  ban-already: '&cO jogador &f{player}&c já está banido do mercado.'
  unbanned: '&aJogador &f{player}&a desbanido do mercado com sucesso.'
  not-banned: '&cO jogador &f{player}&c não está banido do mercado.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/156-yMarket">Site do plugin yMarket</a>
    </category>
</seealso>