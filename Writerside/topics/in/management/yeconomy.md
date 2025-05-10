# yEconomy
<secondary-label ref="management"/>

### Descrição
Gerencie a economia do seu servidor de uma forma simples e eficaz.

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
<video src="//www.youtube.com/watch?v=Pb0N5YV7HOw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/money - Abre o menu principal ou envia a quantia de money do jogador no chat.
/money [player] - Ver a quantia de money de outro jogador.
/money transacoes - Ver as transações recentes.
/money transacoes [player] - Ver as transações recentes de outro jogador.
/money enviar - Enviar coins para um jogador.
/money cheque - Criar um cheque.
/money criarcheque - Gerar um cheque para outro jogador
/money adicionar - Adicionar coins para um jogador.
/money remover - Remover coins de um jogador.
/money setar - Setar coins para um jogador.
/money formatar - Formatar ou deformatar uma quantia.
/money toggle - Ativar
/Desativar o recebimento de coins.
/money top - Abre o menu do top.
/money setnpc  - Setar o NPC do TOP.
/money delnpc  - Deletar o NPC do TOP.
/magnata - Mostra o magnata atual.
/cheque - Cria um cheque
/cheque [quantia] [player] - Gerar um cheque para outro jogador
/pay - Enviar coins para um jogador.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yeconomy.usar - Permissão para o /money
yeconomy.outros - Permissão para o /money
yeconomy.enviar - Permissão para o /money enviar e /pay
yeconomy.cheque - Permissão para o /money cheque e /cheque
yeconomy.criarcheque - Permissão para o /money criarcheque e /cheque [quantia] [player]
yeconomy.adicionar - Permissão para o /money adicionar
yeconomy.remover - Permissão para o /money remover
yeconomy.setar - Permissão para o /money setar
yeconomy.formatar - Permissão para o /money formatar
yeconomy.toggle - Permissão para o /money toggle
yeconomy.top - Permissão para o /money top
yeconomy.setnpc - Permissão para o /money setnpc
yeconomy.delnpc - Permissão para o /money delnpc
yeconomy.magnata - Permissão para o /magnata
yeconomy.transactions.others - Permissão para o /money transacoes [player]
yeconomy.death.bypass - Permissão para não perder money ao morrer</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yeconomy_money% - Retorna a quantia de money do jogador formatado.
%yeconomy_money_raw% - Retorna a quantia de money do jogador sem formatar.&nbsp;
%yeconomy_magnata% - Retorna a tag caso o jogador for o magnata.
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{magnata} - Tag do jogador mais rico (magnata)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEconomy/
    ├── commands.yml
    ├── config.yml
    ├── data.yml
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
# Lista de commands do plugin.

# Utilize "command|command" para criar aliases.
# Por exemplo: "gm|gamemode"
# Você pode criar quantas aliases quiser.
commands:
  money: 'money|coin|coins|balanço|balanco|balance'
  rich: 'rich|rico|magnata'
  pay: 'pay|pagar|enviar'
  check: 'check|cheque|cheques'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         _____
#  _   _| ____|___ ___  _ __   ___  _ __ ___  _   _
# | | | |  _| / __/ _ \| '_ \ / _ \| '_ ` _ \| | | |
# | |_| | |__| (_| (_) | | | | (_) | | | | | | |_| |
#  \__, |_____\___\___/|_| |_|\___/|_| |_| |_|\__, |
#  |___/                                      |___/
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

# Configurações do servidor redis
redis:
  # Ativar a conexão com o redis
  enabled: false
  # Endereço de conexão. [EX: 127.0.0.1]
  host: 'localhost'
  # Porta de conexão. [EX: 3306]
  port: 6379
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

# Sistemas gerais
general:
  # Ativar transações com players não conectados
  offline-transactions: true
  # Ao digitar /money abrir o menu.
  # False = Vai enviar a quantia de money que ele tem no chat
  # True = Vai abrir o menu
  money-menu: true
  # Ao ativar irá abrir o menu do top ao digitar /money top
  top-menu: true
  # Tempo que irá atualizar o top
  # Em segundos
  top-delay: 600
  # Tag do magnata no chat
  top-tag: '&2[$]'

