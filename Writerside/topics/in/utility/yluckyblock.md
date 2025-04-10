# yLuckyBlock
<secondary-label ref="utility"/>

### Descrição
Blocos da sorte que lhe darão recompensas!

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
<video src="//www.youtube.com/watch?v=DoKs8x9dZ_A"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/lb&nbsp;- Envia a mensagem de ajuda
/lb spawn&nbsp;- Spawna uma luckyblock para um jogador
/lb giveopener&nbsp;- Dar abridor para um jogador
/lb give&nbsp;- Dar luckyblock (física) para um jogador
/lb giveanimated&nbsp;- Dar luckyblock (animada) para um jogador
/lb reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yluckyblock.use - Permissão para o /lb
yluckyblock.spawn - Permissão para o /lb spawn
yluckyblock.giveopener - Permissão para o /lb giveopener
yluckyblock.give - Permissão para o /lb give
yluckyblock.giveanimated - Permissão para o /lb giveanimated
yluckyblock.admin.reload - Permissão para o /lb reload
yluckyblock.admin - Permissão para ser reconhecido como admin</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLuckyBlock/
    ├── luckyblocks/
    │    └── default.yml
    ├── luckyblocks_animated/
    │    └── default.yml
    ├── commands.yml
    ├── config.yml
    ├── limit.yml
    ├── menus.yml
    ├── messages.yml
    ├── rarities.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="luckyblocks" collapsible="true">
<chapter title="default.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&eLucky Block &7(Básica)'

# Permissão para poder por a luckyblock
permission: ''

# Cabeça dentro do vidro
head: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'

title: ''
chat: ''
actionbar: '&6&lLUCKY BLOCK &8{progressbar} &7({current_uses}/{total_uses})'

# Ativar a partícula de explosão ao abrir a luckyblock
particle-effect: true

# Precisa de um abridor para abrir
# Irá desativar a abertura ao quebrar
opener-need: false

animation:
  enabled: true
  # Velocidade padrão
  stage-default: 4
  # Tempo máximo que ficará subindo
  # em segundos
  y-max-time: 1.5

# Item da lucky block
# use apenas blocos
item:
  material: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'
  name: '&eLucky Block &7(Básica)'
  lore:
    - '&7Nível: &fBásica'
    - '&7* você irá ganhar itens comuns e raros'
    - ''
    - '&f Usos: &7{total_uses}'
    - ''
    - '&aColoque no chão para ativar'

# Sistema de bloco de vidro
glass:
  # O spawner vai gerar um vidro com uma cabeça dentro?
  enabled: true
  # material do vidro
  material: 'STAINED_GLASS'
  # Data da cor do vidro
  data: 11
  # Ajuste a cabeça dentro do vidro
  off-set: -1.2

# chance,recompensa-raridade
# a raridade, caso não tenha, deixe: none
rewards:
  - '50.00,reward1-none'
  - '50.00,reward2-rare'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="luckyblocks_animated" collapsible="true">
<chapter title="default.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&eLucky Block &7(Básica)'

animation:
  icon: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'
  # Tempo total de animação
  # em segundos
  time: 5
  # Velocidade padrão
  stage-default: 4
  # Tempo (em segundos), velocidade da animação
  stages:
    - '2,20'
    - '3,40'
  # Tempo máximo que ficará subindo
  # em segundos
  y-max-time: 2
  # Premiar após quanto tempo
  reward-time: 6
  # Remover o holograma após quanto tempo
  delete-time: 8
  # Configuração da partícula
  particle:
    # Tempo mínimo para aparecer partículas
    min-time: 3
    # Tipo da partícula
    type: 'happy_villager'
  # Configuração do holograma
  hologram:
    time:
      off-set: 3.0
      lines: ['&aSorteando em {time}...']
    reward:
      off-set: 3.0
      lines: ['{reward}', '[item]{reward_preview}']

# Item da lucky block
# use apenas blocos
item:
  material: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'
  name: '&eLucky Block &7(Básica)'
  lore:
    - '&7Nível: &fBásica'
    - '&7* você irá ganhar itens comuns e raros'
    - ''
    - '&aColoque no chão para ativar'

