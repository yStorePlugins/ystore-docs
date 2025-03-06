# yDominarArena
<secondary-label ref="utility"/>

### Descrição
Crie eventos de dominação no seu servidor

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
<video src="//www.youtube.com/watch?v=a3HXslZWCsQ"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/dominararena - Abre o menu principal
/dominararena armazem - Abre o menu de recompensas
/dominararena top - Abre o menu de top
/dominararena criar - Cria uma nova arena
/dominararena deletar - Deletar uma arena
/dominararena iniciar - Iniciar uma dominação
/dominararena parar - Parar uma dominação=
/dominararena alterarloc - Altera o centro de uma arena
/dominararena reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ydominararena.use - Permissão para o /dominararena, /dominararena top, /dominararena armazem
ydominararena.create - Permissão para o /dominararena criar
ydominararena.delete - Permissão para o /dominararena deletar
ydominararena.start - Permissão para o /dominararena iniciar
ydominararena.stop - Permissão para o /dominararena parar
ydominararena.changeloc - Permissão para o /dominararena alterarloc
ydominararena.reload - Permissão para o /dominararena reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yDominarArena/
    ├── commands.yml
    ├── config.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
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
  arena: 'dominararena'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____  _             _    ____
#  _   _/ ___|| |_ __ _  ___| | _| __ )  ___  ___ ___  ___  ___
# | | | \___ \| __/ _` |/ __| |/ /  _ \ / _ \/ __/ __|/ _ \/ __|
# | |_| |___) | || (_| | (__|   <| |_) | (_) \__ \__ \  __/\__ \
#  \__, |____/ \__\__,_|\___|_|\_\____/ \___/|___/___/\___||___/
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

# Task de atualização da arena
# Partículas e status
# em ticks
update-period: 3

# Enviar a mensagem de dominância global a cada x tempo
# em segundos
message-time: 60

# Começar a dominar apenas depois de uma batalha
first-battle: false

# Ativar as partículas
particles: true
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
  name: '&8Dominação'
  size: 27
  items:
    rewards-slot: 12
    top-slot: 15
    rewards:
      material: 'CHEST'
      name: '&aRecompensas'
      lore:
        - ''
        - ' &fRecompensas no armazém: &a{rewards}&f.'
        - ''
        - '&7Clique para gerenciar'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Clans'
      lore:
        - '&7Clique para ver os melhores'
        - '&7clans em relação às dominações.'

# Menu de recompensas
main-rewards:
  name: '&8Dominação'
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

# Menu de arenas
arenas:
  name: '&8Dominação'
  size: 36
  slots: [ 12, 13, 14, 15, 16 ]
  previous-slot: 10
  next-slot: 18
  back-slot: 31
  #
  item-name: '{arena}'
  lore:
    - ''
    - '&fArena: {arena}'
    - ''
    - '&aClique para ver o TOP.'

# Menu de top
top:
  name: '&8Dominação'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 31
  previous-slot: 9
  next-slot: 17
  items:
    # Item do top dominações
    dominations:
      material: '{banner}'
      name: '&7[{clan_color_tag}&7] &f{clan_name}'
      lore:
        - ''
        - '&fDominações: &7{amount}'
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

    &aDominar arena comandos:

    &a> /dominararena
    &a> /dominararena armazem
    &a> /dominararena top
    &a> /dominararena iniciar
    &a> /dominararena parar
    &a> /dominararena criar
    &a> /dominararena deletar
    &a> /dominararena alterarloc

  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  arena-found: '&cArena não encontrada.<nl>&cDisponíveis: &7{list}'
  arena-active: '&cEsta arena {arena} não está ativa.'
  arena-already: '&cEsta arena {arena} já está ativa.'
  arena-exists: '&cEsta arena {arena} já existe.'
  arena-stop: '&cArena {arena} parada com sucesso.'
  arena-start: '&aArena {arena} foi iniciada com sucesso.'
  arena-created: '&aArena {arena} foi criada com sucesso.'
  arena-deleted: '&aArena {arena} foi deletada com sucesso.'
  arena-changed: '&aA localização da arena {arena} foi alterada com sucesso.'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/116-yDominarArena">Site do plugin yDominarArena</a>
    </category>
</seealso>