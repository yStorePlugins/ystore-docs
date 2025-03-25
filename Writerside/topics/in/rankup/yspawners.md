# ySpawners
<secondary-label ref="rankup"/>

### Descrição
Spawners com amigos e drops armazenados nele mesmo!

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

### Demonstração
<video src="//www.youtube.com/watch?v=eZMcE03CywQ"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/spawnerbooster - Mostra o status do booster
/spawneradmin givebooster - Dar boosters a um jogador
/spawneradmin givespawner - Dar spawners a um jogador
/spawneradmin givelimitstack - Dar limites de stack a um jogador
/spawneradmin givelimitdrop - Dar limites de venda a um jogador
/spawneradmin reload - Recarrega as configurações
/limitdrop - Mostra seu limite de drops
/limitdrop [player] - Mostra o limite de drops de outro jogador
/limitdrop enviar - Envia limite de drops para outro jogador
/limitdrop ajuda - Envia a mensagem de ajuda
/limitdrop set - Seta limite de drops para um jogador
/limitdrop add - Adiciona limite de drops para um jogador
/limitdrop remove - Remove limite de drops de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yspawnersv2.booster - Permissão para o /spawnerboosteryspawnersv2.givespawner - Permissão para o /spawneradmin givespawneryspawnersv2.givebooster - Permissão para o /spawneradmin giveboosteryspawnersv2.givelimit - Permissão para o /spawneradmin givelimitstack e /spawneradmin givelimitdropyspawnersv2.use - Permissão para o /spawneradminyspawnersv2.admin.reload - Permissão para o /spawneradmin reloadyspawnersv2.admin - Permissão para ser reconhecido como um ADM
yspawners.limitdrop.use - Permissão para o /limitdrop
yspawners.limitdrop.others - Permissão para o /limitdrop [player]
yspawners.limitdrop.send - Permissão para o /limitdrop enviar
yspawners.limitdrop.help - Permissão para o /limitdrop ajuda
yspawners.limitdrop.set - Permissão para o /limitdrop set
yspawners.limitdrop.add - Permissão para o /limitdrop add
yspawners.limitdrop.remove - Permissão para o /limitdrop remove</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── ySpawners/
    ├── spawners/
    │    └── cow.yml
    ├── bonus.yml
    ├── boosters.yml
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="spawners" collapsible="true">
<chapter title="cow.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
head: '5d6c6eda942f7f5f71c3161c7306f4aed307d82895f9d2b07ab4525718edc5'
egg: 'MONSTER_EGG:92'

# Item que poderá ser colocado no chão
# Necessário ser um bloco
item:
  material: '5d6c6eda942f7f5f71c3161c7306f4aed307d82895f9d2b07ab4525718edc5'
  name: '&eGerador de entidades'
  lore:
    - ''
    - '&f Tipo: &7Vaca&f.'
    - '&f Stack: &7{stack}'
    - ''
    - '&f Drops armazenados: &c{drops_stored}'
    - ''
    - '&f Upgrades:'
    - '&f  > Drops gerados por mob morto: &b{drops_round}'
    - '&f  > Velocidade de geração: &b{speed}s'
    - ''

# Nome que irá aparecer nas mensagens
name: '&fSpawner de Vaca'

# Nome da entidade
entity-name: 'Vaca'

# Permissão para poder por o spawner
permission: ''

# Permissão para poder matar os mobs
permission-kill: ''

# Entidade que irá spawnar
entity: 'COW'

# Vida do mob
health: 20.0

# Velocidade de geração
speed: 10

# Quebrar somente com silk touch
silk-touch: true

# Nível necessário de silk-touch para quebrar
silk-touch-level: 1

# Fazer o mob spawnar em cima da gaiola
above: false

# Distância que o mob irá spawnar da gaiola
distance: 2

# Gerar apenas com o dono ou amigo online
generate-online: false

# Gerar com o amigo online
generate-friend-online: false

# EXP (vanilla) que será dado ao jogador
exp: 1

