# yLeilao
<secondary-label ref="management"/>

### Descrição
Permita que os jogadores anuncie itens em formato de leilão com lances

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
<video src="//www.youtube.com/watch?v=MD9POR-1iTc"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/leilao&nbsp;- Abre o menu principal
/leilao setnpc&nbsp;- Setar o NPC
/leilao delnpc&nbsp;- Deletar o NPC
/leilao reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yleilao.use - Permissão para o /leilao
yleilao.announce - Permissão para enviar a mensagem de anúncio no chat ao leiloar
yleilao.auction_limit.[numero] - Permissão para ter um limite customizado de leilões simultâneos
yleilao.reload - Permissão para o /leilao reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLeilao/
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
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
  auction: 'auction|leilao'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _         _ _
#  _   _| |    ___(_) | __ _  ___
# | | | | |   / _ \ | |/ _` |/ _ \
# | |_| | |__|  __/ | | (_| | (_) |
#  \__, |_____\___|_|_|\__,_|\___/
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

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Sistemas gerais do plugin
general:
  # Tempo padrão para começar o leilão
  default-time: 1800
  # Quantia máxima de leilões simultâneos que o servidor pode ter
  # deixe 0 para ser infinito
  max-auctions: 10
  # Quantia máxima de leilões simultâneos que o jogador pode fazer
  # deixe 0 para ser infinito
  player-max-auctions: 1
  # Taxa que o leiloador irá pagar sobre o lance vencedor
  # em porcentagem
  auction-tax: 10.0
  # Tempo que irá acrescentar quando um lance maior que um já existente for computado
  # em segundos
  bid-sum-time: 30
  # Tempo mínimo para iniciar um leilão
  # em segundos
  min-time: 900
  # Tempo máximo para iniciar um leilão
  # em segundos
  max-time: 21600

# Sistema de blacklist
black-list:
  # Materiais que estarão na black-list
  materials: [ 'STONE', 'LOG:0' ]
  # NBTTags que estarão na black-list
  nbt-tags: []

# Sistema de whitelist
white-list:
  # Ativar a whitelist
  enabled: false
  # Materiais que estarão na white-list
  materials: [ 'LOG:1', 'TRIPWIRE_HOOK' ]

# Sistema de npc
npc:
  skin: 'Pitombaa'
  hologram:
    offset: 3.4
    hologram:
      - '&6&lLEILÃO'
      - '&7Faça o comércio rápido dos itens!'
      - '[item]EMERALD'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
version: '1.0.0'
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

# Economia padrão que irá vir na placa
# Deixe '' (vazio) para não usar
default: 'money'

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
    permission: 'yleilao.provider.money'
    # ‘Item’ que aparecerá no menu de seleção de economias
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ''
        - '&aClique para alterar'
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

# Ativar o sistema de atualizar o menu principal automaticamente enquanto estiver aberto
menu-updater: true
# Tempo para atualizar o menu automaticamente
# em ticks -> 20 ticks = 1s
menu-updater-time: 200

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
  name: '&8Leilão'
  size: 27
  items:
    center-slot: 10
    bids-slot: 12
    auctions-slot: 14
    courier-slot: 16
    center:
      material: 'GOLD_BLOCK'
      name: '&eCentral de leilões'
      lore:
        - '&7Aqui você pode encontrar os'
        - '&7itens que estão sendo leiloados'
        - '&7pelos jogadores do servidor.'
        - ''
        - '&7Caso você consiga ter maior'
        - '&7lance até o fim do leilão de um'
        - '&7item, ele será seu.'
        - ''
        - '&eClique para ver os leilões.'
    bids:
      material: 'GOLDEN_CARROT'
      name: '&eMeus lances'
      lore:
        - '&7Você possui &f{amount}'
        - '&7lance(s) no momento. :)'
        - ''
        - '&eClique para ver seus lances.'
    bids-none:
      material: 'GOLDEN_CARROT'
      name: '&eMeus lances'
      lore:
        - '&7Você não possui nenhum'
        - '&7lance no momento. :('
    auctions:
      material: 'GOLD_BARDING'
      name: '&eMeus leilões'
      lore:
        - '&7Anuncie seus itens na casa de'
        - '&7leilões para que outros jogadores'
        - '&7possam comprá-los.'
        - ''
        - '&eClique para leiloar.'
    courier:
      material: 'CHEST'
      name: '&eMeu correio'
      lore:
        - '&7Colete aqui suas compras, leilões'
        - '&7cancelados ou expirados e valores'
        - '&7de lances não efetivados.'
        - ''
        - '&eClique para acessar.'

