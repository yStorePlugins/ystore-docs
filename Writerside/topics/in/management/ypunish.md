# yPunish
<secondary-label ref="management"/>

### Descrição
Gerencie e puna seus jogadores

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
<video src="//www.youtube.com/watch?v=keT6c1KN58I"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/punicoes - Abre o menu de punições
/punicoes pendentes - Abre o menu de punições pendentes de aprovação
/avisos - Abre o menu de avisos
/alts - Verifica os jogadores com mesmo IP
/ban - Bane um jogador
/kick - Kicka um jogador
/banip - Bane um ip
/tempban - Bane um jogador temporariamente
/mute - Muta um jogador
/tempmute - Muta um jogador temporariamente
/punir - Pune um jogador
/checkban - Verifica os banimentos de um jogador
/checkmute - Verifica os mutes de um jogador
/checkwarn - Verifica os avisos de um jogador
/iphistory - Verifica os IPS de um jogador
/staffhistory - Verifica o histórico de um staff
/unban - Desbane um jogador
/unmute - Desmuta um jogador
/unbanip - Desbane um ip
/verificar - Verifica se um jogador está banido e mutado 
/ verifica uma punição ou aviso
/warn - Avisa um jogador
/imune - Ativa
/desativa a imunidade
/ypunish reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ypunish.punishes - Permissão para o /punicoes
ypunish.punishes.others - Permissão para o /punicoes [player]
ypunish.punishes.staff - Permissão para o /punicoes de staff
ypunish.punishes.approve - Permissão para o /punicoes pendentes
ypunish.warns - Permissão para o /avisos
ypunish.warns.others - Permissão para o /avisos [player]
ypunish.warns.staff - Permissão para o /avisos de staff
ypunish.alts - Permissão para o /alts
ypunish.ban - Permissão para o /ban
ypunish.kick - Permissão para o /kick
ypunish.tempban - Permissão para o /tempban
ypunish.banip - Permissão para o /banip
ypunish.mute - Permissão para o /mute
ypunish.tempmute - Permissão para o /tempmute
ypunish.punish - Permissão para o /punir
ypunish.checkban - Permissão para o /checkban
ypunish.checkmute - Permissão para o /checkmute
ypunish.checkwarn - Permissão para o /checkwarn
ypunish.iphistory - Permissão para o /iphistory
ypunish.staffhistory - Permissão para o /staffhistory
ypunish.unban - Permissão para o /unban
ypunish.unmute - Permissão para o /unmute
ypunish.unbanip - Permissão para o /unbanip
ypunish.verify - Permissão para o /verify
ypunish.warn - Permissão para o /warn
ypunish.imune - Permissão para o /imune
ypunish.ypunish - Permissão para o /ypunish
ypunish.ban.approve - Permissão para aprovar o ban
ypunish.banip.approve - Permissão para aprovar o ban - ip
ypunish.tempban.approve - Permissão para aprovar o temp - ban
ypunish.mute.approve - Permissão para aprovar o mute
ypunish.tempmute.approve - Permissão para aprovar o temp - mute</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ypunish_current% - Retorna o valor de punições desde o último reinício
%ypunish_total% - Retorna o valor de punições desde a abertura do servidor
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPunish/
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── discord.yml
    ├── menus.yml
    ├── messages.yml
    ├── punishes.yml
    ├── settings.yml
    └── warns.yml
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
  ban: 'ban|banir'
  banip: 'banip|banirip'
  unban: 'unban|desbanir|pardon|perdoar'
  unbanip: 'unbanip|desbanirip'
  kick: 'kick|kickar|expulsar'
  mute: 'mute|mutar'
  unmute: 'unmute|desmutar'
  tempban: 'tempban|tempbanir'
  tempmute: 'tempmute|tempmutar'
  warn: 'warn|avisar'
  iphistory: 'iphistory|iphistorico'
  checkban: 'checkban|checarban'
  checkbanip: 'checkbanip|checarbanip'
  checkmute: 'checkmute|checarmute'
  checkwarn: 'checkwarn|checarwarn'
  verify: 'verify|verificar'
  punish: 'punish|punir'
  alts: 'alts'
  staffhistory: 'staffhistory'
  warns: 'warns|avisos'
  punishes: 'punishes|punicoes'
  imune: 'imune'
  ypunish: 'ypunish'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____
