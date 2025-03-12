# yMcmmoUtil
<secondary-label ref="utility"/>

### Descrição
Um addon essencial para o mcMMO

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
<video src="//www.youtube.com/watch?v=_M5Csj_MaKI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/stats - Abre o menu de habilidades
/mctop - Abre o menu de ranking de habilidades
/mccreditos - Abre o menu de loja de créditos
/mccreditos [player] - Mostra os créditos de outro jogador
/mccreditos enviar [player] [quantia] - ~Envia créditos para outro jogador
/ymcmmoutil- Recarrega as configurações
/mccreditos set - Seta créditos para um jogador
/mccreditos add - Adiciona créditos para um jogador
/mccreditos remove - Remove créditos de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymcmmoutil.stat - Permissão para o /stats
ymcmmoutil.mctop - Permissão para o /mctop
ymcmmoutil.mccredits - Permissão para o /mccreditos
ymcmmoutil.mccredits.send - Permissão para o /mccreditos enviar
ymcmmoutil.mccredits.others - Permissão para o /mccreditos [player]
ymcmmoutil.ymcmmoutil - Permissão para o /ymcmmoutil
ymcmmoutil.mccredits.set - Permissão para o /mccreditos set
ymcmmoutil.mccredits.remove - Permissão para o /mccreditos remove
ymcmmoutil.mccredits.add - Permissão para o /mccreditos add</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ymcmmoutil_credit% - Retorna a quantia de créditos do jogador (Formatado)
%ymcmmoutil_credit_raw% - Retorna a quantia de créditos do jogador (Sem formatar)
%ymcmmoutil_credit_spent% - Retorna a quantia de créditos gastos do jogador (Formatado)
%ymcmmoutil_credit_spent_raw% - Retorna a quantia de créditos gastos do jogador (Sem formatar)
%ymcmmoutil_tags% - Retorna as tags que o jogador tem
%ymcmmoutil_tag_[nome]% - Retorna a tag específica se o jogador tiver
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMcmmoUtil/
    ├── commands.yml
    ├── config.yml
    ├── menus.yml
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
# Lista de comandos do plugin.

# Utilize "comando|comando" para criar aliases.
# Por exemplo: "gm|gamemode"
# Você pode criar quantas aliases quiser.
commands:
  mctop: 'mcmmotop|mctop'
  stat: 'stat|stats|mcmmostats|mcmmostat'
  ymcmmoutil: 'ymcmmoutil'
  mccredits: 'mccredits|mmocredits|mccreditos|mmocreditos|mccredito|mmocredito'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        __  __                                _   _ _   _ _
#  _   _|  \/  | ___ _ __ ___  _ __ ___   ___ | | | | |_(_) |
# | | | | |\/| |/ __| '_ ` _ \| '_ ` _ \ / _ \| | | | __| | |
# | |_| | |  | | (__| | | | | | | | | | | (_) | |_| | |_| | |
#  \__, |_|  |_|\___|_| |_| |_|_| |_| |_|\___/ \___/ \__|_|_|
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

#   __      _   _   _
#  / _\ ___| |_| |_(_)_ __   __ _ ___
#  \ \ / _ \ __| __| | '_ \ / _` / __|
#  _\ \  __/ |_| |_| | | | | (_| \__ \
#  \__/\___|\__|\__|_|_| |_|\__, |___/
#
# Sistemas principais.

# Ativar o sistema de loja no menu
shop-menu: true

# Acumular os bônus que tiver permissão
accumulate-bonus: false

# Sistemas gerais
general:
  formatter-bonus-has: '&a+{bonus}% por ser {display}&a.'
  formatter-bonus-no-has: ''

# Actionbar quando ganhar xp
actionbar:
  enabled: true
  # Mensagem que irá aparecer na actionbar ao ganhar XP do mcMMO
  message: '&a{skill}: {level} ({xp_has} / {xp_need}) +{xp_earned}XP'

# Sistema de mensagem ao upar de nível
level-up:
  enabled: true
  # Enviar mensagem a cada x level ( por exemplo, a cada 100 leveis em tal skill: lvl 100, 200...)
  level: 100
  strike: true
  message: |
    <nl>
    &b&lSKILLS: &bO jogador &f{player}&b atingiu o &fnível {nivel} &bna habilidade &f{skill}&f!
    <nl>

