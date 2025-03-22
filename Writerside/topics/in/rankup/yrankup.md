# yRankup
<secondary-label ref="rankup"/>

### Descrição
Agora é possível evoluir de rank com cabeças e outros meios de economias.

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
<video src="//www.youtube.com/watch?v=TOYnlP6w7WI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/rank - Abre o menu principal
/rankup - Abre o menu de rankup
/prestigio - Dá prestígio
/heads - Abre o menu de heads
/rank top- Abre o menu de top
/rank [player] - Vê as informações de um jogador
/rank giverankup - Dar item rankup para um jogador
/rank giveprestigio - Dar item prestígio para um jogador
/rank setrank - Seta um rank para um jogador
/rank setprestigio - Seta um prestígio para um jogador
/fragmentos - Vê a quantia de fragmentos
/fragmentos [player] - Vê a quantia de fragmentos de um jogador
/fragmentos enviar - Envia seus fragmentos para um jogador
/fragmentos add - Adiciona fragmentos para um jogador
/fragmentos give - Dá fragmentos em forma de itens para um jogador
/fragmentos set - Seta fragmentos para um jogador
/fragmentos remove - Remove fragmentos de um jogador
/heads add - Adiciona heads para um jogador
/heads give - Dá heads em forma de itens para um jogador
/heads set - Seta heads para um jogador
/heads remove - Remove heads de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yrankup.use - Permissão para o /rank
yrankup.giverankup - Permissão para o /rank giverankup
yrankup.giveprestige - Permissão para o /rank giveprestige
yrankup.setrank - Permissão para o /rank setrank
yrankup.setprestige - Permissão para o /rank setprestige
yrankup.admin.reload - Permissão para o /rank reload
yrankup.look - Permissão para o /rank [player]
yrankup.rankup - Permissão para o /rankup
yrankup.rankup.max - Permissão para o /rankup max
yrankup.ranks - Permissão para o /ranks
yrankup.heads - Permissão para o /heads
yrankup.prestige - Permissão para o /prestigio
yrankup.autorankup - Permissão para o /autorankup
yrankup.coin.use - Permissão para o /fragmentos
yrankup.coin.look - Permissão para o /fragmentos [player]
yrankup.coin.send - Permissão para o /fragmentos enviar
yrankup.coin.help - Permissão para o /fragmentos ajuda
yrankup.coin.add - Permissão para o /fragmentos add
yrankup.coin.remove - Permissão para o /fragmentos remove
yrankup.coin.set - Permissão para o /fragmentos set
yrankup.coin.give - Permissão para o /fragmentos give
yrankup.head.help - Permissão para o /heads ajuda
yrankup.head.add - Permissão para o /heads add
yrankup.head.remove - Permissão para o /heads remove
yrankup.head.set - Permissão para o /heads set
yrankup.head.give - Permissão para o /heads give</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yRankup/
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── fragments.yml
    ├── heads.yml
    ├── menus.yml
    ├── messages.yml
    ├── prestiges.yml
    └── ranks.yml
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
  rank: 'rank'
  ranks: 'ranks'
  rankup: 'rankup'
  coin: 'fragmento|fragmentos|fragment|fragments'
  prestige: 'prestige|prestigio'
  head: 'head|heads'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        ____             _
#  _   _|  _ \ __ _ _ __ | | ___   _ _ __
# | | | | |_) / _` | '_ \| |/ / | | | '_ \
# | |_| |  _ < (_| | | | |   <| |_| | |_) |
#  \__, |_| \_\__,_|_| |_|_|\_\\__,_| .__/
#  |___/                            |_|
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

# Bloquear ranks para staff
staff-block: false

# Esconder a tag para quem tem a permissão
# yrankup.hide
hide-enabled: false

# Comando de /rankup abrir menu
rankup-cmd-menu: true

# Desativar por completo o sistema de heads
heads-disabled: false