#  _   _ / ___|__ _ _ __ ___  _ __   ___
# | | | | |   / _` | '_ ` _ \| '_ \ / _ \
# | |_| | |__| (_| | | | | | | |_) | (_) |
#  \__, |\____\__,_|_| |_| |_| .__/ \___/
#  |___/                     |_|
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
  # Permitir entrar neste servidor mesmo banido
  # Necessário estar ativado para o sistema de redirect funcionar
  lobby-mode: true
  # Ative apenas se estiver usando o waterfall
  waterfall-kick: false
  # Permitir de conversar em chat custom quando estiver mutado
  # Chat custom = Legendchat, nChat...
  mute-custom-chat-enabled: false
  # Permitir de conversar em chat do minecraft
  # Chat do minecraft = Quando não tem plugin de chat
  mute-minecraft-chat-enabled: false
  # Permitir de usar comandos quando estiver mutado
  mute-commands-enabled: true
  # Whitelist de comandos permitidos para usar quando estiver mutado
  mute-commands-whitelist: []
  # Tempo para atualizar o report de punições
  # Em segundos
  report-time: 1800

proxy:
  # Nome deste servidor na config do proxy
  server-name: 'lobby'
  # Lista de servidores no proxy
  server-list:
    - 'lobby'
    - 'mina'

redirect:
  enabled: true
  # Tipos disponíveis
  # SERVER (envia para outro servidor)
  # LOCATION (envia para um local definido no próprio lobby)
  type: 'SERVER'
  # Servidor que irá redirecionar o jogador caso esteja banido
  # (legal para fazer uma área de jaula)
  server: 'mina'

discord:
  # exclusivo yDiscordHook
  # enviar o embed no privado
  discordhook:
    enabled: true
    dm-tempmute-embed: 'tempmute'
    dm-mute-embed: 'mute'
    dm-ban-embed: 'ban'
    dm-banip-embed: 'banip'
    dm-tempban-embed: 'tempban'
    dm-unban-embed: 'unban'
    dm-unmute-embed: 'unmute'
    dm-kick-embed: 'kick'
    dm-warn-embed: 'warn'
  # enviar o embed em um chat
  webhook:
    enabled: true
    chat-tempmute-embed: 'tempmute'
    chat-mute-embed: 'mute'
    chat-ban-embed: 'ban'
    chat-banip-embed: 'banip'
    chat-tempban-embed: 'tempban'
    chat-unban-embed: 'unban'
    chat-unmute-embed: 'unmute'
    chat-kick-embed: 'kick'
    chat-warn-embed: 'warn'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locais: {}
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
options:
  tempmute:
    url: ''
    username: 'yPunish - Mutado temporariamente'
  mute:
    url: ''
    username: 'yPunish - Mutado permanentemente'
  ban:
    url: ''
    username: 'yPunish - Banido permanentemente'
  tempban:
    url: ''
    username: 'yPunish - Banido temporariamente'
  kick:
    url: ''
    username: 'yPunish - Kickado'
  warn:
    url: ''
    username: 'yPunish - Avisado'
  unban:
    url: ''
    username: 'yPunish - Desbanido'
  unbanip:
    url: ''
    username: 'yPunish - Desbanido'
  unmute:
    url: ''
    username: 'yPunish - Desmutado'

