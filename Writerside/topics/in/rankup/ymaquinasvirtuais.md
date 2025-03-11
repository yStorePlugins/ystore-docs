# yMaquinasVirtuais
<secondary-label ref="rankup"/>

### Descrição
Crie robôs que irão gerar diversas economias/itens

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
<video src="//www.youtube.com/watch?v=EulF5gQvV9E"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/maquinas - Abre o menu principal
/maquinas top - Abre o menu de top
/maquinas shop - Abre o menu de loja de máquinas
/maquinas amigos - Abre o menu de máquinas de amigos
/maquinas help - Envia a mensagem de ajuda
/maquinas givemaquina - Dá máquinas para um jogador
/maquinas giveslot - Dá slots para um jogador
/maquinas reload - Recarrega as configurações
/limite - Mostra o seu limite
/limite [player] - Mostra o limite de outro jogador
/limite help - Envia a mensagem de ajuda
/limite top - Abre o menu do top limite
/limite enviar - Envia limite para outro jogador
/limite give - Dá limite em item para um jogador
/limite remove - Remove limite de um jogador
/limite add - Adiciona limite para um jogador
/limite set - Seta o limite de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymaquinasvirtuais.admin - Permissão para ser reconhecido como admin
ymaquinasvirtuais.use - Permissão para o /maquinas
ymaquinasvirtuais.top - Permissão para o /maquinas top
ymaquinasvirtuais.shop - Permissão para o /maquinas shop
ymaquinasvirtuais.friends - Permissão para o /maquinas amigos
ymaquinasvirtuais.multiplicador.[quantia] - Permissão para ter uma x quantia de multiplicador
ymaquinasvirtuais.give - Permissão para o /maquina givemaquina
ymaquinasvirtuais.giveslot - Permissão para o /maquina giveslot
ymaquinasvirtuais.admin.reload - Permissão para o /maquina reload
ymaquinasvirtuais.limit.use - Permissão para o /limite
ymaquinasvirtuais.limit.others - Permissão para o /limite [player]
ymaquinasvirtuais.limit.send - Permissão para o /limite enviar
ymaquinasvirtuais.limit.set - Permissão para o /limite set
ymaquinasvirtuais.limit.add - Permissão para o /limite add
ymaquinasvirtuais.limit.remove - Permissão para o /limite remove
ymaquinasvirtuais.limit.give - Permissão para o /limite give
ymaquinasvirtuais.limit.remove - Permissão para o /limite remove</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ymaquinasvirtuais_limit% - Retorna o limite do jogador formatado (1K, 1M, 1T...)
%ymaquinasvirtuais_limit_raw% - Retorna o limite do jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMaquinasVirtuais/
    ├── machines/
    │    └── tokens.yml
    ├── shop/
    │    └── machines.yml
    ├── bonus.yml
    ├── commands.yml
    ├── config.yml
    ├── discounts.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="machines" collapsible="true">
<chapter title="tokens.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome que irá aparecer nas mensagens
name: '&aMáquina de Tokens'

# Permissão para poder ativar a máquina
permission: ''

# Gerar apenas com o dono ou amigo online
generate-online: false

# Item que poderá ser ativado
item:
  material: 'INK_SACK:10'
  name: '&aMáquina de Tokens &fL.{level}'
  lore:
    - ''
    - '&f Tipo: &7Tokens&f.'
    - '&f Stack: &7{stack}'
    - ''
    - '&f Upgrades:'
    - '&f  > Drops gerados por rodada: &b{drops_round}'
    - '&f  > Velocidade de geração: &b{speed}s'
    - ''

# Mensagens
messages:
  sell: '&aVocê vendeu &7{amount}x {drop}&a por &6{yeconomias-tokens} tokens &8{bonus}&a.'