custom-entity:
  # Ativar a entidade custom. Precisa do ySpawnersMPetAddon e do MiniaturePets
  enabled: false
  # Arquivo da entidade da pasta de pets do MiniaturePets
  entity: 'Boxer.mpet'

# Opções das entidades
entity-options:
  # Caso a entidade for um esqueleto, ele vai ser wither?
  wither-skeleton: false
  # Caso a entidade for um zombie ou pig-zombie, ele vai ser bebê?
  baby-zombie: false
  # Tamanho da entidade caso seja um slime ou magma-cube
  slime-size: 1

# Sistema de stack de spawners
stack-spawners:
  # Stack máximo de spawners (total)
  max: 2
  # Limite padrão de stack de spawners
  # Deixe 0 para não usar
  default-limit: 30
  # Raio de verificação de mobs e spawners
  radius: 5
  # Compra de limite por menu
  add-per-level: 10
  prices-per-level:
    price1:
      provider: 'money'
      price: 10000.0

# Sistema de stack de mobs
stack-mobs:
  # Ativar o stackmobs
  enabled: true
  # Nome do stackmob
  name: '&7{amount}x &c{mob}'
  # Quantia máxima do stackmob
  # deixe 0 para ser infinito
  max: 0
  # Desativar a inteligencia artificial do mob
  no-ai: true
  # Aplicar lentidão máxima na entidade (não funciona em entidades que voam)
  slow: true
  # Raio de verificação de mobs
  radius: 5
  # Ao matar segurando shift, irá matar apenas 1 mob do stackmobs.
  shift-unit: true
  # Ao matar sem shift, irá matar apenas 1 mob do stackmob
  no-shift-unit: false
  # Dar recompensas ao matar no shift
  shift-reward: false
  # Dar recompensas ao matar sem shift
  no-shift-reward: false
  # Habilitar os mobs de levar dano do ambiente
  mob-natural-damage: false
  # Habilitar os mobs de atacar players
  mob-attack: false
  # Permitir o creeper explodir (só funciona com o NoAI false)
  creeper-explode: false
  # Recompensas ao matar o mob
  # As recompensas são cadastradas na recompensas.yml
  # Use: chance,recompensa
  rewards: [ '100,reward1' ]
  # Limite padrão de stack de mobs
  # Deixe 0 para não usar
  default-limit: 0
  # Compra de limite por menu
  add-per-level: 10
  prices-per-level:
    price1:
      provider: 'money'
      price: 10000.0

# Sistema de quebrar o spawner
break:
  # Chance do spawner quebrar a cada onda (deixe 0 para não usar)
  chance: 10.0
  # Preço para consertar o spawner
  prices:
    price1:
      provider: 'money'
      amount: 1000.0

# Sistema de bloco de vidro
glass:
  # O spawner vai gerar um vidro com uma cabeça dentro?
  enabled: false
  # material do vidro
  material: 'STAINED_GLASS'
  # Data da cor do vidro
  data: 11
  # Ajuste a cabeça dentro do vidro
  off-set: -1.2
  # Animação da cabeça dentgro do vidro
  # Pode gerar lag
  animation-enabled: false
  # Velocidade da animação
  animation-speed: 4

# Partícula ao redor do spawner
# Pode gerar lag
particle:
  #type: 'SMALL_FLAME'
  # Deixe vazio para não usar
  type: ''
  # Cores
  red: 0.2
  green: 0.2
  blue: 0.2
  # Quantia de partículas
  count: 1
  # Offset - espalhar
  offset:
    x: 0.0
    y: 0.0
    z: 0.0

# Holograma que irá aparecer em cima do spawner
hologram:
  enabled: true
  # Altura em relação ao spawner
  off-set: 3.3
  # Utilize {head} para pegar a cabeça
  # Utilize {egg} para pegar o ovo
  # configurada acima. Ou coloque o material
  # por exemplo: "DIAMOND_BLOCK"
  lines:
  - '&aSpawner de Vaca'
  - '&fDono: &7{owner}&f.'
  - '&fStack: &7x{amount}&f.'
  - '&fDrops armazenados: &bx{drops}&f.'
  - '&fStatus: &r{status}'
  - ''
  - '[item]MONSTER_EGG:92'