# Preferências obrigatórias do sistema de coins
coin-preferences:
  # Quantia de money que o jogador vai começar
  initial-amount: 30.0
  # Formato do money na quantia singular
  singular-format: 'coin'
  # Formato do money no plural
  plural-format: 'coins'

# Configuração do money top em chat
top-chat:
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  rich-format: '{magnata} '
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  prefix-format: '%luckperms_prefix% '
  # Tags juntas
  tags: '{magnata}{prefixo}'
  # Formato geral do jogador no top
  player-format: '  &f{pos}º {tags}&7{player}&2: &7($ {money})'
  # Mensagem do TOP
  message: |
    &r
    &2Top 10 Mais Ricos &7(Atualizado de 10 em 10 minutos)
    &r
    {formato}
    &r

# Sistema de cheques do plugin
checks:
  main-check:
    material: PAPER
    glow: true
    name: '&aCheque de dinheiro'
    lore:
      - ''
      - '&7Criado por: &a{player}&7.'
      - '&7Criado em: &f{data} &8- &f{hora}&7.'
      - ''
      - '&bValor do cheque: &a{money}&b.'
      - ''
      - '&7Clique com botão direito para ativar'
  death-check:
    enabled: true
    # Máximo de money para o morto perder ( x % do seu money )
    maximum: 20000.0
    # Quando o jogador morrer, perder esta % de money
    percentage: 10.0
    item:
      material: PAPER
      glow: true
      name: '&aCheque de dinheiro'
      lore:
        - ''
        - '&7Dropado por: &a{player}&7.'
        - '&7Aniquiliado em: &f{data} &8- &f{hora}&7.'
        - ''
        - '&bValor do cheque: &a{money}&b.'
        - ''
        - '&7Clique com botão direito para ativar'

# Configurações do Holograma do NPC
npc:
  # Altura do holograma em cima do NPC
  offset: 3.1
  # Holograma do NPC
  hologram-lines:
    - '&a&lTOP &7&l#{pos}'
    - ''
    - '&e{nome}'
    - '&7Money: &f{money}'
    - ''
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Ultimo: 'none'

Data: {}
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
  name: '&8Balanço'
  size: 27
  items:
    info:
      slot: 10
      material: '{player}'
      name: '&aSuas informações'
      lore:
        - '&7Veja suas informações'
        - '&7referente ao money.'
        - ''
        - ' &fSaldo atual: &a{saldo}&f.'
        - ' &fTransações realizadas: &b{transacoes}&f.'
        - ' &fRecebimento de coins: &r{toggle}&f.'
        - ''
        - '&7Clique para ativar/desativar o'
        - '&7recebimento de coins.'
        - ''
    transactions:
      slot: 12
      material: '4883d656e49c38c6b5378572f31c63c4c7a5dd4375b6ecbca43f5971c2cc4ff'
      name: '&aTransações'
      lore:
        - '&7Veja as movimentações que'
        - '&7você realizou.'
        - ''
        - '&aClique para visualizar.'
    top:
      slot: 14
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTop jogadores'
      lore:
        - '&7Veja os jogadores que'
        - '&7se destacam sendo os'
        - '&7mais ricos do servidor.'
        - ''
        - '&aClique para visualizar.'
    rich:
      slot: 16
      material: 'f809d2e69610f1e6b75fe0d4598e441e560325d2d52d97cf66859c44fa3d8a79'
      name: '&aMagnata'
      lore:
        - ''
        - ' &fMagnata atual: &6{player}&f.'
        - ' &fSaldo do magnata: &a{saldo} {unidade}&f.'
        - ''

# Menu de top
top:
  name: '&8TOP Ricos'
  size: 36
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 31
  previous-slot: 9
  next-slot: 17
  # Item do top
  item:
    material: '{player}'
    name: '&f#{pos} &7> &a{player}'
    lore:
      - ''
      - '&fCoins: &a{money}&f.'
      - ''

# Menu de transações
transactions:
  name: '&8Histórico de transações'
  size: 45
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  back-slot: 31
  previous-slot: 27
  next-slot: 35
  items:
    added:
      material: '3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
      name: '&a+ {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Quantia adicionada: &a{money}&.'
        - ''
    received:
      material: '3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
      name: '&a+ {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Recebeu de &f{player}&7: &a{money}&.'
        - ''
    removed:
      material: 'bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
      name: '&c- {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Quantia removida: &a{money}&.'
        - ''
    paid:
      material: 'bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
      name: '&c- {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Pagou para &f{player}&7: &a{money}&.'
        - ''
    check:
      material: 'bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
      name: '&c- {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Cheque criado no valor: &a{money}&.'
        - ''

