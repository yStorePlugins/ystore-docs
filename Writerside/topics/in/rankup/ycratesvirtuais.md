# yCratesVirtuais
<secondary-label ref="rankup"/>

### Descrição
Caixas modernas para abrir em menu

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
<video src="//www.youtube.com/watch?v=DreHSqrKRg8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/crate - Abre o menu principal
/crate armazem - Abre o menu de coletar recompensas
/crate give - Dá crates para um jogador
/crate definir - Define um bloco como crate
/crate reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycratesvirtuais.use - Permissão para o /crate e /crate armazem
ycratesvirtuais.open.all - Permissão para o abrir tudo
ycratesvirtuais.open.automatic - Permissão para o abrir automático
ycratesvirtuais.give - Permissão para o /crate give
ycratesvirtuais.define - Permissão para o /crate define
ycratesvirtuais.reload - Permissão para o /crate reload
ycratesvirtuais.admin - Permissão para remover bloco da crate</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ycratesvirtuais_amount% - Retorna a quantia de crates que o jogador possui
%ycratesvirtuais_amount_raw% - Retorna a quantia de crates que o jogador possui sem formatar
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCratesVirtuais/
    ├── commands.yml
    ├── config.yml
    ├── crates.yml
    ├── limit.yml
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
  crate: 'crate|crates'
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
# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
limit:
  enabled: true
  # Máximo que irá recolher por vez
  max: 1000

# Mundos que não poderão coletar recompensas
world-reward-collect-blacklist: [ 'none' ]

# Sistema de abertura automatica
automatic-open:
  enabled: true
  # em ticks -> 20 ticks = 1 segundo
  time: 20

# Sistema de blocos
crate-block:
  # Ajustar a altura do holograma
  offset: 2.5
  hologram:
    - '&6&lCAIXAS'
    - '&7Abra as suas chaves aqui'
    - '&f(/crates)'
    - '[item]TRIPWIRE_HOOK'

# Sistema de botões do menu
menu:
  # Mostrar todas as chaves no menu (mesmo se o jogador não tiver)
  show-all: true
  # Botão para abrir o menu de preview
  preview: 'RIGHT'
  # Botão para abrir o menu de gerenciamento
  management: 'LEFT'
  # Mostrar os ícones de 0 a 64
  numerate: true

# Sistema de lores
lore:
  chance: ['', '&6Chance: &7[{chance_progressbar}&7] &f{chance}%', '']
  filter-add: ['&eClique para adicionar ao filtro']
  filter-remove: ['&cClique para remover do filtro']

# Configuração da progressbar
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-not: '&7'

# Sistema de formatos de money e quantia
format:
  type: 'LETTER' # Tipos: LETTER - NUMBER
  max-decimals: 4
  formats:
    - ''
    - ''
    - 'K'
    - 'M'
    - 'B'
    - 'T'
    - 'Q'
    - 'QQ'
    - 'S'
    - 'SS'
    - 'O'
    - 'N'
    - 'D'
]]>
</code-block>
</chapter>

<chapter title="crates.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#    ____           _
#  / ___|_ __ __ _| |_ ___  ___
# | |   | '__/ _` | __/ _ \/ __|
# | |___| | | (_| | ||  __/\__ \
#  \____|_|  \__,_|\__\___||___/
#

crates:
  vip:
    # Ordem no menu
    order: 1
    display: '&6VIP'
    # Item que poderá ser ativado
    usable:
      material: 'TRIPWIRE_HOOK'
      name: '&6Chave VIP &7[1]'
      lore: [ '&7Utilize esta chave', '&7acessando &f/crates' ]
    # Item da crate no menu
    menu:
      has:
        material: 'TRIPWIRE_HOOK'
        name: '&6Chave VIP'
        lore: [ '&fQuantidade: &7{amount}', '', ' &a> &f{to_gain} &7recompensas a', '&7  serem ganhas.', '', '&aBotão esquerdo para abrir.', '&aBotão direito para ver as recompensas.' ]
      no-has:
        material: 'TRIPWIRE_HOOK'
        name: '&6Chave VIP'
        lore: [ '', '&cVocê não possui essa chave.' ]
    # Recompensas que poderão ser ganhar
    rewards:
      # Quantia de recompensas que serão ganhas
      amount: 1
      # Lista de recompensas
      # Chance,recompensa (rewards.yml)
      list:
        - '50.0,reward1'
        - '30.0,reward2'
        - '10.0,reward3'
]]>
</code-block>
</chapter>

<chapter title="limit.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Limite padrão do jogador
default: 1

# Máximo de limite que o jogador poderá ter
# -1 para ser infinito
maximum: -1

# Slot do display no menu
display-slot: 48

messages:
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  bought: '&aVocê comprou +1 limite de abertura de key.'

# Custos de evolução por nível
costs:
  cost1:
    provider: 'Money'
    amount: 100.0