menu:
  icon:
    material: 'INK_SACK:10'
    name: '&aMáquina de Tokens &fL.{level}'
    lore:
      - '&7Esta maquina gera &aTokens&7.'
      - ''
      - '&f Stack: &7{stack}'
      - '&f Tokens gerados: &a{to_sell}'
      - ''
      - '&f Upgrades:'
      - '&f  > Drops gerados por rodada: &b{drops_round}'
      - '&f  > Velocidade de geração: &b{speed}s'
      - ''
      - '&aClique para gerenciar.'
  icon-friend:
    material: 'INK_SACK:10'
    name: '&aMáquina de Tokens &fL.{level}'
    lore:
      - '&7Esta maquina gera &aTokens&7.'
      - ''
      - '&f* Máquina de: &a{player}'
      - ''
      - '&f Stack: &7{stack}'
      - '&f Tokens gerados: &a{to_sell}'
      - ''
      - '&f Upgrades:'
      - '&f  > Drops gerados por rodada: &b{drops_round}'
      - '&f  > Velocidade de geração: &b{speed}s'
      - ''
      - '&aClique para gerenciar.'
  level:
    material: '365fc0426230a2e88df29d2d8ec4512e6dbdbc0777b4b83cdda2ede81864d6'
    name: '&aEvoluir Nível'
    lore:
      - '&7Evolua o nível da sua máquina'
      - '&7para deixar ela mais eficiente.'
      - ''
      - '&f{current_level} -> &a{next_level}'
      - ''
      - '&7Custo: &e{money} coins.'
      - ''
      - '&aClique para evoluir.'

# Níveis da máquina
levels:
  # nível máximo
  level-max: 2
  level1:
    # ordem do nível
    # default = 1
    order: 1
    # Delay de geração
    # em segundos
    delay: 10
    # Drops gerados por round
    drops: 1
    # Preço para chegar neste nível
    prices:
      price1:
        provider: 'money'
        amount: 1000.0
  level2:
    order: 2
    delay: 5
    drops: 2
    prices:
      price1:
        provider: 'money'
        amount: 10000.0

# Upgrades da máquina
upgrades:
  # Permitir o upgrade apenas ao chegar no nível máximo
  level-max: true
  # Quantidade de drops gerados
  drops:
    prices-per-level:
      price1:
        provider: 'money'
        amount: 10.0
    max: 5
    default: 0
    add-per-level: 1
  # Velocidade de geração de mobs
  speed:
    prices-per-level:
      price1:
        provider: 'money'
        amount: 15.0
    max: 5
    default: 0
    add-per-level: 1