# Desativar por completo o sistema de coins
coin-disabled: false

# Sistema de Auto-Rankup
auto-rankup:
  enabled: true
  # Ativado por padrão
  enabled-default: false
  # Permissão para conseguir ativar o sistema
  permission: 'yrankup.autorankup'
  # Delay para checar o rankup
  # em segundos
  delay: 3

# Sistema de fragmentos
fragment:
  # Metadata do plugin de mob-stack para multiplicar os fragmentos
  # Deixe vazio '' para não usar
  metadata: 'ySpawners-MobStacked'
  # Ao matar com shift, dropar apenas a quantia de fragmentos configurados.
  shift-unit: true
  # Ao matar em pé, dropar apenas a quantia de fragmentos configurados.
  no-shift-unit: false
  # Mundos que não irá dropar fragmentos
  world-blacklist: []

# Sistema de heads
head:
  # Metadata do plugin de mob-stack para multiplicar as heads
  # Deixe vazio '' para não usar
  metadata: 'ySpawners-MobStacked'
  # Ao matar com shift, dropar apenas a quantia de heads configurados.
  shift-unit: true
  # Ao matar em pé, dropar apenas a quantia de heads configurados.
  no-shift-unit: false
  # Mundos que não irá dropar heads
  world-blacklist: []

items:
  # Item de coin ativável
  usable-item:
    material: '1ba16c3890af39c3f2d576586cff443de07dad32b2315e2ff6f0d5d6a3c663dd'
    name: '&b+{amount} Fragmentos'
    lore:
      - ''
      - '&fQuantia: &b{amount}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus fragmentos no inventário em 1 só.'
      - ''

  # Item para evoluir o prestígio
  prestige-item:
    material: '885620b88e0de9b34f76027c7f9c1def5e1de5ae542c6920b5f28693a54'
    name: '&aPrestigio'
    lore:
      - '&fEste item equivale à &7+1 &fnível de prestígio.'
      - ''
      - '&7Clique com botão direito para ativar.'

  # Item para evoluir o rank
  rankup-item:
    material: '1ad6c81f899a785ecf26be1dc48eae2bcfe777a862390f5785e95bd83bd14d'
    URL: 'http://textures.minecraft.net/texture/1ad6c81f899a785ecf26be1dc48eae2bcfe777a862390f5785e95bd83bd14d'
    name: '&aRankup'
    lore:
      - '&7Este item equivale à &f+1 &7nível de rankup.'
      - ''
      - '&7Clique com botão direito para ativar.'

# Sistema de descontos
discounts:
  vip:
    order: 1
    permission: 'yrankup.vip'
    discount: 10.0

# Sistema de bônus
bonus:
  vip:
    order: 1
    permission: 'yrankup.vip'
    bonus: 10.0

# Sistema de formatos
formats:
  # Quando estiver com o progresso 100%
  progress-bar-full: '&a/rankup &7({progressbar}&7)'
  percentage-full: '{percentage}'
  # Quando não tiver próximo rank disponível
  progress-bar-none: ''
  percentage-none: ''
  tag-none: '&cÚltimo'
  name-none: '&cÚltimo'
  # Quando não tiver rank disponível
  actual-tag-none: '&cÚltimo'
  actual-name-none: '&cÚltimo'
  # Quando o jogador for um staff e estiverem bloqueados os ranks para staff
  staff-tag: ''
  staff-name: ''
  staff-progressbar: ''
  staff-percentage: ''

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'
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
    permission: 'yrankup.provider.money'
  yrankup-head-pig:
    provider: 'yrankup-head-pig'
    display: 'Cabeça de Porco'
    abbreviated: 'Porco'
    allow-offline: true
    permission: 'yrankup.provider.head-pig'
  yrankup:
    provider: 'yrankup'
    display: 'Fragmentos'
    abbreviated: 'Frags'
    allow-offline: true
    permission: 'yrankup.provider.fragmentos'
]]>
</code-block>
</chapter>