# Menu de transações de outro jogador
transactions-player:
  name: '&8Transações de {player}'
  size: 45
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]
  previous-slot: 27
  next-slot: 35
  items:
    added:
      material: '3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
      name: '&a+ {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Quantia adicionada: &a{money}&.'
        - ''
    received:
      material: '3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
      name: '&a+ {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Recebeu de &f{player}&7: &a{money}&.'
        - ''
    removed:
      material: 'bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
      name: '&c- {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Quantia removida: &a{money}&.'
        - ''
    paid:
      material: 'bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
      name: '&c- {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Pagou para &f{player}&7: &a{money}&.'
        - ''
    check:
      material: 'bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
      name: '&c- {money}'
      lore:
        - ''
        - '&7Data: &f{data} &8- &f{hora}&7.'
        - '&7Cheque criado no valor: &a{money}&.'
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
# Mensagens a serem enviadas pelo plugin.

# Mensagens do magnata
rich-new:
  chat: |

    &2&l[$]&a O jogador &f{player} &aé o novo &a&nMAGNATA&a do servidor.
    &7O novo magnata possui &f{money} &7{unidade}.

  actionbar: ''
  title: '&6{player}<nl>&aé o novo magnata.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a<--> Comandos da economia <-->

    &f > &a/money &8- &7Ver suas informações.
    &f > &a/money &f<jogador> &8- &7Ver as informações de outro jogador.
    &f > &a/money enviar &f<jogador> <quantia> &8- &7Enviar coins para um jogador.
    &f > &a/money formatar &f<quantia> &8- &7Formata a quantia em (numeros -> letras) ou (letras -> números).
    &f > &a/money toggle &8- &7Ativar/Desativar o recebimento de coins.
    &f > &a/money top &8- &7Ver o TOP mais ricos.
    &f > &a/magnata &8- &7Ver o jogador mais rico do servidor.

  help-staff: |

    &a<--> Comandos da economia &7(STAFF)&a <-->

    &f > &a/money &8- &7Ver suas informações.
    &f > &a/money &f<jogador> &8- &7Ver as informações de outro jogador.
    &f > &a/money enviar &f<jogador> <quantia> &8- &7Enviar coins para um jogador.
    &f > &a/money adicionar &f<jogador> <quantia> &8- &7Adicionar coins para um jogador.
    &f > &a/money remover &f<jogador> <quantia> &8- &7Remover coins de um jogador.
    &f > &a/money setar &f<jogador> <quantia> &8- &7Setar coins para um jogador.
    &f > &a/money formatar &f<quantia> &8- &7Formata a quantia em (numeros -> letras) ou (letras -> números).
    &f > &a/money toggle &8- &7Ativar/Desativar o recebimento de coins.
    &f > &a/money top &8- &7Ver o TOP mais ricos.
    &f > &a/money setnpc &f<1/2/3> &8- &7Setar o TOP NPC.
    &f > &a/money delnpc &f<1/2/3> &8- &7Deletar o TOP NPC.
    &f > &a/magnata &8- &7Ver o jogador mais rico do servidor.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  balance: '&aVocê possui: &f{money}&a {unidade}.'
  balance-target: '&aO jogador &7{player}&a possui: &f{money}&a {unidade}.'
  balance-set: '&aVocê setou o money do jogador &7{player} &apara: &f{money}&a {unidade}.'
  balance-removed: '&aVocê removeu &f{money}&a {unidade} do jogador &7{player}&a.'
  balance-added: '&aVocê adicionou &f{money}&a {unidade} para o jogador &7{player}&a.'
  balance-sent: '&aVocê enviou &f{money}&a {unidade} para o jogador &7{player}&a.'
  balance-received: '&aVocê recebeu &f{money}&a {unidade} do jogador &7{player}&a.'
  balance-format: '&f > &a&n{entrada} &e-> &a&n{saida}&a.'
  balance-check-activated: '&aVocê ativou um cheque no valor de &f{money}&a {unidade}&a.'
  balance-check-created: '&aVocê criou um cheque no valor de &f{money}&a {unidade}&a.'
  balance-check-give: '&aVocê criou um cheque no valor de &f{money}&a {unidade}&a para o jogador &f{player}&a.'
  balance-toggle-enabled: '&aVocê ativou o recebimento de coins.'
  balance-toggle-disabled: '&cVocê desativou o recebimento de coins.'
  rich-actual: |

    &2&l[$]&a O jogador &f{player} &aé o &a&nMAGNATA&a do servidor.
    &7O magnata possui &f{money} &7{unidade}.

  rich-none: '&cNão há nenhum magnata no servidor.'
  receive-disabled: '&cEste jogador desativou o recebimento de coins.'
  ilegal: '&cO argumento contém caracteres ilegais. Use apenas letras e números.'
  top-none: '&cNão há nenhum top nesta posição ainda.'
  no-has: '&cVocê não possui esta quantia de coins.'
  npc-set: '&aNPC setado.'
  npc-removed: '&aNPC removido.'
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEconomy/
    ├── menus/
    │    ├── principal.yml
    │    ├── top.yml
    │    ├── transacoes.yml
    │    └── transacoes_player.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Balanço'
