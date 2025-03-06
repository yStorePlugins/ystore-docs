# yArmorsBonus
<secondary-label ref="utility"/>

### Descrição
Agora suas armaduras acumulam bônus e buffs

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
<video src="https://i.imgur.com/KglCnFT.png"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/armors&nbsp;- Envia a mensagem de ajuda
/armors help&nbsp;- Envia a mensagem de ajuda
/armors givepet&nbsp;- Dá armaduras para um jogador
/armors&nbsp;reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yarmorsbonus.use - Permissão para o /armors
yarmorsbonus.give - Permissão para o /armors givepet
yarmorsbonus.admin.reload - Permissão para o /armors reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yArmorsBonus/
    ├── armors/
    │    └── basic_helmet.yml
    ├── commands.yml
    ├── config.yml
    ├── messages.yml
    └── plugin.yml
</code-block>
</chapter>

<chapter title="armors" collapsible="true">
<chapter title="basic_helmet.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome do PET
display-name: '&aCapacete Básico'

# Placeholders disponíveis
# {bonus_spawners}
# {bonus_machines}
# {bonus_mines}
# {bonus_storage}
# {bonus_farm}
# {bonus_forest}
# {bonus_sell}
# {bonus_fish}
# {bonus_almas}
# {discount_spawners}
# {discount_machines}
item:
  material: 'DIAMOND_HELMET'
  name: '&aCapacete Básico'
  lore:
    - '&7Este capacete garante buffs'
    - '&7nos &fspawners&7.'
    - ''
    - '&6Informações'
    - ' &fBônus &6(spawners)&f: &7{bonus_spawners}%'
    - ' &fDesconto &6(spawners)&f: &7{discount_spawners}%'
    - ''

buffs:
  # Lista de efeitos que o jogador irá ter
  # effect:level
  effect-list: [ 'INCREASE_DAMAGE:1', 'SPEED:1' ]
  # Mundos que o jogador irá ter fly
  fly-worlds: [ 'PlotWorld' ]

# Bônus de Venda de drops de Spawners -> ySpawners
bonus-spawners: 10.0

# Bônus de Venda de drops de Máquinas -> yMaquinas e yMaquinasVirtuais
bonus-machines: 0.0

# Bônus de Venda na mina -> yMinas e yMinasPackets
bonus-mines: 0.0

# Bônus de Venda no armazém -> yArmazem
bonus-storage: 0.0

# Bônus de Venda nas plantas -> yCampo e yPlantacoes
bonus-farm: 0.0

# Bônus de Venda na floresta -> yFloresta
bonus-forest: 0.0

# Bônus de Venda -> yVender
bonus-sell: 0.0

# Bônus de Venda na pesca -> yPesca
bonus-fish: 0.0

# Bônus de Almas -> yAlmas
bonus-almas: 0.0

# Desconto na compra de spawners -> ySpawnersShop
discount-spawners: 5.0

# Desconto na compra de máquinas -> yMaquinas e yMaquinasVirtuais
discount-machines: 0.0
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
  armorsbonus: 'armors|armor|armadura|armaduras'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#           _                                  ____
#  _   _   / \   _ __ _ __ ___   ___  _ __ ___| __ )  ___  _ __  _   _ ___
# | | | | / _ \ | '__| '_ ` _ \ / _ \| '__/ __|  _ \ / _ \| '_ \| | | / __|
# | |_| |/ ___ \| |  | | | | | | (_) | |  \__ \ |_) | (_) | | | | |_| \__ \
#  \__, /_/   \_\_|  |_| |_| |_|\___/|_|  |___/____/ \___/|_| |_|\__,_|___/
#  |___/
# Discord: discord.ystoreplugins.com.br
# Site: ystoreplugins.com.br
#

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

    &aArmors-Bonus comandos:

    &a> /armors give <player> <armor>
    &a> /armors reload

  armor-give: '&aVocê deu &71x {armor}&a para o jogador &7{player}&a.'
  armor-received: '&aVocê recebeu &71x {armor}&a.'
  armor-list: |
    &cArmadura não encontrada.
    &cArmaduras disponíveis: &f{list}
]]>
</code-block>
</chapter>

<chapter title="plugin.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: yArmorsBonus
version: '${project.version}'
main: com.ystoreplugins.yarmorsbonus.Main
depend: [ yPlugins ]
authors: [ yChusy ]
api-version: 1.13

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/157-yArmorsBonus">Site do plugin yArmorsBonus</a>
    </category>
</seealso>