<chapter title="fragments.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
blocks:
  stone:
    material: 'STONE:0'
    chance: 100.0
    amount: 10.0

entities:
  pig:
    entity: 'PIG'
    chance: 100.0
    amount: 10.0
]]>
</code-block>
</chapter>

<chapter title="heads.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
heads:
  pig:
    # Ordem no menu
    order: 1
    # Identificação necessária para a API de Economias do yPlugins
    yplugins-id: 'yrankup-head-pig'
    # Pode usar cor
    name: '&dPorco'
    # Permissão para ativar / receber (caso esteja ativada na config.yml) a head
    # Deixe vazio ou apague para não usar.
    permission: ''
    # Dar a head automatico no menu
    # false = dar o item pro jogador
    automatic: false
    # Ativar o sell
    sell: true
    # Mundos que não droparão a head
    world-blacklist: []
    # Preços para vender a head
    prices:
      price1:
        provider: 'money'
        price: 100.0
    # Delays
    delays:
      delay1:
        order: 1
        permission: ''
        delay: 5
    # Mensagens de venda
    messages:
      chat: '&aVocê vendeu {amount} heads {head} por &6{money} money&a.'
      actionbar: '&aVocê vendeu {amount} heads {head} por &6{money} money&a.'
      title: ''
    # Mensagens de coleta
    messages-collect:
      chat: '&aVocê coletou {amount} heads {head}&a.'
      actionbar: '&aVocê coletou {amount} heads {head}&a.'
      title: ''
    # Este item será dado ao jogador
    item:
      material: 621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4
      name: '&dCabeça de porco'
      lore: [ '&7Quantia armazenada: &f{amount} cabeça(s) de porco.', '', '&7Clique com botão direito para armazenar.' ]
    # Este irá mostrar no /heads
    display:
      material: 621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4
      name: '&dCabeça de porco'
      lore: [ '&7Quantidade: &f{amount}&7.', '', '&f Valores:', '&f > &a{money} coins por unidade&f.', '', '&b > ${money_total} coins no total', '', '&7Botão &fESQUERDO&a para vender', '&7Botão &fDIREITO&a para coletar' ]

# Entidades que irão dropar as heads
entities:
  pig:
    entity: 'PIG'
    head: 'pig'
    chance: 100.0
    amount: 1
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
  name: '&8Rank - Principal'
  size: 27
  items:
    profile-slot: 10
    rankup-slot: 12
    ranks-slot: 13
    heads-slot: 14
    prestige-slot: 15
    top-slot: 16
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7jogador no ranking.'
        - ''
        - '&fAuto-Rankup: &7{autorankup}'
        - ''
        - '&fFragmentos: &a{coin}&f.'
        - '&fSeu rank: {tag} &7(&f{name}&7)&f.'
        - '&fPróximo rank: {next_tag} &7(&f{next_name}&7)&f.'
        - '&f> &7({progressbar}&7) {percentage}'
        - ''
        - '&fSeu prestígio: &7{prestige} &8-> &6{prestige_percentage}%&f'
        - '&fPróximo prestígio: &a{next_prestige}&f'
        - ''
        - '&fSeu bônus: &a{bonus}%&f.'
        - '&fSeu desconto: &a{discount}%&f.'
        - ''
        - '&aClique para alternar o Auto-Rankup'
    rankup-can:
      material: '1ad6c81f899a785ecf26be1dc48eae2bcfe777a862390f5785e95bd83bd14d'
      name: '&aRankUP'
      lore:
        - '&7Clique para acessar o menu de rankup.'
    rankup-cant:
      material: '1ad6c81f899a785ecf26be1dc48eae2bcfe777a862390f5785e95bd83bd14d'
      name: '&aRankUP'
      lore:
        - '&cParabéns, você chegou no último rank.'
    ranks:
      material: '152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
      name: '&aRanks'
      lore:
        - '&7Clique para acessar o menu de ranks.'
    heads:
      material: '621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4'
      name: '&aHeads'
      lore:
        - '&7Clique para ver suas heads armazenadas.'
        - '&7Você possui &f{amount}&7x heads&7.'
    prestige:
      material: '3ee29e8d07c128115dd4094bf48dceed236aa21eb2022e3730ff9bf23b9a3891'
      name: '&aPrestígio'
      lore:
        - '&fSeu prestígio: &7{prestige} &8-> &6{prestige_percentage}%&f'
        - '&fPróximo prestígio: &a{next_prestige}&f'
        - ''
        - '***&7Clique para evoluir seu prestígio.'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em nosso ranking.'
        - ''
        - '&aClique para acessar!'

