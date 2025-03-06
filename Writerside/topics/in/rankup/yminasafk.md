# yMinasAFK
<secondary-label ref="rankup"/>

### Descrição
Minere enquanto seu boneco está parado!

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
<video src="//www.youtube.com/watch?v=yPjP13UE638"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/minaafk - Vai até a mina
/minaafk menu - Abre o menu principal
/minaafk setarentrada - Seta a entrada da mina-afk
/minaafk wand - Pega a varinha de seleção da mina-afk
/minaafk reload - Recarrega os arquivos de configuração</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yminasafkaddon.use - Permissão para o /minaafk e /minaafk menuyminasafkaddon.admin.setenter - Permissão para o /minaafk setarentradayminasafkaddon.admin.wand - Permissão para o /minaafk wandyminasafkaddon.admin.reload - Permissão para o /minaafk reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMinasAFK/
    ├── minas/
    │    ├── default.yml
    │    └── medium.yml
    ├── bonus.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    ├── mine_rewards.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="minas" collapsible="true">
<chapter title="default.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Prioridade da mina
order: 1

# Nome da mina nas mensagens
name: '&5Mina AFK &7(1)'

# Delay para recompensar e cobrar
# em segundos
delay: 5

# Tempo que o jogador poderá ficar minerado
# em segundos
total-time: 1800

# Tempo que irá levar para resetar o total-time do jogador
# em segundos
total-time-reset: 1800

# Ícone no menu de evolução
icons:
  has:
    material: 'INK_SACK:5'
    name: '&5Mina AFK &7(1)'
    lore: [ '&7Esta mina irá consumir', '&c100 coins &7para gerar', '&a10 tokens&7.', '', '&cVocê já possui este upgrade' ]
  upgrade:
    material: 'INK_SACK:5'
    name: '&5Mina AFK &7(1)'
    lore: [ '&7Esta mina irá consumir', '&c100 coins &7para gerar', '&a10 tokens&7.', '', '&aClique para comprar este upgrade', '&apor &f{money} coins&a.' ]

# Mensagens gerais
messages:
  afk:
    title: '&5MINA AFK<nl>&fMinerando...'
    actionbar: '&aVocê ainda pode minerar por {time}.'
    chat: ''
  deposit:
    title: ''
    actionbar: '&a+{yeconomias-tokens} tokens adicionados ┃ &r{bonus}&a.'
    chat: ''
  balance:
    title: ''
    actionbar: '&cVocê não possui {money} coins.'
    chat: ''

# Preços para minerar
withdrawals:
  withdrawal1:
    provider: 'money'
    amount: 100

# Recompensas que o jogador irá ganhar
deposits:
  deposit1:
    provider: 'yeconomias-tokens'
    amount: 10

# Preços para dar upgrade
upgrade-prices:
  price1:
    provider: 'money'
    amount: 1000000
]]>
</code-block>
</chapter>

<chapter title="medium.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Prioridade da mina
order: 2

# Nome da mina nas mensagens
name: '&6Mina AFK &7(2)'

# Delay para recompensar e cobrar
# em segundos
delay: 5

# Tempo que o jogador poderá ficar minerado
# em segundos
total-time: 1800

# Tempo que irá levar para resetar o total-time do jogador
# em segundos
total-time-reset: 1800

# Ícone no menu de evolução
icons:
  has:
    material: 'INK_SACK:14'
    name: '&6Mina AFK &7(2)'
    lore: [ '&7Esta mina irá consumir', '&c200 coins &7para gerar', '&a25 tokens&7.', '', '&cVocê já possui este upgrade' ]
  upgrade:
    material: 'INK_SACK:14'
    name: '&6Mina AFK &7(2)'
    lore: [ '&7Esta mina irá consumir', '&c200 coins &7para gerar', '&a25 tokens&7.', '', '&aClique para comprar este upgrade', '&apor &f{money} coins&a.' ]

# Mensagens gerais
messages:
  afk:
    title: '&6MINA AFK<nl>&fMinerando...'
    actionbar: '&aVocê ainda pode minerar por {time}.'
    chat: ''
  deposit:
    title: ''
    actionbar: '&a+{yeconomias-tokens} tokens adicionados ┃ &r{bonus}&a.'
    chat: ''
  balance:
    title: ''
    actionbar: '&cVocê não possui {money} coins.'
    chat: ''

# Preços para minerar
withdrawals:
  withdrawal1:
    provider: 'money'
    amount: 200

# Recompensas que o jogador irá ganhar
deposits:
  deposit1:
    provider: 'yeconomias-tokens'
    amount: 25

