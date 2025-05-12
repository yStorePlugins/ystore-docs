# yFarmOrbs
<secondary-label ref="utility"/>

### Descrição
Dê aos seus jogadores itens que irão fazer as plantações crescerem rapidamente.

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
<video src="//www.youtube.com/watch?v=V6mDeFerkS0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/orb help&nbsp;- Envia a mensagem de ajuda
/orb give&nbsp;- Dá orbs para um jogador
/orb reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yfarmorbs.use - Permissão para o /orb help
yfarmorbs.give - Permissão para o /pets give
yfarmorbs.admin.reload - Permissão para o /pets reload</code-block>
</chapter>



## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yFarmOrbs/
    ├── orbs/
    │    └── carrot.yml
    ├── commands.yml
    ├── config.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="orbs" collapsible="true">
<chapter title="carrot.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# item da orb
item:
  material: 'e43dca8f3bda01152a1ee351d19bf3a580f0582d6a3f437576e3f6cb233bc6f2'
  name: '&a&lORB DE FARM &8(CENOURA)'
  lore:
    - '&7Ao colocar essa orb no chão'
    - '&7ela irá fazer sua plantação de'
    - '&7cenoura crescer totalmente a cada'
    - '&710 segundos.'
    - ''
    - ' &fTempo de crescimento: &a10 segundos'
    - ' &fOndas: &a6 ondas'
    - ' &fRaio: &a8 blocos'
    - ''
    - '&aAperte com ela no chão para ativar.'

# Nome da ORB
name: '&a&lORB DE FARM &8(CENOURA)'

# Tempo a cada onda para crescer as plantas
# em segundos
feed-time: 10

# efeito ao crescer
feed-particle: 'HAPPY_VILLAGER'

# Quantia de ondas que a ORB irá ter
# deixe 0 para ser infinita
rounds: 5

# Mundos que não poderá colocar essa orb
world-blacklist: []

# Quantia de blocos que a ORB irá afetar
radius:
  x: 8
  y: 10
  z: 8

# Plantas que serão reconhecidas pela ORB
farm-types:
  - 'CARROT'

# Nível que irá crescer a farm
feed-level:
  - 'CARROT:7'

# Cabeça que ficará flutuando
floating:
  # Altura da cabeça em relação ao chão
  off-set: 2.0
  # Item da cabeça que ficará flutuando
  item: 'e43dca8f3bda01152a1ee351d19bf3a580f0582d6a3f437576e3f6cb233bc6f2'
  # Altura do holograma em relação a cabeça
  hologram-off-set : 3.7
  # Holograma da cabeça que ficará flutuando
  hologram:
    - '&a&lORB DE FARM &8(CENOURA)'
    - ''
    - ' &fTempo de crescimento: &a{feed_time} segundos'
    - ' &fOndas restantes: &a{rounds} ondas'
    - ' &fRaio: &a8 blocos'
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
  farmorb: 'farmorbs|orbs|farmorb|orb'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _____                     ___       _
#  _   _|  ___|_ _ _ __ _ __ ___  / _ \ _ __| |__  ___
# | | | | |_ / _` | '__| '_ ` _ \| | | | '__| '_ \/ __|
# | |_| |  _| (_| | |  | | | | | | |_| | |  | |_) \__ \
#  \__, |_|  \__,_|_|  |_| |_| |_|\___/|_|  |_.__/|___/
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

# Sistemas gerais
general:
  # Raio de checagem de orb perto
  # em blocos
  radius: 10
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

    &aOrbs comandos:

    &a> /orb give <player> <orb> <quantia>
    &a> /orb reload

  orb-give: '&aVocê deu &7{amount}x {orb}&a para o jogador &7{player}&a.'
  orb-received: '&aVocê recebeu &7{amount}x {orb}&a.'
  orb-list: |
    &cOrb não encontrada.
    &cOrbs disponíveis: &f{list}
  orb-activated: '&aVocê ativou &7{amount}x {orb}&a.'
  orb-world-blacklist: '&cVocê não pode colocar essa orb nesse mundo.'
  orb-radius: '&cHá uma orb muito perto daqui.'
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yFarmOrbs/
    ├── orbs/
    │    └── carrot.yml
    ├── commands.yml
    ├── config.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="orbs" collapsible="true">
<chapter title="carrot.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# item da orb
item:
  material: 'e43dca8f3bda01152a1ee351d19bf3a580f0582d6a3f437576e3f6cb233bc6f2'
  name: '&a&lORB DE FARM &8(CENOURA)'
  lore:
    - '&7Ao colocar essa orb no chão'
    - '&7ela irá fazer sua plantação de'
    - '&7cenoura crescer totalmente a cada'
    - '&710 segundos.'
    - ''
    - ' &fTempo de crescimento: &a10 segundos'
    - ' &fOndas: &a6 ondas'
    - ' &fRaio: &a8 blocos'
    - ''
    - '&aAperte com ela no chão para ativar.'

# Nome da ORB
name: '&a&lORB DE FARM &8(CENOURA)'

# Tempo a cada onda para crescer as plantas
# em segundos
feed-time: 10

# efeito ao crescer
feed-particle: 'HAPPY_VILLAGER'

# Quantia de ondas que a ORB irá ter
# deixe 0 para ser infinita
rounds: 5

# Mundos que não poderá colocar essa orb
world-blacklist: []

# Quantia de blocos que a ORB irá afetar
radius:
  x: 8
  y: 10
  z: 8

# Plantas que serão reconhecidas pela ORB
farm-types:
  - 'CARROT'

# Nível que irá crescer a farm
feed-level:
  - 'CARROT:7'

# Cabeça que ficará flutuando
floating:
  # Altura da cabeça em relação ao chão
  off-set: 2.0
  # Item da cabeça que ficará flutuando
  item: 'e43dca8f3bda01152a1ee351d19bf3a580f0582d6a3f437576e3f6cb233bc6f2'
  # Altura do holograma em relação a cabeça
  hologram-off-set : 3.7
  # Holograma da cabeça que ficará flutuando
  hologram:
    - '&a&lORB DE FARM &8(CENOURA)'
    - ''
    - ' &fTempo de crescimento: &a{feed_time} segundos'
    - ' &fOndas restantes: &a{rounds} ondas'
    - ' &fRaio: &a8 blocos'
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
  farmorb: 'farmorbs|orbs|farmorb|orb'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        _____                     ___       _
#  _   _|  ___|_ _ _ __ _ __ ___  / _ \ _ __| |__  ___
# | | | | |_ / _` | '__| '_ ` _ \| | | | '__| '_ \/ __|
# | |_| |  _| (_| | |  | | | | | | |_| | |  | |_) \__ \
#  \__, |_|  \__,_|_|  |_| |_| |_|\___/|_|  |_.__/|___/
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

    &aOrbs comandos:

    &a> /orb give <player> <orb> <quantia>
    &a> /orb reload

  orb-give: '&aVocê deu &7{amount}x {orb}&a para o jogador &7{player}&a.'
  orb-received: '&aVocê recebeu &7{amount}x {orb}&a.'
  orb-list: |
    &cOrb não encontrada.
    &cOrbs disponíveis: &f{list}
  orb-activated: '&aVocê ativou &7{amount}x {orb}&a.'
  orb-world-blacklist: '&cVocê não pode colocar essa orb nesse mundo.'
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/160-yFarmOrbs">Site do plugin yFarmOrbs</a>
    </category>
</seealso>