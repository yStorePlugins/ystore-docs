# yCubos
<secondary-label ref="utility"/>

### Descrição
Crie cubos surpresas que poderão ser abertos

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
<video src="//www.youtube.com/watch?v=6V0k1fKlJww"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/cubos - Abre o menu principal
/cubos enviar - Envia seus fragmentos para outro jogador
/cubos darfragmento - Dar fragmentos para um jogador
/cubos add - Adiciona fragmentos para um jogador
/cubos set - Seta fragmentos para um jogador
/cubos remove - Remove fragmentos de um jogador
/cubos reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycubos.use - Permissão para o /cubos
ycubos.fragments.send - Permissão para o /cubos enviar
ycubos.fragments.set - Permissão para o /cubos set
ycubos.fragments.add - Permissão para o /cubos add
ycubos.fragments.remove - Permissão para o /cubos remove
ycubos.admin.reload - Permissão para o /cubos reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCubos/
    ├── cubos/
    │    └── basic.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="cubos" collapsible="true">
<chapter title="basic.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ordem do tipo de cubo
# O jogador começa no cubo de ordem 1
# Ele evolui o nível assim que termina de coletar todos
order: 1

# Nome nas mensagens
display: '&fCubo Básico'

# Permissão para abrir os cubos
permission: ''

# Item do cubo coletado
collected:
  material: 'BARRIER'
  name: '&cCubo resgatado!'
  lore: [ '&7Este cubo já foi resgatado', '&7tente abrir outro cubo!' ]

# Configurações do menu
menu:
  name: '&8Cubos'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 20, 21, 22, 23, 24, 25, 29, 30, 31, 32, 33, 34, 38, 39, 40, 41, 42, 43 ]
  previous-slot: 48
  next-slot: 50
  items:
    info-slot: 0
    collect-slot: 45
    top-slot: 53
    info:
      material: '9a3cc25a16c97b4fc63858ad1a8f5d293ecf285f702efdc4caa31a8cea9e4621'
      name: '&eCubos aleatórios'
      lore: [ '&7Sua recompensa está oculta', '&7em um dos mistérios aqui.', '', '&e* Gaste &l10&e fragmentos para', '&e abrir um cubo.', '', '&fSeu saldo de fragmentos: &e{fragments}' ]
    collect:
      material: 'QUARTZ'
      name: '&eFragmento'
      lore: [ '&7Clique para recolher os', '&7fragmentos que você possui.', '', '&fSeu saldo de fragmentos: &e{fragments}' ]
    top:
      material: 'GOLD_INGOT'
      name: '&eTOP Cubos'
      lore: [ '&7Clique para ver os usuários', '&7que mais ativaram cubos.' ]
  facing:
    1:
      material: 'STAINED_GLASS_PANE:15'
      name: '&r'
      slot: 9
    2:
      material: 'STAINED_GLASS_PANE:15'
      name: '&r'
      slot: 18
    3:
      material: 'STAINED_GLASS_PANE:15'
      name: '&r'
      slot: 27
    4:
      material: 'STAINED_GLASS_PANE:15'
      name: '&r'
      slot: 36

# Configuração de cada cubo
cubos:
  cubo1:
    material: '925aca61e1b8beca9befcadd08262c5821e275be414d94f0b27e8580f20dbf3a'
    name: '&e&kaaaaaaaaaaaa'
    lore: [ '&7Um item misterioso está oculto aqui.', '', '&fRequisitos p/ abrir:', '&e* &f&l{ycubos}x &ffragmentos.', '', '&fClique para abrir.' ]
    # Preços do cubo
    prices:
      price1:
        provider: 'ycubos'
        amount: 10.0
    # Quantia máxima de recompensas que o cubo pode dar
    # Deixe 0 para rodar toda a lista
    max-rewards: 0
    # chance,recompensa
    rewards: [ '100.0,reward1' ]
  cubo2:
    material: '925aca61e1b8beca9befcadd08262c5821e275be414d94f0b27e8580f20dbf3a'
    name: '&e&kaaaaaaaaaaaa'
    lore: [ '&7Um item misterioso está oculto aqui.', '', '&fRequisitos p/ abrir:', '&e* &f&l{ycubos}x &ffragmentos.', '', '&fClique para abrir.' ]
    prices:
      price1:
        provider: 'ycubos'
        amount: 10.0
    max-rewards: 0
    rewards: [ '100.0,reward2' ]
  cubo3:
    material: '925aca61e1b8beca9befcadd08262c5821e275be414d94f0b27e8580f20dbf3a'
    name: '&e&kaaaaaaaaaaaa'
    lore: [ '&7Um item misterioso está oculto aqui.', '', '&fRequisitos p/ abrir:', '&e* &f&l{ycubos}x &ffragmentos.', '', '&fClique para abrir.' ]
    prices:
      price1:
        provider: 'ycubos'
        amount: 10.0
    max-rewards: 0
    rewards: [ '100.0,reward3' ]
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
  cubo: 'cubo|cubos'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____      _
#  _   _ / ___|   _| |__   ___  ___
# | | | | |  | | | | '_ \ / _ \/ __|
# | |_| | |__| |_| | |_) | (_) \__ \
#  \__, |\____\__,_|_.__/ \___/|___/
#  |___/
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

# Resetar os cubos ao completar todos os menus
reset-completed: false

# Item do fragmento
fragment:
  material: 'QUARTZ'
  name: '&eFragmento de Cubo &7[{amount}]'
  lore:
    - '&7Teste a sua sorte e se'
    - '&7habilite a ganhar várias'
    - '&7recompensas incríveis!'
    - ''
    - '&eClique para ativar e acesse'
    - '&f/cubos &epara abrir!'
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
  ycubos:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yCubos'
    # Formato inteiro
    display: 'Fragmentos'
    # Formato abreviado
    abbreviated: 'fragmentos'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'ycubos.provider.ycubos'
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

# Menu de top
top:
  name: '&8TOP Cubos'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 31
  previous-slot: 9
  next-slot: 17
  items:
    # Item do top abertas
    opened:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fCubos abertas: &7{amount}'
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

    &aCubos comandos:

    &a> /cubos
    &a> /cubo enviar
    &a> /cubo darfragmento
    &a> /cubo add
    &a> /cubo set
    &a> /cubo remove
    &a> /cubo reload

  no-has: '&cVocê não possui nenhuma lista de cubos disponível.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  opened: '&aVocê coletou um cubo por &f{ycubos} fragmentos&a.'
  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  fragments-sent: '&bVocê enviou &f{amount} fragmentos&b para o jogador &f{player}&b.'
  fragments-received-player: '&bVocê recebeu &f{amount} fragmentos&b do jogador &f{player}&b.'
  fragments-no-has: '&bVocê não possui &f{amount} fragmentos&b.'
  fragments-changed: '&aFragmentos do jogador &7{player}&a alterado para &7{amount}&a.'
  fragments-give: '&aVocê deu &7{amount}x fragmentos&a para o jogador &7{player}&a.'
  fragments-received: '&aVocê recebeu &7{amount}x fragmentos&a.'
  fragments-converted: '&aVocê converteu todos seus fragmentos em um só.'
  fragments-activated: '&aVocê aumentou o seu fragmentos em {amount}.'
  fragments-collected: '&aVocê coletou {amount} fragmentos.'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/123-yCubos">Site do plugin yCubos</a>
    </category>
</seealso>