# Sistema de drops
drop:
  # Possibilitar recolher o drop no armazém
  collect: true
  # Possibilitar vender o drop no armazém
  sell: true

  # Botão que será realizada a venda (LEFT | RIGHT)
  sell-button: 'LEFT'
  # Botão que será realizado recolher (LEFT | RIGHT)
  collect-button: 'RIGHT'

  # Permissão para recolher drops (deixe vazio '' para não usar)
  collect-permission: 'ymaquinasvirtuais.iron.coletar'
  # Permissão para vender drops (deixe vazio '' para não usar)
  sell-permission: 'ymaquinasvirtuais.iron.vender'

  # Tipos de drop
  types:
    tokens:
      drop:
        material: 'INK_SACK:10'
      name: '&aTokens'
      # ícone que irá ficar no menu de drops
      icon:
        material: 'INK_SACK:10'
        name: '&aTokens'
        lore:
          - ''
          - ' &fDrops armazenados: &a{drops_stored}&f.'
          - ' &fValor por drop: &a1 tokens&f.'
          - ' &fValor total: &a{yeconomias-tokens} tokens&f.'
          - ' &fSeu bônus: &b{bonus_raw}%&f.' # bonus formatado: {bonus}
          - ''
          - '&aBotão &fESQUERDO&a para vender.'
          - '&aBotão &fDIREITO&a para recolher.'
      # Economias que o drop irá dar
      currencies:
        preco1:
          provider: 'yeconomias-tokens'
          amount: 1.0

  # O Drop vai executar um comando ao ser recolhido?
  command:
    enabled: false
    # Preço por drop (para o comando)
    price: 100.0
    # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
    use-amount: true
    # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
    multiply-price: true
    # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
    inv-bypass: true
    # coletar diretamente, sem precisar digitar a quantia no chat (apenas quando os comandos tiverem ativos)
    collect-chat-bypass: true
    # formatar a quantia que será executada no comando. Ex: 1k, 10k, 1M
    amount-format: true
    commands: [ 'give {player} iron_ingot {amount}' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="shop" collapsible="true">
<chapter title="machines.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
machines:
  1:
    # Item da máquina.
    item:
      material: 'INK_SACK:10'
      name: '&aMáquina de Tokens'
      lore:
        - ''
        - '&fPreço: &a{money} coins&f.'
        - ''
        - '&a&lFORMAS DE COMPRA'
        - ''
        - '&7&l• &fBotão direito: &7Comprar 1&f.'
        - '&7&l• &fBotão Q: &7Comprar limite&f.'
        - '&7&l• &fBotão esquerdo: &7Escolher quantia&f.'
        - ''
    # Tipo da maquina
    machine: 'tokens'
    # Nível da máquina
    level: 1
    # Data de liberação para comprar
    release-in: '16/10/2020-10:00'
    # Placeholder {rank} na lore da compra indisponível
    rank: '&7[Membro]'
    # Custos para comprar
    prices:
      price1:
        provider: 'money' #tipos: Money, plugin de pontos
        amount: 1000.0
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
bonus:
  membro:
    order: 1
    # Permissão para ser reconhecido
    permission: 'ymaquinasvirtuais.bonus.membro'
    # Nome que irá aparecer nas mensagens
    display: '&7[Membro]'
    # Quantia do bônus em %
    bonus: 10.0
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
  machine: 'machine|machines|maquina|maquinas'
  limit: 'limit|limite|limits|limites'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __                   _               __     ___      _               _
#  _   _|  \/  | __ _  __ _ _   _(_)_ __   __ _ __\ \   / (_)_ __| |_ _   _  __ _(_)___
# | | | | |\/| |/ _` |/ _` | | | | | '_ \ / _` / __\ \ / /| | '__| __| | | |/ _` | / __|
# | |_| | |  | | (_| | (_| | |_| | | | | | (_| \__ \\ V / | | |  | |_| |_| | (_| | \__ \
#  \__, |_|  |_|\__,_|\__, |\__,_|_|_| |_|\__,_|___/ \_/  |_|_|   \__|\__,_|\__,_|_|___/
#  |___/                 |_|
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

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Sistemas gerais
general:
  # Limite máximo de amigos que uma máquina pode ter
  # deixe 0 para ser infinito
  friend-max: 0
  # Acumular os bônus que tiver permissão
  accumulate-bonus: true
  # Sistema de bolsa de valores (yBolsa, StormEconomy ou HeroBolsa)
  bolsa: true
  # Formatador de bônus
  formatter-bonus-has: '&fBônus: &a{bonus}%&7 ({display}&7)'
  formatter-bonus-no-has: ''
  # Quantia máxima que pode ter de multiplicador
  multiplier-max: 10
  # Ativar a compra usando o limite disponível com o botão "Q"
  # Isto só funciona se o limite estiver ativado
  buy-q: true
  # Delay da compra com Q
  # em segundos
  buy-q-delay: 10
  # Ativar a compra via chat
  # caso desativado, comprará apenas 1 unidade (sem contar o multiplicador)
  buy-chat: true
  # Gastar limite ao comprar
  spend-limit: false
  # Delay da coleta
  # em segundos
  collect-delay: 10

# Limite de compra de máquinas na loja.
limit-shop:
  # Ativar o limite
  enabled: true
  # Quantia de limite que o jogador ganhar ao se registrar.
  default: 1
  # Máximo de limite que o jogador pode ter.
  # Deixe 0 para ser infinito.
  max: 100
  # Item do limite que será ativável
  item:
    material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    name: '&bLimite de compra'
    lore:
      - ''
      - '&fQuantia: &a{amount}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
      - ''

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
]]>
</code-block>
</chapter>

<chapter title="discounts.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
discounts:
  member:
    order: 1
    permission: 'ymaquinasvirtuais.member'
    display: '&7[Membro]'
    discount: 10.0 # em % do valor total
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
    permission: 'ymaquinasvirtuais.provider.money'
  yeconomias-tokens:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yeconomias-tokens'
    # Formato inteiro
    display: 'Tokens'
    # Formato abreviado
    abbreviated: 'tokens'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'ymaquinasvirtuais.provider.yeconomias-tokens'
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

