# yStackBosses
<secondary-label ref="rankup"/>

### Descrição
Agrupe bosses no melhor sistema da atualidade

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
<video src="//www.youtube.com/watch?v=dSRzcTK8J-M"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/boss - Abre o menu principal
/boss shop - Abre o menu do shop
/boss armazem - Abre o menu do armazem
/boss top - Abre o menu do top
/boss amuletos - Abre o menu dos amuletos
/boss bosses - Abre o menu dos bosses do servidor
/boss giveboss - Dar bosses para um jogador
/boss givematadora - Dar matadoras para um jogador
/boss giveamuleto - Dar amuletos para um jogador
/boss givebookdamage - Dar livro de dano ao jogador
/boss givestackdamage - Dar livro de stack ao jogador
/boss reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ystackbosses.use - Permissão para o /boss, /boss armazem, /boss top, /boss amuletos, /boss bosses
ystackbosses.shop - Permissão para o /boss shop
ystackbosses.giveboss - Permissão para o /boss giveboss
ystackbosses.giveamulet - Permissão para o /boss giveamuleto
ystackbosses.givesword - Permissão para o /boss givematadora
ystackbosses.givedamagebook - Permissão para o /boss givebookdamage
ystackbosses.givestackbook - Permissão para o /boss givestackdamage</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ystackbosses_killed% - Retorna a quantia de bosses mortos do jogador formatado (1K, 1M, 1T...)
%ystackbosses_killed_raw% - Retorna&nbsp;a quantia de bosses mortos&nbsp;do&nbsp;jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yStackBosses/
    ├── bosses/
    │    └── creeper.yml
    ├── shop/
    │    └── bosses.yml
    ├── swords/
    │    └── basic.yml
    ├── amulets.yml
    ├── commands.yml
    ├── config.yml
    ├── discounts.yml
    ├── economies.yml
    ├── enchants.yml
    ├── menus.yml
    ├── messages.yml
    └── rewards.yml
</code-block>
</chapter>

<chapter title="bosses" collapsible="true">
<chapter title="creeper.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# item do ovo
egg:
  material: '383:50'
  name: '&a&lBOSS CREEPER'
  lore: [ '&fHP: &4❤&c1000&f.', '', '&fQuantia: &b{amount}' ]

# Entidade que será spawnada
# Lista de entidades: https://helpch.at/docs/1.8.8/org/bukkit/entity/EntityType.html
entity: 'CREEPER'

# Vida do boss
health: 1000

# Nome do boss
name: '&a&lBOSS CREEPER &7x{stack}'

# Bater no boss apenas com uma matadora
sword-hit: true

custom-entity:
  # Ativar a entidade custom. Precisa do yStackBossesMPetAddon e do MiniaturePets
  enabled: false
  # Arquivo da entidade da pasta de pets do MiniaturePets
  entity: 'Boxer.mpet'

# Opções das entidades
entity-options:
  # Ativar/desativar a IA do mob
  ai: false
  # Caso a entidade for um esqueleto, ele vai ser wither?
  wither-skeleton: false
  # Caso a entidade for um zombie ou pig-zombie, ele vai ser bebê?
  baby-zombie: false
  # Tamanho da entidade caso seja um slime ou magma-cube
  slime-size: 1

message:
  kill:
    actionbar: '&c-{stack} &a&lBOSS CREEPER.'
    title: '&c-{stack} &a&lBOSS CREEPER.'
    chat: |

      &a&lBOSS CREEPER: &7Parabéns guerreiro, você conseguiu me matar. Recolha suas recompensas no &f&n/boss&7.

  hit:
    actionbar: '&a&lBOSS CREEPER &7(x{stack}) > &c❤ {health} &4[-{damage}] {progressbar}'
    title: ''
    chat: ''
  interact:
    actionbar: '&a&lBOSS CREEPER &7(x{stack}) > &c❤ {health} {progressbar}'
    title: ''
    chat: ''

