# yPets
<secondary-label ref="utility"/>

### Descrição
Adicione pets que vão seguir seus jogadores para onde forem.

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
<video src="//www.youtube.com/watch?v=ntNJqeatnDQ"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/pets - Abre o menu principal
/pets help - Envia a mensagem de ajuda
/pets givepet - Dá pets para um jogador
/pets givefood - Dá ração para pets para um jogador
/pets givebowl - Dá pote de ração para um jogador
/pets giveslot - Dá slots para um jogador
/pets reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ypets.use - Permissão para o /pets
ypets.give - Permissão para o /pets givepet
ypets.givefood - Permissão para o /pets givefood
ypets.givebowl - Permissão para o /pets givebowl
ypets.giveslot - Permissão para o /pets giveslot
ypets.admin.reload - Permissão para o /pets reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPets/
    ├── pets/
    │    └── lion.yml
    ├── commands.yml
    ├── config.yml
    ├── menus.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="pets" collapsible="true">
<chapter title="lion.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Nome do PET
display-name: '&6&lLeão &8[Nvl. {level}]'

# Permissão para equipar o PET
permission: ''

# A cabeça do PET vai ser pequena?
small: false

# Distância entre o player e o PET
distance-between: 1.3

# Cabeça do PET
skull:
  material: '85b70944ef8967762d53064d21dfe1e260eacfa7b29788c3e3abb45bcf650577'

# Nível padrão do PET
default-level: 0

# Nível máximo do PET
max-level: 100

# Quantia BASE de XP necessária para upar
exp-base: 10.0

# Quantia ADICIONAL POR NÍVEL de XP necessária para upar
exp-per-level: 10.0

# Quanto de EXP cada comida irá dar
exp-per-food: 1.0

# Sistema de sons
# Lista disponível: https://helpch.at/docs/1.8/index.html?org/bukkit/Sound.html
sounds:
  # Som ao evoluir o nível
  up: 'LEVEL_UP'

# Configuração do holograma
hologram:
  enabled: false
  off-set: 2.5
  lines: [ '&6&lLeão &8[Nvl. {level}]' ]

# Item ativável do PET
item:
  material: '85b70944ef8967762d53064d21dfe1e260eacfa7b29788c3e3abb45bcf650577'
  name: '&6&lPet Leão &8[{tier_display}&8]'
  lore:
    - '&7Este pet é um multiplicador'
    - '&7de &fspawners&7.'
    - ''
    - '&6Informações'
    - ' &fNível: &7{level}'
    - ' &fBônus &6(spawners)&f: &7{bonus_spawners}%'
    - ' &fDesconto &6(spawners)&f: &7{discount_spawners}%'
    - ' &fProgresso: &7{progressbar} &7{percentage}'
    - ''
    - ' &8Evolua o seu pet'
    - ' &8alimentando-o com ração.'
    - ''
    - '&6Clique para ativar'

# Item no menu
icon:
  material: '85b70944ef8967762d53064d21dfe1e260eacfa7b29788c3e3abb45bcf650577'
  name: '&6&lPet Leão &8[{tier_display}&8]'
  lore:
    - '&7Este pet é um multiplicador'
    - '&7de &fspawners&7.'
    - ''
    - '&6Informações'
    - ' &fNível: &7{level}'
    - ' &fBônus &6(spawners)&f: &7{bonus_spawners}%'
    - ' &fDesconto &6(spawners)&f: &7{discount_spawners}%'
    - ' &fProgresso: &7{progressbar} &7{percentage}'
    - ''
    - ' &8Evolua o seu pet'
    - ' &8alimentando-o com ração.'
    - ''
    - '&6Botão esquerdo &8-> &fEquipar'
    - '&6Botão direito &8-> &fRecolher'

# Item no menu (equipado)
icon-equipped:
  material: '85b70944ef8967762d53064d21dfe1e260eacfa7b29788c3e3abb45bcf650577'
  name: '&6&lPet Leão &8[{tier_display}&8]'
  lore:
    - '&7Este pet é um multiplicador'
    - '&7de &fspawners&7.'
    - ''
    - '&6Informações'
    - ' &fNível: &7{level}'
    - ' &fBônus &6(spawners)&f: &7{bonus_spawners}%'
    - ' &fDesconto &6(spawners)&f: &7{discount_spawners}%'
    - ' &fProgresso: &7{progressbar} &7{percentage}'
    - ''
    - ' &8Evolua o seu pet'
    - ' &8alimentando-o com ração.'
    - ''
    - '&6Botão esquerdo &8-> &fDesequipar'