# Menu de gerenciar membros
main:
  name: '&8Máquinas'
  size: 45
  slots: [ 10, 11, 12, 13, 14, 15, 16, 20, 21, 22, 23, 24, 25 ]
  previous-slot: 36
  next-slot: 44
  #
  sell-all-slot: 39
  profile-slot: 40
  top-slot: 41
  shop-slot: 37
  friends-machines-slot: 43
  #
  items:
    profile:
      material: '{player}'
      name: '&eSuas informações'
      lore: [ '', ' &fSlots: &c{slots_current}&7/&a{slots_total}', '', ' &fMáquinas funcionando: &a{machines}&f.', ' &fDrops a vender: &7{to_sell}&f.', '' ]
    sell-all:
      material: 'CAULDRON_ITEM'
      name: '&eVender Tudo!'
      lore: [ '&7Venda os drops da sua', '&7máquina de uma só vez.', '', ' &fDrops a vender: &7{to_sell}', '', '&aClique para vender.' ]
    sell-all-permission:
      material: 'CAULDRON_ITEM'
      name: '&cVender Tudo!'
      lore: [ '&7Venda os drops da sua', '&7máquina de uma só vez.', ' &fDrops a vender: &7{to_sell}', '', '&cVocê não tem permissão' ]
    top:
      material: 'SIGN'
      name: '&eTOP'
      lore: [ '&7Clique para ver os', '&7jogadores que possuem', '&7mais máquinas.' ]
    shop:
      material: 'EMERALD'
      name: '&eShop!'
      lore: [ '&7Clique para comprar', '&7mais máquinas.' ]
    friends-machines:
      material: 'GOLD_INGOT'
      name: '&eMáquinas de Amigos!'
      lore: [ '&7Clique para gerenciar as', '&7máquinas dos seus amigos.' ]
  facing:
    e0:
      slot: 10
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e1:
      slot: 11
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e2:
      slot: 12
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e3:
      slot: 13
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e4:
      slot: 14
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e5:
      slot: 15
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e6:
      slot: 16
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e7:
      slot: 19
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e8:
      slot: 20
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e9:
      slot: 21
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e10:
      slot: 22
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e11:
      slot: 23
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e12:
      slot: 24
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e13:
      slot: 25
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []

# Menu de máquinas de amigos
friends-machines:
  name: '&8Máquinas - Amigos'
  size: 45
  slots: [ 10, 11, 12, 13, 14, 15, 16, 20, 21, 22, 23, 24, 25 ]
  previous-slot: 36
  next-slot: 44
  #
  back-slot: 39
  sell-all-slot: 40
  #
  items:
    sell-all:
      material: 'CAULDRON_ITEM'
      name: '&eVender Tudo!'
      lore: [ '&7Venda os drops da sua', '&7máquina de uma só vez.', '', ' &fDrops a vender: &7{to_sell}', '', '&aClique para vender.' ]
    sell-all-permission:
      material: 'CAULDRON_ITEM'
      name: '&cVender Tudo!'
      lore: [ '&7Venda os drops da sua', '&7máquina de uma só vez.', ' &fDrops a vender: &7{to_sell}', '', '&cVocê não tem permissão' ]
  facing:
    e0:
      slot: 10
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e1:
      slot: 11
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e2:
      slot: 12
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e3:
      slot: 13
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e4:
      slot: 14
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e5:
      slot: 15
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e6:
      slot: 16
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e7:
      slot: 19
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e8:
      slot: 20
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e9:
      slot: 21
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e10:
      slot: 22
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e11:
      slot: 23
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e12:
      slot: 24
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []
    e13:
      slot: 25
      material: 'STAINED_GLASS_PANE:14'
      name: ' '
      lore: []