# Efeitos que serão aplicados quando um jogador bater no boss
# Tipos: FOGO, EXPLOSAO, DANO, VENENO, EMPURRAR, NAUSEA, CEGUEIRA
effects:
  e1:
    chance: 10.0
    # Use: EFEITO:AMPLIFIER
    list: [ 'FOGO:10', 'EXPLOSAO:1', 'EMPURRAR:3' ]

# Recompensas do boss
# As recompensas são cadastradas na recompensas.yml
# Use: chance,recompense
# Quantia de recompensas que serão dadas
reward-amount: 1
# Dropar as recompensas no chão
reward-ground: false
rewards: [ '100,reward1' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="shop" collapsible="true">
<chapter title="bosses.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
bosses:
  1:
    # Tipo da maquina
    boss: 'creeper'
    # Placeholder {rank} na lore da compra indisponível
    rank: '&7[Membro]'
    # Permissão para comprar
    permission: ''
    # Data de liberação para comprar
    release-in: '16/10/2020-10:00'
    # Item do boss.
    item:
      material: '383:50'
      name: '&a&lBOSS CREEPER'
      lore:
        - ''
        - '&fPreço: &a{money} coins&f.'
        - ''
        - '&a&lFORMAS DE COMPRA'
        - ''
        - '&7&l• &fBotão direito: &7Comprar 1&f.'
        - '&7&l• &fBotão esquerdo: &7Escolher quantia&f.'
        - ''
    # Item do boss não disponível.
    item-release:
      material: '383:50'
      name: '&a&lBOSS CREEPER'
      lore:
        - ''
        - '&cVocê não pode comprar este boss.'
        - '&7Ele será liberado em: &f{date} - &f{hour}'
        - '&7Tempo para liberar: &f{time_formatted}'
        - ''
    # Item do boss sem permissão.
    item-permission:
      material: '383:50'
      name: '&a&lBOSS CREEPER'
      lore:
        - ''
        - '&cVocê não pode comprar este boss.'
        - '&7Você não possui permissão.'
        - ''
    prices:
      price1:
        provider: 'money'
        amount: 1000.0
]]>
</code-block>
</chapter>

</chapter>

<chapter title="swords" collapsible="true">
<chapter title="basic.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Item da espada
sword:
  material: DIAMOND_SWORD
  name: '&c&lMATADORA DE BOSSES &7(básica)'
  lore: [ '&fDano: &4❤&c{damage}&f.', '&fStack P/x: &bx{stack}&f.', '', '&aShift+Direito para evoluir' ]

display: '&c&lMATADORA DE BOSSES &7(básica)'

# Bosses que não poderão ser atacados com essa espada
bosses-blacklist: []

# Ativar a evolução da espada
evolute: true

# Esta espada vai matar o boss instantaneamente?
hit-kill: false

enchants:
  damage:
    default: 2
    add-per-level: 50
    max: 5
    prices:
      price1:
        provider: 'money'
        price: 1000.0
  stack:
    default: 1
    add-per-level: 1
    max: 5
    prices:
      price1:
        provider: 'money'
        price: 10000.0
]]>
</code-block>
</chapter>

</chapter>

<chapter title="amulets.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#     _                    _      _
#    / \   _ __ ___  _   _| | ___| |_ ___
#   / _ \ | '_ ` _ \| | | | |/ _ \ __/ __|
#  / ___ \| | | | | | |_| | |  __/ |_\__ \
# /_/   \_\_| |_| |_|\__,_|_|\___|\__|___/
#