# Menu de rankup
rankup:
  name: '&8Rank - Rankup'
  size: 27
  items:
    confirm-slot: 11
    cancel-slot: 15
    rankup-slot: 13
    confirm:
      material: 'e9e4bdcf172d5dc77c2bd4e37ad985399a9f2cdebf72463929ea4b666ef6f80'
      name: '&aConfirmar'
      lore: [ '&7Clique para upar seu rank.' ]
    cancel:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cCancelar'
      lore: [ '&7Clique para cancelar.' ]
    rankup:
      material: '1ad6c81f899a785ecf26be1dc48eae2bcfe777a862390f5785e95bd83bd14d'
      name: '&aUpar de rank!'
      lore:
        - '&8Próximo rank: {rank_tag}'
        - ''
        - ' &fPreços'
        - ' &f•&7 &a{money}&7 coins'
        - ' &f•&7 &a{yrankup-head-pig}&7 cabeças de porco'
        - ''
        - '&fProgresso: &8[{progressbar}&8] &7({percentage})'

# Menu de recompensas
ranks:
  name: '&8Rank - ranks'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  items:
    pig:
      material: '621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4'
      name: '&dRank Porco'
      lore:
        - '&7Informações deste rank:'
        - ''
        - '&d PorcoIII -> PorcoII &f: &7&a{money_pig2} coins, {yrankup-head-pig_pig2} Cabeças de Porco'
        - ''
        - '&d PorcoII -> PorcoI &f: &7&a{money_pig1} coins, {yrankup-head-pig_pig1} Cabeças de Porco'
        - ''

# Menu de heads
heads:
  name: '&8Rank - heads'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  empty-slot: 22
  #
  items:
    empty:
      material: 'WEB'
      name: '&eVazio...'
      lore: [ '&7Nenhuma cabeça armazenada :c' ]

