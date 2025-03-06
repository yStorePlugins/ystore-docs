# yVips
<secondary-label ref="management"/>

### Descrição
Venda vantagens no seu servidor

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
<video src="//www.youtube.com/watch?v=lUqLHCAyvZ8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/vip - Abre o menu principal
/vips [player] - Veja os vips ativos.
/keys [player
/admin] - Veja as chaves ativas.
/trocarvip [vip] - Trocqa o seu VIP atual por outro
/vip info [id-vip] - Vê as informações gerais do id selecionado.
/tempovip [jogador] - Mostra o seu tempo de vip ou de outro jogador
/usarkey [key] - Ativa um VIP a partir de uma KEY
/partyvip - Mostra o progresso atual do party-vip
/ativarvip [id] - Ativa um VIP a partir do ID do bônus
/bonusvip dar [player
/random] [vip] [duração] - Dar uma chave bônus para um jogador
/bonusvip enviar [id] [player] - Envia uma chave bônus para um jogador
/bonusvip ativar [id] - Ativa uma chave bônus
/vendervip [id] [economia] [preço] - Vende uma chave VIP
/comprarvip [id] - Compra uma chave VIP
/cancelarvendavip [id] - Cancela a venda de uma chave VIP
/congerlavip - Congela
/descongela o tempo dos vips
/darvip [jogador] [vip] [tempo] - Dá um determinado vip a um jogador
/darchave [jogador] [vip] [tempo] - Dá uma chave de um determinado vip a um jogador
/setarvip [jogador] [vip] [tempo] - Dá um determinado vip a um jogador, porém sem as mensagens e os comandos de ativação
/gerarkey [vip] [tempo] [tipo] [usos] - Cria uma key aleatória de um determinado vip
/criarkey [vip] [tempo] [tipo] [usos] [key] - Cria uma key customizada de um determinado vip
/editarkey [key] [vip] [tempo] [tipo] [usos] - Edita uma key
/deletarkey [key] - Deleta uma key
/removervip [id] - Remove um vip
/removervipplayer [player] - Remove todos os vips de um jogador
/removertempovip [id] [tempo] - Remove tempo de um vip</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yvips.use - Permissão para o /vip
yvips.freeze - Permissão para o /congelarvip
yvips.reload - Permissão para o /vip reload
yvips.bonusvip - Permissão para o /bonusvip
yvips.bonusvip.give - Permissão para o /bonusvip dar
yvips.bonusvip.active - Permissão para o /bonusvip ativar
yvips.bonusvip.send - Permissão para o /bonusvip enviar
yvips.bonusvip.list - Permissão para o /bonusvip lista
yvips.activevip - Permissão para o /ativarvip
yvips.buyvip - Permissão para o /comprarvip
yvips.givekey - Permissão para o /darchave
yvips.keys - Permissão para o /keys
yvips.keys.admin - Permissão para o /keys admin
yvips.keys.others - Permissão para o /keys [player]
yvips.sellcancelvip - Permissão para o /cancelarvendavip
yvips.sellvip - Permissão para o /vendervip
yvips.sellsvip - Permissão para o /vendasvip
yvips.sellsvip.others - Permissão para o /vendasvip [player]
yvips.usekey - Permissão para o /usarkey
yvips.createkey - Permissão para o /criarkey
yvips.editkey - Permissão para o /editarkey
yvips.generatekey - Permissão para o /gerarkey
yvips.removekey - Permissão para o /removerkey
yvips.infovip - Permissão para o /vip info
yvips.partyvip - Permissão para o /partyvip
yvips.timevip - Permissão para o /tempovip
yvips.timevip.others - Permissão para o /tempovip [player]
yvips.tradevip - Permissão para o /trocarvip
yvips.tradevip.others - Permissão para o /trocarvip [vip] [player]
yvips.vips - Permissão para o /vips
yvips.vips.others - Permissão para o /vips [player]
yvips.addvip - Permissão para o /darvip
yvips.setvip - Permissão para o /setarvip
yvips.removevip - Permissão para o /removervip
yvips.removevipplayer - Permissão para o /removervipplayer
yvips.removetime - Permissão para o /removertempovip
yvips.admin - Permissão para ser reconhecido como admin</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yvips_partyvip_has% - Retorna a quantia atual do party-vip
%yvips_partyvip_need% - Retorna a quantia necessária do party-vip
%yvips_partyvip_progressbar% - Retorna a barra de progresso do party-vip
%yvips_partyvip_percentage% - Retorna a porcentagem atual do party-vip
%yvips_credit% - Retorna a quantia de créditos VIP do jogador formatado
%yvips_credit_raw% - Retorna a quantia de créditos VIP do jogador sem formatar
%yvips_vip_raw% - Retorna o tipo do vip
%yvips_vip_tag% - Retorna a tag do vip
%yvips_vip_prefix% - Retorna o prefixo do vip
%yvips_start_raw% - Retorna o horário raw de ativação do vip
%yvips_expire_raw% - Retorna o horário raw de expiração do vip
%yvips_duration_raw% - Retorna o horário raw de duração do vip
%yvips_start_date% - Retorna a data de ativação do vip
%yvips_start_hour% - Retorna a hora de ativação do vip
%yvips_expire_date% - Retorna a data de expiração do vip
%yvips_expire_hour% - Retorna a hora de expiração&nbsp;&nbsp;do vip
%yvips_duration% - Retorna a duração do vip
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{vip_tag} - Retorna a tag do vip
{vip_prefix} - Retorna o prefixo do vip
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yVips/
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── discord.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── vips.yml
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
  vip: 'vip'
  vips: 'vips'
  timevip: 'tempovip|timevip'
  tradevip: 'trocarvip|tradevip'
  usekey: 'usekey|usarkey|usarchave'
  addvip: 'darvip|givevip|addvip|adicionarvip'
  removevip: 'removevip|removervip'
  removetime: 'removetimevip|removertempovip'
  setvip: 'setvip|setarvip|definirvip|definevip'
  generatekey: 'generatekey|gerarkey'
  createkey: 'createkey|criarkey'
  removekey: 'removekey|deletekey|removerkey|deletarkey'
  editkey: 'editkey|editarkey'
  seekeys: 'verkeys|seekeys|keys|verchaves|chaves'
  freeze: 'freezevip|congelarvip'
  givekey: 'givekey|darkey|darchave'
  infovip: 'infovip|vipinfo'
  bonusvip: 'bonusvip|vipbonus'
  activevip: 'activevip|ativarvip'
  sellvip: 'sellvip|vendervip'
  sellcancelvip: 'sellcancelvip|sellcancel|cancelsell|cancelsellvip|cancelarvendavip|vendacancelar|vendacancelarvip|cancelarvenda'
  buyvip: 'buyvip|comprarvip'
  sellsvip: 'sellsvip|vendasvip'
  partyvip: 'partyvip'
  creditovip: 'creditovip|creditosvip'
  removevipplayer: 'removevipplayer|removervipplayer|tirarvipplayer'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#      __     ___