# Preços para dar upgrade
upgrade-prices:
  price1:
    provider: 'money'
    amount: 1000000
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos bônus quiser
bonus:
  membros:
    order: 1
    # Permissão para ser reconhecido
    permission: 'yminas.bonus.membro'
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
  minaafk: 'minaafk'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         __  __ _                    _    _____ _  __
#  _   _|  \/  (_)_ __   __ _ ___   / \  |  ___| |/ /
# | | | | |\/| | | '_ \ / _` / __| / _ \ | |_  | ' /
# | |_| | |  | | | | | | (_| \__ \/ ___ \|  _| | . \
#  \__, |_|  |_|_|_| |_|\__,_|___/_/   \_\_|   |_|\_\
#  |___/
#
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

# Delay para carregar os dados depois do servidor ligar
# Necessário para as crates em bloco
# Recomendado: 20 ticks
load-delay: 20

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Opções gerais
general:
  # Abrir o menu ao digitar apenas /minaafk
  command-menu: false
  # Acumular os bonus
  accumulate-bonus: false
  # Deletar a recompensa ao clicar com botão direito
  right-delete-reward: true

# Formatador de mensagens
format:
  bonus-has: '&a+{bonus}% por ser {display}&a.'
  bonus-no-has: ''

# Mensagens gerais
messages:
  stopped:
    title: '&3MINA AFK<nl>&fParou de minerar.'
    actionbar: ''
    chat: ''
  wait:
    title: ''
    actionbar: '&cAguarde {time}.'
    chat: ''

 # Varinha de seleção da área da mina
wand:
  material: GOLD_AXE
  name: '&eSelecionar região'
  glow: true
  lore: [ '&aBotão esquerdo para selecionar a POS1', '&aBotão direito para selecionar a POS2']
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locais: {}
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
    permission: 'yminasafk.provider.money'
  yeconomias-token:
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
    permission: 'yminasafk.provider.yeconomias-token'
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
  name: '&8MinaAFK'
  size: 27
  go-slot: 15
  rewards-slot: 13
  upgrade-slot: 11
  items:
    go:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&eIr!'
      lore:
        - '&7Ganhe tokens enquanto minera'
        - '&7afk por seus coins.'
        - ''
        - '&aClique para ir.'
    rewards:
      material: 'CHEST'
      name: '&aRecompensas'
      lore:
        - ''
        - ' &fRecompensas no armazém: &a{rewards}&f.'
        - ''
        - '&7Clique para gerenciar'
    upgrade:
      material: 'GOLD_INGOT'
      name: '&eUpgrades!'
      lore:
        - '&7Melhore a eficácia da sua'
        - '&7mina afk.'
        - ''
        - '&aClique para acessar.'

# Menu de upgrades
upgrade:
  name: '&8MinaAFK'
  size: 27
  slots: [ 11, 12, 13, 14, 15  ]
  back-slot: 0
  previous-slot: 9
  next-slot: 17

# Menu de recompensas
main-rewards:
  name: '&8MinaAFK'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  #
  empty-slot: 22
  collect-slot: 50
  #
  items:
    empty:
      material: 'WEB'
      name: '&eVazio...'
      lore: [ '&7Nenhuma recompensa para', '&7coletar.' ]
    collect:
      material: 'a6cc486c2be1cb9dfcb2e53dd9a3e9a883bfadb27cb956f1896d602b4067'
      name: '&eRecolher tudo'
      lore: [ '&7Clique para recolher', '&7todas as recompensas.' ]
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

    &aMina-AFK comandos:

    &a> /minaafk
    &a> /minaafk menu
    &a> /minaafk setarentrada
    &a> /minaafk wand

  set-pos-1: '&aPOS-1 da MinaAFK setada com sucesso.'
  set-pos-2: '&aPOS-2 da MinaAFK setada com sucesso.'
  set-entry: '&aEntrada da MinaAFK setada com sucesso.'
  entry-not-set: '&cA entrada da MinaAFK não foi setada ainda.'
  pos-not-set: '&cAs posições da MinaAFK não foram setadas ainda.'
  previous: '&cPrimeiro evolua o upgrade anterior.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  upgraded: '&aMinaAFK evoluída com sucesso ao nível &7({level})&a.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
]]>
</code-block>
</chapter>

<chapter title="mine_rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
rewards:
  mine_reward1:
    chance: 20.0
    reward: 'reward1'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/124-yMinasAFK">Site do plugin yMinasAFK</a>
    </category>
</seealso>