tiers:
  tier-1:
    # Ordenação dos tiers
    # Padrão: 1
    order: 1
    # Nível necessário para formar este tier
    need-level: 0
    # Nome do tier
    display-name: '&7Comum'
    # Buffs que irá dar ao jogador
    buffs:
      base:
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
      per-level:
        bonus-spawners: 0.01
        bonus-machines: 0.0
        bonus-mines: 0.0
        bonus-storage: 0.0
        bonus-farm: 0.0
        bonus-forest: 0.0
        bonus-sell: 0.0
        bonus-fish: 0.0
        bonus-almas: 0.0
        discount-spawners: 0.005
        discount-machines: 0.0
      # Lista de efeitos que o jogador irá ter
      # effect:level
      effect-list: [ 'INCREASE_DAMAGE:1', 'SPEED:1' ]
      # Mundos que o jogador irá ter fly
      fly-worlds: [ 'PlotWorld' ]
      # Comandos que serão executados ao renascer
      # Caso queira dar um "kit", por exemplo.
      respawn-commands: []
      # Comandos que serão executados ao equipar o pet e ao logar
      equip-login-commands: []
      # Comandos que serão executados ao desequipar o pet e ao deslogar
      unequip-quit-commands: []
  tier-2:
    order: 2
    need-level: 10
    display-name: '&7Mediano'
    buffs:
      base:
        bonus-spawners: 20.0
        bonus-machines: 0.0
        bonus-mines: 0.0
        bonus-storage: 0.0
        bonus-farm: 0.0
        bonus-fish: 0.0
        bonus-almas: 0.0
        discount-spawners: 10.0
        discount-machines: 0.0
      per-level:
        bonus-spawners: 0.01
        bonus-machines: 0.0
        bonus-mines: 0.0
        bonus-storage: 0.0
        bonus-farm: 0.0
        bonus-fish: 0.0
        bonus-almas: 0.0
        discount-spawners: 0.005
        discount-machines: 0.0
      effect-list: [ 'INCREASE_DAMAGE:1', 'SPEED:1' ]
      fly-worlds: [ 'PlotWorld' ]
      respawn-commands: []
      equip-login-commands: []
      unequip-quit-commands: []
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
  pet: 'ypets|pet|pets'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____      _
#  _   _|  _ \ ___| |_ ___
# | | | | |_) / _ \ __/ __|
# | |_| |  __/  __/ |_\__ \
#  \__, |_|   \___|\__|___/
#  |___/

# *** ALERTA
# ESTE PLUGIN REQUER A OPÇÃO "packet-events" ATIVADA NO SEU yPlugins
# ***

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

# Sistemas gerais
general:
  # Este servidor é o principal?
  # Exemplo: servidor rankup
  # Caso esse servidor for uma mina, floresta, campo, etc, deixe false.
  main-server: true
  # Poder stackar PETS de tipos e atributos idênticos
  stack-equal: false
  # Mundos em que não irá mostrar o PET para outros jogadores
  target-world-blacklist: []

# Slots de pet
slots:
  # Quantia padrão de slots que o jogador irá ter
  default: 1
  # Quantia máxima de slots que o jogador poderá ter
  max: 20
  # Item do slot que será ativável
  item:
    material: 'HOPPER'
    name: '&bSlots'
    lore:
      - ''
      - '&fQuantia: &a{amount}'
      - ''
      - '&7Clique com botão direito para ativar.'

# Comida do PET
food:
  material: 'INK_SACK:3'
  name: '&eRação para Pet'
  lore:
    - '&7Utilize esta ração para alimentar'
    - '&7o seu Pet, fazendo-o evoluir.'
    - ''
    - '&eComo usar?'
    - '&fAlimente o seu Pet mirando nele.'

