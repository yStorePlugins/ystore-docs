# yBossArena
<secondary-label ref="rankup"/>

### Descrição
Crie entidades que serão spawnadas em locais definidos

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
<video src="//www.youtube.com/watch?v=dJPComIREJ4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/bossarena - Abre o menu principal
/bossarena criar - Criar um boss novo
/bossarena editar - Editar um boss
/bossarena deletar - Deletar um boss
/bossarena daramuleto - Dar amuletos à um jogador
/bossarena reload- Recarregar as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ybossarena.use - Permissão para o /fragmentos
ybossarena.admin.create - Permissão para o /bossarena create
ybossarena.admin.delete - Permissão para o /bossarena delete
ybossarena.admin.edit - Permissão para o /bossarena edit
ybossarena.admin.reload - Permissão para o /bossarena reload
ybossarena.give - Permissão para o /bossarena daramuleto</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yBossArena/
    ├── commands.yml
    ├── config.yml
    ├── entities.yml
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
  bossarena: 'bossarena|ba'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#        ____                   _
#  _   _| __ )  ___  ___ ___   / \   _ __ ___ _ __   __ _
# | | | |  _ \ / _ \/ __/ __| / _ \ | '__/ _ \ '_ \ / _` |
# | |_| | |_) | (_) \__ \__ \/ ___ \| | |  __/ | | | (_| |
#  \__, |____/ \___/|___/___/_/   \_\_|  \___|_| |_|\__,_|
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

# Raio de checagem de mesmo boss existente
radius: 5

# Delay para hitar os bosses
# Deixe 0 para não usar
# em millisegundos
hit-delay: 500

# Redução de dano caso o jogador tenha protection na armadura
damage-protection:
  # Encantamento que será reconhecido
  enchantment: 'PROTECTION_ENVIRONMENTAL'
  # Quantidade de itens de armaduras que poderão somar na redução
  amount: 1
  # Nível, quantidade de dano que será reduzido
  levels:
    - '1,1.0'
    - '5,2.0'
    - '10,3.0'

# Sistema de spawnar bosses em horários definidos
auto-spawn:
  horario1:
    # nome do arquivo do boss sem o .yml
    boss: ''
    # todos, segunda, terca, quarta, quinta, sexta, sabado, domingo
    # dia-hora-minuto-segundo
    time: 'todos-00:00:01'

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

# Configuração da barra de progresso
progress-bar:
  amount: 10
  symbol: ':'
  color-yes: '&a'
  color-no: '&7'

# Sistema de lores
lore:
  chance: ['', '&6Chance: &f{chance}%', '']

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

<chapter title="entities.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
entities:
  creeper:
    entity: 'CREEPER'
    custom-name: '&aCreeper'
    display:
      selected:
        material: 'MONSTER_EGG:50'
        name: '&aCreeper'
        lore: [ '&fVocê está usando: &aCreeper&f.', '', '&7Clique para alterar a entidade.' ]
      select:
        material: 'MONSTER_EGG:50'
        name: '&aCreeper'
        lore: [ '&7Clique para usar esta entidade.' ]
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

# Settings menu
settings:
  name: '&8Boss configuração'
  size: 45
  items:
    name-slot: 10
    icon-slot: 11
    noai-slot: 13
    entity-slot: 15
    health-slot: 16
    rewards-slot: 21
    locations-slot: 23
    damage-slot: 28
    knockback-slot: 31
    fire-slot: 34
    name:
      material: 'LEGACY_NAME_TAG'
      name: '&aNome do Boss'
      lore:
        - '&fAtual: &a{name}&f.'
        - ''
        - '&7Clique para alterar'
    icon:
      material: 'ITEM_FRAME'
      name: '&aÍcone do Boss'
      lore:
        - '&7Clique em um item do seu inventário para alterar'
    noai:
      material: 'IRON_BOOTS'
      name: '&aMovimentos'
      lore:
        - '&fBoss pode movimentar: &a{noai}&f.'
        - ''
        - '&7Clique para alternar os movimentos'
    health:
      material: 'POTION:69'
      name: '&aVida do Boss'
      lore:
        - '&fAtual: &a{health}&f.'
        - ''
        - '&7Clique para alterar'
    rewards:
      material: 'CHEST'
      name: '&aRecompensas do boss'
      lore:
        - '&7Clique para gerenciar'
    locations:
      material: 'ENDER_PEARL'
      name: '&aLocais do boss'
      lore:
        - '&7Clique para gerenciar'
    damage:
      material: 'DIAMOND_SWORD'
      name: '&aDano do boss'
      lore:
        - '&fAtual: &a{damage}&f.'
        - '&fChance: &a{damage_chance}&f.'
        - ''
        - '&7ESQUERDO para alterar o dano'
        - '&7DIREITO para alterar a chance'
    knockback:
      material: 'FEATHER'
      name: '&aRepulsão'
      lore:
        - '&fEstado: &a{knockback}&f.'
        - '&fChance: &a{knockback_chance}&f.'
        - ''
        - '&7ESQUERDO para alternar o estado'
        - '&7DIREITO para alterar a chance'
    fire:
      material: 'BLAZE_POWDER'
      name: '&aFogo'
      lore:
        - '&fEstado: &a{fire}&f.'
        - '&fChance: &a{fire_chance}&f.'
        - ''
        - '&7ESQUERDO para alternar o estado'
        - '&7DIREITO para alterar a chance'