# Menu de top
top:
  name: '&8Rank - TOP'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 30
  previous-slot: 9
  next-slot: 17
  # Seletor dos tops
  selector:
    slot: 31
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor do TOP'
    # Tipos do seletor
    types:
      rank:
        enabled: true
        name: 'Rank'
      prestige:
        enabled: true
        name: 'Prestígio'
      coin:
        enabled: true
        name: 'Fragmentos'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'
  items:
    # Item do top rank
    rank:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fRank: &7{rank}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top prestígio
    prestige:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fPrestígio: &7{prestige}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top coin
    coin:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fFragmentos: &7{amount}'
        - '&fPosição: &e{pos}º'
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

    &aRank comandos:

    &a> /rankup
    &a> /rank
    &a> /rank <player>
    &a> /rank top
    &a> /rank giverankup
    &a> /rank giveprestigio
    &a> /rank setrank
    &a> /rank setprestigio
    &a> /ranks
    &a> /heads
    &a> /prestigio

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  last-rank: '&cVocê já está no último rank.'
  last-prestige: '&cVocê já está no último prestígio.'
  no-balance: '&cVocê não tem {provider_display} suficiente ({need}) para isto. Disponível: {provider_balance}&c.'
  head-got: '&aVocê ganhou &7{amount}x Heads de {head}&a.'
  coin-help: |

    &a/fragmentos &8- &7Ver os seus fragmentos.
    &a/fragmentos <player> &8- &7Ver os fragmentos de alguém.
    &a/fragmentos enviar <player> <quantia> &8- &7Envia seus fragmentos para alguém.
    &a/fragmentos give <player/all> <quantia> &8- &7Dar fragmentos a alguém.
    &a/fragmentos add <player> <quantia> &8- &7Adiciona fragmentos a alguém.
    &a/fragmentos set <player> <quantia> &8- &7Remove fragmentos de alguém.
    &a/fragmentos remove <player> <quantia> &8- &7Seta fragmentos a alguém.

  head-help: |

    &a/head &8- &7Ver os seus fragmentos.
    &a/head give <player/all> <head> <quantia> &8- &7Dar head a alguém.
    &a/head add <player> <head> <quantia> &8- &7Adiciona head a alguém.
    &a/head set <player> <head> <quantia> &8- &7Remove head de alguém.
    &a/head remove <player> <head> <quantia> &8- &7Seta head a alguém.

  player-info: |

    &bInformações de &f{player}&b:
    &f> &7Rank: {tag} &7(&f{name}&7)&f.
    &f> &7Próx Rank: {next_tag} &7(&f{next_name}&7)&f.

    &f> &7Prestígio: &7{prestige} &8-> &6{prestige_percentage}%&f.
    &f> &7Próx prestígio: &a{next_prestige}&f.

  coin: '&bVocê possui &f{coin} fragmentos&b.'
  coin-player: '&bO jogador &f{player}&b possui &f{coin} fragmentos&b.'
  coin-added: '&bVocê adicionou &f{coin} fragmentos&b ao jogador &f{player}&b.'
  coin-removed: '&bVocê removeu &f{coin} fragmentos&b do jogador &f{player}&b.'
  coin-set: '&bVocê setou &f{coin} fragmentos&b para o jogador &f{player}&b.'
  coin-sent: '&bVocê enviou &f{coin} fragmentos&b para o jogador &f{player}&b.'
  coin-received: '&bVocê recebeu &f{coin} fragmentos&b do jogador &f{player}&b.'
  coin-has: '&cVocê não possui a quantia de &f{coin}&c fragmentos.'
  converted: '&bVocê compactou todos seus fragmentos em 1.'
  activated: '&bVocê ativou &f{coin} fragmentos&b.'
  give: '&bVocê deu &f{coin} &bfragmentos para o jogador &f{player}&b.'
  give-all: |

    &bO usuário &f{player}&b deu &f{coin} &bfragmentos para todos os jogadores online&b.

  coin-added-all: '&bVocê adicionou &f{coin} fragmentos&b para todos os jogadores&b.'
  rank-wait: |

    &cEste rank ainda não foi liberado.
    &cLibera em: &7{date} - {hour}'

  head-wait: '&cVocê deve aguardar {time} para ativar heads novamente.'
  head-converted: '&aVocê compactou todas as suas heads &7{head}&a em 1.'
  head-activated: '&aVocê ativou &e{amount} &ade heads &7{head}&a.'
  head-digit: |

    &aDigite a quantia de heads que deseja vender.
    &f> Digite &6TUDO&f para vender tudo.
    &7para cancelar digite &ncancelar&7.

  head-has: '&cVocê não possui essa quantia {amount} de heads.'
  prestige-need: '&cVocê precisa estar no rank {rank} &cpara dar prestígio.'
  autorankup-alterned-on: '&aAuto-Rankup ativado.'
  autorankup-alterned-off: '&cAuto-Rankup desativado.'
  give-rankup: '&bVocê deu &f{amount} &b+1 Rankup para o jogador &f{player}&b.'
  give-rankup-all: |

    &bO usuário &f{player}&b deu &f{amount} &b+1 Rankup para todos os jogadores online&b.

  give-prestige: '&bVocê deu &f{amount} &b+1 Prestígio para o jogador &f{player}&b.'
  give-prestige-all: |

    &bO usuário &f{player}&b deu &f{amount} &b+1 Prestígio para todos os jogadores online&b.

  head-added: '&bVocê adicionou &f{amount} {head}&b ao jogador &f{player}&b.'
  head-removed: '&bVocê removeu &f{amount} {head}&b do jogador &f{player}&b.'
  head-set: '&bVocê setou &f{amount} {head}&b para o jogador &f{player}&b.'
  head-give: '&bVocê deu &f{amount} &b{head} para o jogador &f{player}&b.'
  head-give-all: |

    &bO usuário &f{player}&b deu &f{amount} &b{head} para todos os jogadores online&b.

  head-added-all: '&bVocê adicionou &f{amount} {head}&b para todos os jogadores&b.'
  head-list: |
    &cHead não encontrada.
    &7Disponíveis: {list}
  rank-list: |
    &cRank não encontrado.
    &7Disponíveis: {list}
  rank-set: '&bVocê setou o rank do jogador &f{player}&b para &f{rank}&b.'
  prestige-set: '&bVocê setou o prestígio do jogador &f{player}&b para &f{prestige}&b.'
  prestige-max: '&cO máximo de prestígio é {max}.'
  rankup-wait: '&cVocê deve aguardar {time} para dar rankup novamente.'
]]>
</code-block>
</chapter>

