# yClearPlot
<secondary-label ref="rankup"/>

### Descrição
Limpe seu terreno com apoio de pedreiros

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
<video src="//www.youtube.com/watch?v=Wx9-h12nl6A"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/clearplot - Mostra a lista de comandos
/clearplot give - Dar o limpador para um jogador
/clearplot reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yclearplot.use - Permissão para o /clearplot
yclearplot.give - Permissão para o /clearplot give
yclearplot.reload - Permissão para o /clearplot reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yClearPlot/
    ├── commands.yml
    ├── config.yml
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
  clearplot: 'clearplot|limpador'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____ _
#  _   _ / ___| | __ _ _ __  ___
# | | | | |   | |/ _` | '_ \/ __|
# | |_| | |___| | (_| | | | \__ \
#  \__, |\____|_|\__,_|_| |_|___/
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

# Limite de limpezas por vez
# Ideal para não lagar seu servidor
limit: 10

# Opções gerais do plugin
general:
  # Precisar de shift para ativar o limpador
  need-shift: true
  # Abrir o menu de confirmação
  open-menu: true
  # Utilizar o WorldEdit
  worldedit: false
  # Limpar de forma instantânea
  # Pode gerar LAG
  instant: false
  # Ativar para apenas o dono da plot conseguir limpar
  just-owner: true
  # Mundos que não será possível usar o limpador
  world-blacklist: []
  # Blocos que não serão limpos
  block-blacklist: ['RAW_NAME:0']
  # Comandos bloqueados para o jogador que está limpando a plot
  command-blacklist:
    - '/p'
    - '/plot'

hologram:
  enabled: true
  off-set: 2.0
  lines:
    - '&a&lLIMPADOR'
    - '&eRealizando limpeza...'
    - ''
    - '&fBlocos: &a{min}&7/&c{max}'
    - '&8[{progressbar}&8] &7{percentage}'

# Item da limpeza
item:
  material: 'DIAMOND_SPADE'
  name: '&aLimpador'
  lore:
    - '&7Use este item no seu plot para'
    - '&7limpá-lo por completo.'
    - ''
    - '&7Clique com botão direito para ativar.'

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'
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

# Menu de confirmação
confirm:
  name: '&8Limpador'
  size: 27
  items:
    confirm-slot: 11
    cancel-slot: 15
    confirm:
      material: 'e9e4bdcf172d5dc77c2bd4e37ad985399a9f2cdebf72463929ea4b666ef6f80'
      name: '&aConfirmar'
      lore: [ '&7Clique para limpar seu terreno.' ]
    cancel:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cCancelar'
      lore: [ '&7Clique para cancelar.' ]
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

actionbar:
  clearing: '&a&lLIMPADOR: &eStatus -> &8[{progressbar}&8] &7{percentage}'
  finished: '&a&lLIMPADOR: &eLimpeza concluída.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &aClearPlot comandos:

    &a> /clearplot give
    &a> /clearplot reload

  clearplot-give: '&aVocê deu &7{amount}x Limpador de Plot&a para o jogador &7{player}&a.'
  clearplot-give-all: |

    &bO usuário &f{player}&b deu &f{amount}x Limpador de Plot&bpara todos os jogadores online&b.

  clearplot-received: '&aVocê recebeu &7{amount}x Limpador de Plot&a.'
  clearplot-finished: |

    &a&lLIMPADOR: &eLimpeza concluída.

  clearplot-activated: '&a&lLIMPADOR: &eIniciando limpeza...'
  clearplot-confirm: |

    &a&lLIMPADOR: &eUtilize &ashift + botão direito&e para confirmar o uso do limpador.

  limit-reached: '&cTodos os {limit} pedreiros estão trabalhando. Aguarde para limpar seu terreno.'
  world-blacklisted: '&cVocê não pode usar isto neste mundo.'
  plot-permission: '&cVocê não tem permissão neste terreno.'
  already: '&cVocê já está limpando um terreno.'
  already-plot: '&cEste plot já está sendo limpo.'
  command-block: '&cVocê deve aguardar seu plot ficar limpo.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/113-yClearPlot">Site do plugin yClearPlot</a>
    </category>
</seealso>