# Upgrades do spawner
upgrades:
  # Quantidade de drops por mob morto
  drops:
    prices-per-level:
      price1:
        provider: 'money'
        amount: 10.0
    max: 5
    default: 1
    add-per-level: 2
  # Velocidade de geração de mobs
  speed:
    prices-per-level:
      price1:
        provider: 'money'
        amount: 15.0
    max: 5
    default: 0
    add-per-level: 1

# Hook com o mcMMO
mcmmo:
  swords: 1
  axes: 1
  unarmed: 1

# Sistema de drops
drop:
  # Ativar o armazém de drops
  storage: true
  # Dropar os drops no chão caso o spawner esteja público
  published-drop: true
  # Possibilitar recolher o drop no armazém
  collect: true
  # Possibilitar vender o drop no armazém
  sell: true

  # Botão que será realizada a venda (LEFT | RIGHT)
  sell-button: 'LEFT'
  # Botão que será realizado recolher (LEFT | RIGHT)
  collect-button: 'RIGHT'

  # Permissão para recolher drops (deixe vazio '' para não usar)
  collect-permission: 'yspawnersv2.cow.coletar'
  # Permissão para vender drops (deixe vazio '' para não usar)
  sell-permission: 'yspawnersv2.cow.vender'

  # Tipos de drop
  types:
    leather:
      # Chance de dropar
      chance: 100.0
      drop:
        material: 'LEATHER:0'
      name: '&fCouro'
      # ícone que irá ficar no menu de drops
      icon:
        material: 'LEATHER:0'
        name: '&fCouro'
        lore:
          - ''
          - ' &fDrops armazenados: &a{drops_stored}&f.'
          - ' &fValor por drop: &a100 coins&f.'
          - ' &fValor total: &a{money} coins&f.'
          - ' &fSeu bônus: &b{bonus_raw}%&f.' # bonus formatado: {bonus}
          - ''
          - '&aBotão &fESQUERDO&a para vender.'
          - '&aBotão &fDIREITO&a para recolher.'
      # Economias que o drop irá dar
      currencies:
        preco1:
          provider: 'money'
          amount: 100.0

  # O Drop vai executar um comando ao ser recolhido?
  # Caso seja um comando e o armazem estiver desativado
  # o spawner irá dropar itens que ao serem ativados
  # executarão o comando
  command:
    enabled: false
    # Preço por drop (para o comando)
    price: 100.0
    # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
    use-amount: true
    # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
    multiply-price: true
    # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
    inv-bypass: true
    # coletar diretamente, sem precisar digitar a quantia no chat (apenas quando os comandos tiverem ativos)
    collect-chat-bypass: true
    # formatar a quantia que será executada no comando. Ex: 1k, 10k, 1M
    amount-format: true
    commands: [ 'give {player} iron_ingot {quantia}' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
bonus:
  membro:
    order: 1
    # Permissão para ser reconhecido
    permission: 'yspawnersv2.bonus.membro'
    # Nome que irá aparecer nas mensagens
    display: '&7[Membro]'
    # Quantia do bônus em %
    bonus: 10.0
]]>
</code-block>
</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
boosters:
   booster1:
      # Duração do booster em segundos
      time: 60
      # Bônus de venda
      bonus: 10.0
      # Item do booster
      item:
         material: EXP_BOTTLE
         glow: true
         name: '&aBônus de Venda &7(drops)'
         lore: [ '', '&aTempo: &e{time}', '&aBônus: &e{bonus}%', '' ]
]]>
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
  spawner: 'spawner|spawners|spawneradmin'
  limitdrop: 'limitdrop'
  booster: 'spawnerbooster'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        ____                                         __     ______