#  _   \ \   / (_)_ __  ___
# | | | \ \ / /| | '_ \/ __|
# | |_| |\ V / | | |_) \__ \
#  \__, | \_/  |_| .__/|___/
#  |___/         |_|
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

general:
  # Nome deste servidor na proxy
  proxy-name: 'rankup'
  # Reduzir o tempo dos vips que não estão equipados; reduzir apenas do vip ativo
  reduce-non-equiped: false
  # Setar o grupo do vip sempre ao logar
  login-set-group: true
  # Reduzir tempo dos vips nesse servidor (desative caso tenha vários no mesmo MYSQL -> deixe ativado apenas em um dos servidores)
  reduce-this: true
  # Delay para trocar VIP
  # em segundos
  trade-delay: 300
  # Permitir o jogador ter ativado todos os vips ao mesmo tempo
  active-all: false

party-vip:
  enable: true
  # Valor que precisa ser acumulado para executar a ração
  value: 100.0
  # Resetar ao atingir
  reset-completed: true
  # Somar valor ao utilizar /setvip
  set-sum: false
  # Comando que será executado
  command: [ 'alert &cAtingimos a META de R$ 100,00 em VIPs vendidos.' ]
  # Mensagens do party-vip
  message:
    disabled: '&cEste sistema foi desativado.'
    add: |

      &b&lPARTY VIP: &aUm novo VIP foi ativado!
      &eProgresso atual: &7(&fR$ {has}&7/&bR$ {need}&7)

    got: |

      &b&lPARTY VIP: &aA META foi atingida!
      &eValor alcançado: &7(&fR$ {has}&7/&bR$ {need}&7)

    progress: |

      &b&lPARTY VIP
      &eProgresso atual: &7(&fR$ {has}&7/&bR$ {need}&7)

# Configuração da progressbar
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-not: '&7'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
freeze: false
party-vip: 0.0
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
options:
  url: ''
  username: 'yVips'

embeds:
  activated:
    title: ':mailbox: Um novo VIP foi ativado'
    thumbnail: 'https://minotar.net/body/{player}/100.png'
    color: '#fff'
    content: ''
    footer:
      text: 'yStore © Todos os direitos reservados'
      image: ''
    fields:
      player:
        inline: true
        header: 'Player'
        content: '```{player}```'
      vip:
        inline: true
        header: 'VIP'
        content: '```{vip}```'
      time:
        inline: true
        header: 'Duração'
        content: '```{time}```'
      date_activated:
        inline: true
        header: 'Ativado em'
        content: '```{activation_date} às {activation_hour}```'
      date_expire:
        inline: true
        header: 'Expira em'
        content: '```{expire_date} às {expire_hour}```'
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
    permission: 'yvips.provider.money'
    # ‘Item’ que aparecerá para os jogadores ao interagir com a placa
    item:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &aEsta loja está comercializando com &fMoney&a.'
        - ''
    # ‘Item’ que aparecerá para o dono ao editar/criar a placa
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
  name: '&8VIPs ➜ Principal'
  size: 36
  items:
    profile:
      slot: 10
      material: '{player}'
      name: '&bPerfil'
      lore:
        - ''
        - ' &fVIP Atual: &r{vip_display}'
        - ' &fTAG: &r{vip_prefix}'
        - ''
        - ' &fCréditos: &b&l♦ &f{credit}'
        - ''
        - ' &fExpira em: &7{expire_remaining}'
        - ' &fAtivado em: &7{activation_date} às {activation_hour}'
        - ''
    profile-no-vip:
      material: '{player}'
      name: '&aPerfil'
      lore:
        - ' &fCréditos: &b♦&f{credit}'
        - ''
        - ' &cAdquira um VIP e'
        - ' &cdesbloqueie o acesso ao menu.'
        - ''
    historic:
      slot: 12
      material: 'EMPTY_MAP'
      name: '&bHistórico de VIPS'
      lore:
        - '&7Clique para visualizar o seu'
        - '&7histórico de VIPs utilizados.'
        - ''
    stored:
      slot: 13
      material: 'TRIPWIRE_HOOK'
      name: '&bChaves'
      lore:
        - '&7Clique para visualizar as suas chaves'
        - '&7armazenadas do seu VIPs'
        - ''
        - ' &7Você possui &f{amount_stored} &7chave(s) armazenada(s).'
        - ' &7Total de chaves obtidas: &f{amount_obtained}&7.'
        - ''
    shop:
      slot: 14
      material: 'GOLD_INGOT'
      name: '&bLoja de Créditos'
      lore:
        - '&7Aqui você pode adquirir itens utilizando'
        - '&7os seus &nCréditos VIP&7.'
        - ''
        - '&aClique para abrir a loja.'
    keys-shop:
      slot: 15
      material: 'DIAMOND'
      name: '&bLoja de Chaves'
      lore:
        - '&7Aqui você pode adquirir chaves VIP'
        - '&7de outros jogadores.'
        - ''
        - '&aClique para abrir a loja.'
    top:
      slot: 16
      material: 'BOOK_AND_QUILL'
      name: '&b&lTOP'
      lore:
        - '&7Veja os jogadores que mais ativaram'
        - '&7vip no servidor.'
        - ''
        - '&aClique para abrir'
    activation:
      slot: 21
      material: 'CHEST'
      name: '&b&lAtivações'
      lore:
        - '&7Recolha as suas ativações pendentes.'
        - ''
        - '&aClique para abrir'
    upgrade-yes:
      slot: 22
      material: 'EMERALD'
      name: '&b&lUpar VIP'
      lore:
        - '&7Faça um upgrade do seu VIP atual para um melhor.'
        - ''
        - '&aClique para abrir'
    upgrade-no:
      material: 'EMERALD'
      name: '&b&lUpar VIP'
      lore:
        - '&cVocê não possui nenhum vip.'

