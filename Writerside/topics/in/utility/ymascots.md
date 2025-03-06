# yMascots
<secondary-label ref="utility"/>

### Descrição
Mascotes seu ou do seu clan no seu plot!

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
<video src="//www.youtube.com/watch?v=bTxLOPqS3yI?start=2"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mascotes - Abre o menu principal
/mascotes help - Envia a mensagem de ajuda
/mascotes give - Dá mascotes para um jogador
/mascotes giveslot - Dá slots para um jogador
/mascotes reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymascots.admin - Permissão para ser reconhecido como admin
ymascots.use - Permissão para o /mascotes
ymascots.give - Permissão para o /mascotes give
ymascots.giveslot - Permissão para o /mascotes giveslot
ymascots.admin.reload - Permissão para o /mascotes reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMascots/
    ├── mascots/
    │    └── gorilla.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="mascots" collapsible="true">
<chapter title="gorilla.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome padrão do mascote
name: '&eMascote Gorilla'

# Entidade do mascote
entity: 'ZOMBIE'

# Item ativável
item:
  material: '20a969b6ec7deae807cc362e5aca5a35b36b0f9c76514767bb5ca4bb3d7f2b9d'
  name: '&eMascote Gorilla'
  lore:
    - '&7Considerado um dos mais fortes,'
    - '&7este mascote irá trazer aos membros'
    - '&7do seu clan vários buffs.'
    - ''
    - '&8> &fBônus venda &8(spawners)&f: &b10%'
    - '&8> &5Força 1 ∞'
    - '&8> &bSpeed 1 ∞'
    - ''
    - '&aClique para ativar.'

# Entidade customizada do MiniturePets
custom-entity:
  # Ativar a entidade custom. Precisa do MiniaturePets
  enabled: true
  # Arquivo da entidade da pasta de pets do MiniaturePets
  entity: 'Boxer.mpet'

# Holograma do mascote
hologram:
  enabled: true
  # Altura em relação ao spawner
  off-set: 2.0
  lines:
    - '{name}'
    - '&eMascote do clan: {clan_colortag}'

# Buffs que irá dar aos jogadores
# Se o mascote for de clan, irá dar os bônus para todos os membros
buffs:
  # Bônus de Venda de drops de Spawners -> ySpawners
  bonus-spawners: 10.0
  # Bônus de Venda de drops de Máquinas -> yMaquinas e yMaquinasVirtuais
  bonus-machines: 10.0
  # Bônus de Venda na mina -> yMinas
  bonus-mines: 10.0
  # Bônus de Venda no armazém -> yArmazem
  bonus-storage: 10.0
  # Bônus de Venda nas plantas -> yCampo, yPlantacoes
  bonus-farm: 10.0
  # Bônus de Venda na floresta -> yFloresta
  bonus-forest: 0.0
  # Bônus de Venda -> yVender
  bonus-sell: 0.0
  # Bônus de Venda na pesca -> yPesca
  bonus-fish: 10.0
  # Desconto na compra de spawners -> ySpawnersShop
  discount-spawners: 5.0
  # Desconto na compra de máquinas -> yMaquinas e yMaquinasVirtuais
  discount-machines: 5.0
  # Lista de efeitos que o jogador irá ter
  # effect:level
  effect-list: [ 'INCREASE_DAMAGE:1', 'SPEED:1' ]
  # Mundos que o jogador irá ter fly
  fly-worlds: [ 'PlotWorld' ]
  # Comandos que será executado ao renascer
  # Caso queira dar um "kit", por exemplo.
  respawn-commands: []

# Preços para comprar o mascote
costs:
  cost1:
    provider: 'money'
    amount: 1000.0

# Itens que irão ficar no menu
displays:
  buy:
    material: '20a969b6ec7deae807cc362e5aca5a35b36b0f9c76514767bb5ca4bb3d7f2b9d'
    name: '&eMascote Gorilla'
    lore:
      - '&7Considerado um dos mais fortes,'
      - '&7este mascote irá trazer aos membros'
      - '&7do seu clan vários buffs.'
      - ''
      - '&f* Preço: &a{money} coins'
      - ''
      - '&8> &fBônus venda &8(spawners)&f: &b10%'
      - '&8> &5Força 1 ∞'
      - '&8> &bSpeed 1 ∞'
      - ''
      - '&aClique para comprar.'
  equipped:
    material: '20a969b6ec7deae807cc362e5aca5a35b36b0f9c76514767bb5ca4bb3d7f2b9d'
    name: '&eMascote Gorilla'
    lore:
      - '&7Considerado um dos mais fortes,'
      - '&7este mascote irá trazer aos membros'
      - '&7do seu clan vários buffs.'
      - ''
      - '&8> &fBônus venda &8(spawners)&f: &b10%'
      - '&8> &5Força 1 ∞'
      - '&8> &bSpeed 1 ∞'
      - ''
      - '&f* Nome Atual: &b{name}'
      - ''
      - '&aClique para editar o nome.'
  active:
    material: '20a969b6ec7deae807cc362e5aca5a35b36b0f9c76514767bb5ca4bb3d7f2b9d'
    name: '&eMascote Gorilla'
    lore:
      - '&7Considerado um dos mais fortes,'
      - '&7este mascote irá trazer aos membros'
      - '&7do seu clan vários buffs.'
      - ''
      - '&8> &fBônus venda &8(spawners)&f: &b10%'
      - '&8> &5Força 1 ∞'
      - '&8> &bSpeed 1 ∞'
      - ''
      - '&aClique para equipar.'
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
  mascot: 'mascot|mascots|mascotes|mascote'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __                     _