# Recompensas do boss
rewards:
  name: '&8Boss configuração'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  # item lore
  lore:
    - ''
    - '&fChance: &a{chance}%'
    - ''
    - '&7ESQUERDO para alterar a chance'
    - '&7BOTÃO Q para deletar'
  items:
    back-slot: 47
    add-slot: 49
    options-slot: 51
    add:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aAdicionar recompensa'
      lore:
        - '&7Clique para adicionar uma recompensa'
    options:
      material: 'REDSTONE'
      name: '&aConfigurações'
      lore:
        - ''
        - '&fQuantia de recompensas para dar: &7{amount}&f.'
        - '&fEnviar recompensas pro armazém: &7{storage}&f.'
        - '&fDropar no chão &7(caso a opção acima estiver false): &7{ground}&f.'
        - ''
        - '&7ESQUERDO para alterar a quantia'
        - '&7DIREITO para alternar enviar'
        - '&7SHIFT+ESQUERDO para alternar dropar no chão'

# Adicionar recompensa
add-reward:
  name: '&8Boss configuração'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Selecionar entidade
select-entity:
  name: '&8Boss configuração'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Locais do boss
locations:
  name: '&8Boss configuração'
  size: 54
  slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34 ]
  previous-slot: 18
  next-slot: 26
  items:
    back-slot: 48
    add-slot: 50
    location:
      material: 'PAPER'
      name: '&aLocal #{pos}'
      lore:
        - ''
        - '&fDelay de spawn: &a{delay}'
        - '&fSpawnando em: &a{delay_now}'
        - ''
        - '&fX: &a{x} &7- &fY: &a{y} &7- &fZ: &a{z} &7({world})'
        - ''
        - '&7ESQUERDO para alterar o delay'
        - '&7BOTÃO Q para deletar'
    add:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aAdicionar locais'
      lore:
        - '&7Clique para adicionar um novo local'

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
    <nl>
    &aBoss-Arena comandos:
    <nl>
    &a> /bossarena criar <boss>
    &a> /bossarena editar <boss>
    &a> /bossarena deletar <boss>
    &a> /bossarena daramuleto
    <nl>
  already-exists: '&cEste boss {boss} já existe.'
  no-exists: '&cEste boss {boss} não existe. Bosses cadastrados: {bosses}'
  created: '&aEste boss {boss} foi criado.'
  deleted: '&aEste boss {boss} foi deletado.'
  digit-name: |
    <nl>
    &aDigite o NOME que você quer.
    &7Para cancelar, digite &ncancelar&7.
    <nl>
  digit-chance: |
    <nl>
    &aDigite a CHANCE que você quer.
    &7Para cancelar, digite &ncancelar&7.
    <nl>
  digit-health: |
    <nl>
    &aDigite a VIDA que você quer.
    &7Para cancelar, digite &ncancelar&7.
    <nl>
  digit-damage: |
    <nl>
    &aDigite o DANO que você quer.
    &7Para cancelar, digite &ncancelar&7.
    <nl>
  digit-delay: |
    <nl>
    &aDigite o DELAY que você quer.
    &7Para cancelar, digite &ncancelar&7.
    <nl>
  digit-amount: |
    <nl>
    &aDigite a QUANTIA que você quer.
    &7Para cancelar, digite &ncancelar&7.
    <nl>
  change-name: '&aNome alterado para &f{name}&a.'
  change-health: '&aVida alterada para &f{health}&a.'
  change-chance: '&aChance alterada para &f{chance}&a.'
  change-damage: '&aDano alterado para &f{damage}&a.'
  change-delay: '&aDelay alterado para &f{delay}&a.'
  change-amount: '&aQuantia alterada para &f{amount}&a.'
  health-error: '&cA vida precisa ser maior que 0.'
  chance-error: '&cA chance não pode ser menor que 0 ou maior que 100.'
  delay-error: '&cO delay não pode ser menor ou igual a 0.'
  amount-error: '&cA quantia não pode ser menor ou igual a 0.'
  reward-collected: '&eItem recolhido com sucesso.'
  reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'
  amulet-give: '&aVocê deu {amount}x amuleto(s) do BossArena para o jogador {player}.'
  amulet-give-target: '&aVocê recebeu {amount}x amuleto(s) do BossArena.'
  amulet-give-all: |
    <nl>
    &aTodos os jogadores receberam {amount}x amuleto(s) do BossArena.
    <nl>
  amulet-already: '&cVocê já possui este amuleto ativado.'
  amulet-activated: '&aAmuleto ativado com sucesso.'
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


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/100-yBossArena">Site do plugin yBossArena</a>
    </category>
</seealso>