# yLixeiro
<secondary-label ref="management"/>

### Descrição
Plugin de lixeiro um pouco diferente.

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
<video src="//www.youtube.com/watch?v=fyYF8cAx2b8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/lixeiro - Ver informações da coleta anterior.
/lixeiro forcar&nbsp;- Força a coleta de entidades e itens.
/lixeiro historico&nbsp;- Abre o menu de histórico de itens limpos (3)
/lixeiro reload&nbsp;- Recarrega as configurações
/lixeira - Abre uma lixeira virtual.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ylixeiro.use - Permissão para o /lixeiro
ylixeiro.historic - Permissão para o /lixeiro historico
ylixeiro.force - Permissão para o /lixeiro forcar
ylixeiro.admin.reload - Permissão para o /lixeiro reload
ylixeiro.trash - Permissão para o /lixeira</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLixeiro/
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
  lixeiro: 'lixeiro'
  trash: 'trash|trashcan|lixeira|lixo'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         _     _          _
#  _   _| |   (_)_  _____(_)_ __ ___
# | | | | |   | \ \/ / _ \ | '__/ _ \
# | |_| | |___| |>  <  __/ | | | (_) |
#  \__, |_____|_/_/\_\___|_|_|  \___/
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

general:
  # Tempo para realizar a limpeza
  # em segundos
  time: 130
  # Limpar itens
  items: true
  # Limpar entidades
  entities: true
  # Não limpar entidades renomeadas
  blacklist-renamed: false
  # Não limpar entidades do AuraMobs
  blacklist-auramobs: false
  # Mundos que não serão limpos
  world-blacklist: []
  # Blacklist de items para não serem removidos
  items-blacklist:
    - 'BARRIER'
    - 'BEDROCK:0'
  # Blacklist de items que não serão limpar (com certa nbt-tag)
  items-nbt-tag-blacklist: []
  # Blacklist de entidades que não serão limpar
  entities-blacklist:
    - 'ARMOR_STAND'
    - 'ENDER_CRYSTAL'
    - 'FISHING_HOOK'
    - 'FALLING_BLOCK'
    - 'FIREBALL'
    - 'FIREWORK'
    - 'ITEM_FRAME'
    - 'LEASH_HITCH'
    - 'LIGHTNING'
    - 'PAINTING'
    - 'PRIMED_TNT'
    - 'SMALL_FIREBALL'
    - 'SPLASH_POTION'
    - 'THROWN_EXP_BOTTLE'
    - 'WEATHER'
  # Blacklist de entidades que não serão limpas (com certa nbt-tag)
  entities-nbt-tag-blacklist:
    - 'ySpawnersV2-Type'
    - 'yBossArena-Type'
    - 'yStackBosses-Type'
  # Blacklist de entidades que não serão limpas (com certa metadata)
  metadata-blacklist:
    - 'ySpawners-MobStacked'
    - 'ySpawnersV2-MobStacked'

# Limitador de entidades por Chunk
chunk-limiter:
  # Ativar o sistema
  enabled: false
  # Entidades que serão limitadas
  whitelist:
    - 'COW:10'

# Configuração dos sons
sounds:
  # Som que será enviado ao executar o /lixeiro
  command: 'NOTE_PLING'
  # Volume dos sons
  volume: 20
  # Volume de expansão dos sons
  pitch: 20
  # Sons que serão enviados a cada x tempo
  timer:
    - '120,NOTE_STICKS'
    - '60,NOTE_STICKS'
    - '30,NOTE_STICKS'
    - '10,NOTE_STICKS'
    - '5,NOTE_STICKS'
    - '4,NOTE_STICKS'
    - '3,NOTE_STICKS'
    - '2,NOTE_STICKS'
    - '1,NOTE_STICKS'
    - '0,NOTE_PLING'

# Configurações das mensagens temporizadas
message-timer:
  # Mensagem que irá ser enviada no chat
  # Utilize <nl> para uma nova linha (Mini-Messages permitido)
  chat:
    - '120, &eTodos os itens no chão serão removidos em 2 minutos!<nl> &8♻ &fPara visualizar o tempo, digite &7/lixeiro&f.'
    - '60, &eTodos os itens no chão serão removidos em 1 minuto!<nl> &8♻ &fPara visualizar o tempo, digite &7/lixeiro&f.'
    - '10, &eTodos os itens no chão serão removidos em 10 segundos!'
    - '5, &eTodos os itens no chão serão removidos em 5 segundos!'
    - '4, &eTodos os itens no chão serão removidos em 4 segundos!'
    - '3, &eTodos os itens no chão serão removidos em 3 segundos!'
    - '2, &eTodos os itens no chão serão removidos em 2 segundos!'
    - '1, &eTodos os itens no chão serão removidos em 1 segundo!'
    - '0, &eForam removidos &e&l{total}&e itens do chão!'
  # Mensagem que irá ser enviada no actionbar
  actionbar:
    - '120, &eTodos os itens no chão serão removidos em 2 minutos!'
    - '60, &eTodos os itens no chão serão removidos em 1 minuto!'
    - '30, &eTodos os itens no chão serão removidos em 30 segundos!'
    - '10, &eTodos os itens no chão serão removidos em 10 segundos!'
    - '5, &eTodos os itens no chão serão removidos em 5 segundos!'
    - '4, &eTodos os itens no chão serão removidos em 4 segundos!'
    - '3, &eTodos os itens no chão serão removidos em 3 segundos!'
    - '2, &eTodos os itens no chão serão removidos em 2 segundos!'
    - '1, &eTodos os itens no chão serão removidos em 1 segundo!'
    - '0, &eForam removidos &e&l{total}&e itens do chão!'
  # Titles que serão enviados a cada x segundos
  # Utilize <nl> para uma nova linha
  title:
    - '30,&eLixeiro<nl>&7Limpando em 30 segundos.'
    - '10,&eLixeiro<nl>&7Limpando em 10 segundos.'
    - '0,&eLixeiro<nl>&7{total} itens limpos.'
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
  name: '&8Lixeiro'
  size: 27
  slots: [ 11, 13, 15 ]
  previous-slot: 9
  next-slot: 17
  items:
    historic:
      material: 'PAPER'
      name: '&eHistórico de Limpeza &8[{index}]'
      lore: [ '&7Veja os itens que foram limpos', '&7nesta limpeza.', '', '&aClique para acessar.' ]
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
  inv-full: '&cO seu inventário está cheio.'
  help: |

    &aLixeiro comandos:

    &a> /lixeiro
    &a> /lixeiro forcar
    &a> /lixeiro reload

  force: '&aVocê forçou a limpeza de itens e entidades.'
  next: '&r &eTempo para a próxima limpeza: {time}.<nl>&r &8♻ &fNa última limpeza foram limpos &7{items_total}&f itens e &7{entities_total}&f entidades.'
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/45-yLixeiro">Site do plugin yLixeiro</a>
    </category>
</seealso>