<chapter title="prestiges.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Rank necessário para dar prestígio
need-rank: 3

# Deixe -1 para ser infinito
max: 10

# Tag do prestígio
tag: '&c[{current}]'

# Tag do prestígio caso o valor for 0
tag-zero: '&cNenhum prestígio'

# Acrescimo em % para o valor dos ranks (cost-add * current-prestige)
cost-add: 2.0

# Calcular o custo por potenciação
pow: false

# Custo para dar prestígio (custo * nível de prestígio)
prices:
  price1:
    provider: 'money'
    price: 200000.0

# Comandos que serão executados ao dar prestígio
command: [ 'give {player} diamond 1' ]

# Comandos que serão executados ao alcançar determinado prestígio
# prestígio-necessário,cmd
specific-rewards: [ '1,give {player} diamond 2' ]

# Mensagens que serão enviadas ao dar prestígio
messages:
  chat: |

    &c{player} upou seu prestigio para {current}

  actionbar: ''
  title: ''
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
ranks:
  pig3:
    # Ordem do rank
    # Registro = padrão 1
    order: 1
    # Tag do rank
    tag: '&d[PorcoIII]'
    # Nome do rank
    name: 'Porco III'
    # Data que o rank será liberado para rankup
    release-date: '01/01/2020-10:00'
    # Preços para upar ao rank
    prices:
      price1:
        provider: 'money'
        price: 10000.0
    # Ações de rankup
    rankup:
      # Comandos que serão executados ao dar rankup
      # Será executado ao registrar (ordem 1)
      command: [ 'give {player} stone 1' ]
      # Mensagens que serão enviadas ao dar rankup
      # Será executado ao registrar (ordem 1)
      messages:
        chat: '&cO jogador &7{player} &cregistrou-se e é agora &7PorcoIII&c.'
        actionbar: '&cO jogador &7{player} &cregistrou-se e é agora &7PorcoIII'
        title: ''
      # Mensagens que serão enviadas AO JOGADOR ao dar rankup
      private-messages:
        chat: ''
        actionbar: ''
        title: ''
        balance: |
          &6&lRANKUP! &fRequisitos para evoluir de rank:
          &r
          &8 * &fCoins: &2$&a{money_has}&7/&a{money_need}
  pig2:
    order: 2
    tag: '&d[PorcoII]'
    name: 'Porco II'
    release-date: '01/01/2020-10:00'
    prices:
      price1:
        provider: 'money'
        price: 20000.0
      price2:
        provider: 'yrankup-head-pig'
        price: 100.0
    rankup:
      command: [ 'give {player} stone 2' ]
      messages:
        chat: '&cO jogador &7{player} &cupou e é agora &7PorcoII&c.'
        actionbar: '&cO jogador &7{player} &cupou e é agora &7PorcoII'
        title: ''
      private-messages:
        balance: |
          &6&lRANKUP! &fRequisitos para evoluir de rank:
          &r
          &8 * &fCoins: &2$&a{money_has}&7/&a{money_need}
          &8 * &fCabeças: &5#&d{yrankup-head-pig_has}&7/&d{yrankup-head-pig_need}
  pig1:
    order: 3
    tag: '&d[PorcoI]'
    name: 'Porco I'
    release-date: '01/01/2020-10:00'
    prices:
      price1:
        provider: 'money'
        price: 30000.0
      price2:
        provider: 'yrankup-head-pig'
        price: 200.0
    rankup:
      command: [ 'give {player} stone 3' ]
      messages:
        chat: '&cO jogador &7{player} &cupou e é agora &7PorcoI&c.'
        actionbar: '&cO jogador &7{player} &cupou e é agora &7PorcoI'
        title: ''
      private-messages:
        balance: |
          &6&lRANKUP! &fRequisitos para evoluir de rank:
          &r
          &8 * &fCoins: &2$&a{money_has}&7/&a{money_need}
          &8 * &fCabeças: &5#&d{yrankup-head-pig_has}&7/&d{yrankup-head-pig_need}
]]>
</code-block>
</chapter>

