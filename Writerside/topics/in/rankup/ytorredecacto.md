# yTorreDeCacto
<secondary-label ref="rankup"/>

### Descrição
Crie estruturas que podem ser colocadas nos plots!

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
<video src="//www.youtube.com/watch?v=xBMdm8NuAL4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/torre - Envia a mensagem de ajuda
/torre help - Envia a mensagem de ajuda
/torre give - Dá estruturas para um jogador
/torre reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytorredecacto.use - Permissão para o /torre e /torre help
ytorredecacto.give - Permissão para o /torre give
ytorredecacto.admin.reload - Permissão para o /pets reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTorreDeCacto/
    ├── structures/
    │    └── cactus_tower.yml
    ├── commands.yml
    ├── config.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="structures" collapsible="true">
<chapter title="cactus_tower.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome da ESTRUTURA
display-name: '&aTorre de Cacto'

# Bloco que irá aparecer no preview caso esteja bloqueado de por
preview-block: 'STAINED_GLASS:14'

# Alterar a altura do y ao colocar (se quiser colocar pra setar no ar/setar dentro do solo)
y-offset: 0

# Blocos que serão desconsiderados e removidos ao setar a estrutura
block-blacklist: [ 'GRASS', 'STONE' ]

# Quantia de vezes que a estrutura irá se repetir (para cima)
y-repeat-amount: 3

# Quantia de vezes que a estrutura irá se repetir (para os lados)
xz-repeat-amount: 1

# Distância em blocos pros lados
xz-distance: 4.0

# Colocar de modo gradual
gradual: false

# Item que o jogador irá receber
item:
  material: CACTUS
  name: '&aTorre de Cactos'
  lore:
    - '&fTamanho: &76x'
    - ''
    - '&fSHIFT + Direito'

# Siglas de cada bloco para identificação no pattern
blocks:
  - 'C,CACTUS'
  - 'X,AIR'
  - 'D,DIRT'
  - 'S,SAND'
  - 'L,WOOD_STEP'

# Modelagem da estrutura
patterns:
  sand1:
    y: 1
    pattern:
      - 'SXS'
      - 'XSX'
      - 'SXS'
  cactus:
    y: 2
    pattern:
      - 'CLC'
      - 'LCL'
      - 'CLC'
  sand2:
    y: 3
    pattern:
      - 'XSX'
      - 'SXS'
      - 'XSX'
  cactus2:
    y: 4
    pattern:
      - 'LCL'
      - 'CLC'
      - 'LCL'
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
  tower: 'torre|torres|tower|towers'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#       _____                   ____        ____           _
#  _   |_   _|__  _ __ _ __ ___|  _ \  ___ / ___|__ _  ___| |_ ___
# | | | || |/ _ \| '__| '__/ _ \ | | |/ _ \ |   / _` |/ __| __/ _ \
# | |_| || | (_) | |  | | |  __/ |_| |  __/ |__| (_| | (__| || (_) |
#  \__, ||_|\___/|_|  |_|  \___|____/ \___|\____\__,_|\___|\__\___/
#  |___/
#

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

general:
  # Ativar o preview no shift
  shift-preview-enabled: true
  # Ativar o preview sem shift
  no-shift-preview-enabled: true
  # Ativar o preview no shift
  shift-preview: true
  # Ativar o preview sem shift
  no-shift-preview: false
  # Tempo que levará para atualizar o preview
  # em ticks (20 ticks = 1 segundo)
  refresh-time: 5
  # Distância do preview
  # em blocos
  preview-distance: 5
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

    &a/tower give &8- &7Dar uma estrutura para um/todos os jogadores.
    &a/tower reload &8- &7Recarrega as configurações.

  structure-give: '&aVocê deu &7{amount}x {structure}&a para o jogador &7{player}&a.'
  structure-received: '&aVocê recebeu &7{amount}x {structure}&a.'
  structure-list: |
    &cEstrutura não encontrada.
    &cEstruturas disponíveis: &f{list}
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTorreDeCacto/
    ├── structures/
    │    └── cactus_tower.yml
    ├── commands.yml
    ├── config.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="structures" collapsible="true">
<chapter title="cactus_tower.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome da ESTRUTURA
display-name: '&aTorre de Cacto'

# Bloco que irá aparecer no preview caso esteja bloqueado de por
preview-block: 'RED_STAINED_GLASS'

# Quantia de vezes que a estrutura irá se repetir (para cima)
repeat-amount: 5

# Item que o jogador irá receber
item:
  material: CACTUS
  name: '&aTorre de Cactos'
  lore:
    - '&7Este item irá gerar uma'
    - '&7incrível torre de cactos.'
    - ''
    - '&f Quantia da torre: &a5 níveis'
    - ''
    - '&aClique para ativar.'

# Siglas de cada bloco para identificação no pattern
blocks:
  - 'C,CACTUS'
  - 'X,AIR'
  - 'D,DIRT'
  - 'S,SAND'

# Modelagem da estrutura
patterns:
  bottom:
    y: 1
    pattern:
      - 'XDX'
      - 'DXD'
      - 'XDX'
  sands:
    y: 2
    pattern:
      - 'XSX'
      - 'SXS'
      - 'XSX'
  cactus:
    y: 3
    pattern:
      - 'XCX'
      - 'CXC'
      - 'XCX'
  top:
    y: 4
    pattern:
      - 'XXX'
      - 'XDX'
      - 'XXX'
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
  tower: 'torre|torres|tower|towers'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#       _____                   ____        ____           _
#  _   |_   _|__  _ __ _ __ ___|  _ \  ___ / ___|__ _  ___| |_ ___
# | | | || |/ _ \| '__| '__/ _ \ | | |/ _ \ |   / _` |/ __| __/ _ \
# | |_| || | (_) | |  | | |  __/ |_| |  __/ |__| (_| | (__| || (_) |
#  \__, ||_|\___/|_|  |_|  \___|____/ \___|\____\__,_|\___|\__\___/
#  |___/
#

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

general:
  # Ativar o preview no shift
  shift-preview-enabled: true
  # Ativar o preview sem shift
  no-shift-preview-enabled: true
  # Ativar o preview no shift
  shift-preview: true
  # Ativar o preview sem shift
  no-shift-preview: false
  # Tempo que levará para atualizar o preview
  # em ticks (20 ticks = 1 segundo)
  refresh-time: 5
  # Distância do preview
  # em blocos
  preview-distance: 5
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

    &a/tower give &8- &7Dar uma estrutura para um/todos os jogadores.
    &a/tower reload &8- &7Recarrega as configurações.

  structure-give: '&aVocê deu &7{amount}x {structure}&a para o jogador &7{player}&a.'
  structure-received: '&aVocê recebeu &7{amount}x {structure}&a.'
  structure-list: |
    &cEstrutura não encontrada.
    &cEstruturas disponíveis: &f{list}
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/152-yTorreDeCacto">Site do plugin yTorreDeCacto</a>
    </category>
</seealso>