# Sistema de amuletos
amulets:
  anti-damage:
    material: 'dd9850f0a95937be428d96e7b6f8a3e28d68afd5a688568b6936a44085639386'
    name: '&cBloquear dano'
    lore:
      - ''
      - '&7Este amuleto permite que você não'
      - '&7sofra dano dos bosses.'
      - ''
      - '&aClique para ativar'
  anti-knockback:
    material: '61a9ae9db36f70d467354069fbbdcc7d279baf6721561381da60d339b23d8829'
    name: '&cBloquear KnockBack'
    lore:
      - ''
      - '&7Este amuleto permite que você não'
      - '&7sofra knockback dos bosses.'
      - ''
      - '&aClique para ativar'
  anti-fire:
    material: '311e2e8f23609001106c07f1697a5a032646a85de8227033d33caab8c12c5e92'
    name: '&cBloquear fogo'
    lore:
      - ''
      - '&7Este amuleto permite que você não'
      - '&7receba fogo dos bosses.'
      - ''
      - '&aClique para ativar'
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
  boss: 'boss|bosses'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____  _             _    ____
#  _   _/ ___|| |_ __ _  ___| | _| __ )  ___  ___ ___  ___  ___
# | | | \___ \| __/ _` |/ __| |/ /  _ \ / _ \/ __/ __|/ _ \/ __|
# | |_| |___) | || (_| | (__|   <| |_) | (_) \__ \__ \  __/\__ \
#  \__, |____/ \__\__,_|\___|_|\_\____/ \___/|___/___/\___||___/
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
  # Habilitar o sistema de stack-bosses
  stack: true
  # Permitir colocar bosses e matar bosses apenas nos plots
  plot: false
  # Verifica se há mobs (ou outros bosses) por perto antes de spawnar
  # Raio em blocos.
  radius: 5
  # Delay para hitar os bosses
  # Deixe 0 para não usar
  # em millisegundos
  hit-delay: 500
  # Mundos bloqueados para colocar bosses
  world-blacklist: [ 'none' ]
  # Matar todos no shift
  shift-all: false
  # Matar todos sem shift
  no-shift-all: false
  # Quantia máxima que poderá matar
  # Cuidado com valores altos
  # -1 para infinito
  kill-maximum: 1000
  # Deletar a recompensa ao clicar com botão direito
  right-delete-reward: true
  # Blacklist de entidades que não serão verificadas no raio de "Mobs por perto"
  nearby-entity-blacklist: [ 'PLAYER', 'DROPPED_ITEM', 'ARROW', 'SPLASH_POTION', 'EXPERIENCE_ORB', 'THROWN_EXP_BOTTLE', 'SNOWBALL', 'EGG', 'ITEM' ]
  # Blacklist de metadata que não serão verificadas no raio de "Mobs por perto"
  nearby-metadata-blacklist: [ 'mascote' ]

effects:
  explosion:
    # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/Sound.html
    # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/Sound.html
    # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/Sound.html
    sound: 'EXPLODE'
    # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/Effect.html
    # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/Effect.html
    # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/Effect.html
    particle1: 'LAVA'
    particle2: 'VILLAGER_ANGRY'
    particle3: 'CLOUD'
  # Lista da 1.8: https://helpch.at/docs/1.8/org/bukkit/potion/PotionEffectType.html
  # Lista da 1.16: https://helpch.at/docs/1.16.2/org/bukkit/potion/PotionEffectType.html
  # Lista da 1.18: https://helpch.at/docs/1.18/org/bukkit/potion/PotionEffectType.html
  poison: 'POISON'
  confusion: 'CONFUSION'
  blindness: 'BLINDNESS'

# Sistema de lores
lore:
  chance: ['', '&6Chance: &f{chance}%', '']

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'

# Livro do encantamento damage
damage:
  # Mensagens
  give-book: '&bVocê deu &71x Livro de Dano {damage}&b para o jogador &f{player}.'
  received-book: '&bVocê recebeu &71x Livro de Dano {damage}&b.'
  maximum: '&cVocê não pode encantar esta espada, pois ela já está no máximo, com {damage} em Dano.'
  converted: '&bVocê compactou todos seus livros em 1.'
  # Item da sharpness ativável
  usable-item:
    material: ENCHANTED_BOOK
    name: '&b+{damage} Dano'
    lore:
      - ''
      - '&fDano: &b{damage}'
      - ''
      - '&7Clique em uma matadora para ativar.'