# Menu da máquina
machine:
  name: '&8Máquina'
  size: 27
  back-slot: 0
  items:
    info-slot: 10
    drops-slot: 11
    friends-slot: 13
    upgrades-slot: 15
    level-slot: 16
    remove-slot: 12
    # ícones do menu upgrades direto no principal
    upgrades-drops-slot: -1
    upgrades-speed-slot: -1
    #
    info:
      material: '{machine}'
      name: '&a{machine} &fL.{level}'
      lore:
        - ''
        - ' &fDono: &7{owner}&f.'
        - ' &fStack: &7{stack}&f.'
        - ' &fDrops armazenados: &a{to_sell}&f.'
        - ''
        - ' &f> Drops gerados por rodada: &b{drops_round}&f.'
        - ' &f> Velocidade de geração: &b{speed}s&f.'
        - ''
    drops:
      material: '12ef39437d7d43a034c5a40b974e8d2c6734a218c76485d04910f507bdc2e809'
      name: '&aDrops'
      lore:
        - '&7Gerencie os drops que estão'
        - '&7armazenados nesta máquina.'
        - ''
        - ' &fDrops armazenados: &a{to_sell}&f.'
        - ''
        - '&aClique para gerenciar.'
    upgrades:
      material: '365fc0426230a2e88df29d2d8ec4512e6dbdbc0777b4b83cdda2ede81864d6'
      name: '&aUpgrades'
      lore:
        - '&7Sua máquina necessita de'
        - '&7melhorias para ficar mais'
        - '&7eficiente.'
        - ''
        - '&aClique para acessar.'
    level-cant:
      material: 'BARRIER'
      name: '&cEvoluir Nível'
      lore:
        - '&cA máquina já está no nível máximo.'
    friends:
      material: '1cba7277fc895bf3b673694159864b83351a4d14717e476ebda1c3bf38fcf37'
      name: '&aAmigos'
      lore:
        - '&7Acesse as preferências de'
        - '&7amizade desta máquina.'
        - ''
        - '&aClique para acessar.'
    remove:
      material: BARRIER
      name: '&cRemover'
      lore:
        - '&7Remova máquinas deste stack de'
        - '&7máquinas.'
        - ''
        - '&aBotão &fESQUERDO&a para remover TODOS.'
        - '&aBotão &fDIREITO&a para escolher a quantia.'

# Menu de top
top:
  name: '&8TOP MÁQUINAS'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 31
  previous-slot: 9
  next-slot: 17
  items:
    # Item do top máquinas
    machines:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fMáquinas funcionando: &7{amount}'
        - '&fPosição: &e{pos}º'
        - ''

# Menu upgrades
upgrades:
  name: '&8Máquina'
  size: 27
  back-slot: 18
  items:
    drops-slot: 12
    speed-slot: 14
    drops:
      material: EYE_OF_ENDER
      name: '&aUpgrade de Drops'
      lore:
        - '&7Esta evolução faz com que a'
        - '&7máquina produza mais drops'
        - '&7por rodada.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fDrops obtidos por mob: &7{drops_actual}/{drops_max}&f.'
        - ' &fCusto para próx nível: &7{money} coins&f.'
        - ''
        - '&aClique para evoluir.'
    drops-max:
      material: EYE_OF_ENDER
      name: '&aUpgrade de Drops'
      lore:
        - '&7Esta evolução faz com que a'
        - '&7máquina produza mais drops'
        - '&7por rodada.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fDrops obtidos por mob: &7{drops_actual}/{drops_max}&f.'
        - ''
        - '&cVocê já está no máximo.'
    speed:
      material: EXP_BOTTLE
      name: '&aUpgrade de Velocidade'
      lore:
        - '&7Esta evolução faz com que o'
        - '&7tempo de geração da máquina'
        - '&7seja reduzido.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fTempo: &7{speed_actual}s/{speed_max}s&f.'
        - ' &fCusto para próx nível: &7{money} coins&f.'
        - ''
        - '&aClique para evoluir.'
    speed-max:
      material: EXP_BOTTLE
      name: '&aUpgrade de Velocidade'
      lore:
        - '&7Esta evolução faz com que o'
        - '&7tempo de geração da máquina'
        - '&7seja reduzido.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fTempo: &7{speed_actual}s/{speed_max}s&f.'
        - ''
        - '&cVocê já está no máximo.'