# Item do menu
display:
  material: 'INK_SACK:10'
  name: '&eLimite de abertura'
  lore:
    - '&7Abra mais keys ao mesmo'
    - '&7tempo.'
    - ''
    - '&7Limite Atual: &b{limit}'
    - ''
    - '&f* +1 por: &a{Money} coins&f.'
    - ''
    - '&aClique para adquirir.'

# Item do menu
display-max:
  material: 'INK_SACK:10'
  name: '&eLimite de abertura'
  lore:
    - '&7Abra mais keys ao mesmo'
    - '&7tempo.'
    - ''
    - '&7Limite Atual: &b{limit}'
    - ''
    - '&cVocê está no máximo.'
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

# Menu de gerenciar membros
main:
  name: '&8Crates'
  size: 54
  slots: [ 11, 12, 13, 20, 21, 22, 29, 30, 31 ]
  previous-slot: 18
  next-slot: 26
  #
  empty-slot: -1
  open-all-slot: 15
  open-automatic-slot: 33
  filter-slot: 24
  info-slot: 47
  top-slot: 49
  rewards-slot: 51
  #
  items:
    empty:
      material: 'WEB'
      name: '&cVocê não possui nenhuma chave'
      lore: []
    open-all:
      material: '4ced34211fed4010a8c85724a27fa5fb205d67684b3da517b6821279c6b65d3f'
      name: '&cAbrir todas chaves!'
      lore: [ '&7Abra todas suas crates', '&7de uma só vez.', '', ' &fChaves a abrir: &7{to_open}', '', '&aClique para abrir.' ]
    open-all-permission:
      material: '4ced34211fed4010a8c85724a27fa5fb205d67684b3da517b6821279c6b65d3f'
      name: '&cAbrir todas chaves!'
      lore: [ '&7Abra todas suas crates', '&7de uma só vez.', ' &fChaves a abrir: &7{to_open}', '', '&cVocê não tem permissão' ]
    open-automatic-on:
      material: 'a7695f96dda626faaa010f4a5f28a53cd66f77de0cc280e7c5825ad65eedc72e'
      name: '&cAbrir automaticamente'
      lore: [ '&7Abra todas suas crates', '&7automaticamente.', ' &fChaves a abrir: &7{to_open}', '', '&fStatus: &aATIVADO', '' ]
    open-automatic-off:
      material: 'df4dc3c3753bf5b0b7f081cdb49b83d37428a12e4187f6346dec06fac54ce'
      name: '&cAbrir automaticamente'
      lore: [ '&7Abra todas suas crates', '&7automaticamente.', ' &fChaves a abrir: &7{to_open}', '', '&fStatus: &cDESATIVADO', '' ]
    open-automatic-permission:
      material: 'df4dc3c3753bf5b0b7f081cdb49b83d37428a12e4187f6346dec06fac54ce'
      name: '&cAbrir automaticamente'
      lore: [ '&7Abra todas suas crates', '&7automaticamente.', ' &fChaves a abrir: &7{to_open}', '', '&cVocê não tem permissão.' ]
    filter:
      material: 'HOPPER'
      name: '&eItens filtrados'
      lore: [ '&7Clique para gerenciar', '&7os &f{filtered}&7 itens filtrados.' ]
    info:
      material: 'd01afe973c5482fdc71e6aa10698833c79c437f21308ea9a1a095746ec274a0f'
      name: '&eSuas informações'
      lore: [ '', ' &fChaves abertas: &7{opened}', ' &fChaves a abrir: &7{to_open}', '', ' &fRecompensas a coletar: &7{rewards}', '' ]
    top:
      material: 'BOOK'
      name: '&eTOP'
      lore: [ '&7Clique para ver os', '&7jogadores que abriram', '&7mais crates.' ]
    rewards:
      material: 'CHEST'
      name: '&eSuas recompensas'
      lore: [ '&7Clique para gerenciar', '&7suas &f{rewards}&7 recompensas.' ]
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
open:
  name: '&8Crates'
  size: 36
  back-slot: 31
  open-1-slot: 11
  open-all-slot: 12
  collect-1-slot: 14
  collect-all-slot: 15
  items:
    open-1:
      material: '71bc2bcfb2bd3759e6b1e86fc7a79585e1127dd357fc202893f9de241bc9e530'
      name: '&aAbrir 1x'
      lore: [ '', ' &fChaves disponíveis: &7{amount}', '', '&aClique para abrir' ]
    open-all:
      material: '49dd36759307db8e2d9f4b0c2aed2556db1ddcf3f67fa19cc826acbd965fe'
      name: '&aAbrir tudo'
      lore: [ '', ' &fChaves disponíveis: &7{amount}', '', '&aClique para abrir' ]
    collect-1:
      material: 'd9b30303f94e7c785a31e5727a9381535daf4753449ea41db746e1234e9dd2b5'
      name: '&aRetirar 1x'
      lore: [ '', ' &fChaves disponíveis: &7{amount}', '', '&aClique para retirar' ]
    collect-all:
      material: '1a6f1bce5461368a40707c54dc0b895bd61499e812145093db32f9eb12c32954'
      name: '&aRetirar tudo'
      lore: [ '', ' &fChaves disponíveis: &7{amount}', '', '&aClique para retirar' ]