# Menu de correio
courier:
  name: '&8Leilão'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 47
  #
  empty-slot: 22
  currencies-slot: 49
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVazio...'
      lore: [ '&7Você não tem nenhum lance ativo!' ]
    currencies-none:
      material: 'GOLD_INGOT'
      name: '&cValores'
      lore: [ '&7Você não tem nenhum valor para coletar!' ]
    currencies:
      material: 'GOLD_INGOT'
      name: '&eValores'
      lore:
        - '&r'
        - ' &eValores a receber:'
        - ' {format}'
        - ''
        - '&eClique para coletar os valores.'
  formats:
    currency: ' &7> &f{amount} {provider_abbreviated}'

# Menu de lances
bids:
  name: '&8Leilão'
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
      name: '&cVazio...'
      lore: [ '&7Você não tem nenhum lance ativo!' ]
  lore:
    - '&f'
    - ' &fLeiloador: &7{owner}'
    - ''
    - ' {format}'
    - ''
    - '&8> &fTermina em: &7{time}'
    - '&8> &fSeu lance: &6{amount} {provider_abbreviated}'
    - ''
    - '&eClique para aumentar o seu lance.'
  formats:
    bid: ' &7> {pos}º {player}: &f{amount} {provider_abbreviated}'
    none: ' &cNenhum lance até o momento'
    has: ' &eMaiores lances:<nl>{formats}'

# Menu de leilões
auctions:
  name: '&8Leilão'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  #
  empty-slot: 22
  filter-slot: 50
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVazio...'
      lore: [ '&7Não há nenhum leilão ocorrendo!' ]
    filter:
      material: HOPPER
      name: '&aFiltro'
  lore:
    - '&r'
    - ' &fLeiloador: &7{owner}'
    - ''
    - ' {format}'
    - ''
    - '&8> &fTermina em: &7{time}'
    - '&8> &fLance inicial: &6{amount} {provider_abbreviated}'
    - ''
    - '&eClique para dar um lance.'
  lore-has:
    - '&r'
    - ' &fLeiloador: &7{owner}'
    - ''
    - ' {format}'
    - ''
    - '&8> &fTermina em: &7{time}'
    - '&8> &fLance inicial: &6{amount} {provider_abbreviated}'
    - ''
    - '&eClique para aumentar seu lance.'
  formats:
    bid: ' &7> {pos}º {player}: &f{amount} {provider_abbreviated}'
    none: ' &cNenhum lance até o momento'
    has: ' &eMaiores lances:<nl>{formats}'
  filter:
    types:
      oldest: 'Menor tempo restante'
      newest: 'Maior tempo restante'
    format:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de lances
my-auctions:
  name: '&8Leilão'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  previous-slot: 9
  next-slot: 17
  back-slot: 27
  #
  empty-slot: 13
  create-slot: 31
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVazio...'
      lore: [ '&7Você não tem nenhum leilão ativo!' ]
    create:
      material: '2ddcfe7d91cd80b364cc060160a0699386d096e0e5adf98e8e45e0a198631d8f'
      name: '&aIniciar um leilão'
      lore: [ '&7Faça um leilão do seu item para', '&7ver quem paga mais por ele.', '', '&aClique para iniciar.' ]
  lore:
    - '&f'
    - '{format}'
    - ''
    - '&8> &fTermina em: &7{time}'
    - '&8> &fLance inicial: &6{amount} {provider_abbreviated}'
    - ''
    - '&eClique para remover o leilão.'
  formats:
    bid: ' &7> {pos}º {player}: &f{amount} {provider_abbreviated}'
    none: ' &cNenhum lance até o momento'
    has: ' &eMaiores lances:<nl>{formats}'

# Menu de criação
create:
  name: '&8Leilão'
  size: 45
  back-slot: 0
  items:
    item-slot: 13
    confirm-slot: 28
    provider-slot: 30
    start-bid-slot: 32
    duration-slot: 34
    item:
      material: 'BARRIER'
      name: '&eClique em algum item do seu inventário'
      lore:
        - '&7Selecione algum item para leiloar.'
    confirm:
      material: 'STAINED_CLAY:5'
      name: '&aIniciar leilão'
      lore:
        - '&7Esse item será leiloado para'
        - '&7outros jogadores comprarem.'
        - ''
        - '&8> &fItem: &7{item}'
        - '&8> &fDuração: &6{time}'
        - '&8> &fLance inicial: &6{amount} {provider_abbreviated}'
        - ''
    confirm-cant:
      material: 'STAINED_CLAY:14'
      name: '&cIniciar leilão'
      lore:
        - '&7Selecione um item do seu inventário'
        - '&7para iniciar este leilão.'
    provider:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aMoeda do leilão'
      lore:
        - '&7Moeda que será utilizada no leilão'
        - '&7deste item.'
        - ''
        - '&7Atual: &fNenhuma'
        - ''
        - '&aClique para alterar a moeda'
    start-bid:
      material: 'GOLD_INGOT'
      name: '&6Lance inicial'
      lore:
        - '&7Defina o valor mínimo que um jogador'
        - '&7pode oferecer pelo seu item.'
        - ''
        - '&7Lance inicial: &f{amount} {provider_abbreviated}'
        - ''
        - '&eClique para modificar.'
    duration:
      material: 'WATCH'
      name: '&aDuração customizada'
      lore:
        - '&7Defina um tempo específico'
        - '&7para a duração do seu leilão.'
        - ''
        - '&fDuração: &6{time}'
        - ''
        - '&eClique para modificar.'