embeds:
  mute:
    title: ':mailbox: Um novo jogador foi mutado permanentemente'
    thumbnail: 'https://minotar.net/body/{player}/100.png'
    color: '#fff'
    content: ''
    footer:
      text: 'yStore © Todos os direitos reservados'
      image: ''
    fields:
      id:
        inline: true
        header: 'Punição Nº'
        content: '```#{id}```'
      player:
        inline: true
        header: 'Player'
        content: '```{player}```'
      sender:
        inline: true
        header: 'Staff'
        content: '```{sender}```'
      reason:
        inline: true
        header: 'Motivo'
        content: '```{reason}```'
      proof:
        inline: true
        header: 'Prova'
        content: '```{proof}```'
      duration:
        inline: true
        header: 'Término'
        content: '```Nunca```'
  tempmute:
    title: ':mailbox: Um novo jogador foi mutado temporariamente'
    thumbnail: 'https://minotar.net/body/{player}/100.png'
    color: '#fff'
    content: ''
    footer:
      text: 'yStore © Todos os direitos reservados'
      image: ''
    fields:
      id:
        inline: true
        header: 'Punição Nº'
        content: '```#{id}```'
      player:
        inline: true
        header: 'Player'
        content: '```{player}```'
      sender:
        inline: true
        header: 'Staff'
        content: '```{sender}```'
      reason:
        inline: true
        header: 'Motivo'
        content: '```{reason}```'
      proof:
        inline: true
        header: 'Prova'
        content: '```{proof}```'
      duration:
        inline: true
        header: 'Término'
        content: '```{expire_date} às {expire_hour}```'
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

# Menu de avisos
warns:
  name: '&8Punições'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 47
  # Item do warn
  items:
    active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fAviso #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Avisado por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - '&f> &7Aviso: &c#{min}/{max}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
    inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fAviso #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Avisado por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - '&f> &7Aviso: &c#{min}/{max}'
        - ''
        - '&cEsta punição já expirou'
  # Seletor dos tops
  selector:
    slot: 49
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor de STATUS'
    # Tipos do seletor
    types:
      active:
        enabled: true
        name: 'Ativos'
      inactive:
        enabled: true
        name: 'Inativos'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de avisos para staff
warns-staff:
  name: '&8Punições'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  info-slot: 51
  # Item do warn
  items:
    info:
      material: '{player}'
      name: '&aSeus Avisos'
      lore:
        - '&7Aqui estão concentrados os avisos'
        - '&7que você recebeu.'
        - ''
        - '&aClique para abrir'
    active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fAviso #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador avisado: &c{punished}'
        - '&f> &7Avisado por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - '&f> &7Aviso: &c#{min}/{max}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para editar'
    inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fAviso #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Jogador avisado: &c{punished}'
        - '&f> &7Avisado por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - '&f> &7Aviso: &c#{min}/{max}'
        - ''
        - '&cEsta punição já expirou'
        - ''
        - '&aClique para editar'
  # Seletor dos tops
  selector:
    slot: 49
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor de STATUS'
    # Tipos do seletor
    types:
      active:
        enabled: true
        name: 'Ativos'
      inactive:
        enabled: true
        name: 'Inativos'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de editar o aviso
warn-edit:
  name: '&8Punições'
  size: 27
  back-slot: 9
  server-slot: 12
  proof-slot: 15
  # Item do warn
  items:
    server:
      material: 'BOOK'
      name: '&eEditar Servidor'
      lore:
        - ''
        - '&7Atual: &f{server}'
        - ''
        - '&aClique para editar'
    proof:
      material: 'EMERALD'
      name: '&eProva'
      lore:
        - ''
        - '&7Atual: &f{proof}'
        - ''
        - '&aClique para editar'

# Menu de punições
punishes:
  name: '&8Punições'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 47
  # Item do warn
  items:
    temp-ban-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Temporário #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Banido TEMPORARIAMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
    temp-ban-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fBanimento Temporário #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Banido TEMPORARIAMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
    temp-mute-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fMute Temporário #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Mutado TEMPORARIAMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
    temp-mute-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fMute Temporário #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Mutado TEMPORARIAMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
    mute-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fMute Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Mutado PERMANENTEMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
    mute-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fMute Permanente #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Mutado PERMANENTEMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
    ban-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
    ban-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fBanimento Permanente #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
  # Seletor dos tops
  selector:
    slot: 49
    material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
    name: '&aSeletor de TIPO'
    # Tipos do seletor
    types:
      ban:
        enabled: true
        name: 'Ban'
      mute:
        enabled: true
        name: 'Mute'
      temp-ban:
        enabled: true
        name: 'Temp-Ban'
      temp-mute:
        enabled: true
        name: 'Temp-Mute'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'
  # Seletor dos tops
  selector-status:
    slot: 51
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor de STATUS'
    # Tipos do seletor
    types:
      active:
        enabled: true
        name: 'Ativos'
      inactive:
        enabled: true
        name: 'Inativos'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de punições