#  _   _/ ___| _ __   __ ___      ___ __   ___ _ __ __\ \   / /___ \
# | | | \___ \| '_ \ / _` \ \ /\ / / '_ \ / _ \ '__/ __\ \ / /  __) |
# | |_| |___) | |_) | (_| |\ V  V /| | | |  __/ |  \__ \\ V /  / __/
#  \__, |____/| .__/ \__,_| \_/\_/ |_| |_|\___|_|  |___/ \_/  |_____|
#  |___/      |_|
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
  # Verifica se há mobs (ou outros spawners) por perto antes de colocar o spawner
  # Raio em blocos.
  radius: 5
  # Delay para hitar os mobs
  # Deixe 0 para não usar
  # em millisegundos
  hit-delay: 500
  # Mundos bloqueados para colocar spawners
  world-blacklist: [ 'none' ]
  # Formato do status do spawner quebrado
  broken-status: '&cQUEBRADO'
  # Fechar inventário dos jogadores que estiverem com o spawner aberta após ele ser quebrado
  close-broken: true
  # Limite máximo de amigos que um spawner pode ter
  # deixe 0 para ser infinito
  friend-max: 0
  # Acumular os bônus que tiver permissão
  accumulate-bonus: true
  # Sistema de bolsa de valores (yBolsa, StormEconomy ou HeroBolsa)
  bolsa: true
  # Formatador de bônus
  formatter-bonus-has: '&fBônus: &a{bonus}%&7 ({display}&7)'
  formatter-bonus-no-has: ''
  # Blacklist de nbttags que não pode bater no spawner
  nbttag-blacklist: [ 'yMinas-Pickaxe', 'yPlantacoes-Enxada', 'yCampo-Tool-Type' ]
  # Blacklist de nbttags que não vai descontar durabilidade
  nbttag-durability-blacklist: [ 'yMinas-Pickaxe', 'yPlantacoes-Enxada', 'yCampo-Tool-Type' ]
  # Habilitar o spawn de mob em spawners naturais
  natural-enabled: false
  # Rodar a task de limpeza de spawners inexistentes após 5 segundos do load do servidor
  spawner-clear-task: true
  # Permitir os jogadores desligarem as máquinas
  status-change: true
  # Permitir o jogador colocar apenas 1 stack de spawner de cada tipo
  just-one: false
  # Deletar as entidades ao desligar o servidor
  delete-shutdown: false
  # Deletar a entidade quando sobrar a entidade 0
  delete-zero: false

# Sistema para detectar matadoras
sword-detect:
  enabled: false
  whitelist-nbt: ['yEspadasFarm-Sword']

# Limite de stack de spawners.
limit-stack:
  material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  name: '&bLimite de stack'
  lore:
    - ''
    - '&fQuantia: &a{amount}'
    - ''
    - '&7Clique com botão direito no spawner para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
    - ''

# Limite de stack de mobs.
limit-mobs:
  material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
  name: '&bLimite de mobs'
  lore:
    - ''
    - '&fQuantia: &a{amount}'
    - ''
    - '&7Clique com botão direito no spawner para ativar.'
    - ''
    - '&7Clique com shift + botão direito para compactar'
    - '&7todos os seus limites no inventário em 1 só.'
    - ''

