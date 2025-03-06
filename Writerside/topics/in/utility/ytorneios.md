# yTorneios
<secondary-label ref="utility"/>

### Descrição
Incentive a competição dentro do teu servidor

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
<video src="//www.youtube.com/watch?v=KM_O6BPspHs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/torneios&nbsp;- Abre o menu principal
/torneios help&nbsp;- Envia a mensagem de ajuda
/torneios start&nbsp;- Inicia um torneio
/torneios stop&nbsp;- Para um torneio
/torneios cancel&nbsp;- Cancela um torneio
/torneios&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytorneios.use - Permissão para o /torneios
ytorneios.start - Permissão para o /torneios start
ytorneios.stop - Permissão para o /torneios stop
ytorneios.cancel - Permissão para o /torneios cancel
ytorneios.admin.reload - Permissão para o /torneios reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTorneios/
    ├── tournaments/
    │    └── yminaspackets.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="tournaments" collapsible="true">
<chapter title="yminaspackets.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Tipos disponíveis:
# yMinas (quebrar blocos)
# yMinasPackets (quebrar blocos)
# yPlantacoes (quebrar plantacoes)
# yFloresta (quebrar blocos)
# yCampo (quebrar plantações)
# yPesca (pescar peixes)
# yBosses (matar bosses)
# yStackBosses (matar bosses)
# yRankup (upar de rank)
# ySpawners (matar mobs)
# yEventos (ganhar eventos)
event-type: 'yMinasPackets'

# Sistemas gerais
general:
  # Horários que o evento irá ativar
  # todos, segunda, terca, quarta, quinta, sexta, sabado, domingo
  # dia-hora-minuto-segundo;duração
  # duração = Duração do evento (em segundos)
  auto-start:
    - 'todos-12:00:00,60'
  # Segundos em que os anúncios irão aparecer
  announces: [ 50, 40, 30, 20, 10 ]
  # chance,recompensa
  rewards: [ '100,reward1' ]

# Sistema de comprar a ativação do torneio
buy:
  # Ativar o sistema
  enabled: true
  # Duração que irá ativar ao comprar
  # em segundos
  duration: 60
  # Mensagem de compra
  message:
    private: '&aVocê ativou o torneio por &f{money}&a.'
    broadcast: ''
  # Preços para comprar
  prices:
    price1:
      provider: 'money'
      amount: 1000.0

# Ícones no menu
icons:
  buy:
    material: 'LAPIS_ORE'
    name: '&eTorneio de Mineração &7(yMinasPackets)'
    lore:
      - '&7Neste torneio, o jogador que conseguir'
      - '&7minerar mais blocos irá ganhar uma'
      - '&7recompensa misteriosa.'
      - ''
      - ' &fPreço para ativar: &2$ &a{money} coins'
      - ''
      - '&aClique para ativar'
  running:
    material: 'LAPIS_ORE'
    name: '&eTorneio de Mineração &7(yMinasPackets)'
    lore:
      - '&7Neste torneio, o jogador que conseguir'
      - '&7minerar mais blocos irá ganhar uma'
      - '&7recompensa misteriosa.'
      - ''
      - '&f 1º {player_1}: &a{amount_1}'
      - '&f 2º {player_2}: &a{amount_2}'
      - '&f 3º {player_3}: &a{amount_3}'
      - '&f 4º {player_4}: &a{amount_4}'
      - '&f 5º {player_5}: &a{amount_5}'
      - ''

# Mensagens do torneio
messages:
  already: '&cO torneio já está rolando.'
  nothing: '&cO torneio não está rolando.'
  start: |

    &a&lMINERAÇÃO: &eO torneio começou!
    &bTempo restante: &a{time}

  cancel: |

    &a&lMINERAÇÃO: &eO torneio acabou!
    &cCANCELADO!

  stop: |

    &a&lMINERAÇÃO: &eO torneio acabou!
    &bGanhador: &a{player} com {amount} quebradas!

  stop-none: |

    &a&lMINERAÇÃO: &eO torneio acabou!
    &cNINGUÉM GANHOU!

  announce: |

    &a&lMINERAÇÃO: &eO torneio está rolando!
    &bTempo restante: &a{time}

    &f> 1# &6{player_1} &7- &e{amount_1}
    &f> 2# &6{player_2} &7- &e{amount_2}
    &f> 3# &6{player_3} &7- &e{amount_3}
    &f> 4# &6{player_4} &7- &e{amount_4}
    &f> 5# &6{player_5} &7- &e{amount_5}

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
  torneio: 'torneio|torneios|tournament|tournaments'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _____                     _
#  _   |_   _|__  _ __ _ __   ___(_) ___  ___
# | | | || |/ _ \| '__| '_ \ / _ \ |/ _ \/ __|
# | |_| || | (_) | |  | | | |  __/ | (_) \__ \
#  \__, ||_|\___/|_|  |_| |_|\___|_|\___/|___/
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

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

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
  Money:
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
    permission: 'ytorneios.provider.money'
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

# Menu de recompensas
main:
  name: '&8Torneios'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  previous-slot: 9
  next-slot: 18
  #
  rewards-slot: 31
  #
  items:
    rewards:
      material: 'CHEST'
      name: '&6Recompensas'
      lore:
        - '&7Gerencie as recompensas'
        - '&7que você ganhou.'
        - ''
        - ' &8▶ &fRecompensas: &7{rewards}'
        - ''
        - '&6Clique para gerenciar!'

# Menu de recompensas
main-rewards:
  name: '&8Torneios'
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

    &a/torneios &8- &7Abre o menu principal.
    &a/torneios start &8- &7Inicia um torneio.
    &a/torneios cancel &8- &7Cancela um torneio.
    &a/torneios stop &8- &7Para um torneio.

  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  tournament-null: |
    &cEste torneio não existe.
    &cDisponíveis: &7{list}
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
      lore: [ '&aEsta pedra vale muito dinheiro!', '', '&6Chance: {chance}%' ]
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
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', '&6Chance: {chance}%' ]
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
      lore: [ '&aEsmeraldas valem muito?', '', '&6Chance: {chance}%' ]
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/150-yTorneios">Site do plugin yTorneios</a>
    </category>
</seealso>