punishes-staff:
  name: '&8Punições'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  info-slot: 47
  approve-slot: 45
  # Item do warn
  items:
    info:
      material: '{player}'
      name: '&aSuas Punições'
      lore:
        - '&7Aqui estão concentrados as punições'
        - '&7que você recebeu.'
        - ''
        - '&aClique para abrir'
    approve:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aPunições Pendentes'
      lore:
        - '&7Aqui estão concentradas as punições'
        - '&7que ainda não receberam aprovação.'
        - ''
        - '&aClique para abrir'
    temp-ban-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Temporário #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Banido TEMPORARIAMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para editar'
    temp-ban-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fBanimento Temporário #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Banido TEMPORARIAMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
        - ''
        - '&aClique para editar'
    temp-mute-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fMute Temporário #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Mutado TEMPORARIAMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para editar'
    temp-mute-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fMute Temporário #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Mutado TEMPORARIAMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
        - ''
        - '&aClique para editar'
    mute-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fMute Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Mutado PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para editar'
    mute-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fMute Permanente #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Mutado PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
        - ''
        - '&aClique para editar'
    ban-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para editar'
    ban-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fBanimento Permanente #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
        - ''
        - '&aClique para editar'
    banip-active:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7IP punido: &c{punished}'
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para editar'
    banip-inactive:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&fBanimento Permanente #{id} &7(&cInativo&7)'
      lore:
        - ''
        - '&f> &7IP punido: &c{punished}'
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&cEsta punição já expirou'
        - ''
        - '&aClique para editar'
  # Seletor dos tops
  selector:
    slot: 49
    material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
    name: '&aSeletor de TIPO'
    # Tipos do seletor
    types:
      ban:
        enabled: true
        name: 'Ban'
      mute:
        enabled: true
        name: 'Mute'
      temp-ban:
        enabled: true
        name: 'Temp-Ban'
      temp-mute:
        enabled: true
        name: 'Temp-Mute'
      banip:
        enabled: true
        name: 'Ban-IP'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'
  # Seletor dos tops
  selector-status:
    slot: 51
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor de STATUS'
    # Tipos do seletor
    types:
      active:
        enabled: true
        name: 'Ativos'
      inactive:
        enabled: true
        name: 'Inativos'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de editar a punição
punish-edit:
  name: '&8Punições'
  size: 27
  back-slot: 9
  server-slot: 12
  proof-slot: 13
  reason-slot: 14
  # Item do warn
  items:
    server:
      material: 'BOOK'
      name: '&eEditar Servidor'
      lore:
        - ''
        - '&7Atual: &f{server}'
        - ''
        - '&aClique para editar'
    proof:
      material: 'EMERALD'
      name: '&eProva'
      lore:
        - ''
        - '&7Atual: &f{proof}'
        - ''
        - '&aClique para editar'
    reason:
      material: 'PAPER'
      name: '&aMotivo'
      lore:
        - ''
        - '&7Atual: &f{reason}'
        - ''
        - '&aClique para editar'