#  _   _|  \/  | __ _ ___  ___ ___ | |_ ___
# | | | | |\/| |/ _` / __|/ __/ _ \| __/ __|
# | |_| | |  | | (_| \__ \ (_| (_) | |_\__ \
#  \__, |_|  |_|\__,_|___/\___\___/ \__|___/
#  |___/
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

# Sistemas gerais
general:
  # Permitir colocar spawners apenas nos plots
  plot: false
  # Ativar o sistema de mascotes por clan
  use-clans: false
  # Ativar o modo bungeecord
  bungeecord: false
  # Número padrão de slots para o mascote do clan
  clan-slot-default: 1
  # Número máximo de slots para o mascote do clan
  clan-slot-maximum: 10
  # Item do slot que será ativável
  clan-slot-item:
    material: 'HOPPER'
    name: '&bSlots'
    lore:
      - ''
      - '&fQuantia: &a{amount}'
      - ''
      - '&7Clique com botão direito para ativar.'
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
    permission: 'ymascots.provider.money'
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
  name: '&8Mascotes'
  size: 45
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 ]
  previous-slot: 28
  next-slot: 34
  items:
    location-slot: 30
    clan-members-slot: 31
    unequip-slot: 32
    location:
      material: 'INK_SACK:10'
      name: '&eLocalização'
      lore:
        - '&7Localização do seu mascote na'
        - '&7base do seu clan :)'
        - ''
        - ' &7Local: &f{location}'
        - ''
        - '&aClique para alterar.'
        - '&cBotão direito para deletar.'
    clan-members:
      material: 'SKULL_ITEM:3'
      name: '&eMembros do Clan'
      lore:
        - '&7Clique para acessar os membros'
        - '&7que terão os efeitos do mascote'
        - '&7do seu clan.'
    unequip:
      material: 'INK_SACK:13'
      name: '&cDesequipar'
      lore:
        - '&aClique para desequipar seu mascote.'

clan-members:
  name: '&8Mascotes'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
  previous-slot: 9
  next-slot: 17
  back-slot: 18
  items:
    slots-slot: 27
    slots:
      material: 'INK_SACK:10'
      name: '&eSlots'
      lore:
        - ''
        - ' &fSlots: &c{slots_current}&7/&a{slots_total}'
        - ''
    friend:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&fAtivado: {status}&f.'
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

    &aMascote comandos:

    &a> /mascotes
    &a> /mascotes give <player> <mascote>
    &a> /mascotes giveslot <player> <quantia>

  mascot-give: '&aVocê deu 1x {mascot}&a para o jogador &7{player}&a.'
  mascot-received: '&aVocê recebeu &71x {mascot}&a.'
  mascot-list: |
    &cMascote não encontrado.
    &cMascotes disponíveis: &f{list}
  plot-permission: '&cVocê não tem permissão neste terreno.'
  clan-have: '&cVocê não possui um clan.'
  mascot-have: '&cSeu clan já possui este mascote.'
  mascot-activated: '&aVocê ativou o mascote para o seu clan.'
  location-set: '&aLocalização setada com sucesso.'
  location-removed: '&aLocalização removida com sucesso.'
  location-found: '&cLocalização não encontrada.'
  just-leader: '&cApenas o líder do clan pode realizar esta ação.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  bought: '&aVocê comprou o mascote {mascot}&a.'
  digit-name: |

    &aDigite o nome que você quer.
    &7para cancelar digite &ncancelar&7.

  name-changed: '&aNome alterado para &f{name}&a.'
  slots-need: '&cVocê precisa de mais slots livres.'
  slot-activated: '&aVocê ativou &e{amount} &ade slots.'
  slot-max: '&cVocê já chegou no máximo.'
  slot-give: '&aVocê deu &e{amount} &ade slots para o jogador &e{player}&a.'
  location-already: '&cA localização já está setada.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/126-yMascots">Site do plugin yMascots</a>
    </category>
</seealso>