# Menu histórico de vips
history:
  name: '&8VIP'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  # Seletor dos tops
  selector:
    slot: 50
    material: HOPPER
    name: '&aFiltro'
    # Tipos do seletor
    types:
      active:
        enabled: true
        name: 'VIP Equipado'
      pending:
        enabled: true
        name: 'VIP(s) Pendente'
      expired:
        enabled: true
        name: 'VIP(s) Expirados'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu top
top:
  name: '&8TOP VIP'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 30
  previous-slot: 9
  next-slot: 17
  # Seletor dos tops
  selector:
    slot: 31
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor do TOP'
    # Tipos do seletor
    types:
      credit:
        enabled: true
        name: 'Créditos VIP'
      activated-vip:
        enabled: true
        name: 'VIPs ativados'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{nome}'
      select: ' &f• &7{nome}'
  items:
    # Item do top peixe mais pesado
    credit:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fCréditos VIP: &7{amount}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top tempo pescando
    activated-vip:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fVIPs ativados: &7{amount}'
        - '&fPosição: &e{pos}º'
        - ''

# Menu de shop
shop:
  name: '&8VIP SHOP'
  size: 27
  back-slot: 10
  profile:
    slot: 12
    material: '{player}'
    name: '&a{player}'
    lore: [ '&7Seus créditos: &f{credit}', "&7Créditos gastos: &f{spent}" ]
  items:
    swords:
      price: 1.0
      preview:
        slot: 14
        material: 'DIAMOND'
        name: '&b&lVIP DIAMANTE'
        lore: ['&7Compre seu vip diamante', '&7muito especial para o servidor.']
      item:
        material: 'DIAMOND'
        name: 'EOQ'
        lore: []
      command: [ 'darvip {player} diamante 10000' ]

# Menu keys
keys:
  name: '&8VIP KEYS'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  #
  bonus-slot: 40
  #
  items:
    bonus:
      material: 'TRIPWIRE_HOOK'
      name: '&eKeys bônus!'
      lore: [ '&7Gerencie suas chaves bônus', '&7adquiridas em ativações.', '', '&aClique para abrir' ]
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

# Menu keys bonus
keys-bonus:
  name: '&8VIP KEYS BÔNUS'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
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

# Menu keys vendendo
keys-sell:
  name: '&8VIP KEYS VENDENDO'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
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

# Menu de configuração
sell:
  name: '&8VIP VENDER KEY'
  size: 27
  items:
    back-slot: 10
    provider-slot: 12
    price-slot: 14
    selling-slot: 16
    provider:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aMoeda da venda'
      lore:
        - '&7Moeda que será utilizada no comércio'
        - '&7desta key.'
        - ''
        - '&7Atual: &fNenhuma'
        - ''
        - '&aClique para alterar a moeda'
    price:
      material: '945f47feb4d75cb333914bfdb999a489c9d0e320d548f310419ad738d1e24b9'
      name: '&aPreço da key'
      lore:
        - '&7Quantia que o jogador vai pagar por esta key:'
        - ''
        - ' &fPreço atual: &7{price}'
        - ''
        - '&aClique para alterar'
    selling:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aAtivar venda'
      lore:
        - '&7Esta key não está sendo vendida no momento.'
        - '&7Jogadores não poderão comprar.'
        - ''
        - '&aClique para ativar a venda'
    selling-not:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cDesativar venda'
      lore:
        - '&7Esta key está sendo vendida no momento.'
        - '&7Jogadores poderão comprar.'
        - ''
        - '&aClique para desativar a venda'

# Menu de seleção de economias
providers:
  name: '&8Selecionar economia'
  size: 27
  previous: 9
  next: 17
  back: 18
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]

# Menu de confirmação
confirm:
  name: '&8Confirmação de compra'
  size: 27
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  items:
    item-slot: 13
    confirm-slot: 11
    cancel-slot: 15
    confirm:
      material: 'WOOL:5'
      name: '&aConfirmar'
      lore: [ '&7Clique para &aconfirmar&7 a compra.' ]
    cancel:
      material: 'WOOL:14'
      name: '&cCancelar'
      lore: [ '&7Clique para &ccancelar&7 a compra.' ]

# Menu ativações
activations:
  name: '&8VIP ATIVAÇÕES'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
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