# Livro do encantamento damage
stack:
  # Mensagens
  give-book: '&bVocê deu &71x Livro de Kill-Stack {stack}&b para o jogador &f{player}.'
  received-book: '&bVocê recebeu &71x Livro de Kill-Stack {stack}&b.'
  maximum: '&cVocê não pode encantar esta espada, pois ela já está no máximo, com {stack} em Kill-Stack.'
  converted: '&bVocê compactou todos seus livros em 1.'
  # Item da sharpness ativável
  usable-item:
    material: ENCHANTED_BOOK
    name: '&b+{stack} Kill-Stack'
    lore:
      - ''
      - '&fKill-Stack: &b{stack}'
      - ''
      - '&7Clique em uma matadora para ativar.'
]]>
</code-block>
</chapter>

<chapter title="discounts.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
discounts:
  member:
    order: 1
    permission: 'ystackbosses.membro'
    display: '&7[Membro]'
    discount: 10.0 # em % do valor total
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
    permission: 'ystackbosses.provider.money'
]]>
</code-block>
</chapter>

<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#  _____            _                 _
# | ____|_ __   ___| |__   __ _ _ __ | |_ ___
# |  _| | '_ \ / __| '_ \ / _` | '_ \| __/ __|
# | |___| | | | (__| | | | (_| | | | | |_\__ \
# |_____|_| |_|\___|_| |_|\__,_|_| |_|\__|___/
#

enchants:
  damage:
    order: 1
    display: 'Dano'
    # Aparecer no menu de evolução
    menu: true
    can: # quando puder evoluir
      material: DIAMOND_SWORD
      name: '&cDano'
      lore:
        - '&fDano atual: &4❤&c{actual}&f.'
        - '&fDano próximo: &4❤&c{next}&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    can-not: # quando não puder evoluir
      material: DIAMOND_SWORD
      name: '&cDano'
      Lore:
        - '&fDano atual: &4❤&c{actual}&f.'
        - '&fDano próximo: &4❤&c{next}&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem coins suficientes.'
    max: # quando já estiver no máximo
      material: DIAMOND_SWORD
      name: '&cDano'
      Lore:
        - '&fDano atual: &4❤&c{actual}&f.'
        - ''
        - '&cVocê já está no máximo.'
    book:
      material: DIAMOND_SWORD
      name: '&cDano'
      Lore:
        - '&fDano: &4❤&c{amount}&f.'
        - ''
        - '&aClique na espada para adicionar.'
  stack:
    order: 2
    display: 'Stack'
    menu: true
    can: # quando puder evoluir
      material: BOOK
      name: '&bStack'
      lore:
        - '&fStack atual P/x: &bx{actual}&f.'
        - '&fStack próximo P/x: &bx{next}&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    can-not: # quando não puder evoluir
      material: BOOK
      name: '&bStack'
      Lore:
        - '&fStack atual P/x: &bx{actual}&f.'
        - '&fStack próximo P/x: &bx{next}&f.'
        - ''
        - '&f > Custo: &a{money} coins&f.'
        - ''
        - '&cVocê não tem coins suficientes.'
    max: # quando já estiver no máximo
      material: BOOK
      name: '&bStack'
      Lore:
        - '&fStack atual P/x: &bx{actual}&f.'
        - ''
        - '&cVocê já está no máximo.'
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
  name: '&8Bosses'
  size: 27
  items:
    profile-slot: 10
    amulets-slot: 11
    rewards-slot: 13
    bosses-slot: 14
    top-slot: 16
    shop-slot: 15
    profile:
      material: '{player}'
      name: '&aPerfil'
      lore:
        - ''
        - ' &fBosses mortos: &a{killed}&f.'
        - ' &fDano causado: &a{damage}&f.'
        - ' &fRecompensas no armazém: &a{rewards}&f.'
        - ''
    amulets:
      material: 'NETHER_STAR'
      name: '&aAmuletos'
      lore:
        - '&7Clique para gerenciar seus amuletos'
    rewards:
      material: 'CHEST'
      name: '&aRecompensas'
      lore:
        - ''
        - ' &fRecompensas no armazém: &a{rewards}&f.'
        - ''
        - '&7Clique para gerenciar'
    bosses:
      material: 'MONSTER_EGG'
      name: '&aBosses &7(PREVIEW)'
      lore:
        - '&7Clique para ver as possíveis'
        - '&7recompensas dos bosses do'
        - '&7nosso servidor.'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Jogadores'
      lore:
        - '&7Clique para ver os melhores'
        - '&7jogadores em relação aos bosses.'
    shop:
      material: 'EMERALD'
      name: '&6Loja'
      lore:
        - '&7Clique para comprar bosses!'