# Sistema de recompensas ao upar de nível
rewards:
  mining_lvl100:
    skill: 'MINING'
    level: 100
    reward:
      - 'give {player} stone 1'

# Sistema de tasks
task:
  # Segundos para atualizar o ranking
  ranking: 1800
  # Segundos para atualizar as tags
  tags: 1800

# Sistema de tags
tags:
  all:
    skill: ''
    tag: '&9[⚒] '
    # {ymcmmoutil_global} e %ymcmmoutil_ymcmmoutil_global%
    placeholder: 'ymcmmoutil_global'
    min-level: 0

# Você pode criar quantos bônus quiser
# Será dado o bônus ao ganhar XP.
bonus:
  membros:
    order: 1
    # Permissão para ser reconhecido
    permission: 'ymcmmoutil.bonus.membro'
    # Nome que irá aparecer nas mensagens
    display: '&7[Membro]'
    # Quantia do bônus em %
    bonus: 10.0

# Sistema de formatos de money e quantia
format:
  type: 'LETTER' # Tipos: LETTER - NUMBER
  max-decimals: 4
  formats:
    - ''
    - ''
    - 'K'
    - 'M'
    - 'B'
    - 'T'
    - 'Q'
    - 'QQ'
    - 'S'
    - 'SS'
    - 'O'
    - 'N'
    - 'D'
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

# Menu de habilidades
skills:
  name: '&8Habilidades'
  size: 54
  items:
    profile:
      slot: 12
      material: '{player}'
      name: '&a{player}'
      lore: [ '&7Nível total: &f{level}', '&7XP total: &f{xp}' ]
    ranking:
      slot: 14
      material: 'BOOK_AND_QUILL'
      name: '&eRanking de Habilidades'
      lore: [ '&7Clique para abrir o TOP de habilidades.' ]
    shop:
      slot: 13
      material: 'GOLD_INGOT'
      name: '&eShop de Habilidades'
      lore: [ '&7Clique para abrir o SHOP de habilidades.' ]
    skills:
      alchemy:
        slot: 20
        skill: 'ALCHEMY'
        material: 'POTION:8275'
        name: '&aAlquimia'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      swords:
        slot: 24
        skill: 'SWORDS'
        material: 'DIAMOND_SWORD'
        name: '&aEspadas'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      archery:
        slot: 29
        skill: 'ARCHERY'
        material: 'BOW'
        name: '&aArqueria'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      mining:
        slot: 30
        skill: 'MINING'
        material: 'DIAMOND_PICKAXE'
        name: '&aMineração'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      excavation:
        slot: 31
        skill: 'EXCAVATION'
        material: 'DIAMOND_SPADE'
        name: '&aEscavação'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      acrobactics:
        slot: 32
        skill: 'ACROBATICS'
        material: 'DIAMOND_BOOTS'
        name: '&aAcrobacias'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      axes:
        slot: 33
        skill: 'AXES'
        material: 'DIAMOND_AXE'
        name: '&aMachados'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      herbalism:
        slot: 39
        skill: 'HERBALISM'
        material: 'SAPLING'
        name: '&aHerbalismo'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      woodcutting:
        slot: 40
        skill: 'WOODCUTTING'
        material: 'LOG'
        name: '&aArvorismo'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]
      fishing:
        slot: 41
        skill: 'FISHING'
        material: 'FISHING_ROD'
        name: '&aPescaria'
        lore: [ '&7Nível: &f{level}', '&7XP: &f{xp}' ]

