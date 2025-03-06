# yRoleta
<secondary-label ref="utility"/>

### Descrição
Recompense seus jogadores de maneira interativa

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
<video src="//www.youtube.com/watch?v=W7hdpqNLg7g"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/roleta - Envia a mensagem de ajuda
/roleta give - Dar roletas para um jogador
/roleta reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yroleta.use - Permissão para o /roleta
yroleta.give - Permissão para o /roleta give
yroleta.admin.reload - Permissão para o /roleta reload
yroleta.admin - Permissão para ser reconhecido como admin</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yRoleta/
    ├── roulettes/
    │    └── default.yml
    ├── commands.yml
    ├── config.yml
    ├── menus.yml
    ├── messages.yml
    ├── rarities.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="roulettes" collapsible="true">
<chapter title="default.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
display: '&eRoleta da Sorte &7(Básica)'

# Permissão para poder usar a roleta
permission: ''

# Cabeças que irão aparecer na roleta
# Pode ser qualquer bloco (além da skull)
skulls:
  - '8534b17d2d3b5a64c57f5f080dd777945761d9f71d82e8f599f242976e4d0c05'
  - 'c133414759f9e5315156017023a8b1b31cfbf177dcafb0603b8e9d94036a23f1'
  - '300c817432585fadcbd9ca8cfedfeedbce5851b7c07d1b073fb52fa8283e8f23'
  - 'f171a0c0572824da80366d71c5413a7e3355abec79b8f529f1dc9dad2632f485'
  - '6ab180e820f71629f01f25b62bdeb9c324d50a38af74e6a9321439471046dc41'
  - '65fed46b39c6c34d491143b72ce728797d16f9b5aa40bbdec61667f5ff9d3d45'
  - '17bc1b64cba3dc4cefe4e121c3cdbbb0fa99aba0e113b5c916815fc9b304e636'
  - '29942dd1338abeae8b8274a41ae1dcdf2b7be449f28d6b650ec06e491e70f570'

# Configuração do holograma
hologram:
  off-set: 2.2
  lines: [ '&a{reward}', '[item]{reward_preview}' ]

# Sistema de partículas
# Lista disponível: https://github.com/retrooper/packetevents/blob/f0b15c3f949ce80577420e64c6ff973ce5a218bd/api/src/main/java/com/github/retrooper/packetevents/protocol/particle/type/ParticleTypes.java#L43
particles:
  # Partícula ao aparecer as skulls na roleta
  appear: 'ENCHANT'
  # Partícula ao sumir as skulls da roleta
  disappear: 'LARGE_SMOKE'
  # Partícula de sorteando a recompensa
  sorting: 'HAPPY_VILLAGER'
  # Partícula ao receber a recompensa e apagar a última skull
  appear-reward: 'CLOUD'

# Sistema de sons
# Lista disponível:
sounds:
  # Som ao aparecer as skulls na roleta
  appear: 'NOTE_PLING'
  # Som ao sumir as skulls da roleta
  disappear: 'NOTE_BASS'
  # Som enquanto a roleta estiver rodando
  running: 'NOTE_STICKS'
  # Som de sorteando a recompensa
  sorting: 'FIRE_IGNITE'
  # Som ao receber a recompensa e apagar a última skull
  appear-reward: 'LEVEL_UP'

# Item da roleta
# use apenas blocos
item:
  material: '8534b17d2d3b5a64c57f5f080dd777945761d9f71d82e8f599f242976e4d0c05'
  name: '&eRoleta da Sorte &7(Básica)'
  lore:
    - '&7Nível: &fBásica'
    - '&7* você irá ganhar itens comuns.'
    - ''
    - '&aColoque no chão para ativar'

# Mensagens da roleta
messages:
  # Mensagem ao aparecer as skulls na roleta
  appear:
    title: ''
    actionbar: '&f&l.&c&l.&f&l.'
    chat: ''
  # Mensagem enquanto a roleta estiver rodando
  running:
    title: ''
    actionbar: '&f&lG&c&lI&f&lR&c&lA&f&lN&c&lD&f&lO&c&l.'
    chat: ''
  # Mensagem de sorteando a recompensa
  sorting:
    title: ''
    actionbar: '&f&lS&c&lO&f&lR&c&lT&f&lE&c&lA&f&lN&c&lD&f&lO&c&l.'
    chat: ''

# chance,recompensa-raridade
# a raridade, caso não tenha, deixe: none
rewards:
  - '20.0,reward1-none'
  - '30.0,reward2-none'
  - '50.0,reward3-none'
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
  roulette: 'roulette|roulettes|roleta|roletas'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        ____       _      _
#  _   _|  _ \ ___ | | ___| |_ __ _
# | | | | |_) / _ \| |/ _ \ __/ _` |
# | |_| |  _ < (_) | |  __/ || (_| |
#  \__, |_| \_\___/|_|\___|\__\__,_|
#  |___/

# *** ALERTA
# ESTE PLUGIN REQUER A OPÇÃO "packet-events" ATIVADA NO SEU yPlugins
# ***

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Sistemas gerais
general:
  # Mundos proibidos de colocar roletas
  world-blacklist: [ 'none' ]

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

# Menu de preview das recompensas
preview:
  name: '&8Roleta'
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

    &aRoleta comandos:

    &a> /roulette give <player> <roleta> <quantia>
    &a> /roulette reload

  roulette-give: '&aVocê deu &7{amount}x {roulette}&a para o jogador &7{player}&a.'
  roulette-received: '&aVocê recebeu &7{amount}x {roulette}&a.'
  roulette-list: |
    &cRoleta não encontrada.
    &cRoleta disponíveis: &f{list}

  perm-world: '&cVocê não pode colocar roletas neste mundo.'
  perm-roulette: '&cVocê não tem permissão para colocar este tipo de roleta.'
  roulette-opening: '&aVocê está abrindo uma {roulette}&a.'
  roulette-cant: '&cVocê já está abrindo uma roleta.'
]]>
</code-block>
</chapter>

<chapter title="rarities.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
rarities:
  rare:
    display: '&6Raro'
    strike: false # pode causar lag
    bat: false # pode causar lag
    actionbar: '&e[Roleta] &fO jogador &e{player}&f encontrou uma recompensa rara na Roleta&f.'
    title: ''
    chat: |
      &e[Roleta] &fO jogador &e{player}&f encontrou uma recompensa rara na Roleta&f.
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
      lore: [ '&aEsta pedra vale muito dinheiro!', '', '&fChance: &6{chance}%' ]
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
    # Mensagens da recompensa
    messages:
      title: ''
      actionbar: '&7Você ganhou pedras!'
      chat: ''
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!', '', '&fChance: &6{chance}%' ]
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
    # Mensagens da recompensa
    messages:
      title: ''
      actionbar: '&bVocê ganhou diamantes!'
      chat: ''
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?', '', '&fChance: &6{chance}%' ]
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
    # Mensagens da recompensa
    messages:
      title: ''
      actionbar: '&aVocê ganhou esmeraldas!'
      chat: ''
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/140-yRoleta">Site do plugin yRoleta</a>
    </category>
</seealso>