# Item para obter o pote
bowl:
  material: 'FLOWER_POT_ITEM'
  name: '&ePote de Ração'
  lore:
    - '&7Utilize este item para obter'
    - '&7o pote de ração.'
    - ''
    - '&aClique para ativar.'

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'
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
  name: '&8Pets'
  size: 36
  slots: [ 11, 12, 13, 14, 15 ]
  previous-slot: 9
  next-slot: 17
  items:
    jar-slot: 30
    unequip-slot: 32
    hidden-slot: 33
    hidden:
      material: 'ENDER_PEARL'
      name: '&cOcultar'
      lore: ['&7Escolhe entre exibir seu pet', '&7a você e outros jogadores, ou', '&7apenas receber os buffs.', '', '&f Oculto: &r{status}', '', '&aClique para alternar']
    unequip:
      material: 'BARRIER'
      name: '&cDesequipar'
      lore: ['&7Clique aqui para desequipar', '&7o seu pet.']
    jar-no-has:
      material: 'FLOWER_POT_ITEM'
      name: '&ePote de Ração'
      lore:
        - '&7Armazene aqui a ração que'
        - '&7o seu PET irá consumir.'
        - ''
        - '&cVocê não possui o pote de ração para PET.'
    jar:
      material: 'FLOWER_POT_ITEM'
      name: '&ePote de Ração'
      lore:
        - '&7Armazene aqui a ração que'
        - '&7o seu PET irá consumir.'
        - ''
        - ' &fArmazenado: &a{amount}'
        - ''
        - '&8 * Tenha em mente que ao alimentar'
        - '&8   o seu PET, irá consumir a ração'
        - '&8   até ela acabar ou seu PET atingir'
        - '&8   o nível máximo.'
        - ''
        - '&7Botão esquerdo &8-> &fAlimentar o PET'
        - '&7Botão direito &8-> &fArmazenar'
    slot-empty:
      material: 'STAINED_GLASS_PANE:5'
      name: '&aSlot Livre'
      lore: []
    slot-need:
      material: 'STAINED_GLASS_PANE:14'
      name: '&cSlot Bloqueado'
      lore: []
  facing:
    e0:
      slot: 0
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e1:
      slot: 1
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e2:
      slot: 2
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e3:
      slot: 3
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e4:
      slot: 4
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e5:
      slot: 5
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e6:
      slot: 6
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e7:
      slot: 7
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e8:
      slot: 8
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e9:
      slot: 10
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e11:
      slot: 16
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e12:
      slot: 18
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e13:
      slot: 19
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e14:
      slot: 20
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e15:
      slot: 21
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e16:
      slot: 22
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e17:
      slot: 23
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e18:
      slot: 24
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e19:
      slot: 25
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []
    e20:
      slot: 26
      material: 'STAINED_GLASS_PANE:8'
      name: ' '
      lore: []

# Menu de armazenar comida
main-food:
  name: '&8Pets'
  size: 54
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

    &aPets comandos:

    &a> /pet givepet <player> <pet> <tier> <quantia>
    &a> /pet givefood <player> <quantia>
    &a> /pet giveslot <player> <quantia>
    &a> /pet givebowl <player> <quantia>
    &a> /pet reload

  slot-activated: '&aVocê ativou &e{amount} &ade slots.'
  slot-max: '&cVocê já chegou no máximo.'
  slot-give: '&aVocê deu &e{amount} &ade slots para o jogador &e{player}&a.'
  slot-enough: '&cVocê não possui slot disponíveis.'
  food-give: '&aVocê deu &e{amount} &ade ração para pet para o jogador &e{player}&a.'
  pet-give: '&aVocê deu &7{amount}x {pet}&a para o jogador &7{player}&a.'
  pet-received: '&aVocê recebeu &7{amount}x {pet}&a.'
  pet-list: |
    &cPet não encontrado.
    &cPet disponíveis: &f{list}
  pet-perm: '&cVocê não tem permissão para equipar este tipo de pet.'
  pet-equipped: '&aVocê está equipando o {pet}&a.'
  pet-already: '&cVocê já possui um pet deste tipo. Ademais, nenhum upgrade de tier foi possível.'
  pet-activated: '&aVocê ativou &7{amount}x {pet}&a.'
  pet-unequipped: '&cVocê desequipou seu PET.'
  pet-unequipped-none: '&cVocê não está equipando nenhum PET.'
  pet-collected: '&aVocê recolheu o seu PET.'
  pet-info: |

    &eInformações do PET

    &8-> &fNome: &r{pet} &8({player})
    &8-> &fTier: &6{tier} &7- {tier_display}

    &8-> &fEXP: &a{exp_has}&7/&c{exp_need} &8(Lvl. {level}/{level_max})
    &8-> &fProgresso: &7{progressbar} &7{percentage}

  pet-need-level: '&cOs PETS necessitam estar no mínimo no nível {level} para se juntarem e formarem o novo tier.'
  pet-equal-level: '&cOs PETS necessitam estar no mesmo nível para se juntarem e formarem o novo tier.'
  pet-tier-upgrade: '&aVocê evoluiu seu PET &f{pet} &a para o Tier &f{tier}&a.'
  pet-upgrade: '<nl>&eSeu &f{pet}&e atingiu o &fLvl. {level}&e e aprimorou o seu bônus!<nl>'
  pet-max: '&cO PET já está no nível máximo.'
  pet-none: '&cVocê não está equipando nenhum PET.'
  food-stored: '&aVocê armazenou &f{amount}&a rações para PET.'
  bowl-give: '&aVocê deu &e{amount} &ade pote de ração para pet para o jogador &e{player}&a.'
  bowl-already: '&cVocê já possui o pote de ração para PET.'
  bowl-activated: '&aVocê ativou o pote de ração para PET.'
  not-main-server: '&cNão é possível abrir o menu de pets, mas o seu bonus continua ativo.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/146-yPets">Site do plugin yPets</a>
    </category>
</seealso>