# Menu de punições para aprovar
punishes-staff-approve:
  name: '&8Punições'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  info-slot: 47
  # Item do warn
  items:
    temp-ban:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Temporário #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Banido TEMPORARIAMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para aprovar'
    temp-mute:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fMute Temporário #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Mutado TEMPORARIAMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para aprovar'
    mute:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fMute Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Mutado PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para aprovar'
    ban:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7Jogador punido: &c{punished}'
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para aprovar'
    banip:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&fBanimento Permanente #{id} &7(&aAtivo&7)'
      lore:
        - ''
        - '&f> &7IP punido: &c{punished}'
        - '&f> &7Banido PERMANENTEMENTE por: &c{sender}'
        - ''
        - '&f> &7Servidor: &f{server}'
        - '&f> &7Motivo: &f{reason}'
        - '&f> &7Prova: &f{proof}'
        - ''
        - '&fTérmino: &c{expire_date} às {expire_hour}'
        - ''
        - '&aClique para aprovar'
  # Seletor dos tops
  selector:
    slot: 49
    material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
    name: '&aSeletor de TIPO'
    # Tipos do seletor
    types:
      ban:
        enabled: true
        name: 'Ban'
      mute:
        enabled: true
        name: 'Mute'
      temp-ban:
        enabled: true
        name: 'Temp-Ban'
      temp-mute:
        enabled: true
        name: 'Temp-Mute'
      banip:
        enabled: true
        name: 'Ban-IP'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'
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

announces:
  ban:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi punido por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &cNunca

  banip:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &cSeu IP &e{punished}&f foi punido por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &cNunca

  tempban:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi punido temporariamente por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &c{expire_date} às {expire_hour}

  mute:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi mutado por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &cNunca

  tempmute:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi mutado temporariamente por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &c{expire_date} às {expire_hour}

  warn:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi avisado por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fAviso: &c#{min}/{max}

  kick:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi expulso por &c{sender}
      &fMotivo: &c{reason}
      &fProva: &c{proof}

  kick-all:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &cTodos os jogadores foram expulsos por &c{sender}
      &fMotivo: &c{reason}
      &fProva: &c{proof}

  unban:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi desbanido por &c{sender}
      &fServidor: &c{server}

  unbanip:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &cO IP &e{punished}&f foi desbanido por &c{sender}
      &fServidor: &c{server}

  unmute:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &c{punished}&f foi desmutado por &c{sender}
      &fServidor: &c{server}

  #

logout:
  ban: |

    &c&lPUNIÇÕES

    <s><s><s><s><s><s><s><s>&cVocê&f foi punido PERMANENTEMENTE por &c{sender}

    &fServidor: &c{server}
    &fMotivo: &c{reason}
    &fProva: &c{proof}

    &fTérmino: &cNunca

    &eEsta punição possui o id &c#{id}&e, para contestá-la acesse google.com.br

  tempban: |

    &c&lPUNIÇÕES

    <s><s><s><s><s><s><s><s>&cVocê&f foi punido temporariamente por &c{sender}

    &fServidor: &c{server}
    &fMotivo: &c{reason}
    &fProva: &c{proof}

    &fTérmino: &c{expire_date} às {expire_hour}

    &eEsta punição possui o id &c#{id}&e, para contestá-la acesse google.com.br

  banip: |

    &c&lPUNIÇÕES

    <s><s><s><s><s><s><s><s>&cSeu IP &e{punished}&f foi punido por &c{sender}

    &fServidor: &c{server}
    &fMotivo: &c{reason}
    &fProva: &c{proof}

    &fTérmino: &c{expire_date} às {expire_hour}

    &eEsta punição possui o id &c#{id}&e, para contestá-la acesse google.com.br

  kick: |

    &c&lPUNIÇÕES

    <s><s><s><s><s><s><s><s>&cVocê&f foi kickado por &c{sender}

    &fMotivo: &c{reason}
    &fProva: &c{proof}

  #

private:
  mute:
    actionbar: ''
    title: ''
    chat: ''
  tempmute:
    actionbar: ''
    title: ''
    chat: ''
  warn:
    actionbar: ''
    title: ''
    chat: ''
  unmute:
    actionbar: ''
    title: ''
    chat: ''
  ban:
    actionbar: ''
    title: ''
    chat: ''
  banip:
    actionbar: ''
    title: ''
    chat: ''
  tempban:
    actionbar: ''
    title: ''
    chat: ''
  #