# Menu de habilidades
ranking:
  name: '&8Ranking de Habilidades'
  size: 54
  back-slot: 27
  items:
    skills:
      all:
        slot: 13
        skill: ''
        material: 'BOOK_AND_QUILL'
        name: '&eNível Total'
        lore:
         - '&f1º: &7{player_1} &8- &7{level_1}'
         - '&f2º: &7{player_2} &8- &7{level_2}'
         - '&f3º: &7{player_3} &8- &7{level_3}'
         - '&f4º: &7{player_4} &8- &7{level_4}'
         - '&f5º: &7{player_5} &8- &7{level_5}'
         - '&f6º: &7{player_6} &8- &7{level_6}'
         - '&f7º: &7{player_7} &8- &7{level_7}'
         - '&f8º: &7{player_8} &8- &7{level_8}'
         - '&f9º: &7{player_9} &8- &7{level_9}'
         - '&f10º: &7{player_10} &8- &7{level_10}'
      alchemy:
        slot: 20
        skill: 'ALCHEMY'
        material: 'POTION:8275'
        name: '&aAlquimia'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      swords:
        slot: 24
        skill: 'SWORDS'
        material: 'DIAMOND_SWORD'
        name: '&aEspadas'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      archery:
        slot: 29
        skill: 'ARCHERY'
        material: 'BOW'
        name: '&aArqueria'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      mining:
        slot: 30
        skill: 'MINING'
        material: 'DIAMOND_PICKAXE'
        name: '&aMineração'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      excavation:
        slot: 31
        skill: 'EXCAVATION'
        material: 'DIAMOND_SPADE'
        name: '&aEscavação'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      acrobactics:
        slot: 32
        skill: 'ACROBATICS'
        material: 'DIAMOND_BOOTS'
        name: '&aAcrobacias'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      axes:
        slot: 33
        skill: 'AXES'
        material: 'DIAMOND_AXE'
        name: '&aMachados'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      herbalism:
        slot: 39
        skill: 'HERBALISM'
        material: 'SAPLING'
        name: '&aHerbalismo'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      woodcutting:
        slot: 40
        skill: 'WOODCUTTING'
        material: 'LOG'
        name: '&aArvorismo'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'
      fishing:
        slot: 41
        skill: 'FISHING'
        material: 'FISHING_ROD'
        name: '&aPescaria'
        lore:
          - '&f1º: &7{player_1} &8- &7{level_1}'
          - '&f2º: &7{player_2} &8- &7{level_2}'
          - '&f3º: &7{player_3} &8- &7{level_3}'
          - '&f4º: &7{player_4} &8- &7{level_4}'
          - '&f5º: &7{player_5} &8- &7{level_5}'
          - '&f6º: &7{player_6} &8- &7{level_6}'
          - '&f7º: &7{player_7} &8- &7{level_7}'
          - '&f8º: &7{player_8} &8- &7{level_8}'
          - '&f9º: &7{player_9} &8- &7{level_9}'
          - '&f10º: &7{player_10} &8- &7{level_10}'

# Menu de shop
shop:
  name: '&8Shop de Habilidades'
  size: 27
  back-slot: 10
  profile:
    slot: 12
    material: '{player}'
    name: '&a{player}'
    lore: [ '&7Seus créditos: &f{credit}', "&7Créditos gastos: &f{spent}" ]
  items:
    swords:
      slot: 14
      skill: 'SWORDS'
      price: 1
      xp-amount: 500.0
      material: 'DIAMOND_SWORD'
      name: '&aEspadas'
      lore:
        - ''
        - ' &7XP: &f500'
        - ' &7Preço: &a1 crédito'
        - ''
        - '&aClique para comprar'
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
  credit: '&bVocê possui &f{credit}&b créditos.'
  credit-other: '&bO jogador &f{player}&b possui &f{credit}&b créditos.'
  credit-changed: '&bVocê alterou os créditos do jogador &f{player}&b para &f{credit}&b.'
  credit-self: '&cVocê não pode enviar para sí mesmo.'
  credit-has: '&cVocê não possui &f{credit}&c créditos&c.'
  credit-sent: '&bVocê enviou &f{credit}&b créditos para o jogador &f{player}&b.'
  credit-received: '&bVocê recebeu &f{credit}&b créditos do jogador &f{player}&b.'
  credit-buy: '&bVocê comprou xp no shop de habilidades.'
  help: |
    &bComandos disponíveis:
    &b-> &f/mccredits
    &b-> &f/mccredits <player>
    &b-> &f/mccredits enviar <player> <quantia>
    &b-> &f/mccredits set <player> <quantia>
    &b-> &f/mccredits add <player> <quantia>
    &b-> &f/mccredits remove <player> <quantia>
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/98-yMcmmoUtil">Site do plugin yMcmmoUtil</a>
    </category>
</seealso>