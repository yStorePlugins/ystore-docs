# yStackDrops
<secondary-label ref="gestão"/>

### Descrição
Agrupe itens de maneira eficaz em seu servidor

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
<video src="//www.youtube.com/watch?v=iBhUqs88uX4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/stackdrops&nbsp;- Envia a mensagem de ajuda
/stackdrops reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ystackdrops.use - Permissão para o /stackdrops
ystackdrops.admin.reload - Permissão para o /stackdrops reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yStackDrops/
    ├── commands.yml
    ├── config.yml
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
# Lista de commands do plugin.

# Utilize "command|command" para criar aliases.
# Por exemplo: "gm|gamemode"
# Você pode criar quantas aliases quiser.
commands:
  stackdrops: 'stackdrops|stackdrop'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____  _             _    ____
#  _   _/ ___|| |_ __ _  ___| | _|  _ \ _ __ ___  _ __  ___
# | | | \___ \| __/ _` |/ __| |/ / | | | '__/ _ \| '_ \/ __|
# | |_| |___) | || (_| | (__|   <| |_| | | | (_) | |_) \__ \
#  \__, |____/ \__\__,_|\___|_|\_\____/|_|  \___/| .__/|___/
#  |___/                                         |_|
#
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Sistemas gerais
general:
  # Raio para stackar os itens
  # em blocos
  stack-radius: 5
  # Som ao pegar um item
  sound: ITEM_PICKUP
  # Lista de mundos que o plugin não irá funcionar
  world-blacklist: []
  # Lista de materiais que não serão stackados
  material-blacklist: []
  # Lista de NBT-TAGS que não serão stackadas
  nbt-tag-blacklist: []

# Sistema de black-list de spawn natural de itens
# por exemplo, o cacto gerado pela farm
# NÃO AFETA ITENS DROPADOS POR JOGADORES (SOMENTE NO BLACKLIST GENERAL)
spawn-blacklist:
  # Lista de materiais que não serão stackados naturalmente
  material: [ 'CACTUS' ]
  # Lista de NBT-TAGS que não serão stackadas naturalmente
  nbt-tag: []

# Sistema de nome em cima do item
custom-name:
  # Ativar o sistema
  enabled: true
  # Formato do nome
  format: '&f{amount}x &a{material}'

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
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |
    &r
    &a<--> Comandos do stack-drops <-->
    &r
    &f > &a/stackdrops &8- &7Ver a mensagem de ajuda.
    &f > &a/stackdrops reload &8- &7Recarrega as configurações.
    &r
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/163-yStackDrops">Site do plugin yStackDrops</a>
    </category>
</seealso>