# Menu de amuletos
amulets:
  name: '&8Bosses'
  size: 27
  items:
    damage-slot: 11
    knockback-slot: 13
    fire-slot: 15
    back-slot: 9
    anti-damage-has:
      material: 'dd9850f0a95937be428d96e7b6f8a3e28d68afd5a688568b6936a44085639386'
      name: '&cBloquear dano'
      lore:
        - ''
        - '&7Este amuleto permite que você não'
        - '&7sofra dano dos bosses.'
        - ''
    anti-damage-no-has:
      material: '6193f8064d36a01787d3e59f5266b0e497dffb5f59f9ed8dd9dd508406e486b3'
      name: '&cBloquear dano'
      lore:
        - ''
        - '&7Este amuleto permite que você não'
        - '&7sofra dano dos bosses.'
        - ''
        - '&cVocê não possui este amuleto'
    anti-knockback-has:
      material: '61a9ae9db36f70d467354069fbbdcc7d279baf6721561381da60d339b23d8829'
      name: '&cBloquear KnockBack'
      lore:
        - ''
        - '&7Este amuleto permite que você não'
        - '&7sofra knockback dos bosses.'
        - ''
    anti-knockback-no-has:
      material: '6193f8064d36a01787d3e59f5266b0e497dffb5f59f9ed8dd9dd508406e486b3'
      name: '&cBloquear KnockBack'
      lore:
        - ''
        - '&7Este amuleto permite que você não'
        - '&7sofra knockback dos bosses.'
        - ''
        - '&cVocê não possui este amuleto'
    anti-fire-has:
      material: '311e2e8f23609001106c07f1697a5a032646a85de8227033d33caab8c12c5e92'
      name: '&cBloquear fogo'
      lore:
        - ''
        - '&7Este amuleto permite que você não'
        - '&7receba fogo dos bosses.'
        - ''
    anti-fire-no-has:
      material: '6193f8064d36a01787d3e59f5266b0e497dffb5f59f9ed8dd9dd508406e486b3'
      name: '&cBloquear fogo'
      lore:
        - ''
        - '&7Este amuleto permite que você não'
        - '&7receba fogo dos bosses.'
        - ''
        - '&cVocê não possui este amuleto'

# Menu de recompensas
main-rewards:
  name: '&8Bosses'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 16, 19, 21, 22, 23, 24, 25, 28, 29, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  #
  empty-slot: 22
  collect-slot: 50
  #
  items:
    empty:
      material: 'WEB'
      name: '&eVazio...'
      lore: [ '&7Nenhuma recompensa para', '&7coletar.' ]
    collect:
      material: 'a6cc486c2be1cb9dfcb2e53dd9a3e9a883bfadb27cb956f1896d602b4067'
      name: '&eRecolher tudo'
      lore: [ '&7Clique para recolher', '&7todas as recompensas.' ]

# Preview de bosses
bosses:
  name: '&8Bosses'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49
  lore:
    - '&fVocê já matou &b{amount}&f bosses desse tipo.'
    - ''
    - '&7Clique para ver as recompensas'

# Preview de recompensas
rewards-preview:
  name: '&8Bosses'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Preview de recompensas
