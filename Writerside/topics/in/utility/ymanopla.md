# yManopla
<secondary-label ref="utility"/>

### Descrição
Dê efeitos permanentes aos jogadores por meio de joias

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
<video src="//www.youtube.com/watch?v=qveiqizWFac"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/manopla&nbsp;- Abre o menu principal
/manopla help&nbsp;- Envia a mensagem de ajuda
/manopla give&nbsp;- Dá joias para um jogador
/manopla&nbsp;giveslot&nbsp;- Dá slots para um jogador
/manopla&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymascots.use - Permissão para o /manopla
ymanopla.give - Permissão para o /manopla give
ymanopla.giveslot - Permissão para o /manopla giveslot
ymanopla.admin.reload - Permissão para o /manopla reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yManopla/
    ├── commands.yml
    ├── config.yml
    ├── jewelries.yml
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
  manopla: 'manopla|manoplas'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __                         _
#  _   _|  \/  | __ _ _ __   ___  _ __ | | __ _
# | | | | |\/| |/ _` | '_ \ / _ \| '_ \| |/ _` |
# | |_| | |  | | (_| | | | | (_) | |_) | | (_| |
#  \__, |_|  |_|\__,_|_| |_|\___/| .__/|_|\__,_|
#  |___/                         |_|
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

# Blacklist de mundos que os efeitos (poções) não irão funcionar
world-blacklist: []

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