actionbar:
  not-cancelled: '&cA operação ainda não foi cancelada.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  help: |

    &bComandos do plugin:

    &b-> &f/vip &8-&7 Abre o menu principal
    &b-> &f/vips &8-&7 Veja os vips ativos.
    &b-> &f/keys &8-&7 Veja as chaves ativas.
    &b-> &f/tempovip &8-&7 Mostra o seu tempo de vip
    &b-> &f/trocarvip [vip] &8-&7 Trocqa o seu VIP atual por outro
    &b-> &f/usarkey [key] &8-&7 Ativa um VIP a partir de uma KEY
    &b-> &f/partyvip &8-&7 Mostra o progresso atual do party-vip
    &b-> &f/ativarvip [id] &8-&7 Ativa um VIP a partir do ID do bônus
    &b-> &f/bonusvip enviar [id] [player] &8-&7 Envia uma chave bônus para um jogador
    &b-> &f/bonusvip ativar [id] &8-&7 Ativa uma chave bônus
    &b-> &f/vendervip [id] [economia] [preço] &8-&7 Vende uma chave VIP
    &b-> &f/comprarvip [id] &8-&7 Compra uma chave VIP
    &b-> &f/cancelarvendavip [id] &8-&7 Cancela a venda de uma chave VIP

  help-admin: |

    &bComandos do plugin:

    &b-> &f/vip &8-&7 Abre o menu principal
    &b-> &f/vips [player] &8-&7 Veja os vips ativos.
    &b-> &f/keys [player/admin] &8-&7 Veja as chaves ativas.
    &b-> &f/trocarvip [vip] &8-&7 Trocqa o seu VIP atual por outro
    &b-> &f/vip info [id-vip] &8-&7 Vê as informações gerais do id selecionado.
    &b-> &f/tempovip [jogador] &8-&7 Mostra o seu tempo de vip ou de outro jogador
    &b-> &f/usarkey [key] &8-&7 Ativa um VIP a partir de uma KEY
    &b-> &f/partyvip &8-&7 Mostra o progresso atual do party-vip
    &b-> &f/ativarvip [id] &8-&7 Ativa um VIP a partir do ID do bônus
    &b-> &f/bonusvip dar [player/random] [vip] [duração] &8-&7 Dar uma chave bônus para um jogador
    &b-> &f/bonusvip enviar [id] [player] &8-&7 Envia uma chave bônus para um jogador
    &b-> &f/bonusvip ativar [id] &8-&7 Ativa uma chave bônus
    &b-> &f/vendervip [id] [economia] [preço] &8-&7 Vende uma chave VIP
    &b-> &f/comprarvip [id] &8-&7 Compra uma chave VIP
    &b-> &f/cancelarvendavip [id] &8-&7 Cancela a venda de uma chave VIP
    &b-> &f/congerlavip &8-&7 Congela/descongela o tempo dos vips
    &b-> &f/darvip [jogador] [vip] [tempo] &8-&7 Dá um determinado vip a um jogador
    &b-> &f/darchave [jogador] [vip] [tempo] &8-&7 Dá uma chave de um determinado vip a um jogador
    &b-> &f/setarvip [jogador] [vip] [tempo] &8-&7 Dá um determinado vip a um jogador, porém sem as mensagens e os comandos de ativação
    &b-> &f/gerarkey [vip] [tempo] [tipo] [usos] &8-&7 Cria uma key aleatória de um determinado vip
    &b-> &f/criarkey [vip] [tempo] [tipo] [usos] [key] &8-&7 Cria uma key customizada de um determinado vip
    &b-> &f/editarkey [key] [vip] [tempo] [tipo] [usos] &8-&7 Edita uma key
    &b-> &f/deletarkey [key] &8-&7 Deleta uma key
    &b-> &f/removervip [id] &8-&7 Remove um vip
    &b-> &f/removertempovip [id] [tempo] &8-&7 Remove tempo de um vip

  vip-found: '&cEste vip não foi encontrado. Disponíveis: &7{list}&c.'
  vip-found-player: '&cVocê não possui nenhum vip ativo.'
  vip-found-player-target: '&cO jogador {player} não possui nenhum vip ativo.'
  vip-set: '&aVocê setou o &r{vip}&a para o jogador &f{player}&a.'
  vip-add: '&aVocê adicionou o &r{vip}&a para o jogador &f{player}&a.'
  vip-trade: '&aVocê alterou seu vip para o &r{vip}&a.'
  vip-trade-target: '&aVocê alterou o vip do jogador &f{player}&a para o &r{vip}&a.'
  vip-time: |

    &aInformações do seu VIP:

    &7Seu VIP: &f{vip_display}
    &7Tag especial: &f{vip_prefix}

    &7Expira em: &f{expire_remaining}
    &7Ativado em: &f{activation_date} às {activation_hour}

  vip-time-target: |

    &aInformações do VIP de &f{player}&a:

    &7VIP: &f{vip_display}
    &7Tag especial: &f{vip_prefix}

    &7Expira em: &f{expire_remaining}
    &7Ativado em: &f{activation_date} às {activation_hour}

  vip-key-not-found: '&cEsta key {key} não existe.'
  vip-key-found: '&cEsta key {key} já existe.'
  vip-key-delete: '&aEsta key {key} foi deletada.'
  vip-key-generate: |

    &aInformações da KEY gerada:

    &7KEY: &f<click:suggest_command:{key}><hover:show_text:"<red>{key}<newline>Clique para copiar</red>">{key}</hover></click>
    &7VIP: &f{vip}

    &7Usos: &f{use}
    &7Duração: &f{duration}

  vip-key-edit: |

    &aInformações da KEY editada:

    &7KEY: &f<click:suggest_command:{key}><hover:show_text:"<red>{key}<newline>Clique para copiar</red>">{key}</hover></click>
    &7VIP: &f{vip}

    &7Usos: &f{use}
    &7Duração: &f{duration}

  vip-key-use: |

    &aVocê usou uma KEY VIP, informações:

    &7KEY: &f{key}
    &7VIP: &f{vip}

    &7Duração: &f{duration}

  vips-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>)&f {vip_display}&6 -> &7{expire_remaining}'
  vips-none: '&cVocê não possui nenhum vip.'
  vips-none-target: '&cO jogador {player} não possui nenhum vip.'
  vips: |

    &aInformações sobre os seus VIPs:
    &r
    &f  ID:            &fVIP:
    &r
    {format}

  vips-target: |

    &aInformações sobre os VIPs de &f{player}&a:

    &f  ID:            &fVIP:

    {format}

  vip-trade-found: '&cVocê não possui um VIP com id {id}.'
  vip-trade-found-target: '&cO jogador {player} não possui um VIP com id {id}.'
  vip-already: '&cVocê já está usando um VIP com o id {id}.'
  vip-already-target: '&cO jogador {player} já está usando um VIP com o id {id}.'
  vip-expired: '&cO seu VIP {id} está expirado.'
  vip-expired-target: '&cO VIP {id} do jogador {player} está expirado.'
  keys-format: '  &8(<click:suggest_command:{key}><hover:show_text:"<red>{key}<newline>Clique para copiar</red>">{key}</hover></click>)&f {vip_display}&6 -> &7{duration}'
  keys-none: '&cNão há nenhuma key disponível.'
  keys: |

    &aInformações sobre as KEYs disponíveis:

    &f  KEY:                      &fVIP:

    {format}

  keys-player-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>)&f {vip_display}&6 -> &7{expire_remaining}'
  keys-player-none: '&cVocê não possui nenhuma key.'
  keys-player: |

    &aInformações sobre as suas KEYs disponíveis:

    &f  KEY:                      &fVIP:

    {format}

  keys-target-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>)&f {vip_display}&6 -> &7{expire_remaining}'
  keys-target-none: '&cO jogador {player} não possui nenhuma key.'
  keys-target: |

    &aInformações sobre as KEYs de {player} disponíveis:

    &f  KEY:                      &fVIP:

    {format}

  vip-data-found: '&cNenhum VIP encontrado com o ID {id}.'
  vip-data-remove: '&aVIP {id} deletado.'
  vip-data-remove-permanent: '&cNão é possível alterar o tempo deste VIP, ele é permanente.'
  vip-data-remove-time: '&aTempo do VIP {id} alterado para duração: {time}.'
  shop-credit-has: '&cVocê não possui a quantia de {amount} créditos VIP.'
  shop-credit-spent: '&aVocê comprou na loja utilizando {amount} créditos VIP.'
  freeze-yes: '&aO tempo dos VIPS agora estão congelados neste servidor.'
  freeze-no: '&cO tempo dos VIPS não mais estão congelados neste servidor.'
  key-give: '&aVocê deu uma key do &r{vip}&a para o jogador &f{player}&a.'
  key-received: '&aVocê recebeu uma key do &r{vip}&a.'
  key-active: '&aVocê ativou sua key do &r{vip}&a de id {id}&a.'
  key-active-found: '&cEssa chave de id {id} não foi encontrada na sua conta.'
  key-copy: '&7Seu ID do VIP: &r {vip_display}&6 -> &7<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>'
  vip-info: |

    &aInformações sobre o VIP &7({id})&a de &f{player}&a:

    &7VIP: &r{vip_display}
    &7Tag Especial: &r{vip_prefix}

    &fStatus: &r{status}

    &7Expira em: &f{expire_remaining}
    &7Ativado em: &f{activation_date} às {activation_hour}

  bonus-give: '&aVocê deu um bônus do &r{vip}&a para o jogador &f{player}&a.'
  bonus-active: '&aVocê ativou seu bônus do &r{vip}&a de id {id}&a.'
  bonus-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>)&f {vip_display}&6 -> &7{expire_remaining}'
  bonus-none: '&cNão há nenhum bônus disponível.'
  bonus: |

    &aInformações sobre as KEYs disponíveis:

    &f  ID:            &fVIP:

    {format}

  bonus-not-found: '&cEste bônus de id {id} não existe.'
  digit-player: |

    &aDigite o PLAYER que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-price: |

    &aDigite o PREÇO que você quer.
    &7Para cancelar, digite &ncancelar&7.

  bonus-sent: '&aVocê enviou o bônus de id {id} ao jogador {player}.'
  provider-permission: '&cVocê não tem permissão para comercializar com esta economia.'
  change-price: '&aVocê alterou o preço para {price}.'
  key-selling: |

    &aVocê colocou uma chave à venda

    &7ID: &e{id}
    &7Preço: &e{price}
    &7Economia: &e{provider}

    &7VIP: &b{vip}
    &7Duração: &b{duration}

  key-selling-cancel: |

    &aVocê cancelou a venda de uma chave

    &7ID: &e{id}
    &7VIP: &b{vip}
    &7Duração: &b{duration}

  provider-found: '&cEste tipo de economia não foi encontrado. Disponíveis: &7{list}&c.'
  key-buy-found: '&cEssa chave de id {id} não foi encontrada para venda.'
  key-buy-self: '&cVocê não pode comprar sua própria chave.'
  key-buy-target: '&cEste jogador {player} não foi encontrado na base de dados.'
  key-buy-economy: '&cEsta economia não foi encontrada.'
  key-buy-offline: '&cEsta economia não permite que comercialize com o dono da venda offline.'
  key-buy: |

    &aVocê comprou uma chave VIP

    &7ID: &e{id}
    &7Preço: &e{price}
    &7Economia: &e{provider}

    &7VIP: &b{vip}
    &7Duração: &b{duration}

  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  sell-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>)&f {vip_display}&6 -> &7{expire_remaining} &6-> &a{price} {provider_abbreviated} &6-> &f{player}'
  sell-none: '&cNão há nenhuma key à venda.'
  sell: |

    &aInformações sobre KEYs à venda disponíveis:

    &f  KEY:                      &fVIP:

    {format}

  sell-target-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{id}<newline>Clique para copiar</red>">{id}</hover></click>)&f {vip_display}&6 -> &7{expire_remaining} &6-> &a{price} {provider_abbreviated}'
  sell-target-none: '&cNão há nenhuma key à venda deste jogador.'
  sell-target: |

    &aInformações sobre KEYs à venda de {player} disponíveis:

    &f  KEY:                      &fVIP:

    {format}

  credit-balance: |
    &aVocê possui: &f{amount}&a créditos.
  credit-balance-target: |
    &aO jogador &7{player}&a possui: &f{amount}&a créditos.
  credit-set: |
    &aVocê setou os tokens do jogador &7{player} &apara: &f{amount}&a créditos.
  credit-remove: |
    &aVocê removeu &f{amount}&a créditos do jogador &7{player}&a.
  credit-add: |
    &aVocê adicionou &f{amount}&a créditos para o jogador &7{player}&a.
  credit-send: |
    &aVocê enviou &f{amount}&a créditos para o jogador &7{player}&a.
  credit-received: |
    &aVocê recebeu &f{amount}&a créditos do jogador &7{player}&a.
  credit-self: |
    &cVocê não pode enviar créditos para sí mesmo.
  bonus-receive: '&aVocê recebeu um bônus do &r{vip}&a do jogador &f{player}&a.'
  trade-delay: '&cAguarde &e{time} &cpara trocar de vip novamente.'
  remove-player-none: '&cNenhum VIP pôde ser removido. O jogador {player} não possui VIPs ativos.'
  remove-player: '&aTodos os VIPs do jogador &f{player}&a foram removidos.'
]]>
</code-block>
</chapter>