# Menu de preview das recompensas
preview:
  name: '&8Crates'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  collect-slot: 38
  open-slot: 42
  #
  items:
    collect:
      material: 'TRIPWIRE_HOOK'
      name: '&eRetirar as chaves!'
      lore: [ '&7Receba a chave em', '&7seu inventário.', '', ' &8> &f{amount}&7 chaves', '', '&8>&f Botão esquerdo: &7Retira 100', '&8>&f Botão direito: &7Retira 1', '&8>&f Botão Q: &7Retira todas' ]
    open:
      material: '4ced34211fed4010a8c85724a27fa5fb205d67684b3da517b6821279c6b65d3f'
      name: '&eAbrir as chaves!'
      lore: [ '&7Abrir as chaves e', '&7receber recompensas.', '', ' &8> &f{amount}&7 chaves', '', '&8>&f Botão esquerdo: &7Abre 100', '&8>&f Botão direito: &7Abre 1', '&8>&f Botão Q: &7Abre todas' ]
  facing:
    e0:
      slot: 11
      material: 'BARRIER'
      name: ' '
      lore: []
    e1:
      slot: 12
      material: 'BARRIER'
      name: ' '
      lore: []
    e2:
      slot: 13
      material: 'BARRIER'
      name: ' '
      lore: []
    e3:
      slot: 14
      material: 'BARRIER'
      name: ' '
      lore: []
    e4:
      slot: 15
      material: 'BARRIER'
      name: ' '
      lore: []
    e5:
      slot: 20
      material: 'BARRIER'
      name: ' '
      lore: []
    e6:
      slot: 21
      material: 'BARRIER'
      name: ' '
      lore: []
    e7:
      slot: 22
      material: 'BARRIER'
      name: ' '
      lore: []
    e8:
      slot: 23
      material: 'BARRIER'
      name: ' '
      lore: []
    e9:
      slot: 24
      material: 'BARRIER'
      name: ' '
      lore: []

# Menu de recompensas
rewards:
  name: '&8Crates'
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

# Menu de filtro das recompensas
filter:
  name: '&8Crates'
  size: 45
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 40
  facing:
    e0:
      slot: 11
      material: 'BARRIER'
      name: ' '
      lore: []
    e1:
      slot: 12
      material: 'BARRIER'
      name: ' '
      lore: []
    e2:
      slot: 13
      material: 'BARRIER'
      name: ' '
      lore: []
    e3:
      slot: 14
      material: 'BARRIER'
      name: ' '
      lore: []
    e4:
      slot: 15
      material: 'BARRIER'
      name: ' '
      lore: []
    e5:
      slot: 20
      material: 'BARRIER'
      name: ' '
      lore: []
    e6:
      slot: 21
      material: 'BARRIER'
      name: ' '
      lore: []
    e7:
      slot: 22
      material: 'BARRIER'
      name: ' '
      lore: []
    e8:
      slot: 23
      material: 'BARRIER'
      name: ' '
      lore: []
    e9:
      slot: 24
      material: 'BARRIER'
      name: ' '
      lore: []

# Menu de top
top:
  name: '&8Top crates'
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
        - '&fChaves abertas: &7{amount}'
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
    &e-> &f/crates &8-&7 Abre o menu principal
    &e-> &f/crates armazem &8-&7 Abre o menu de coletar recompensas
    <nl>
    &c-> /crates give <item/direto> <player/all> <crate> <quantia> - Dá chaves para um jogador
    &c-> /crates definir - Defini um bloco como crate
    &c-> /crates reload - Recarrega as configurações
    <nl>
  crate-found: |
    &cEsta crate não foi encontrada.
    &7Disponíveis: {list}
  crate-give: '&eVocê deu &f{amount}x chaves(s) &r{crate}&e para o jogador &f{player}&e.'
  crate-give-all: '&eVocê deu &f{amount}x chaves(s) &r{crate}&e para todos os jogadores online.'
  crate-give-all-target: |
    <nl>
    &eTodos os jogadores receberam &f{amount}x chaves(s) &r{crate}&e.
    <nl>
  crate-activated: '&eForam adicionadas &f{amount}x chaves(s) &r{crate}&e em seu /crates.'
  crate-collect: '&eColete as recompensas obtidas em &f/crates armazem&e.'
  crate-collected: '&eVocê retirou &f{amount}x chaves(s) &r{crate}&e.'
  crate-reward-collected: '&eItem recolhido com sucesso.'
  crate-reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  crate-defined: '&eBloco da crate definido com sucesso.'
  crate-define-enter: '&eClique em um bloco para definir como crate. Para sair digite /crate definir novamente.'
  crate-define-leave: '&eVocê saiu do modo definição.'
  crate-define: '&cVocê está no modo definir. Para sair: /crate definir'
  world-blacklisted: '&cVocê não pode coletar recompensas neste mundo.'
  wait-collect: '&cAguarde parar recolher recompensas novamente.'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/97-yCratesVirtuais">Site do plugin yCratesVirtuais</a>
    </category>
</seealso>