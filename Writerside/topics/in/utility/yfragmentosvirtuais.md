# yFragmentosVirtuais
<secondary-label ref="utility"/>

### Descrição
Armazene pedaços de itens que podem ser utilizados como moeda de troca

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
<video src="//www.youtube.com/watch?v=aKlZuImwhWI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/fragmentos - Abre o menu de fragmentos
/fragmentos shop - Abre o menu de loja
/fragmentos enviar - Envia fragmentos para um jogador
/fragmentos give - Dar fragmentos à um jogador
/fragmentos reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yfragmentosvirtuais.use - Permissão para o /fragmentos
yfragmentosvirtuais.shop - Permissão para o /fragmentos shop
yfragmentosvirtuais.send - Permissão para o /fragmentos enviar
yfragmentosvirtuais.give - Permissão para o /fragmentos give
yfragmentosvirtuais.reload - Permissão para o /fragmentos reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yfragmentosvirtuais_amount% - Retorna a quantia de fragmentos que o jogador possui
%yfragmentosvirtuais_amount_raw% - Retorna a quantia de fragmentos que o jogador possui sem formatar
%yfragmentosvirtuais_[identificador_da_config]_amount% - Retorna a quantia de tal fragmentos do jogador
%yfragmentosvirtuais_[identificador_da_config]_amount_raw% - Retorna a quantia de tal fragmentos&nbsp;do jogador sem formatar
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yFragmentosVirtuais/
    ├── commands.yml
    ├── config.yml
    ├── fragmentos.yml
    ├── menus.yml
    ├── messages.yml
    └── shop.yml
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
  fragmento: 'fragmento|fragmentos'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____           _          __     ___      _               _
#  _   _ / ___|_ __ __ _| |_ ___  __\ \   / (_)_ __| |_ _   _  __ _(_)___
# | | | | |   | '__/ _` | __/ _ \/ __\ \ / /| | '__| __| | | |/ _` | / __|
# | |_| | |___| | | (_| | ||  __/\__ \\ V / | | |  | |_| |_| | (_| | \__ \
#  \__, |\____|_|  \__,_|\__\___||___/ \_/  |_|_|   \__|\__,_|\__,_|_|___/
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

# Máximo permitido para evoluir com Q
q-max: 0

# Sistema de botões do menu
menu:
  # Mostrar todas as chaves no menu (mesmo se o jogador não tiver)
  show-all: true
  # Mostrar os ícones de 0 a 64
  numerate: true

# Tipos disponíveis:
# yPlugins -> Usa a formatação do yPlugins
# LETRA -> Força usar a formatação em letra
# NUMERO -> Força usar a formatação em número
format: 'yPlugins'
]]>
</code-block>
</chapter>

<chapter title="fragmentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#    ____           _
#  / ___|_ __ __ _| |_ ___  ___
# | |   | '__/ _` | __/ _ \/ __|
# | |___| | | (_| | ||  __/\__ \
#  \____|_|  \__,_|\__\___||___/
#

fragmentos:
  rocha:
    # Ordem no menu
    order: 1
    # Identificação necessária para a API de Economias do yPlugins
    yplugins-id: 'yfragmentosvirtuais-rocha'
    # Nome nas mensagens
    display: '&8Rocha'
    # Ativar a coleta
    collect: true
    # Comando
    command:
      command: 'rocha'
      aliases: [ 'rochas' ]
    # Mensagem de uso do comando
    usage:
      pay: '&cUse: /{command} {arg} <player> <quantia>'
    # Permissões dos comandos
    permission:
      look: 'yfragmentosvirtuais.rocha.look'
      pay: 'yfragmentosvirtuais.rocha.pay'
    # Mensagens do comando
    message:
      balance: '&aVocê possui: &f{fragment}&a rochas.'
      balance-target: '&aO jogador &7{player}&a possui: &f{fragment}&a rochas.'
      has: '&cVocê não possui esta quantia de rochas.'
      send: '&aVocê enviou &f{fragment}&a rochas para o jogador &7{player}&a.'
      received: '&aVocê recebeu &f{fragment}&a rochas do jogador &7{player}&a.'
    # Item que poderá ser ativado
    usable:
      material: 'f8d818e65ee36cdcab6e315f499d3f5dde2323bf2df56f1e914089cebefa37f6'
      name: '&8Fragmento de rocha &7[{amount}]'
      lore: [ '&7Utilize este fragmento', '&7acessando &f/fragmentos' ]
    # Item da crate no menu
    menu:
      has:
        material: 'f8d818e65ee36cdcab6e315f499d3f5dde2323bf2df56f1e914089cebefa37f6'
        name: '&8Fragmento de rocha'
        lore: [ '&fQuantidade: &7{amount}', '', '&aClique para recolher.' ]
      no-has:
        material: 'f8d818e65ee36cdcab6e315f499d3f5dde2323bf2df56f1e914089cebefa37f6'
        name: '&8Fragmento de rocha'
        lore: [ '', '&cVocê não possui esse fragmento.' ]
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
  name: '&8Fragmentos'
  size: 45
  slots: [ 11, 12, 13, 20, 21, 22, 29, 30, 31 ]
  previous-slot: 18
  next-slot: 26
  #
  empty-slot: -1
  shop-slot: 24
  info-slot: 15
  top-slot: 33
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVocê não possui nenhum fragmento'
      lore: []
    shop:
      material: 'GOLD_INGOT'
      name: '&eLoja'
      lore: [ '&7Clique para abrir a loja', '&7de fragmentos.' ]
    info:
      material: 'd01afe973c5482fdc71e6aa10698833c79c437f21308ea9a1a095746ec274a0f'
      name: '&eSuas informações'
      lore: [ '', ' &fFragmentos Armazenados: &7{stored}', '' ]
    top:
      material: 'BOOK'
      name: '&eTOP'
      lore: [ '&7Clique para ver os', '&7jogadores que possuem', '&7mais fragmentos.' ]
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
      slot: 20
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e4:
      slot: 21
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e5:
      slot: 22
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e6:
      slot: 29
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e7:
      slot: 30
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []
    e8:
      slot: 31
      material: '3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
      name: ' '
      lore: []