chatting:
  mute:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &cVocê&f foi mutado por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &cNunca

      &eEsta punição possui o id &c#{id}&e, para contestá-la acesse google.com.br

  tempmute:
    actionbar: ''
    title: ''
    chat: |

      &c&lPUNIÇÕES
      &cVocê&f foi mutado temporariamente por &c{sender}
      &fServidor: &c{server}
      &fMotivo: &c{reason}
      &fProva: &c{proof}
      &fTérmino: &c{expire_date} às {expire_hour}

      &eEsta punição possui o id &c#{id}&e, para contestá-la acesse google.com.br

  #

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  targetip: '&cIP {ip} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/punicoes &8- &7Abre o menu de punições.
    &a/avisos &8- &7Abre o menu de avisos.

  help-admin: |

    &a/punicoes &8- &7Abre o menu de punições.
    &a/avisos &8- &7Abre o menu de avisos.

    &a/ban <player> <server/all> <prova/null> <motivo> &8- &7Executa um banimento.
    &a/kick <player/all> <prova/null> <motivo> &8- &7Executa um kick.
    &a/banip <player/ip> <server/all> <prova/null> <motivo> &8- &7Executa um banimento no IP.
    &a/mute <player> <server/all> <prova/null> <motivo> &8- &7Executa um mute.
    &a/punir <player> <motivo> <prova/null> <server/all> &8- &7Executa uma punição.
    &a/tempban <player> <tempo> <server/all> <prova/null> <motivo> &8- &7Executa um banimento temporário.
    &a/tempmute <player> <tempo> <server/all> <prova/null> <motivo> &8- &7Executa um mute temporário.
    &a/checkban <player> &8- &7Verifica os banimentos de um player.
    &a/checkmute <player> &8- &7Verifica os mutes de um player.
    &a/checkwarn <player> &8- &7Verifica os avisos de um player.
    &a/iphistory <player> &8- &7Verifica os IPS de um player.
    &a/staffhistory <player> &8- &7Verifica o histórico de um staff.
    &a/unban <player> &8- &7Desbane um jogador.
    &a/unbanip <player> &8- &7Desbane um IP.
    &a/unmute <player> &8- &7Desmuta um jogador.
    &a/verificar <player/id> &8- &7Verifica se o jogador está banido e mutado / verifica uma punição ou aviso.
    &a/warn <player> <server/all> <prova/null> <tipo> &8- &7Avisa um jogador.
    &a/ypunish reload &8- &7Recarrega as configurações.

  yourself: '&cVocê não pode aplicar punições para sí mesmo.'
  not-ban: '&cEste jogador {player} não possui nenhum banimento em registro. &7Server: {server}'
  not-banip: '&cEste IP {ip} não possui nenhum banimento em registro. &7Server: {server}'
  not-mute: '&cEste jogador {player} não possui nenhum mute em registro. &7Server: {server}'
  not-warn: '&cEste jogador {player} não possui nenhum warn em registro. &7Server: {server}'
  already-ban: '&cEste jogador {player} já está PERMANENTEMENTE banido. &7Server: {server}'
  already-banip: '&cEste IP {ip} já está PERMANENTEMENTE banido. &7Server: {server}'
  already-mute: '&cEste jogador {player} já está PERMANENTEMENTE mutado. &7Server: {server}'
  applied-ban: '&aO jogador &f{player} &afoi banido permanentemente. &7Server: {server}'
  applied-banip: '&aO IP &f{ip} &afoi banido permanentemente. &7Server: {server}'
  applied-tempban: '&aO jogador &f{player} &afoi banido temporariamente. &7Server: {server}'
  applied-mute: '&aO jogador &f{player} &afoi mutado permanentemente. &7Server: {server}'
  applied-tempmute: '&aO jogador &f{player} &afoi mutado temporariamente. &7Server: {server}'
  applied-kick: '&aO jogador &f{player} &afoi expulso.'
  applied-kick-all: '&aVocê expulsou todos os jogadores.'
  applied-unban: '&aO jogador &f{player} &afoi desbanido. &7Server: {server}'
  applied-unbanip: '&aO IP &f{ip} &afoi desbanido. &7Server: {server}'
  applied-unmute: '&aO jogador &f{player} &afoi desmutado. &7Server: {server}'
  applied-warn: '&aO jogador &f{player} &afoi avisado. &7Server: {server}'
  report: |

    &a&lRELATÓRIO
    &7Confira o relatório atual das punições aplicadas

    &f-> &aPunições desde o último reinício: &b{current}
    &f-> &aPunições totais em toda a rede: &b{total}

  history: |
    &aHistórico de IP do jogador &7{player}

    &fAtual: &b{ip}

    &fOutros IPs: &7({list})
  checkban-format: '&f> <click:suggest_command:/verificar {id}><hover:show_text:"<red>#{id}<newline>Clique para copiar</red>">#{id}</hover></click> &7- &6{sender} &7- &b{server} &7- &8({status}&8)'
  checkban-temp-format: '&f> #{id} &7- &6{sender} &7- &a{expire_date} às {expire_hour} &7- &b{server} &7- &8({status}&8)'
  checkban: |

    &aHistórico de BANIMENTOS do jogador &7{player}

    {format}

    &7Clique em um #ID para verificar as informações completas
    &ePágina &a{page} &ede &a{total_page}
    <click:suggest_command:/checkban {player} {back}>❮ Anterior</click> <click:suggest_command:/checkban {player} {next}>Próxima ❯</click>

  checkbanip-format: '&f> <click:suggest_command:/verificar {id}><hover:show_text:"<red>#{id}<newline>Clique para copiar</red>">#{id}</hover></click> &7- &6{sender} &7- &b{server} &7- &8({status}&8)'
  checkbanip: |

    &aHistórico de BANIMENTOS do IP &7{ip}

    {format}

    &7Clique em um #ID para verificar as informações completas
    &ePágina &a{page} &ede &a{total_page}
    <click:suggest_command:/checkbanip {ip} {back}>❮ Anterior</click> <click:suggest_command:/checkbanip {ip} {next}>Próxima ❯</click>

  checkmute-format: '&f> <click:suggest_command:/verificar {id}><hover:show_text:"<red>#{id}<newline>Clique para copiar</red>">#{id}</hover></click> &7- &6{sender} &7- &b{server} &7- &8({status}&8)'
  checkmute-temp-format: '&f> #{id} &7- &6{sender} &7- &a{expire_date} às {expire_hour} &7- &b{server} &7- &8({status}&8)'
  checkmute: |

    &aHistórico de MUTES do jogador &7{player}

    {format}

    &7Clique em um #ID para verificar as informações completas
    &ePágina &a{page} &ede &a{total_page}
    <click:suggest_command:/checkmute {player} {back}>❮ Anterior</click> <click:suggest_command:/checkmute {player} {next}>Próxima ❯</click>

  checkwarn-format: '&f> <click:suggest_command:/verificar {id}><hover:show_text:"<red>#{id}<newline>Clique para copiar</red>">#{id}</hover></click> &7- &6{sender} &7- &b{server} &7- &8({status}&8)'
  checkwarn: |

    &aHistórico de WARNS do jogador &7{player}

    {format}

    &7Clique em um #ID para verificar as informações completas
    &ePágina &a{page} &ede &a{total_page}
    <click:suggest_command:/checkwarn {player} {back}>❮ Anterior</click> <click:suggest_command:/checkwarn {player} {next}>Próxima ❯</click>

  staffhistory-format: '&f> <click:suggest_command:/verificar {id}><hover:show_text:"<red>#{id}<newline>Clique para copiar</red>">#{id}</hover></click> &7- &6{type} &7- &6{punished} &7- &b{server} &7- &8({status}&8)'
  staffhistory: |

    &aHistórico de PUNIÇÕES APLICADAS do staff &7{player}

    {format}

    &7Clique em um #ID para verificar as informações completas
    &ePágina &a{page} &ede &a{total_page}
    <click:suggest_command:/staffhistory {player} {back}>❮ Anterior</click> <click:suggest_command:/staffhistory {player} {next}>Próxima ❯</click>

  info: |

    &aInformações do jogador &7{player}

    &f> Banido: &r{ban}
    &f> Mutado: &r{mute}

  info-punish: |

    &aInformações da punição &7#{id}

    &f> Tipo: &a{type}
    &f> Status: &r{status}

    &f> Jogador punido: &c{punished}
    &f> Staff: &c{sender}

    &f> Servidor: &c{server}
    &f> Motivo: &c{reason}
    &f> Prova: &c{proof}

    &f> Término: &e{formatted_expire_date}

  info-warn: |

    &aInformações do aviso &7#{id}

    &f> Status: &r{status}

    &f> Jogador avisado: &c{punished}
    &f> Staff: &c{sender}

    &f> Servidor: &c{server}
    &f> Motivo: &c{reason}
    &f> Prova: &c{proof}

    &f> Término: &e{formatted_expire_date}

  not-found: '&cNenhum jogador, punição ou aviso foi encontrado(a) de acordo com o dado fornecido {data}.'
  not-found-alt: '&cNenhum jogador ou IP foi encontrado de acordo com o dado fornecido {data}.'
  not-found-warn: |
    &cEste tipo de warn não foi encontrado.
    &7Disponíveis: {list}
  not-found-punish: |
    &cEste tipo de punição não foi encontrada.
    &7Disponíveis: {list}

  punish-format: '&6>&f <click:suggest_command:/punir {player} {punish}><hover:show_text:"<red>/punir {player} {reason}<newline>Clique para copiar</red>">{reason}</hover></click>'
  punish: |

    &aSelecione um dos motivos abaixos

    {format}

    &7Clique em um motivo para punir o jogador {player}

  alts: |

    &aInformações do IP &7{ip}

    &f> Usuários encontrados: &a{list}

    &7Estes são todos os usuários que utilizaram do mesmo IP.

  change-server: '&aServidor alterado para &f{server}&a.'
  change-proof: '&aProva alterado para &f{proof}&a.'
  change-reason: '&aMotivo alterado para &f{reason}&a.'
  digit-server: |

    &aDigite o SERVIDOR que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-proof: |

    &aDigite a PROVA que você quer.
    &7Para cancelar, digite &ncancelar&7.

  digit-reason: |

    &aDigite o MOTIVO que você quer.
    &7Para cancelar, digite &ncancelar&7.

  set-local: '&aLocal setado com sucesso.'
  imune: '&cO jogador {player} está imune.'
  imune-on: '&aImunidade ativada.'
  imune-off: '&cImunidade desativada.'
]]>
</code-block>
</chapter>