evolute:
  name: '&8Bosses'
  size: 36
  slots: [ 11, 13, 15 ]
  back-slot: 29
  previous-slot: 18
  next-slot: 26
  # Slot onde ficará a espada do jogador
  sword-slot: 31
  profile-slot: 33
  items:
    profile:
      material: '{player}'
      name: '&a{player}'
      lore: [ '', '&fCoins: &b{money}', '' ]

# Menu do shop
shop:
  name: '&8Bosses'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34  ]
  back-slot: 27
  previous-slot: 45
  next-slot: 53
  items:
    info-slot: 48
    info:
      material: '1cba7277fc895bf3b673694159864b83351a4d14717e476ebda1c3bf38fcf37'
      name: '&aInformações gerais'
      lore:
        - '&fCoins: &7{money}&f.'
        - '&fDesconto: &7{discount}%&f.'

# Menu de top
top:
  name: '&8Top bosses'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 30
  previous-slot: 9
  next-slot: 17
  # Seletor dos tops
  selector:
    slot: 31
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor do TOP'
    # Tipos do seletor
    types:
      killed:
        enabled: true
        name: 'Bosses mortos'
      damage:
        enabled: true
        name: 'Dano causado'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'
  items:
    # Item do top bosses mortos
    killed:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fBosses mortos: &7{amount}'
        - '&fPosição: &e{pos}º'
        - ''
    # Item do top dano causado
    damage:
      material: '{player}'
      name: '&7{player}'
      lore:
        - ''
        - '&fDano causado: &7{amount}'
        - '&fPosição: &e{pos}º'
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

    &aBoss comandos:

    &a> /boss
    &a> /boss armazem
    &a> /boss top
    &a> /boss amuletos
    &a> /boss bosses
    &a> /boss giveboss <player> <boss> <quantia>
    &a> /boss givematadora <player> <matadora> <quantia>
    &a> /boss giveamuleto <damage/knockback/fire> <player/all> <quantia>

  boss-give: '&aVocê deu &7{amount}x {boss}&a para o jogador &7{player}&a.'
  boss-received: '&aVocê recebeu &7{amount}x {boss}&a.'
  boss-spawned: '&aVocê spawnou &7{amount}x {boss}&a.'
  boss-list: |
    &cBoss não encontrado.
    &cBosses disponíveis: &f{list}
  plot-permission: '&cVocê não tem permissão neste terreno.'
  spawners-mobs: '&cHá mobs ou spawners num raio de 5 blocos.'
  sword-list: |
    &cMatadora não encontrada.
    &cMatadoras disponíveis: &f{list}
  sword-give: '&aVocê deu &7{amount}x {sword}&a para o jogador &7{player}&a.'
  sword-received: '&aVocê recebeu &7{amount}x {sword}&a.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  amulet-give: '&aVocê deu {amount}x amuleto(s) do Boss para o jogador {player}.'
  amulet-give-target: '&aVocê recebeu {amount}x amuleto(s) do Boss.'
  amulet-give-all: |
    <nl>
    &aTodos os jogadores receberam {amount}x amuleto(s) do Boss.
    <nl>
  amulet-already: '&cVocê já possui este amuleto ativado.'
  amulet-activated: '&aAmuleto ativado com sucesso.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  evolute: '&aO encantamento &f{enchant}&a foi evoluído para o nível &f{level}&a.'
  holding: '&cVocê deve estar segurando sua matadora.'
  converted: '&bVocê compactou todos seus bosses em 1.'
  inv-full: '&cSeu inventário está cheio.'
  digit: |
    &aDigite a quantia de bosses que deseja.
    &7para cancelar digite &ncancelar&7.
  bought: |
    &bObrigado por adquirir bosses na loja de bosses. Confira as informações da compra:

    &7&l| &fBoss: &7{boss}&f.
    &7&l| &fQuantia: &7{amount}&f.
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
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static StackBossAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;StackBossAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(StackBossAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/106-yStackBosses">Site do plugin yStackBosses</a>
    </category>
</seealso>