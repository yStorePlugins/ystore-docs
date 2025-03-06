# yRecompensasDiarias
<secondary-label ref="utility"/>

### Descrição
Dê aos seus jogadores recompensas que, podem ser definidas com qualquer item e qualquer horário.

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
<video src="//www.youtube.com/watch?v=kC0ln03z7LY"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/dailyreward - Abrir o menu do entregador.
/dailyreward setnpc - Setar o NPC do entregador.
/dailyreward delnpc - Deletar o NPC do entregador.
/dailyreward reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yrecompensasdiarias.use - Permissão para o /dailyreward
yrecompensasdiarias.setnpc - Permissão para o /dailyreward setnpc
yrecompensasdiarias.delnpc - Permissão para o /dailyreward delnpc
yrecompensasdiarias.admin.reload - Permissão para o /dailyreward delnpc</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yRecompensasDiarias/
    ├── commands.yml
    ├── config.yml
    ├── daily_rewards.yml
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
  daily-reward: 'dr|dailyreward|rd|recompensadiaria'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____                                                         ____  _            _
#  _   _|  _ \ ___  ___ ___  _ __ ___  _ __   ___ _ __  ___  __ _ ___|  _ \(_) __ _ _ __(_) __ _ ___
# | | | | |_) / _ \/ __/ _ \| '_ ` _ \| '_ \ / _ \ '_ \/ __|/ _` / __| | | | |/ _` | '__| |/ _` / __|
# | |_| |  _ <  __/ (_| (_) | | | | | | |_) |  __/ | | \__ \ (_| \__ \ |_| | | (_| | |  | | (_| \__ \
#  \__, |_| \_\___|\___\___/|_| |_| |_| .__/ \___|_| |_|___/\__,_|___/____/|_|\__,_|_|  |_|\__,_|___/
#  |___/                              |_|
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

# Fechar o menu ao coletar a recompensa
close-menu-collect: false

# Sistema de npc
npc:
  skin: 'deliveryman'
  hologram:
    offset: 3.4
    hologram:
      - '&6&lRecompensas Diárias'
      - '&7Clique para coletar as entregas.'
      - '[item]DIAMOND'

# Sistema de lores
lore:
  chance: ['', '&6Chance: &f{chance}%', '']

# Tipos disponíveis:
# yPlugins -> Usa a formatação do yPlugins
# LETRA -> Força usar a formatação em letra
# NUMERO -> Força usar a formatação em número
format: 'yPlugins'
]]>
</code-block>
</chapter>

<chapter title="daily_rewards.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#   ____                            _
# |  _ \ _____      ____ _ _ __ __| |___
# | |_) / _ \ \ /\ / / _` | '__/ _` / __|
# |  _ <  __/\ V  V / (_| | | | (_| \__ \
# |_| \_\___| \_/\_/ \__,_|_|  \__,_|___/
#

daily-rewards:
  daily_reward1:
    order: 1
    display: '&7Membro'
    permission: ''
    delay: 60 # em segundos
    # Tempo online necessário para coletar a recompensa
    # Em segundos (yTempoOnline)
    online-time-need: 0
    item:
      can:
        material: 'c5a9cd58d4c67bccc8fb1f5f756a2d381c9ffac2924b7f4cb71aa9fa13fb5c'
        name: '&aRecompensa de &7Membros'
        lore: [ '', '&7Recompensa: &f1x Pedra', '', '&aClique para pegar.', '' ]
      cant:
        material: 'c5a9cd58d4c67bccc8fb1f5f756a2d381c9ffac2924b7f4cb71aa9fa13fb5c'
        name: '&aRecompensa de &7Membros'
        lore: [ '', '&7Recompensa: &f1x Pedra', '', '&cVocê precisa aguardar &f{time}&c antes.', '&cde pegar novamente.', '' ]
      permission:
        material: 'c5a9cd58d4c67bccc8fb1f5f756a2d381c9ffac2924b7f4cb71aa9fa13fb5c'
        name: '&aRecompensa de &7Membros'
        lore: [ '', '&7Recompensa: &f1x Pedra', '', '&cVocê não tem permissão para pegar.', '' ]
    message:
      title: '&aRecompensa &7MEMBRO<nl>&eColetada!'
      actionbar: '&aRecompensa &7MEMBRO &ecoletada!'
      chat: |
        <nl>
        &aRecompensa &7MEMBRO &ecoletada!
        <nl>
    rewards:
      - '100.0,reward1'
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
  name: '&8Recompensas Diárias'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
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
    <nl>
    &aRecompensas Diárias comandos:
    <nl>
    &a> /dailyreward
    &a> /dailyreward setnpc
    &a> /dailyreward delnpc
    &a> /dailyreward reload
    <nl>
  npc-set: '&aNPC setado com sucesso.'
  npc-deleted: '&aNPC removido com sucesso.'
  npc-not-set: '&cNPC não está definido.'
  time-need: '&cVocê precisa ter jogador por pelo menos {time}.'
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/6-yRecompensasDiarias">Site do plugin yRecompensasDiarias</a>
    </category>
</seealso>