<chapter title="vips.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
vips:
  iron:
    display: '&f[VIP Ferro]'
    prefix: '&f&l✔' # exclusivo yClans e yRankup
    # ONLINE -> O tempo do VIP é descontado apenas quando o jogador estiver online
    # SERVER -> O tempo do VIP é descontado apenas quando o servidor estiver online
    # BASIC -> O tempo do VIP é descontado até quando o servidor estiver offline
    time-type: 'SERVER'
    # Créditos VIP que serão dados ao jogador ao ativar este vip
    credit: 10.0
    # Valor que acumulará no party-vip
    party-vip-value: 10.0
    # Enviar a ativação pro menu de ativações do jogador
    activation-menu: false
    # Integração com o yLeague
    yleague:
      # Pontos que será dado no yLeague
      points: 10.0
      # Título da embed que é enviada no discord
      # Deixe '' para não enviar
      embed-title: 'VIP Ferro Ativado'
    # Sistema de upar o vip
    upgrade:
      vip-type: 'ouro'
      command: []
      message: |

        &b&lUPGRADE
        &aVocê upou do &f[VIP Ferro] &apara o &e&lVIP OURO
        &aVocê pagou &2$&a 10k em coins

      message-broadcast: ''
      price:
        price1:
          provider: 'money'
          price: 10000
    icon:
      material: 'IRON_INGOT'
      name: '&fVIP Ferro'
      lore: []
    announces:
      sound: ''
      effect: ''
      actionbar: '&7{player}&b acaba de ativar o &fVIP Ferro'
      title: '&7{player}&b ativou o<nl>&fVIP Ferro'
      chat: |

        &a&lVIPS
        &bO jogador &7{player} &bacaba de
        &bse tornar &7(&fVIP Ferro&7)&b.

      chat-private: |

        &a&lVIPS
        &7Recolha sua ativação no /vip

    discord:
      # exclusivo yDiscordHook
      # enviar o embed no privado
      discordhook:
        enable: true
        dm-embed: ''
      # enviar o embed em um chat
      webhook:
        enable: true
        chat-embed: 'activated'
    item:
      key-preview:
        material: TRIPWIRE_HOOK
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '', ' &7Vip: &f[VIP Ferro]', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara vender' ]
      key-sell-preview:
        material: TRIPWIRE_HOOK
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '', ' &7Vip: &f[VIP Ferro]', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara cancelar a venda' ]
      key-sell:
        material: TRIPWIRE_HOOK
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '', ' &7Vip: &f[VIP Ferro]', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', ' &fVendedor: &7{player}', '', '&aBotão &fESQUERDO &apara comprar' ]
      key-bonus-preview:
        material: TRIPWIRE_HOOK
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '', ' &7Vip: &f[VIP Ferro]', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara enviar' ]
      active:
        material: IRON_INGOT
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '' ,' &fAtivado por: &a{player}', '&f Status: &aAtivo', '', '&7 Ativado em: &f{activation_date} às {activation_hour}' , ' &7Expira em: &f {expire_remaining}' , '', '&eClique para copiar a KEY do vip']
      change:
        material: IRON_INGOT
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '', ' &fStatus: &eAGUARDANDO', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&cClique para usar este vip' ]
      expired:
        material: IRON_INGOT
        name: '&f[VIP Ferro] &8{id}'
        lore: [ '', ' &fStatus: &cEXPIRADO', ' &7Ativado em: &f{activation_date} às {activation_hour}', ''  ]
      activation:
        material: IRON_INGOT
        name: '&f[VIP Ferro]'
        lore: [ '&7Clique para coletar a ativação' ]
      upgrade:
        material: GOLD_INGOT
        name: '&f[VIP Ferro] -> &e&lVIP OURO'
        lore: [ '&7Faça o upgrade para o VIP OURO.', '', '&fPreço: &2$&a 10k em coins', '', '&aClique para upar' ]
    group-command:
      add: [ 'lp user {player} parent add vip_ferro' ]
      remove: [ 'lp user {player} parent remove vip_ferro' ]
    activation-commands: [ '100.0,give {player} iron_ingot 64' ]
    activation-items:
      item-1:
        chance: 100.0
        material: 'IRON_INGOT'
        name: '&fFerro do VIP'
        lore: []
        enchants: ['DURABILITY:1']
    bungee-activation:
      bungee1:
        server: 'mina'
        commands: [ '100.0,give {player} diamond 64' ]
        items: {}
  ouro:
    display: '&e&lVIP OURO'
    prefix: '&e&l✔' # exclusivo yClans e yRankup
    # ONLINE -> O tempo do VIP é descontado apenas quando o jogador estiver online
    # SERVER -> O tempo do VIP é descontado apenas quando o servidor estiver online
    # BASIC -> O tempo do VIP é descontado até quando o servidor estiver offline
    time-type: 'SERVER'
    # Créditos VIP que serão dados ao jogador ao ativar este vip
    credit: 20.0
    # Valor que acumulará no party-vip
    party-vip-value: 20.0
    # Enviar a ativação pro menu de ativações do jogador
    activation-menu: false
    # Sistema de upar o vip
    upgrade:
      vip-type: 'diamante'
      command: []
      message: |

        &b&lUPGRADE
        &aVocê upou do &e&lVIP OURO &apara o &b&lVIP DIAMANTE
        &aVocê pagou &2$&a 30k em coins

      message-broadcast: ''
      price:
        price1:
          provider: 'money'
          price: 30000
    icon:
      material: 'GOLD_INGOT'
      name: '&e&lVIP OURO'
      lore: []
    announces:
      sound: ''
      effect: ''
      actionbar: '&a{player}&f acaba de ativar o &e&lVIP OURO'
      title: '&a{player}&f ativou o <nl> &e&lVIP OURO'
      chat: |

        &a&lVIPS
        &fO jogador &a{player} &facaba de
        &fse tornar &e&lVIP OURO&f.

      chat-private: |

        &a&lVIPS
        &7Recolha sua ativação no /vip

    discord:
      # exclusivo yDiscordHook
      # enviar o embed no privado
      discordhook:
        enable: true
        dm-embed: ''
      # enviar o embed em um chat
      webhook:
        enable: true
        chat-embed: 'activated'
    item:
      key-preview:
        material: TRIPWIRE_HOOK
        name: '&e&lVIP OURO &8{id}'
        lore: [ '', ' &7Vip: &e&lVIP OURO', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara vender' ]
      key-sell-preview:
        material: TRIPWIRE_HOOK
        name: '&e&lVIP OURO &8{id}'
        lore: [ '', ' &7Vip: &e&lVIP OURO', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara cancelar a venda' ]
      key-sell:
        material: TRIPWIRE_HOOK
        name: '&e&lVIP OURO &8{id}'
        lore: [ '', ' &7Vip: &e&lVIP OURO', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', ' &fVendedor: &7{player}', '', '&aBotão &fESQUERDO &apara comprar' ]
      key-bonus-preview:
        material: TRIPWIRE_HOOK
        name: '&e&lVIP OURO &8{id}'
        lore: [ '', ' &7Vip: &e&lVIP OURO', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara enviar' ]
      active:
        material: GOLD_INGOT
        name: '&e&lVIP OURO &8{id}'
        lore: [ '', ' &fStatus: &aAtivo&f.', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '' ]
      change:
        material: GOLD_INGOT
        name: '&e&lVIP OURO &8{id}'
        lore: [ '', ' &fStatus: &eAguardando&f.', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&cClique para usar este vip' ]
      expired:
        material: GOLD_INGOT
        name: '&e&lVIP Ouro &8{id}'
        lore: [ '', ' &fStatus: &cExpirado&f.', ' &7Ativado em: &f{activation_date} às {activation_hour}', ''  ]
      activation:
        material: GOLD_INGOT
        name: '&e&lVIP Ouro'
        lore: [ '&7Clique para coletar a ativação' ]
      upgrade:
        material: DIAMOND
        name: '&e&lVIP OURO -> &b&lVIP DIAMANTE'
        lore: [ '&7Faça o upgrade para o VIP DIAMANTE.', '', '&fPreço: &2$&a 30k em coins', '', '&aClique para upar' ]
    group-command:
      add: [ 'lp user {player} parent add vip_ouro' ]
      remove: [ 'lp user {player} parent remove vip_ouro' ]
    activation-commands: [ '100.0,give {player} gold_ingot 64' ]
    activation-items:
      item-1:
        chance: 100.0
        material: 'GOLD_INGOT'
        name: '&6Ouro do VIP'
        lore: []
        enchants: ['DURABILITY:1']
  diamante:
    display: '&b&lVIP DIAMANTE'
    prefix: '&b&l✔' # exclusivo yClans e yRankup
    # ONLINE -> O tempo do VIP é descontado apenas quando o jogador estiver online
    # SERVER -> O tempo do VIP é descontado apenas quando o servidor estiver online
    # BASIC -> O tempo do VIP é descontado até quando o servidor estiver offline
    time-type: 'SERVER'
    # Créditos VIP que serão dados ao jogador ao ativar este vip
    credit: 30.0
    # Valor que acumulará no party-vip
    party-vip-value: 30.0
    # Enviar a ativação pro menu de ativações do jogador
    activation-menu: false
    # Sistema de upar o vip
    upgrade:
      vip-type: 'esmeralda'
      command: []
      message: |

        &b&lUPGRADE
        &aVocê upou do &b&lVIP DIAMANTE &apara o &a&lVIP ESMERALDA
        &aVocê pagou &2$&a 70k em coins

      message-broadcast: ''
      price:
        price1:
          provider: 'money'
          price: 70000
    icon:
      material: 'DIAMOND'
      name: '&b&lVIP DIAMANTE'
      lore: []
    announces:
      sound: ''
      effect: ''
      actionbar: '&a{player}&f acaba de ativar o &b&lVIP DIAMANTE'
      title: '&a{player}&f ativou o <nl> &b&lVIP DIAMANTE'
      chat: |

        &a&lVIPS
        &fO jogador &a{player} &facaba de
        &fse tornar &b&lVIP DIAMANTE&f.

      chat-private: |

        &a&lVIPS
        &7Recolha sua ativação no /vip

    discord:
      # exclusivo yDiscordHook
      # enviar o embed no privado
      discordhook:
        enable: true
        dm-embed: ''
      # enviar o embed em um chat
      webhook:
        enable: true
        chat-embed: 'activated'
    item:
      key-preview:
        material: TRIPWIRE_HOOK
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &7Vip: &b&lVIP DIAMANTE', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara vender' ]
      key-sell-preview:
        material: TRIPWIRE_HOOK
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &7Vip: &b&lVIP DIAMANTE', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara cancelar a venda' ]
      key-sell:
        material: TRIPWIRE_HOOK
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &7Vip: &b&lVIP DIAMANTE', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', ' &fVendedor: &7{player}', '', '&aBotão &fESQUERDO &apara comprar' ]
      key-bonus-preview:
        material: TRIPWIRE_HOOK
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &7Vip: &b&lVIP DIAMANTE', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara enviar' ]
      active:
        material: DIAMOND
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &fAtivado por: &a{player}', ' &fStatus: &aAtivo', '', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&eClique para copiar o ID do VIP' ]
      change:
        material: DIAMOND
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &fAtivado por: &a{player}', ' &fStatus: &eAguardando', '', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&eClique para copiar o ID do VIP' ]
      expired:
        material: DIAMOND
        name: '&b&lVIP DIAMANTE &8{id}'
        lore: [ '', ' &fAtivado por: &a{player}', ' &fStatus: &cExpirado', '', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&eClique para copiar o ID do VIP' ]
      activation:
        material: DIAMOND
        name: '&b&lVIP DIAMANTE'
        lore: [ '&7Clique para coletar a ativação' ]
      upgrade:
        material: EMERALD
        name: '&b&lVIP DIAMANTE -> &a&lVIP ESMERALDA'
        lore: [ '&7Faça o upgrade para o VIP ESMERALDA.', '', '&fPreço: &2$&a 70k em coins', '', '&aClique para upar' ]
    group-command:
      add: [ 'lp user {player} parent add vip_diamante' ]
      remove: [ 'lp user {player} parent remove vip_diamante' ]
    activation-commands: [ '100.0,give {player} diamond 22' ]
    activation-items:
      item-1:
        chance: 100.0
        material: 'DIAMOND'
        name: '&bDiamante do VIP'
        lore: []
        enchants: ['DURABILITY:1']
  esmeralda:
    display: '&a&lVIP ESMERALDA'
    prefix: '&a&l✔' # exclusivo yClans e yRankup
    # ONLINE -> O tempo do VIP é descontado apenas quando o jogador estiver online
    # SERVER -> O tempo do VIP é descontado apenas quando o servidor estiver online
    # BASIC -> O tempo do VIP é descontado até quando o servidor estiver offline
    time-type: 'SERVER'
    # Créditos VIP que serão dados ao jogador ao ativar este vip
    credit: 50.0
    # Valor que acumulará no party-vip
    party-vip-value: 50.0
    # Enviar a ativação pro menu de ativações do jogador
    activation-menu: false
    # Sistema de upar o vip
    upgrade:
      vip-type: ''
      command: []
      message: ''
      message-broadcast: ''
      price: {}
    icon:
      material: 'DIAMOND'
      name: '&a&lVIP ESMERALDA'
      lore: []
    announces:
      sound: ''
      effect: ''
      actionbar: '&a{player}&f acaba de ativar o &a&lVIP ESMERALDA'
      title: '&a{player}&f ativou o <nl> &a&lVIP ESMERALDA'
      chat: |

        &a&lVIPS
        &fO jogador &a{player} &facaba de
        &fse tornar &a&lVIP ESMERALDA&f.

      chat-private: |

        &a&lVIPS
        &7Recolha sua ativação no /vip

    discord:
      # exclusivo yDiscordHook
      # enviar o embed no privado
      discordhook:
        enable: true
        dm-embed: ''
      # enviar o embed em um chat
      webhook:
        enable: true
        chat-embed: 'activated'
    item:
      key-preview:
        material: TRIPWIRE_HOOK
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '', ' &7Vip: &a&lVIP ESMERALDA', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara vender' ]
      key-sell-preview:
        material: TRIPWIRE_HOOK
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '', ' &7Vip: &a&lVIP ESMERALDA', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara cancelar a venda' ]
      key-sell:
        material: TRIPWIRE_HOOK
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '', ' &7Vip: &a&lVIP ESMERALDA', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', ' &fStatus: &aVendendo por {price} {provider_abbreviated}', ' &fVendedor: &7{player}', '', '&aBotão &fESQUERDO &apara comprar' ]
      key-bonus-preview:
        material: TRIPWIRE_HOOK
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '', ' &7Vip: &a&lVIP ESMERALDA', ' &7ID: &f{id}', ' &7Duração: &f{expire_remaining}', '', '&aBotão &fESQUERDO &apara ativar', '&aBotão &fDIREITO &apara enviar' ]
      active:
        material: EMERALD
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '' ,' &fAtivado por: &a{player}', '&f Status: &aAtivo', '', ' &7Ativado em: &f{activation_date} às {activation_hour}' , ' &7Expira em: &f {expire_remaining}' , '', '&eClique para copiar a KEY do vip']
      change:
        material: EMERALD
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '', ' &fStatus: &eAguardando&f.', ' &7Expira em: &f{expire_remaining}', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&cClique &fESQUERDO&a para usar este vip', '&eClique DIREITO para copiar a KEY do vip' ]
      expired:
        material: EMERALD
        name: '&a&lVIP ESMERALDA &8{id}'
        lore: [ '', ' &fStatus: &cExpirado&f.', ' &7Ativado em: &f{activation_date} às {activation_hour}', '', '&eClique para copiar a KEY do vip'  ]
      activation:
        material: EMERALD
        name: '&a&lVIP ESMERALDA'
        lore: [ '&7Clique para coletar a ativação' ]
      upgrade:
        material: BARRIER
        name: '&cNenhum'
        lore: [ '&7Não há nenhum VIP para upar' ]
    group-command:
      add: [ 'lp user {player} parent add vip_esmeralda' ]
      remove: [ 'lp user {player} parent remove vip_esmeralda' ]
    activation-commands: [ '100.0,give {player} emerald 64' ]
    activation-items:
      item-1:
        chance: 100.0
        material: 'EMERALD'
        name: '&aEsmeralda do VIP'
        lore: []
        enchants: ['DURABILITY:1']
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static VipAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;VipAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(VipAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/103-yVips">Site do plugin yVips</a>
    </category>
</seealso>