# Menu de drops
drops:
  name: '&8Máquina'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu de amigos
friends:
  name: '&8Máquina'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
  previous-slot: 9
  next-slot: 17
  back-slot: 18
  items:
    add-slot: 27
    add:
      material: '8e9b27fccd80921bd263c91dc511d09e9a746555e6c9cad52e8562ed0182a2f'
      name: '&aAdicionar amigo'
      lore:
        - '&7Clique aqui para adicionar'
        - '&7amigos para poder usar'
        - '&7esta máquina.'
    friend:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&aBotão &fDIREITO&a para deletar.'
        - ''

shop:
  name: '&8Loja de máquinas'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 47
  next-slot: 53
  back-slot: 45
  # Itens da loja
  items:
    info-slot: 49
    multiplier-slot: 50
    info:
      material: '1cba7277fc895bf3b673694159864b83351a4d14717e476ebda1c3bf38fcf37'
      name: '&aInformações gerais'
      lore:
        - '&7Máquinas são uma das partes mais'
        - '&7importantes do servidor! Com'
        - '&7elas, é possível receber muuuitos'
        - '&7coins!'
        - ''
        - '&fDesconto: &7{discount}% ( {group} &7)&f.'
        - '&fLimite de compra: &7{limit}&f.'
    multiplier:
      material: 'b73e87235a2f691cf14bb0d414fda2563f040865c74273bf2c8bc095fecb228'
      name: '&aMultiplicador de compra'
      lore:
        - '&7Quanto mais limite de compra,'
        - '&7mais máquinas é possível comprar'
        - '&7por vez, porém, há mais um jeito'
        - '&7de comprar máquinas mais rápido,'
        - '&7que é o multiplicador de compra!'
        - '&7Ele fornece mais máquinas a'
        - '&7cada compra feita.'
        - ''
        - ' &fMultiplicador ativo: &7{active}&f.'
        - ' &fMultiplicador máximo: &7{max}&f.'
        - ''
        - '&aClique para alterar seu multiplicador.'
    # Configurações gerais dos itens
    # Quando a máquina não foi liberado na data ainda.
    wait:
      material: BARRIER
      name: '{machine}'
      lore:
        - ''
        - '&cVocê não pode comprar esta máquina.'
        - '&7Ela será liberado em: &f{date} - &f{hour}'
        - '&7Tempo para liberar: &f{time_formatted}'
        - ''
    # Quando o jogador não tiver permissão de comprar aquela máquina.
    permission:
      material: BARRIER
      name: '{machine}'
      lore:
        - ''
        - '&cVocê não pode comprar esta máquina.'
        - '&7Você não possui permissão.'
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

    &aMáquinas comandos:

    &a> /maquinas
    &a> /maquinas top
    &a> /maquinas shop
    &a> /maquinas amigos
    &a> /maquinas givemaquina <player> <maquina> <level> <quantia>
    &a> /maquinas giveslot <player> <quantia>

  help-limit: |
    &bComandos disponíveis:
    &b > &3/limite &8- &fMostra o seu limite
    &b > &3/limite <player> &8- &fMostra o limite de outro jogador
    &b > &3/limite help &8- &fEnvia essa mensagem
    &b > &3/limite give <player> <quantia> &8- &fDá limite em item para um jogador
    &b > &3/limite remove <player> <quantia> &8- &fRemove limite de um jogador
    &b > &3/limite add <player> <quantia> &8- &fAdiciona limite para um jogador
    &b > &3/limite set <player> <quantia> &8- &fSeta o limite de um jogador
  machine-give: '&aVocê deu &7{amount}x {machine}&a para o jogador &7{player}&a.'
  machine-received: '&aVocê recebeu &7{amount}x {machine}&a.'
  machine-list: |
    &cMáquina não encontrada.
    &cMáquinas disponíveis: &f{list}
  level-list: |
    &cLevel não encontrado.
    &cLéveis disponíveis: &f{list}
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  digit-remove: |

    &aDigite a quantia de máquinas que deseja remover.
    &7para cancelar digite &ncancelar&7.

  digit-add: |

    &aDigite no chat o nome do seu amigo que quer adicionar.'
    &7para cancelar digite &ncancelar&7.'

  collect-need: '&cEste stack possui apenas {stack} máquinas.'
  max-friend: '&cEsta máquina atingiu o limite máximo de amigos.'
  added: '&aVocê adicionou o jogador &7{player}&a na sua máquina.'
  already-added: '&cEste jogador já está adicionado.'
  add-owner: '&cVocê não pode adicionar o dono como amigo na máquina.'
  upgraded: '&aVocê adquiriu &f+1 nível&a do upgrade por &f{money} coins&a.'
  evolved: '&aVocê evoluiu &f+1 nível&a da sua máquina por &f{money} coins&a.'
  digit-collect: |

    &aDigite a quantia que você quer coletar.

    &8| &fVocê possui &6{amount}&f disponível.
    &8| &fDigite &8TUDO &fpara coletar tudo.

    &7Para cancelar digite &ncancelar&7.

  digit-multiplier: |

    &8| &aDigite no chat a quantia de multiplicador que deseja.

    &f> &7Atual: &b{active}&7.
    &f> &7Máximo: &b{max}&7.

  digit-machines: |

    &aDigite a quantia de máquinas que deseja.
    &7para cancelar digite &ncancelar&7.

  collect: '&aVocê coletou &7{amount}x {drop} (&8{bonus})&a.'
  inv-full: '&cSeu inventário está cheio.'
  insufficient: '&cEsta máquina não possui drops suficiente.'
  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  perm-this-machine: '&cVocê não tem permissão para nesta máquina.'
  need-level-max: '&cA máquina precisa estar no nível máximo.'
  just-owner: '&cApenas o dono da máquina pode fazer isto.'
  not-enough-slot: '&cVocê não possui slot disponíveis.'
  sell-all: '&aVocê vendeu &fx{amount} drops&a.'
  delay: '&cAguarde &e{time} &cpara adquirir novamente.'
  limit-insuficient: '&cVocê não possui limite suficiente. Disponível: &7{limit}&c.'
  bought: |
    &bObrigado por adquirir máquinas na loja de máquinas. Confira as informações da compra:

    &7&l| &fMáquina: &7{machine}&f.
    &7&l| &fQuantia: &7{amount}&f.

  multiplier-max: '&cVocê não pode definir mais que o seu máximo: &7{max}&c.'
  multiplier-defined: '&aVocê definiu seu multiplicador para &7{multiplier}&a.'
  limit: |
    &bQuantidade de limite que você possui: &f{limit}&b.
  limit-changed: '&aLimite do jogador &7{player}&a alterado para &7{amount}&a.'
  limit-give: '&aVocê deu &e{amount} &ade limite para o jogador &e{player}&a.'
  limit-no-balance: '&bVocê não possui &f{limit} limite&b.'
  limit-target-max: '&bO jogador já possui o máximo de limite permitido: &f{limit}&b.'
  limit-sent: '&bVocê enviou &f{limit} limite&b para o jogador &f{player}&b.'
  limit-received: '&bVocê recebeu &f{limit} limite&b do jogador &f{player}&b.'
  limit-target: |
    &bQuantidade de limite que &7{player}&b possui: &f{limit}&b.
  limit-converted: '&cVocê compactou todos seus limites em 1.'
  limit-activated: '&aVocê ativou &e{amount} &ade limites.'
  limit-max: '&cVocê já chegou no máximo.'
  slot-activated: '&aVocê ativou &e{amount} &ade slots.'
  slot-max: '&cVocê já chegou no máximo.'
  slot-give: '&aVocê deu &e{amount} &ade slots para o jogador &e{player}&a.'
  machine-activated: '&cMáquina ativada com sucesso.'
  machine-collected: '&a{amount}x {machine} &aremovida(s).'
  delay-collect: '&cAguarde &e{time} &cpara coletar novamente.'
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/125-yMaquinasVirtuais">Site do plugin yMaquinasVirtuais</a>
    </category>
</seealso>