# Menu de abrir as chaves
collect:
  name: '&8Fragmentos'
  size: 36
  back-slot: 31
  collect-1-slot: 11
  collect-all-slot: 15
  items:
    collect-1:
      material: 'd9b30303f94e7c785a31e5727a9381535daf4753449ea41db746e1234e9dd2b5'
      name: '&aRetirar 1x'
      lore: [ '', ' &fFragmentos disponíveis: &7{amount}', '', '&aClique para retirar' ]
    collect-all:
      material: '1a6f1bce5461368a40707c54dc0b895bd61499e812145093db32f9eb12c32954'
      name: '&aRetirar tudo'
      lore: [ '', ' &fFragmentos disponíveis: &7{amount}', '', '&aClique para retirar' ]

# Menu de shop
shop:
  name: '&8Loja fragmentos'
  size: 36
  back-slot: 31

# Menu de top
top:
  name: '&8Top fragmentos'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 31
  previous-slot: 9
  next-slot: 17
  items:
    # Item do top fragmentos
    stored:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fFragmentos Armazenados: &7{amount}'
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
# Mensagens a serem enviadas pelo plugin.

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  help: |
    <nl>
    &eComandos do plugin:
    <nl>
    &e-> &f/fragmentos &8-&7 Abre o menu principal
    <nl>
    &c-> /fragmentos give <item/direto> <player/all> <fragmento> <quantia> - Dá fragmentos para um jogador
    &c-> /fragmentos reload - Recarrega as configurações
    <nl>
  fragmento-found: |
    &cEste fragmento não foi encontrado.
    &7Disponíveis: {list}
  fragmento-give: '&eVocê deu &f{amount}x fragmento(s) &r{fragmento}&e para o jogador &f{player}&e.'
  fragmento-give-all: '&eVocê deu &f{amount}x fragmento(s) &r{fragmento}&e para todos os jogadores online.'
  fragmento-give-all-target: |
    <nl>
    &eTodos os jogadores receberam &f{amount}x fragmento(s) &r{fragmento}&e.
    <nl>
  fragmento-activated: '&eForam adicionados &f{amount}x fragmento(s) &r{fragmento}&e em seu /fragmentos.'
  fragmento-collected: '&eVocê retirou &f{amount}x fragmento(s) &r{fragmento}&e.'
  shop-has: '&cVocê não possui &f{amount}x fragmento(s) &r{fragmento}&c.'
  shop-buy: '&aVocê adquiriu itens no shop fragmentos.'
  yourself: '&cVocê não pode pagar à si mesmo.'
]]>
</code-block>
</chapter>

<chapter title="shop.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#
#    /\/\   ___ _ __  _   _ ___
#   /    \ / _ \ '_ \| | | / __|
#  / /\/\ \  __/ | | | |_| \__ \
#  \/    \/\___|_| |_|\__,_|___/
#

items:
  sell1:
    cost:
      - 'rocha,3'
    display:
      slot: 10
      material: 'STONE'
      name: ''
      lore: ['&7Esta pedra custa &f3 fragmentos de rocha']
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
      list: [ 'give {player} stone 1' ]
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static CrateHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;CrateHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(CrateHolder.class);
        return rsp == null ? null : rsp.getProvider();
    } catch (Throwable var1) {
        return null;
    }
}
</code-block>

## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/99-yFragmentosVirtuais">Site do plugin yFragmentosVirtuais</a>
    </category>
</seealso>