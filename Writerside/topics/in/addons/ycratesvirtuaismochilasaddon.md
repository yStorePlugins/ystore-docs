# yCratesVirtuaisMochilasAddon
<secondary-label ref="addons"/>

### Descrição
Uma nova forma de armazenar e interagir com as keys!

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
<video src="//www.youtube.com/watch?v=MKeYx3S37Ik"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/cratebackpack&nbsp;- Envia a mensagem de ajuda
/cratebackpack give&nbsp;- Dá mochila para um jogador
/cratebackpack giveautomatic&nbsp;- Dá abridor automático para um jogador
/cratebackpack&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycratesvirtuaismochilasaddon.use - Permissão para o /cratebackpack
ycratesvirtuaismochilasaddon.give - Permissão para o /cratebackpack give
ycratesvirtuaismochilasaddon.giveautomatic - Permissão para o /cratebackpack giveautomatic
ycratesvirtuaismochilasaddon.admin.reload - Permissão para o /cratebackpack reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCratesVirtuaisMochilasAddon/
    ├── commands.yml
    ├── config.yml
    ├── crates.yml
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
  cratebackpack: 'cratebackpack|cratemochila'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____           _          __     ___      _               _     __  __            _     _ _              _       _     _
#  _   _ / ___|_ __ __ _| |_ ___  __\ \   / (_)_ __| |_ _   _  __ _(_)___|  \/  | ___   ___| |__ (_) | __ _ ___   / \   __| | __| | ___  _ __
# | | | | |   | '__/ _` | __/ _ \/ __\ \ / /| | '__| __| | | |/ _` | / __| |\/| |/ _ \ / __| '_ \| | |/ _` / __| / _ \ / _` |/ _` |/ _ \| '_ \
# | |_| | |___| | | (_| | ||  __/\__ \\ V / | | |  | |_| |_| | (_| | \__ \ |  | | (_) | (__| | | | | | (_| \__ \/ ___ \ (_| | (_| | (_) | | | |
#  \__, |\____|_|  \__,_|\__\___||___/ \_/  |_|_|   \__|\__,_|\__,_|_|___/_|  |_|\___/ \___|_| |_|_|_|\__,_|___/_/   \_\__,_|\__,_|\___/|_| |_|
#  |___/
#

general:
  # Delay de abertura automática
  # em segundos
  automatic-delay: 10

# Sistema de upgrade
upgrades:
  storage-limit:
    # Máximo de limite de keys
    maximum: 4000
    # Limite de keys armazenadas por padrão
    default: 500
    # Quantidade que será acrescida a cada upgrade
    per-upgrade-add: 500
    prices-per-upgrade:
      price1:
        provider: 'money'
        amount: 200.0
  open-limit:
    # Máximo de quantidade de abertura de keys por vez
    maximum: 100
    # Quantidade padrão de abertura de keys por vez
    default: 10
    # Quantidade que será acrescida a cada upgrade
    per-upgrade-add: 10
    prices-per-upgrade:
      price1:
        provider: 'money'
        amount: 200.0

# Item da mochila
backpack:
  material: 'ENDER_CHEST'
  name: '&6Mochila de Chaves'
  lore:
    - '&7Esta mochila armazena todas'
    - '&7as chaves recebidas.'
    - ''
    - ' &6Armazenamento:'
    - ' &7{actual}/{total} {progressbar} &8{percentage}'
    - ''
    - '&6Clique para acessar.'

# Item do abridor automático
automatic:
  material: 'STONE_BUTTON'
  name: '&dAbertura automática'
  lore:
    - '&7Utilize este item para'
    - '&7ativar a abertura das chaves'
    - '&7de forma automática.'
    - ''
    - '&7Arraste em uma mochila.'

# Configuração da progressbar
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-not: '&7'
]]>
</code-block>
</chapter>