# Limite de venda de drops de spawners.
limit-drop:
  # Ativar o sistema
  enabled: false
  # Padrão que o jogador irá receber
  default: 64
  # Deixe 0 para ser infinito
  max: 0
  # Item do limite
  item:
    material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
    name: '&bLimite de Drops'
    lore:
      - ''
      - '&fQuantia: &a{amount}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus limites no inventário em 1 só.'
      - ''
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
    permission: 'yspawnersv2.provider.money'
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
  name: '&8Spawner'
  size: 36
  items:
    info-slot: 10
    drops-slot: 12
    upgrades-slot: 13
    options-slot: 14
    friends-slot: 21
    working-slot: 22
    broken-slot: 22
    public-slot: 23
    remove-slot: 19
    remove-limit-slot: -1
    remove-limit-mobs-slot: -1
    stack-spawners-limit-slot: 16
    stack-mobs-limit-slot: 25
    info:
      material: '{spawner}'
      name: '&aInformações Gerais'
      lore:
        - ''
        - ' &fDono: &7{owner}&f.'
        - ' &fStack: &7{stack}&f.'
        - ' &fStatus: &r{status}&f.'
        - ' &fDrops armazenados: &a{drops_stored}&f.'
        - ''
        - ' &f> Drops gerados por mob morto: &b{drops_round}&f.'
        - ' &f> Velocidade de geração: &b{speed_upgrade}s&f.'
        - ''
    drops:
      material: '12ef39437d7d43a034c5a40b974e8d2c6734a218c76485d04910f507bdc2e809'
      name: '&aDrops'
      lore:
        - '&7Gerencie os drops que estão'
        - '&7armazenados neste spawner.'
        - ''
        - ' &fDrops armazenados: &a{drops_stored}&f.'
        - ''
        - '&aClique para gerenciar.'
    upgrades:
      material: '365fc0426230a2e88df29d2d8ec4512e6dbdbc0777b4b83cdda2ede81864d6'
      name: '&aUpgrades'
      lore:
        - '&7Seu spawner necessita de'
        - '&7melhorias para ficar mais'
        - '&7eficiente.'
        - ''
        - '&aClique para acessar.'
    options:
      material: SULPHUR
      name: '&aOpções'
      lore:
        - '&7Gerencie as opções gerais da'
        - '&7seu spawner.'
        - ''
        - ' &fStatus: &r{status}&f.'
        - ' &fHolograma: &r{hologram_status}&f.'
        - ''
        - '&aBotão &fESQUERDO&a para alternar o status.'
        - '&aBotão &fDIREITO&a para alternar o holograma.'
    friends:
      material: '1cba7277fc895bf3b673694159864b83351a4d14717e476ebda1c3bf38fcf37'
      name: '&aAmigos'
      lore:
        - '&7Acesse as preferências de'
        - '&7amizade deste spawner.'
        - ''
        - '&aClique para acessar.'
    working:
      material: '333dcfb4da10177264968b449e724adebee3bc33b72bae85842b4aab9bd9c4db'
      name: '&aFuncional'
      lore:
        - '&7Seu spawner está funcionando normalmente.'
        - '&7Nenhum problema detectado.'
    broken:
      material: '1fdeaa7e3ce7e7434f8c983a3bad0ac2d020f81533bffc238bfb73cf824c92e'
      name: '&cQuebrada'
      lore:
        - '&7Seu spawner está quebrad0!'
        - ''
        - ' &fConserto: &a{money} coins&f.'
        - ''
        - '&aClique para consertar.'
    remove:
      material: BARRIER
      name: '&cRemover'
      lore:
        - '&7Remova spawners deste stack de'
        - '&7geradores.'
        - ''
        - '&aBotão &fESQUERDO&a para remover TODOS.'
        - '&aBotão &fDIREITO&a para escolher a quantia.'
    public:
      material: BOOK
      name: '&aPúblico'
      lore:
        - '&7Torne seu spawner público para'
        - '&7todos os jogadores do servidor.'
        - ''
        - ' &fStatus: &r{status}&f.'
        - ''
        - '&aBotão &fESQUERDO&a para alternar.'
    remove-limit:
      material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
      name: '&cRemover Limite Stack'
      lore:
        - '&7Remova limite de stack deste stack de'
        - '&7geradores.'
        - ''
        - '&fQuantia: &a{amount}'
        - ''
        - '&aClique para escolher a quantia.'
    remove-limit-mobs:
      material: '667da379f51d85d74fdba39a164d3f5062ef2ffc0b3e04d339376773931a4e'
      name: '&cRemover Limite Mobs'
      lore:
        - '&7Remova limite de mobs deste stack de'
        - '&7geradores.'
        - ''
        - '&fQuantia: &a{amount}'
        - ''
        - '&aClique para escolher a quantia.'
    stack-spawners-limit:
      material: FIREBALL
      name: '&aUpgrade de Limite-Stack'
      lore:
        - ''
        - ' &fAtual: &7{actual}/{maximum}&f.'
        - ' &fCusto para +{addperlevel}: &7{money} coins&f.'
        - ''
        - '&aClique para evoluir.'
    stack-spawners-limit-maximum:
      material: FIREBALL
      name: '&aUpgrade de Limite-Stack'
      lore:
        - ''
        - ' &fAtual: &7{actual}/{maximum}&f.'
        - ''
        - '&cEste armazém já está no máximo.'
    stack-mobs-limit:
      material: SLIME_BALL
      name: '&aUpgrade de Stack Mobs'
      lore:
        - ''
        - ' &fAtual: &7{actual}/{maximum}&f.'
        - ' &fCusto para +{addperlevel}: &7{money} coins&f.'
        - ''
        - '&aClique para evoluir.'
    stack-mobs-limit-maximum:
      material: SLIME_BALL
      name: '&aUpgrade de Stack Mobs'
      lore:
        - ''
        - ' &fAtual: &7{actual}/{maximum}&f.'
        - ''
        - '&cEste armazém já está no máximo.'