# chance,recompensa-raridade
# a raridade, caso não tenha, deixe: none
rewards:
  - '50.00,reward1-none'
  - '50.00,reward2-rare'
]]>
</code-block>
</chapter>

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
  luckyblock: 'luckyblock|lb'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# *** ALERTA
# ESTE PLUGIN REQUER A OPÇÃO "packet-events" ATIVADA NO SEU yPlugins
# ***

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

# Sistemas gerais
general:
  # Permitir colocar spawners apenas nos plots
  plot: false
  # Abridor gastar 1 uso por luckyblock (mesmo que esta tenha ex: 50 tentativas)
  opener-one-decrease: false
  # Abrir automaticamente a lucky-block (bloco) ao colocar no chão
  # permissão necessária: yluckyblock.open.bypass
  # deixe "false" para não usar
  open-automatic-bypass: false

# Limite de stack de spawners.
opener:
  material: 'LEASH'
  name: '&6&lOPEN LUCKY BLOCK'
  lore:
    - '&fUsos restantes: &e{uses}'

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'
]]>
</code-block>
</chapter>

<chapter title="limit.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Quantia de limite que o jogador ganhar ao se registrar.
default: 1

# Máximo de limite que o jogador pode ter.
# Deixe 0 para ser infinito.
maximum: 100

# Delay para compactar
# em segundos
delay: 5

give: '&aVocê deu &7{amount}x &6&lLimite Lucky Block&a para o jogador &7{player}&a.'
received: '&aVocê recebeu &7{amount}x &6&lLimite Lucky Bloc&a.'
converted: '&cVocê compactou todos seus limites em 1.'
activated: '&aVocê ativou &e{amount} &ade limites.'
max: '&cVocê já chegou no máximo.'
converted-lb: '&cVocê compactou suas lucky-blocks.'
delay-msg: '&cVocê deve aguardar {time}.'

# Item do limite que será ativável
item:
  material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  name: '&bLimite de LukcyBlock'
  lore:
    - ''
    - '&fQuantia: &a{amount}'
    - ''
    - '&7Clique com botão direito para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
    - ''
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

# Menu de preview das recompensas
preview:
  name: '&8Lucky Block'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  facing:
    e0:
      slot: 11
      material: 'BARRIER'
      name: ' '
      lore: []
    e1:
      slot: 12
      material: 'BARRIER'
      name: ' '
      lore: []
    e2:
      slot: 13
      material: 'BARRIER'
      name: ' '
      lore: []
    e3:
      slot: 14
      material: 'BARRIER'
      name: ' '
      lore: []
    e4:
      slot: 15
      material: 'BARRIER'
      name: ' '
      lore: []
    e5:
      slot: 20
      material: 'BARRIER'
      name: ' '
      lore: []
    e6:
      slot: 21
      material: 'BARRIER'
      name: ' '
      lore: []
    e7:
      slot: 22
      material: 'BARRIER'
      name: ' '
      lore: []
    e8:
      slot: 23
      material: 'BARRIER'
      name: ' '
      lore: []
    e9:
      slot: 24
      material: 'BARRIER'
      name: ' '
      lore: []
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

    &aLucky-Block comandos:

    &a> /luckyblock giveopener <player <usos> <quantia>
    &a> /luckyblock giveanimated <player> <luckyblock> <quantia>
    &a> /luckyblock give <player> <luckyblock> <usos> <quantia>
    &a> /luckyblock reload

  animated-luckyblock-give: '&aVocê deu &7{amount}x {luckyblock}&a para o jogador &7{player}&a.'
  animated-luckyblock-received: '&aVocê recebeu &7{amount}x {luckyblock}&a.'
  animated-luckyblock-list: |
    &cLuckyBlock Animada não encontrada.
    &cLuckyBlocks Animadas disponíveis: &f{list}
  luckyblock-give: '&aVocê deu &7{amount}x {luckyblock} &7({uses} usos)&a para o jogador &7{player}&a.'
  luckyblock-received: '&aVocê recebeu &7{amount}x {luckyblock} &7({uses} usos)&a.'
  luckyblock-list: |
    &cLuckyBlock não encontrada.
    &cLuckyBlocks disponíveis: &f{list}
  plot-permission: '&cVocê não tem permissão neste terreno.'
  perm-luckyblock: '&cVocê não tem permissão para colocar este tipo de luckyblock.'
  placed: '&a{amount}x {luckyblock} &acolocada(s).'
  already: '&cVocê já possui uma luckyblock colocada.'
  just-owner: '&cSomente o dono da luckyblock pode realizar esta ação.'
  opener-give: '&aVocê deu &7{amount}x &6&lOPEN LUCKY BLOCK &7({uses} usos)&a para o jogador &7{player}&a.'
  opener-received: '&aVocê recebeu &7{amount}x &6&lOPEN LUCKY BLOCK &7({uses} usos)&a.'
  animated-luckyblock-spawn: '&aVocê spawnou &7{amount}x {luckyblock}&a na localização do jogador &7{player}&a.'
  opener-need: '&cVocê precisa de um abridor para fazer isso.'
  all-luckyblock-list: |
    &r
    &cLuckyBlock não encontrada.
    &r
    &cLuckyBlocks disponíveis: &f{list}
    &r
    &cLuckyBlocks (animadas) disponíveis: &f{list_animated}
    &r
]]>
</code-block>
</chapter>