<chapter title="jewelries.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
jewelries:
  add:
    order: 1
    # Nome da joia nas mensagens
    display: '&aJoia da Adição'
    # Esta joia será apenas de amplificação
    amplifier: true
    # Quantia que irá adicionar de aplificação
    to-add: 1
    # Item utilizável
    item:
      material: 'INK_SACK:1'
      name: '&aJoia da Adição'
      lore: [ '', '&7Por meio desta joia você irá', '&7adquirir &f+1 amplificador em todas as', '&7outras joias&7 permanentemente.', '', '&aClique para ativar.' ]
    # Item do menu
    menu:
      material: 'INK_SACK:1'
      name: '&aJoia da Adição'
      lore: [ '', '&7Por meio desta joia você está', '&7adquirindo &f+1 amplificador em todas as', '&7outras joias&7 permanentemente.', '', '&aClique para remover.' ]
  time:
    order: 2
    # Nome da joia nas mensagens
    display: '&aJoia do Tempo'
    # Item utilizável
    item:
      material: 'INK_SACK:10'
      name: '&aJoia do Tempo'
      lore: [ '', '&7Por meio desta joia você irá', '&7adquirir &fSuper Pulo I&7 permanentemente.', '', '&aClique para ativar.' ]
    # Item  do menu
    menu:
      material: 'INK_SACK:10'
      name: '&aJoia do Tempo'
      lore: [ '', '&7Por meio desta joia você está', '&7adquirindo &fSuper Pulo I&7 permanentemente.', '', '&aClique para remover.' ]
    # Efeitos da joia
    potion-effects:
      effect1:
        type: 'JUMP'
        amplifier: 1
  power:
    order: 3
    # Nome da joia nas mensagens
    display: '&5Joia do Poder'
    # Item utilizável
    item:
      material: 'INK_SACK:5'
      name: '&5Joia do Poder'
      lore: [ '', '&7Por meio desta joia você irá', '&7adquirir &fResistência I&7 permanentemente.', '', '&aClique para ativar.' ]
    # Item  do menu
    menu:
      material: 'INK_SACK:5'
      name: '&5Joia do Poder'
      lore: [ '', '&7Por meio desta joia você está', '&7adquirindo &fResistência I&7 permanentemente.', '', '&aClique para remover.' ]
    # Efeitos da joia
    potion-effects:
      effect1:
        type: 'DAMAGE_RESISTANCE'
        amplifier: 1
  space:
    order: 4
    # Nome da joia nas mensagens
    display: '&1Joia do Espaço'
    # Item utilizável
    item:
      material: 'INK_SACK:4'
      name: '&1Joia do Espaço'
      lore: [ '', '&7Por meio desta joia você irá', '&7adquirir &fVelocidade I&7 permanentemente.', '', '&aClique para ativar.' ]
    # Item  do menu
    menu:
      material: 'INK_SACK:4'
      name: '&1Joia do Espaço'
      lore: [ '', '&7Por meio desta joia você está', '&7adquirindo &fVelocidade I&7 permanentemente.', '', '&aClique para remover.' ]
    # Efeitos da joia
    potion-effects:
      effect1:
        type: 'SPEED'
        amplifier: 1
  mind:
    order: 5
    # Nome da joia nas mensagens
    display: '&eJoia da Mente'
    # Item utilizável
    item:
      material: 'INK_SACK:11'
      name: '&eJoia da Mente'
      lore: [ '', '&7Por meio desta joia você irá', '&7adquirir &fPressa I&7 permanentemente.', '', '&aClique para ativar.' ]
    # Item  do menu
    menu:
      material: 'INK_SACK:11'
      name: '&eJoia da Mente'
      lore: [ '', '&7Por meio desta joia você está', '&7adquirindo &fPressa I&7 permanentemente.', '', '&aClique para remover.' ]
    # Efeitos da joia
    potion-effects:
      effect1:
        type: 'FAST_DIGGING'
        amplifier: 1
  reality:
    order: 5
    # Nome da joia nas mensagens
    display: '&dJoia da Realidade'
    # Item utilizável
    item:
      material: 'INK_SACK:9'
      name: '&dJoia da Realidade'
      lore: [ '', '&7Por meio desta joia você irá', '&7adquirir &fForça I&7 permanentemente.', '', '&aClique para ativar.' ]
    # Item  do menu
    menu:
      material: 'INK_SACK:9'
      name: '&dJoia da Realidade'
      lore: [ '', '&7Por meio desta joia você está', '&7adquirindo &fForça I&7 permanentemente.', '', '&aClique para remover.' ]
    # Efeitos da joia
    potion-effects:
      effect1:
        type: 'INCREASE_DAMAGE'
        amplifier: 1
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
  name: '&8Manopla'
  size: 27
  slots: [ 11, 12, 14, 15 ]
  previous-slot: 9
  next-slot: 17
  items:
    slot-empty:
      material: 'STAINED_GLASS_PANE:5'
      name: '&aSlot Livre'
      lore: []
    slot-need:
      material: 'STAINED_GLASS_PANE:14'
      name: '&cSlot Bloqueado'
      lore: []
  facing:
    e0:
      slot: 0
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e1:
      slot: 1
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e2:
      slot: 2
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e3:
      slot: 3
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e4:
      slot: 4
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e5:
      slot: 5
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e6:
      slot: 6
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e7:
      slot: 7
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e8:
      slot: 8
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e9:
      slot: 10
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e10:
      slot: 13
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e11:
      slot: 16
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e12:
      slot: 18
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e13:
      slot: 19
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e14:
      slot: 20
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e15:
      slot: 21
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e16:
      slot: 22
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e17:
      slot: 23
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e18:
      slot: 24
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e19:
      slot: 25
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e20:
      slot: 26
      material: 'STAINED_GLASS_PANE:8'
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

    &aManopla comandos:

    &a> /manopla
    &a> /manopla give <player> <joia> <quantia>
    &a> /manopla giveslot <player> <quantia>

  jewelry-give: '&aVocê deu 1x {jewelry}&a para o jogador &7{player}&a.'
  jewelry-received: '&aVocê recebeu &71x {jewelry}&a.'
  jewelry-list: |
    &cJoia não encontrada.
    &cJoias disponíveis: &f{list}
  jewelry-have: '&cVocê já possui esta joia {jewelry}&c.'
  jewelry-activated: '&aVocê ativou a joia {jewelry}&a.'
  jewelry-removed: '&aVocê removeu a joia {jewelry}&a.'
  slots-need: '&cVocê precisa de mais slots livres.'
  slot-activated: '&aVocê ativou &e{amount} &ade slots.'
  slot-max: '&cVocê já chegou no máximo.'
  slot-give: '&aVocê deu &e{amount} &ade slots para o jogador &e{player}&a.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/139-yManopla">Site do plugin yManopla</a>
    </category>
</seealso>