<chapter title="crates.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
crates:
  vip:
    # Identificador da key no yCratesVirtuais
    ycratesvirtuais-key: 'vip'
    # Ícone no menu
    menu:
      material: 'TRIPWIRE_HOOK'
      name: '&6Chave VIP'
      lore: [ '', '&fQuantidade: &7{amount}', '', '&aClique para recolher.' ]
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
    permission: 'ycratesvirtuaismochilasaddon.provider.money'
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
menu-updater-time: 20

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
  name: '&8Mochila de Chaves'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 21, 22, 23 ]
  previous-slot: 18
  next-slot: 26
  items:
    automatic-slot: 38
    upgrade-open-slot: 39
    upgrade-storage-slot: 40
    store-slot: 42
    automatic-has:
      material: '1c8e0ddf2432f4332b87691b5952c7679763ef4f275b874e9bceb888ed5b5b9'
      name: '&cAbertura automática'
      lore:
        - '&7A mochila consegue abrir'
        - '&7suas chaves automaticamente!'
        - ''
        - ' &8> &fPeríodo: &7{time}'
        - ''
        - ' &7Adquira este item:'
        - ' &fystoreplugins.com.br'
        - ''
    automatic:
      material: '1391203d3752afc71d8f8cb0da8dbc7f13a3baafe0bf5f911cb21c38341f87db'
      name: '&aAbertura automática'
      lore:
        - '&7A mochila consegue abrir'
        - '&7suas chaves automaticamente!'
        - ''
        - ' &8> &fPeríodo: &7{time}'
        - ' &8> &fStatus: &7{status}'
        - ''
        - '&aClique para alternar.'
    upgrade-open:
      material: '4ce36fcb1e5f6b36517fbbeb9cbf4b0c05c30d8bdb5154824e60e6d550f528e9'
      name: '&aQuantidade de abertura'
      lore:
        - '&7Evolua a quantidade que'
        - '&7sua mochila consegue abrir'
        - '&7chaves por vez.'
        - ''
        - ' &aAtual:'
        - ' &8> &fQuantidade: &7{actual}'
        - ''
        - ' &aEvolução:'
        - ' &8> &fPreço: &2$&f{money}'
        - ' &8> &fQuantidade: &7{next}'
        - ''
        - '&aClique para evoluir.'
    upgrade-open-max:
      material: '4ce36fcb1e5f6b36517fbbeb9cbf4b0c05c30d8bdb5154824e60e6d550f528e9'
      name: '&aQuantidade de abertura'
      lore:
        - '&7Evolua a quantidade que'
        - '&7sua mochila consegue abrir'
        - '&7chaves por vez.'
        - ''
        - ' &aAtual:'
        - ' &8> &fQuantidade: &7{actual}'
        - ''
        - '&cEsta mochila já está no upgrade máximo.'
    upgrade-storage:
      material: '4ce36fcb1e5f6b36517fbbeb9cbf4b0c05c30d8bdb5154824e60e6d550f528e9'
      name: '&aQuantidade de armazenamento'
      lore:
        - '&7Evolua a quantidade que'
        - '&7sua mochila consegue armazenar'
        - '&7de chaves.'
        - ''
        - ' &aAtual:'
        - ' &8> &fQuantidade: &7{actual}'
        - ''
        - ' &aEvolução:'
        - ' &8> &fPreço: &2$&f{money}'
        - ' &8> &fQuantidade: &7{next}'
        - ''
        - '&aClique para evoluir.'
    upgrade-storage-max:
      material: '4ce36fcb1e5f6b36517fbbeb9cbf4b0c05c30d8bdb5154824e60e6d550f528e9'
      name: '&aQuantidade de armazenamento'
      lore:
        - '&7Evolua a quantidade que'
        - '&7sua mochila consegue armazenar'
        - '&7de chaves.'
        - ''
        - ' &aAtual:'
        - ' &8> &fQuantidade: &7{actual}'
        - ''
        - '&cEsta mochila já está no upgrade máximo.'
    store:
      material: 'ef221b33f5b39e99ee6fd343abaaa9abdf66d93d4306cf01cca9f202e8773fd6'
      name: '&dGuardar chaves'
      lore:
        - '&7Clique para guardar todas'
        - '&7as chaves disponíveis em'
        - '&7seu inventário.'
  facing:
    e0:
      slot: 11
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e1:
      slot: 12
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e2:
      slot: 13
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e3:
      slot: 14
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e4:
      slot: 15
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e5:
      slot: 21
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e6:
      slot: 22
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e7:
      slot: 23
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
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

    &aCrate Mochilas comandos:

    &a> /cratebackpack
    &a> /cratebackpack give <player> <automatico:[sim/nao]>
    &a> /cratebackpack giveautomatic <player> <quantia>

  inv-full: '&cSeu inventário está cheio.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  backpack-give: '&aVocê deu &61x Mochila de Chaves&a para o jogador &7{player}&a.'
  backpack-received: '&aVocê recebeu &61x Mochila de Chaves&a.'
  backpack-full: '&cSua mochila já está cheia.'
  automatic-give: '&aVocê deu &e{amount} &ade *ATIVADOR AUTOMÁTICO* para o jogador &e{player}&a.'
  automatic-activated: '&aO *ATIVADOR AUTOMÁTICO* foi ativado na mochila.'
  automatic-already: '&cEsta mochila já possui o ativador automático.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/154-yCratesVirtuaisMochilasAddon">Site do plugin yCratesVirtuaisMochilasAddon</a>
    </category>
</seealso>