<chapter title="rarities.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
rarities:
  rare:
    display: '&6Raro'
    strike: false # pode causar lag
    bat: false # pode causar lag
    actionbar: '&e[Lucky Block] &fO jogador &e{player}&f encontrou uma recompensa rara na LuckyBlock&f.'
    title: ''
    chat: |
      &e[Lucky Block] &fO jogador &e{player}&f encontrou uma recompensa rara na LuckyBlock&f.
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', '&fChance: &6{chance}%' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', '&fChance: &6{chance}%' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', '&fChance: &6{chance}%' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLuckyBlock/
    ├── luckyblocks/
    │    └── default.yml
    ├── luckyblocks_animated/
    │    └── default.yml
    ├── commands.yml
    ├── config.yml
    ├── messages.yml
    ├── rarities.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="luckyblocks" collapsible="true">
<chapter title="default.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&eLucky Block &7(Básica)'

# Permissão para poder por a luckyblock
permission: ''

# Cabeça dentro do vidro
head: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'

title: ''
chat: ''
actionbar: '&6&lLUCKY BLOCK &8{progressbar} &7({current_uses}/{total_uses})'

# Ativar a partícula de explosão ao abrir a luckyblock
particle-effect: true

animation:
  enabled: true
  # Velocidade padrão
  stage-default: 4
  # Tempo máximo que ficará subindo
  # em segundos
  y-max-time: 1.5

# Item da lucky block
# use apenas blocos
item:
  material: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'
  name: '&eLucky Block &7(Básica)'
  lore:
    - '&7Nível: &fBásica'
    - '&7* você irá ganhar itens comuns e raros'
    - ''
    - '&f Usos: &7{total_uses}'
    - ''
    - '&aColoque no chão para ativar'

# Sistema de bloco de vidro
glass:
  # O spawner vai gerar um vidro com uma cabeça dentro?
  enabled: true
  # material do vidro
  material: 'STAINED_GLASS'
  # Data da cor do vidro
  data: 11
  # Ajuste a cabeça dentro do vidro
  off-set: -1.2

# chance,recompensa-raridade
# a raridade, caso não tenha, deixe: none
rewards:
  - '50.00,reward1-none'
  - '50.00,reward2-rare'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="luckyblocks_animated" collapsible="true">
<chapter title="default.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&eLucky Block &7(Básica)'

animation:
  icon: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'
  # Tempo total de animação
  # em segundos
  time: 5
  # Velocidade padrão
  stage-default: 4
  # Tempo (em segundos), velocidade da animação
  stages:
    - '2,20'
    - '3,40'
  # Tempo máximo que ficará subindo
  # em segundos
  y-max-time: 2
  # Premiar após quanto tempo
  reward-time: 6
  # Remover o holograma após quanto tempo
  delete-time: 8
  # Configuração da partícula
  particle:
    # Tempo mínimo para aparecer partículas
    min-time: 3
    # Tipo da partícula
    type: 'happy_villager'
  # Configuração do holograma
  hologram:
    time:
      off-set: 3.0
      lines: ['&aSorteando em {time}...']
    reward:
      off-set: 3.0
      lines: ['{reward}', '[item]{reward_preview}']