Tamanho: 27
Itens:
  Informacoes:
    Slot: 10
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSuas informações'
    Lore:
      - '&7Veja suas informações'
      - '&7referente ao money.'
      - ''
      - ' &fSaldo atual: &a{saldo}&f.'
      - ' &fTransações realizadas: &b{transacoes}&f.'
      - ' &fRecebimento de coins: &r{toggle}&f.'
      - ''
      - '&7Clique para ativar/desativar o'
      - '&7recebimento de coins.'
      - ''
  Transacoes:
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4883d656e49c38c6b5378572f31c63c4c7a5dd4375b6ecbca43f5971c2cc4ff'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTransações'
    Lore:
      - '&7Veja as movimentações que'
      - '&7você realizou.'
      - ''
      - '&aClique para visualizar.'
  Top:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTop jogadores'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacam sendo os'
      - '&7mais ricos do servidor.'
      - ''
      - '&aClique para visualizar.'
  Magnata:
    Slot: 16
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/f809d2e69610f1e6b75fe0d4598e441e560325d2d52d97cf66859c44fa3d8a79'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aMagnata'
    Lore:
      - ''
      - ' &fMagnata atual: &6{player}&f.'
      - ' &fSaldo do magnata: &a{saldo} {unidade}&f.'
      - ''

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Magnata:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Ricos'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17
# Item do top
Item:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f#{pos} &7> &a{player}'
  Lore:
    - ''
    - '&fCoins: &a{money}&f.'
    - ''
]]>
</code-block>
</chapter>

<chapter title="transacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Histórico de transações'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
VoltarSlot: 27
ProximoSlot: 35

Adicionou:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Quantia adicionada: &a{money}&.'
      - ''

Recebeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Recebeu de &f{player}&7: &a{money}&.'
      - ''

Removeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Quantia removida: &a{money}&.'
      - ''

Pagou:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Pagou para &f{player}&7: &a{money}&.'
      - ''

Cheque:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Cheque criado no valor: &a{money}&.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="transacoes_player.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Transações de {player}'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
VoltarSlot: 27
ProximoSlot: 35

Adicionou:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Quantia adicionada: &a{money}&.'
      - ''

Recebeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
   ID: 0
   Data: 0
   Glow: true
   Name: '&a+ {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Recebeu de &f{player}&7: &a{money}&.'
      - ''

Removeu:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Quantia removida: &a{money}&.'
      - ''

Pagou:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Pagou para &f{player}&7: &a{money}&.'
      - ''

Cheque:
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/bd8a99db2c37ec71d7199cd52639981a7513ce9cca9626a3936f965b131193'
   ID: 0
   Data: 0
   Glow: true
   Name: '&c- {money}'
   Lore:
      - ''
      - '&7Data: &f{data} &8- &f{hora}&7.'
      - '&7Cheque criado no valor: &a{money}&.'
      - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
  Tipo: SQLITE #Tipos: MYSQL, SQLITE, MYSQL_FAST
  IP: localhost:3306
  DB: test
  User: admin
  Pass: ''
  Debug: true
  Avancado:
    CacheMemoryEntries: 150 # Numeros de jogadores que irão fizer armazenados na ram.
    CacheDiskSpace: 1024 # Espaço disponivel (em MB) no disco para armazenar o resto. Sempre coloque um numero muito superior ao necessário para não ter problemas
