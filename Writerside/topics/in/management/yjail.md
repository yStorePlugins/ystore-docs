# yJail
<secondary-label ref="management"/>

### Descrição
Prenda seus jogadores malfeitores e faça-os quebrar blocos duros!

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
<video src="//www.youtube.com/watch?v=p32fkh-_VGM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/jail - Abre o menu de presos
/presos - Abre o menu de presos
/soltar - Solta um jogador
/jail setarsaida - Seta a saída da jail
/jail setarjail - Seta o local da jail
/jail soltar - Solta um jogador
/jail [player] - Prende um jogador
/jail ajuda - Mostra a mensagem de ajuda
/jail reload - Recarrega os arquivos de configuração</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yjail.use - Permissão para o /jail e /presos
yjail.release - Permissão para o /jail soltar e /soltar
yjail.arrest - Permissão para o /jail [player]
yjail.admin.setexit - Permissão para o /jail setexit
yjail.admin.setlocation - Permissão para o /jail setjail
yjail.admin.reload - Permissão para o /jail reload
yjail.vanish.bypass - Permissão para o player de fora (solto) conseguir enxergar o preso
yjail.vanish.bypass.arrested - Permissão para o player preso conseguir enxergar o solto
yjail.staff - Permissão para ser reconhecido como staff</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yJail/
    ├── jails/
    │    └── obsidian.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="jails" collapsible="true">
<chapter title="obsidian.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&5Prisão de Obsidian'
location: ''

# Bloco que o jogador irá quebrar para reduzir a pena
block:
  type: 'OBSIDIAN'
  # tempo que irá reduzir da pena, em segundos
  time-reduce: 10

# Comandos liberados
allowed-commands: [ '/jail' ]

# Comandos que serão executados no jogador ao ser preso
# Placeholder de player: {player}
arrested-commands: []

# Comandos que serão executados no jogador ao ser solto
# Placeholder de player: {player}
released-commands: []

# Ferramenta para quebrar o bloco
tool:
  material: 'DIAMOND_PICKAXE'

release:
  enabled: true
  # Permissão para poder soltar
  permission: ''
  # Preço para libertar o prisioneiro
  prices:
    price1:
      provider: 'money'
      amount: 1000.0

increase:
  enabled: true
  # Permissão para poder aumentar a pena
  permission: ''
  # Tempo que irá aumentar, em segundos
  time: 60
  # Delay para aumentar novamente, em segundos
  delay: 3600
  # Preço para libertar o prisioneiro
  prices:
    price1:
      provider: 'money'
      amount: 1000.0

tax:
  enabled: true
  # Taxa que irá cobrar do jogador, em %
  taxes:
    tax1:
      provider: 'money'
      amount: 10.0

messages:
  arrested: |

    &cVocê foi preso por &f{staff}
    &cTempo: &f{time}&c.
    &cMotivo: &f{reason}&c.

  stuck: |

    &cVocê está preso por &f{time_left}&c.
    &cMotivo: &f{reason}&c.

  reduce: '&aPena reduzida em &f{time}&a.'
  actionbar: '&cVocê ainda ficará preso por {time_left}&c.'
  released: '&aSua pena acabou. Você está livre.'

broadcast:
  arrested:
    chat: |

      &f{player}&c foi preso por &f{staff}
      &cTempo: &f{time}&c.
      &cMotivo: &f{reason}&c.

    actionbar: ''
    title: ''
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
  jail: 'jail|prender'
  release: 'release|soltar'
  prisoners: 'prisoners|prisioneiros|presos'
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

# Quebrar somente com o item dado pelo plugin?
break-only-plugin: true

# Diminuir o tempo de jogadores offline
minus-offline: false

# Prender por IP
arrest-ip: false

# Tag para o jogador preso
# é uma placeholder relacional
# Placeholder: %rel_yjail_arrested_tag%
tag: '&c[PRESO]'

# NBT de Itens que não serão guardados, mas sim deletados
nbt-item-delete:
  - 'yEventos-Item'
  - 'yGuerra-Item'
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
    permission: 'yjail.provider.money'
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
  name: '&8Presos online'
  size: 54
  slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
  previous-slot: 9
  next-slot: 17
  items:
    arrested:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&cTempo: &f{time}&c'
        - '&cTempo Restante: &f{time_left}&c'
        - '&cMotivo: &f{reason}&c'
        - ''
        - '&f > &a{money_increase} coins &fp/ aumentar &7({increase_time})&f.'
        - '&f > &a{money_release} coins &fp/ soltar.'
        - ''
        - '&aClique para visualizar opções.'

# Menu de opções
options:
  name: '&8{player}'
  size: 27
  back-slot: 9
  release-slot: 12
  increase-slot: 14
  items:
    release:
      material: 'FEATHER'
      name: '&aSoltar'
      lore:
        - ''
        - '&f > &a{money_release} coins &fp/ soltar.'
        - ''
        - '&aClique para pagar a fiança.'
    release-no:
      material: 'FEATHER'
      name: '&cSoltar'
      lore:
        - '&cVocê não pode soltar esse jogador.'
    release-permission:
      material: 'FEATHER'
      name: '&cSoltar'
      lore:
        - '&cVocê não tem permissão para soltar.'
    increase:
      material: 'BARRIER'
      name: '&aAumentar Pena'
      lore:
        - ''
        - '&f > &a{money_increase} coins &fp/ aumentar &7({increase_time})&f.'
        - ''
        - '&aClique para aumentar a pena.'
    increase-no:
      material: 'BARRIER'
      name: '&cAumentar Pena'
      lore:
        - '&cVocê não pode aumentar a pena desse jogador.'
    increase-already:
      material: 'BARRIER'
      name: '&cAumentar Pena'
      lore:
        - '&cVocê já aumentou a pena desse jogador.'
    increase-wait:
      material: 'BARRIER'
      name: '&cAumentar Pena'
      lore:
        - '&cAguarde {time} para aumentar a pena desse jogador.'
    increase-permission:
      material: 'BARRIER'
      name: '&cAumentar Pena'
      lore:
        - '&cVocê não tem permissão para aumentar a pena.'
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

    &aPrisão comandos:

    &a> /jail
    &a> /jail setarsaida
    &a> /jail setarjail <jail>
    &a> /jail <player> <jail> <tempo> <motivo>
    &a> /jail soltar <player>

  jail-list: |
    &cJail não encontrada.
    &cJail disponíveis: &f{list}
  set-exit: '&aLocal da saída definido com sucesso.'
  set-jail: '&aLocal da JAIL definido com sucesso.'
  arrest: '&aVocê prendeu o jogador &f{player}&a.'
  jail-location: '&cA entrada da jail não está setada.'
  exit-location: '&cA saída da jail não está setada.'
  released: '&aVocê soltou o jogador &f{player}&a.'
  arrest-self: '&cVocê não pode prender a sí mesmo.'
  arrest-staff: '&cVocê não pode prender este jogador.'
  not-arrested: '&cO jogador &f{player}&c não está preso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  release: '&aVocê soltou o jogador &f{player}&a por &f{money} coins&a.'
  release-broadcast: '&f{player}&a soltou o jogador &f{target}&a e pagou &f{money} coins&a.'
  increase: '&aVocê aumentou em &f{time}&a a pena do jogador &f{player}&a por &f{money} coins&a.'
  increase-broadcast: '&f{player}&a aumentou em &f{time}&a a pena do jogador &f{target}&a e pagou &f{money} coins&a.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/120-yJail">Site do plugin yJail</a>
    </category>
</seealso>