# Item da lucky block
# use apenas blocos
item:
  material: '238c0d2f1ec26754dca3c7cdae31f1f164883d453e688643da047568e7fa5cc9'
  name: '&eLucky Block &7(Básica)'
  lore:
    - '&7Nível: &fBásica'
    - '&7* você irá ganhar itens comuns e raros'
    - ''
    - '&aColoque no chão para ativar'

# chance,recompensa-raridade
# a raridade, caso não tenha, deixe: none
rewards:
  - '50.00,reward1-none'
  - '50.00,reward2-rare'
]]>
</code-block>
</chapter>

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
  luckyblock: 'luckyblock|lb'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
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

# Limite de stack de spawners.
opener:
  material: 'LEASH'
  name: '&6&lOPEN LUCKY BLOCK'
  lore:
    - '&fUsos restantes: &e{uses}'

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'
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

    &aSpawners comandos:

    &a> /luckyblock giveanimated <player> <luckyblock> <quantia>
    &a> /luckyblock give <player> <luckyblock> <quantia>
    &a> /luckyblock reload

  animated-luckyblock-give: '&aVocê deu &7{amount}x {luckyblock}&a para o jogador &7{player}&a.'
  animated-luckyblock-received: '&aVocê recebeu &7{amount}x {luckyblock}&a.'
  animated-luckyblock-list: |
    &cLuckyBlock Animada não encontrada.
    &cLuckyBlocks Animadas disponíveis: &f{list}

  luckyblock-give: '&aVocê deu &7{amount}x {luckyblock} &7({uses} usos)&a para o jogador &7{player}&a.'
  luckyblock-received: '&aVocê recebeu &7{amount}x {luckyblock} &7({uses} usos)&a.'
  luckyblock-list: |
    &cLuckyBlock não encontrada.
    &cLuckyBlocks disponíveis: &f{list}
  plot-permission: '&cVocê não tem permissão neste terreno.'
  perm-luckyblock: '&cVocê não tem permissão para colocar este tipo de luckyblock.'
  placed: '&a{amount}x {luckyblock} &acolocada(s).'
  already: '&cVocê já possui uma luckyblock colocada.'
  just-owner: '&cSomente o dono da luckyblock pode realizar esta ação.'
  opener-give: '&aVocê deu &7{amount}x &6&lOPEN LUCKY BLOCK &7({uses} usos)&a para o jogador &7{player}&a.'
  opener-received: '&aVocê recebeu &7{amount}x &6&lOPEN LUCKY BLOCK &7({uses} usos)&a.'
]]>
</code-block>
</chapter>

<chapter title="rarities.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
rarities:
  rare:
    display: '&6Raro'
    strike: false # pode causar lag
    bat: false # pode causar lag
    actionbar: '&e[Lucky Block] &fO jogador &e{player}&f encontrou uma recompensa rara na LuckyBlock&f.'
    title: ''
    chat: |
      &e[Lucky Block] &fO jogador &e{player}&f encontrou uma recompensa rara na LuckyBlock&f.
]]>
</code-block>
</chapter>

<chapter title="rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

rewards:
  reward1:
    # Item que aparecerá no preview.
    preview:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!' ]
      enchants: []
    # Item que aparecerá para coletar.
    collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Item que será dado ao player
    item:
      give: true
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEu valho muito!' ]
      enchants: []
    # Comandos que será dado ao player
    command:
      give: false
      # quantia padrão da placeholder {amount} no comando (valor base)
      placeholder-amount: 1
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      multiply-placeholder: true
      list: [ 'give {player} stone {amount}' ]
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
      enchants: []
    collect:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    command:
      give: true
      placeholder-amount: 1
      multiply-placeholder: true
      list: [ 'give {player} diamond {amount}' ]
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
      enchants: []
    collect:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    item:
      give: true
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEu valho muito!' ]
      enchants: []
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/122-yLuckyBlock">Site do plugin yLuckyBlock</a>
    </category>
</seealso>