#Coloque Legendchat, OpeNChat (ou nChat), UltimateChat, NoxusChat ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'
# Comandos e aliases do plugin
Comando:
  Money:
    Comando: 'money'
    Aliases: [ coin, coins, balanço, balanco, balance ]
  Magnata:
    Comando: 'magnata'
    Aliases: [ rico ]
  Pagar:
    Comando: 'pay'
    Aliases: [ pagar, enviar ]
  Cheque:
    Comando: 'cheque'
    Aliases: [ cheques ]
# Opções gerais do plugin
Opcoes:
  # Ativar para funcionar transações com players offline
  Offline: true
  # Formato do money na quantia singular
  Singular: 'coin'
  # Formato do money no plural
  Plural: 'coins'
  # Ao digitar /money abrir o menu.
  # False = Vai enviar a quantia de money que ele tem no chat
  # True = Vai abrir o menu
  Menu money: true
  # Ao ativar irá abrir o menu do top ao digitar /money top
  Top menu: true
  # Quantia de money que o jogador vai começar
  Money inicial: 30.0
  # Tempo que irá atualizar o top
  # Em segundos
  Top atualizar: 600
  # Tag do magnata no chat
  Tag: '&2[$]'
  # Title que será enviado quando houver um
  # novo magnata.
  # Deixe '' para não usar
  Magnata title: '&6{player}<nl>&aé o novo magnata.'
  # Quantidade de casas decimais que irá mostrar nas placeholders (FORMATAÇÃO NUMERO)
  MaxDecimals: 4
# Configurações do Holograma do NPC
Holograma:
  # Altura do holograma em cima do NPC
  Altura: 3.1
  # Holograma do NPC
  Holograma:
    - '&a&lTOP &7&l#{pos}'
    - ''
    - '&e{nome}'
    - '&7Money: &f{money}'
    - ''
# Configuração do money top em chat
Top chat:
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  Magnata formato: '{magnata} '
  # O plugin irá reconhecer quando isto for apenas espaços e vai removê-los.
  Prefixo formato: '%luckperms_prefix% '
  Tags: '{magnata}{prefixo}'
  Formato: '  &f{pos}º {tags}&7{player}&2: &7($ {money})'
  Mensagem:
    - '&2Top 10 Mais Ricos &7(Atualizado de 10 em 10 minutos)'
    - ''
    - '{formato}'
    - ''
# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Nao encontrado: '&cEste jogador não está online.'
  Nao e numero: '&cO argumento não é um número.'
  Nao possui: '&cVocê não possui esta quantia de coins.'
  Si mesmo: '&cVocê não pode pagar à si mesmo.'
  Sem magnata: '&cNão há nenhum magnata no servidor.'
  Nenhum top: '&cNão há nenhum top nesta posição ainda.'
  Setado: '&aNPC setado.'
  Removido: '&aNPC removido.'
  Desativou: '&cEste jogador desativou o recebimento de coins.'
  Ilegal: '&cO argumento contém caracteres ilegais. Use apenas letras e números.'
  Balanco:
    - '&aVocê possui: &f{money}&a {unidade}.'
  Balanco target:
    - '&aO jogador &7{player}&a possui: &f{money}&a {unidade}.'
  Setou:
    - '&aVocê setou o money do jogador &7{player} &apara: &f{money}&a {unidade}.'
  Removeu:
    - '&aVocê removeu &f{money}&a {unidade} do jogador &7{player}&a.'
  Adicionou:
    - '&aVocê adicionou &f{money}&a {unidade} para o jogador &7{player}&a.'
  Enviou:
    - '&aVocê enviou &f{money}&a {unidade} para o jogador &7{player}&a.'
  Ativou:
    - '&aVocê ativou um cheque no valor de &f{money}&a {unidade}&a.'
  Criou:
    - '&aVocê criou um cheque no valor de &f{money}&a {unidade}&a.'
  DeuCheque:
    - '&aVocê criou um cheque no valor de &f{money}&a {unidade}&a para o jogador &f{player}&a.'
  Recebeu:
    - '&aVocê recebeu &f{money}&a {unidade} do jogador &7{player}&a.'
  Toggle ativou:
    - '&aVocê ativou o recebimento de coins.'
  Toggle desativou:
    - '&cVocê desativou o recebimento de coins.'
  Formatado:
    - '&f > &a&n{entrada} &e-> &a&n{saida}&a.'
  Novo magnata:
    - ''
    - '&2&l[$]&a O jogador &f{player} &aé o novo &a&nMAGNATA&a do servidor.'
    - '&7O novo magnata possui &f{money} &7{unidade}.'
    - ''
  Magnata atual:
    - ''
    - '&2&l[$]&a O jogador &f{player} &aé o &a&nMAGNATA&a do servidor.'
    - '&7O magnata possui &f{money} &7{unidade}.'
    - ''
  Help:
    - '&a<--> Comandos da economia <-->'
    - ''
    - '&f > &a/money &8- &7Ver suas informações.'
    - '&f > &a/money &f<jogador> &8- &7Ver as informações de outro jogador.'
    - '&f > &a/money enviar &f<jogador> <quantia> &8- &7Enviar coins para um jogador.'
    - '&f > &a/money formatar &f<quantia> &8- &7Formata a quantia em (numeros -> letras) ou (letras -> números).'
    - '&f > &a/money toggle &8- &7Ativar/Desativar o recebimento de coins.'
    - '&f > &a/money top &8- &7Ver o TOP mais ricos.'
    - '&f > &a/magnata &8- &7Ver o jogador mais rico do servidor.'
    - ''
  Help staff:
    - '&a<--> Comandos da economia &7(STAFF)&a <-->'
    - ''
    - '&f > &a/money &8- &7Ver suas informações.'
    - '&f > &a/money &f<jogador> &8- &7Ver as informações de outro jogador.'
    - '&f > &a/money enviar &f<jogador> <quantia> &8- &7Enviar coins para um jogador.'
    - '&f > &a/money adicionar &f<jogador> <quantia> &8- &7Adicionar coins para um jogador.'
    - '&f > &a/money remover &f<jogador> <quantia> &8- &7Remover coins de um jogador.'
    - '&f > &a/money setar &f<jogador> <quantia> &8- &7Setar coins para um jogador.'
    - '&f > &a/money formatar &f<quantia> &8- &7Formata a quantia em (numeros -> letras) ou (letras -> números).'
    - '&f > &a/money toggle &8- &7Ativar/Desativar o recebimento de coins.'
    - '&f > &a/money top &8- &7Ver o TOP mais ricos.'
    - '&f > &a/money setnpc &f<1/2/3> &8- &7Setar o TOP NPC.'
    - '&f > &a/money delnpc &f<1/2/3> &8- &7Deletar o TOP NPC.'
    - '&f > &a/magnata &8- &7Ver o jogador mais rico do servidor.'
    - ''

Cheque:
  ID: 339
  Glow: true
  Name: '&aCheque de dinheiro'
  Lore:
    - ''
    - '&7Criado por: &a{player}&7.'
    - '&7Criado em: &f{data} &8- &f{hora}&7.'
    - ''
    - '&bValor do cheque: &a{money}&b.'
    - ''
    - '&7Clique com botão direito para ativar'

Cheque morte:
  enabled: true
  # máximo de money para o morto perder ( x % do seu money )
  maximum: 20000.0
  # quando o jogador morrer, perder esta % de money
  percentage: 10.0
  item:
    ID: 339
    Glow: true
    Name: '&aCheque de dinheiro'
    Lore:
      - ''
      - '&7Dropado por: &a{player}&7.'
      - '&7Aniquiliado em: &f{data} &8- &f{hora}&7.'
      - ''
      - '&bValor do cheque: &a{money}&b.'
      - ''
      - '&7Clique com botão direito para ativar'

# Setas dos menus.
Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
  Anterior:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para ir à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróximo'
    Lore:
      - '&7Clique para ir à próxima página.'
# Sistema de formatos de money e quantia
format:
  type: 'LETRA' # Tipos: LETRA - NUMERO
  max-decimals: 4
  decimal-separator: ','
  grouping-separator: '.'
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

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/51-yEconomy">Site do plugin yEconomy</a>
    </category>
</seealso>