# Menu de amigos
friends:
  name: '&8Spawner'
  size: 54
  slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
  previous-slot: 9
  next-slot: 17
  back-slot: 18
  items:
    add-slot: 27
    add:
      material: '8e9b27fccd80921bd263c91dc511d09e9a746555e6c9cad52e8562ed0182a2f'
      name: '&aAdicionar amigo'
      lore:
        - '&7Clique aqui para adicionar'
        - '&7amigos para poder usar'
        - '&7este spawner.'
    friend:
      material: '{player}'
      name: '&a{player}'
      lore:
        - ''
        - '&aBotão &fDIREITO&a para deletar.'
        - ''

# Menu upgrades
upgrades:
  name: '&8Spawner'
  size: 27
  back-slot: 18
  items:
    drops-slot: 12
    speed-slot: 14
    drops:
      material: EYE_OF_ENDER
      name: '&aUpgrade de Drops'
      lore:
        - '&7Esta evolução faz com que o'
        - '&7mob produza mais drops'
        - '&7por morte.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fDrops obtidos por mob: &7{drops_actual}/{drops_max}&f.'
        - ' &fCusto para próx nível: &7{money} coins&f.'
        - ''
        - '&aClique para evoluir.'
    drops-max:
      material: EYE_OF_ENDER
      name: '&aUpgrade de Drops'
      lore:
        - '&7Esta evolução faz com que o'
        - '&7mob produza mais drops'
        - '&7por morte.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fDrops obtidos por mob: &7{drops_actual}/{drops_max}&f.'
        - ''
        - '&cVocê já está no máximo.'
    speed:
      material: EXP_BOTTLE
      name: '&aUpgrade de Velocidade'
      lore:
        - '&7Esta evolução faz com que o'
        - '&7tempo de geração do spawner'
        - '&7seja reduzido.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fTempo: &7{speed_actual}s/{speed_max}s&f.'
        - ' &fCusto para próx nível: &7{money} coins&f.'
        - ''
        - '&aClique para evoluir.'
    speed-max:
      material: EXP_BOTTLE
      name: '&aUpgrade de Velocidade'
      lore:
        - '&7Esta evolução faz com que o'
        - '&7tempo de geração do spawner'
        - '&7seja reduzido.'
        - ''
        - ' &fNível: &7{nivel_actual}/{nivel_max}&f.'
        - ' &fTempo: &7{speed_actual}s/{speed_max}s&f.'
        - ''
        - '&cVocê já está no máximo.'