# Menu de seleção de economias
providers:
  name: '&8Selecionar economia'
  size: 27
  previous: 9
  next: 17
  back: 18
  slots: [ 11, 12, 13, 14, 15 ]

# Menu de seleção de duração
durations:
  name: '&8Selecionar duração'
  size: 36
  previous: 9
  next: 17
  back: 27
  slots: [ 11, 12, 13, 14, 15 ]
  items:
    select-slot: 31
    select:
      material: 'WATCH'
      name: '&aDuração customizada'
      lore:
        - '&7Defina um tempo específico'
        - '&7para a duração do seu leilão.'
        - ''
        - '&eClique para definir.'
    15min:
      material: 'PAPER'
      name: '&a15m'
      nbt-tag: [ 'yLeilao-Duration=>900' ]
    30min:
      material: 'PAPER'
      name: '&a30m'
      nbt-tag: [ 'yLeilao-Duration=>1800' ]
    1hour:
      material: 'PAPER'
      name: '&a1h'
      nbt-tag: [ 'yLeilao-Duration=>3600' ]
    2hour:
      material: 'PAPER'
      name: '&a2h'
      nbt-tag: [ 'yLeilao-Duration=>7200' ]
    3hour:
      material: 'PAPER'
      name: '&a3h'
      nbt-tag: [ 'yLeilao-Duration=>10800' ]
    4hour:
      material: 'PAPER'
      name: '&a4h'
      nbt-tag: [ 'yLeilao-Duration=>14400' ]
    5hour:
      material: 'PAPER'
      name: '&a5h'
      nbt-tag: [ 'yLeilao-Duration=>18000' ]
    6hour:
      material: 'PAPER'
      name: '&a6h'
      nbt-tag: [ 'yLeilao-Duration=>21600' ]
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

    &a/leilao &8- &7Abre o menu principal.
    &a/leilao setnpc &8- &7Setar o NPC.
    &a/leilao delnpc &8- &7Deletar o NPC.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  provider-permission: '&cVocê não tem permissão para leiloar com esta economia.'
  start-bid: '&aLance inicial alterado para &f{amount}&a.'
  start-bid-digit: |

    &aDigite o preço mínimo que você quer leiloar o item.
    &7para cancelar digite &ncancelar&7.

  time-digit: |

    &aDigite o tempo que você deseja.
    &7para cancelar digite &ncancelar&7.

  bid-digit: |

    &aDigite o lance que você quer dar no item.
    &7para cancelar digite &ncancelar&7.

  bid-high: |

    &cOPS! Parece que alguém, deu um lance maior que o seu em um leilão que você estava participando, porém foi adicionado &f{time}&c no leilão para você tentar recuperar seu lugar.

  auction-cancelled: |

    &cOPS! Um leilão no qual você participava foi cancelado pelo leiloador, o seu lance foi devolvido.

  auction-winner: |

    &cOPS! Um leilão no qual você participava foi arrematado pelo jogador &f{player}&c.

  auction-win: |

    &aOPA! Um leilão no qual você participava foi arrematado.

  auction-new: |

    &6&l[Leilão]&e O jogador &f{player}&e adicionou um novo item no leilão.

  max-auctions: '&cA casa de leilões já está com seu limite máximo simultâneo ({max}).'
  player-max-auctions: '&cVocê já está com seu limite máximo simultâneo ({max}).'
  start-auction: '&aVocê iniciou um novo leilão.'
  cancel-auction: '&aVocê cancelou o leilão.'
  no-balance: '&cVocê não tem {amount} {provider_abbreviated} suficiente para isto. Disponível: {provider_balance}&c.'
  bid-minimum: '&cO seu lance deve ser no mínimo {amount} {provider_abbreviated}.'
  bid-updated: '&aO seu lance foi atualizado para {amount} {provider_abbreviated}.'
  bid-success: '&aO seu lance foi dado em {amount} {provider_abbreviated}.'
  inv-full: '&cO seu inventário está cheio.'
  courier-collected-item: '&aVocê coletou um item do seu correio do leilão.'
  courier-collected-currencies: '&aVocê coletou os valores a receber.'
  cant-auction: '&cEste item não pode ser leiloado.'
  currency-found: '&cConfigure a moeda do leilão.'
  time-found: '&cVocê precisa definir um tempo entre {min} e {max} para iniciar um leilão.'
  npc-set: '&aNPC setado com sucesso.'
  npc-deleted: '&aNPC removido com sucesso.'
  npc-not-set: '&cNPC não está definido.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/144-yLeilao">Site do plugin yLeilao</a>
    </category>
</seealso>