<chapter title="punishes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
punishes:
  chatting:
    reason: 'Ofensa-Chat'
    # Permissão para executar a punição
    permission: 'ypunish.punish.chatting'
    # Mensagem de permissão
    message: '&cVocê precisa ser SUPORTE para executar esta punição.'
    # Tipo de punição
    # BAN - TEMPBAN - MUTE - TEMPMUTE - KICK
    type: 'TEMPMUTE'
    # Duração da punição (apenas para o TEMPMUTE e TEMPBAN)
    duration: 10
]]>
</code-block>
</chapter>

<chapter title="settings.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____
#  _   _ / ___|__ _ _ __ ___  _ __   ___
# | | | | |   / _` | '_ ` _ \| '_ \ / _ \
# | |_| | |__| (_| | | | | | | |_) | (_) |
#  \__, |\____\__,_|_| |_| |_| .__/ \___/
#  |___/                     |_|
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
]]>
</code-block>
</chapter>

<chapter title="warns.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
warns:
  chatting:
    reason: 'Ofensa-Chat'
    # máximo de warns para executar o comando
    max: 2
    # em segundos
    expire: 60
    # comando que será executado ao atingir o max
    commands: [ "tempmute {player} 1d {server} null Ofensa-Chat" ]
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/114-yPunish">Site do plugin yPunish</a>
    </category>
</seealso>