# Menu de drops
drops:
  name: '&8Spawner'
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

    &aSpawners comandos:

    &a> /spawner
    &a> /spawner top
    &a> /spawner givespawner <player> <spawner> <quantia>
    &a> /spawner givelimitstack <player> <quantia>
    &a> /spawner givelimitdrop <player> <quantia>

  spawner-give: '&aVocê deu &7{amount}x {spawner}&a para o jogador &7{player}&a.'
  spawner-received: '&aVocê recebeu &7{amount}x {spawner}&a.'
  spawner-list: |
    &cSpawner não encontrado.
    &cSpawners disponíveis: &f{list}
  plot-permission: '&cVocê não tem permissão neste terreno.'
  spawners-mobs: '&cHá mobs ou spawners num raio de 5 blocos.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  gamemode: '&cEssa ação só pode ser realizada no modo survival.'
  perm-spawner: '&cVocê não tem permissão para colocar este tipo de spawner.'
  perm-this-spawner: '&cVocê não tem permissão para neste spawner.'
  perm-kill: '&cVocê não tem permissão para matar este mob.'
  perm-plot: '&cVocê não tem permissão neste terreno.'
  placed: '&a{amount}x {spawner} &acolocada(s).'
  broken: '&a{amount}x {spawner} &aremovida(s).'
  has-spawners: '&cHá spawners num raio de {radius} blocos.'
  silk-touch: '&cVocê precisa de uma picareta com toque suave para quebrar este spawner.'
  just-owner: '&cSomente o dono do spawner pode realizar esta ação.'
  repair: '&aVocê reparou seu spawner por {money} coins.'
  digit-remove: |

    &aDigite a quantia de spawners que deseja remover.
    &7para cancelar digite &ncancelar&7.

  digit-add: |

    &aDigite no chat o nome do seu amigo que quer adicionar.'
    &7para cancelar digite &ncancelar&7.'

  collect-need: '&cEste stack possui apenas {stack} spawners.'
  max-friend: '&cEste spawner atingiu o limite máximo de amigos.'
  added: '&aVocê adicionou o jogador &7{player}&a no seu spawner.'
  already-added: '&cEste jogador já está adicionado.'
  add-owner: '&cVocê não pode adicionar o dono como amigo no spawner.'
  upgraded: '&aVocê adquiriu &f+1 nível&a do upgrade por &f{money} coins&a.'
  limit-stack-give: '&aVocê deu &7{amount}x limites&a para o jogador &7{player}&a.'
  limit-stack-received: '&aVocê recebeu &7{amount}x limites&a.'
  limit-stack-converted: '&aVocê converteu todos seus limites em um só.'
  limit-stack-full: '&cEste spawner está no limite de stack máximo ({amount}).'
  limit-stack-fill: '&aVocê aumentou o limite de stack do spawner para {amount}.'
  sell: '&aVocê vendeu &7{amount}x {drop}&a por &6{money} coins &8{bonus}&a.'
  digit-collect: |

    &aDigite a quantia que você quer coletar.

    &8| &fVocê possui &6{amount}&f disponível.
    &8| &fDigite &8TUDO &fpara coletar tudo.

    &7Para cancelar digite &ncancelar&7.

  collect: '&aVocê coletou &7{amount}x {drop} (&8{bonus})&a.'
  inv-full: '&cSeu inventário está cheio.'
  insufficient: '&cEste spawner não possui drops suficiente.'
  nbttag-blacklist: '&cVocê não pode bater com este item.'
  world-blacklist: '&cVocê não pode colocar spawners neste mundo.'
  limit-drop-give: '&aVocê deu &7{amount}x limites&a para o jogador &7{player}&a.'
  limit-drop-received: '&aVocê recebeu &7{amount}x limites&a.'
  limit-drop-converted: '&aVocê converteu todos seus limites em um só.'
  limit-drop-full: '&cVocê já está no limite máximo ({amount}).'
  limit-drop-activated: '&aVocê aumentou o seu limite de drops para {amount}.'
  digit-limit-collect: |

    &aDigite a quantia que você quer coletar.

    &8| &fVocê possui &6{amount}&f disponível.

    &7Para cancelar digite &ncancelar&7.

  limit-default: '&cVocê não pode recolher uma quantia de limite que diminua o valor padrão.'
  limit-break: '&cVocê precisa quebrar alguns spawners.'
  limit-need: '&cVocê não possui limite suficiente.'
  limit-collect: '&aVocê coletou {amount} limites.'
  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  limit-drop-sent: '&bVocê enviou &f{amount} limite&b para o jogador &f{player}&b.'
  limit-drop-received-player: '&bVocê recebeu &f{amount} limite&b do jogador &f{player}&b.'
  limit-drop-no-has: '&bVocê não possui &f{amount} limite&b.'
  limit-drop-target-max: '&bO jogador já possui o máximo de limite permitido: &f{amount}&b.'
  limit-drop: '&bQuantidade de limite que você possui: &f{amount}&b.'
  limit-drop-target: '&bQuantidade de limite que &7{player}&b possui: &f{amount}&b.'
  limit-drop-changed: '&aLimite do jogador &7{player}&a alterado para &7{amount}&a.'
  limit-drop-help: |
    &aComandos do /limitedrop

    &f-> &b/limitedrop
    &f-> &b/limitedrop set
    &f-> &b/limitedrop add
    &f-> &b/limitedrop remove
    &f-> &b/limitedrop send
    &f-> &b/limitedrop help
    &f-> &b/limitedrop [player]
  spawner-already-placed: '&cVocê já colocou um spawner deste tipo.'
  booster-give: '&aVocê deu &7{amount}x Booster(s)&a para o jogador &7{player}&a.'
  booster-received: '&aVocê recebeu &7{amount}x Booster(s)&a.'
  booster-list: |
    &cBooster não encontrado.
    &cBooster disponíveis: &f{list}
  booster-finished: '&cSeu booster de drops acabou.'
  booster-already: '&cVocê já está usando um booster.'
  booster-activated: '&aVocê ativou um booster de drops. Multiplicador: &e{bonus}&a. Tempo: &e{time}&a.'
  booster-active: |

    &aSeu booster de drops está ativo!
    &f> &bTempo: &7{time}&f.
    &f> &bBônus: &7{bonus}%&f.

  booster-none: '&cVocê não possui nenhum booster de drops ativo.'
  limit-mobs-give: '&aVocê deu &7{amount}x limites&a para o jogador &7{player}&a.'
  limit-mobs-received: '&aVocê recebeu &7{amount}x limites&a.'
  limit-mobs-converted: '&aVocê converteu todos seus limites em um só.'
  limit-mobs-full: '&cEste spawner está no limite de mobs máximo ({amount}).'
  limit-mobs-fill: '&aVocê aumentou o limite de mobs do spawner para {amount}.'
  upgraded-mobs: '&aVocê adquiriu uma expansão da capacidade de stack mobs do spawner.'
  upgraded-spawners: '&aVocê adquiriu uma expansão da capacidade de stack do spawner.'
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
  reward2:
    preview:
      material: 'DIAMOND:0'
      name: '&bDiamante'
      amount: 1
      lore: [ '&bQuem não adora uma pedra preciosa?!' ]
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
  reward3:
    preview:
      material: 'EMERALD:0'
      name: '&aEsmeralda'
      amount: 1
      lore: [ '&aEsmeraldas valem muito?' ]
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
]]>
</code-block>
</chapter>

</chapter>
## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yspawners_limitdrop% - Retorna o limite de drops formatado (1K, 1M, 1T...)
%yspawners_limitdrop_raw% - Retorna o limite de drops sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static SpawnerV2APIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;SpawnerV2APIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(SpawnerV2APIHolder.class);
        return rsp == null ? null : rsp.getProvider();
    } catch (Throwable var1) {
        return null;
    }
}
</code-block>

## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/72-ySpawners">Site do plugin ySpawners</a>
    </category>
</seealso>