</chapter>
## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yrankup_rank_name% - Retorna o nome do rank
%yrankup_rank_tag% - Retorna a tag do rank
%yrankup_next_rank_name% - Retorna o nome do próximo rank
%yrankup_next_rank_tag% - Retorna a tag do próximo rank
%yrankup_prestige_tag% - Retorna a tag do prestígio
%yrankup_prestige% - Retorna o prestígio
%yrankup_prestige_raw% - Retorna o prestígio sem formatar
%yrankup_next_prestige% - Retorna o próximo prestígio
%yrankup_next_prestige_raw% - Retorna o próximo prestígio sem formatar
%yrankup_progressbar% - Retorna a barra de progresso do rank
%yrankup_percentage% - Retorna a porcentagem de rankup
%yrankup_percentage_raw% - Retorna a porcentagem de rankup (decimais claros)
%yrankup_heads% - Retorna a quantia de heads
%yrankup_heads_raw% - Retorna a quantia de heads sem formatar
%yrankup_head_[head]% - Retorna a quantia de uma head específica
%yrankup_head_[head]_raw% - Retorna a quantia de uma head específica sem formatar
%yrankup_autorankup% - Retorna o estado do auto-rankup
%yrankup_autorankup_raw% - Retorna o estado do auto-rankup sem formatar
%yrankup_coin% - Retorna a quantia de fragmentos
%yrankup_coin_raw% - Retorna a quantia de fragmentos sem formatar
%yrankup_next_price_[provider]% - Retorna a quantia necessária de tal economia para dar rankup
%yrankup_next_price_[provider]_nodiscount% - Retorna a quantia necessária de tal economia para dar rankup sem desconto
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{rank_name} - Retorna o nome do rank
{rank_tag} - Retorna a tag do rank
{next_rank_name} - Retorna o nome do próximo rank
{next_rank_tag} - Retorna a tag do próximo rank
{prestige} - Retorna o prestígio
{prestige_raw} - Retorna o prestígio sem formatar
{prestige_tag} - Retorna a tag do prestígio
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static RankupAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;RankupAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(RankupAPIHolder.class);
        return rsp == null ? null : rsp.getProvider();
    } catch (Throwable var1) {
        return null;
    }
}
</code-block>

## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/32-yRankup">Site do plugin yRankup</a>
    </category>
</seealso>