# yPayments
<secondary-label ref="management"/>

### Descrição
Seu site agora dentro do servidor!

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
<video src="//www.youtube.com/watch?v=6Yd1vvgoprs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/shop - Abre o menu principal
/virtualshop - Abre o menu de loja
/shop transacoes - Abre o menu de transações
/shop historico - Abre o menu de compras
/shop correio - Abre o menu de correio de produtos
/shop admin - Abre o menu principal de ADM
/shop resetarcorreio - Ativa os produtos comprados novamente para todos
/shop criardesconto - Cria um cupom de desconto
/shop deletardesconto - Deleta um cupom de desconto
/shop descontos - Lista os descontos disponíveis
/shop setnpc - Seta o NPC
/shop delnpc- Deleta o NPC
/shop reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ypayments.shop - Permissão para o /shop
ypayments.virtualshop - Permissão para o /virtualshop
ypayments.shop.transactions - Permissão para o /shop transacoes
ypayments.shop.historic - Permissão para o /shop historico
ypayments.shop.courier - Permissão para o /shop correio
ypayments.shop.resetcourier - Permissão para o /shop resetarcorreio
ypayments.shop.creatediscount - Permissão para o /shop criardesconto
ypayments.shop.deletediscount - Permissão para o /shop deletardesconto
ypayments.shop.discounts - Permissão para o /shop discounts
ypayments.shop.admin - Permissão para o /shop admin
ypayments.setnpc - Permissão para o /shop setnpc
ypayments.delnpc - Permissão para o /shop delnpcycambio.admin.reload - Permissão para o /cambio reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ypayments_spent% - Retorna o valor que o jogador já gastou
%ypayments_spent_raw% - Retorna o valor que o jogador já gastou sem formatar
%ypayments_refunded% - Retorna o valor que o jogador já reembolsou
%ypayments_refunded_raw% - Retorna o valor que o jogador já rembolsou sem formatar
%ypayments_price_[product]% - Retorna o valor que o produto custa
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPayments/
    ├── notifications/
    ├── categories.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── discord.yml
    ├── menus.yml
    ├── messages.yml
    └── products.yml
</code-block>
</chapter>

<chapter title="notifications" collapsible="true">
</chapter>

<chapter title="categories.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
categories:
  items:
    # Comando para acessar a categoria
    command: 'diamantes'
    # Permissão para acessar a categoria
    permission: ''
    # Categoria aparecer no menu principal
    main-menu: true
    # Slot no menu principal
    slot: 13
    # Ícone no menu principal
    icon:
      material: 'DIAMOND'
      name: '&aLoja de &bDiamantes'
      lore: ['&7Compre aqui os diamantes mais', '&7bonitos já lapidados.', '', '&aClique para acessar']
    # Configurações do menu
    menu:
      title: '&8Loja Virtual'
      size: 27
      back-slot: 9
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
  shop: 'loja|shop'
  buy: 'comprar|buy'
  virtual-shop: 'virtualshop|shopvirtual|lojavirtual|virtualloja'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#          ____
#  _   _ / ___|__ _ _ __ ___  _ __   ___
# | | | | |   / _` | '_ ` _ \| '_ \ / _ \
# | |_| | |__| (_| | | | | | | |_) | (_) |
#  \__, |\____\__,_|_| |_| |_| .__/ \___/
#  |___/                     |_|
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

# Sistemas gerais
general:
  # Delay para checagem da notificação de pagamento (automático)
  # Em segundos
  notification-delay: 10
  # Delay para checagem da notificação de pagamento (manual)
  # Em segundos
  manual-delay: 30
  # Embed do yDiscorHook para enviar a cobrança no privado
  dm-charge-embed: 'ypayments_private'
  # Tempo para enviar a mensagem de alerta de coleta
  # em minutos
  alert-message-time: 600

# Configuração do mercado-pago
mercado-pago:
  secret: ''
  id: ''
  notification-url: 'https://ystoreteste.000webhostapp.com/notification_mp.php'

# Configuração do picpay
picpay:
  picpay-token: ''
  seller-token: ''
  notification-url: 'https://ystoreteste.000webhostapp.com/notification_picpay.php'

# Configuração do paypal
paypal:
  email: ''
  notification-url: 'https://ystoreteste.000webhostapp.com/notification_paypal.php'

# Configuração do coinbase
coinbase:
  version: '2018-03-22'
  api-key: ''

# Configuração do Stripe
stripe:
  secret-key: ''
  success-url: 'https://ystoreplugins.com.br'

# Configuração do short.io
# Utilizado para encurtar o link do paypal
short-io:
  enabled: true
  # Deixe vazio para usar o da yStore
  secret-key: ''
  # Deixe vazio para usar o da yStore
  domain: ''

# Sistema de npc
npc:
  skin: 'Pitombaa'
  hologram:
    offset: 3.4
    hologram:
      - '&6&lLOJA VIRTUAL'
      - '&7Seu site agora ingame!'
      - '[item]EMERALD'

# Sistema de lores
lores:
  map:
    - ''
    - ' &fGerado em: &7{date} às {hour}'
    - ' &fProduto: &b{product}'
    - ' &fReferência: &b{reference}'
    - ''
  transaction-not-completed:
    - ''
    - ' &aBotão &fESQUERDO &apara atualizar.'
    - ' &aBotão &fDIREITO &apara pegar o mapa.'
    - ''

# Sistema de status
status:
  approved: '&aAprovado'
  processing: '&bProcessando...'
  pending: '&ePendente...'
  canceled: '&cCancelado'
  refunded: '&cReembolsado'
  in-mediation: '&dEm mediação...'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
version: '1.0.0'
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
options:
  approved:
    url: ''
    username: 'yPayments - Nova Compra'
  mediation:
    url: ''
    username: 'yPayments - Pedido de Reembolso'
  refunded:
    url: ''
    username: 'yPayments - Novo Reembolso'

embeds:
  bought:
    title: ':mailbox: Uma nova compra foi detectada'
    thumbnail: 'https://minotar.net/body/{player}/100.png'
    color: '#fff'
    content: ''
    footer:
      text: 'yStore © Todos os direitos reservados'
      image: ''
    fields:
      player:
        inline: true
        header: 'Player'
        content: '```{player}```'
      product:
        inline: true
        header: 'Produto'
        content: '```{product}```'
      price:
        inline: true
        header: 'Preço'
        content: '```{price}```'
      discount:
        inline: true
        header: 'Desconto'
        content: '```{discount}% - {coupon}```'
      reference:
        inline: true
        header: 'Referência'
        content: '```{reference} | {gateway}```'
      date_activated:
        inline: true
        header: 'Comprado em'
        content: '```{bought_date} às {bought_hour}```'
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
  name: '&8Loja Virtual'
  size: 27
  items:
    profile-slot: 10
    courier-slot: 11
    shop-slot: 13
    historic-slot: 14
    transactions-slot: 15
    top-slot: 16
    profile:
      material: '{player}'
      name: '&eSeu Perfil'
      lore:
        - '&7Confira detalhes do seu'
        - '&7jogador na nossa loja.'
        - ''
        - ' &8▶ &fDinheiro gasto: &aR$ {spent}'
        - ''
        - ' &8▶ &fReembolso: &cR$ {refunded}'
        - ''
        - ' &8▶ &fProdutos no correio: &7{to_collect}'
        - ' &8▶ &fCompras realizadas: &7{bought_amount}'
        - ''
    shop:
      material: 'GOLD_INGOT'
      name: '&6Shop'
      lore:
        - '&6Clique para comprar produtos!'
    courier:
      material: 'CHEST'
      name: '&6Correio'
      lore:
        - '&7Gerencie as compras'
        - '&7que você precisa recolher.'
        - ''
        - ' &8▶ &fProdutos no correio: &7{to_collect}'
        - ''
        - '&6Clique para gerenciar!'
    historic:
      material: 'EMERALD'
      name: '&dHistórico de Compras'
      lore:
        - '&7Consulte o histórico de'
        - '&7compras aprovadas realizadas'
        - '&7na loja.'
        - ''
        - '&dClique para acessar!'
    transactions:
      material: 'BOOK'
      name: '&cTransações'
      lore:
        - '&7Consulte a lista de'
        - '&7transações realizadas'
        - '&7na loja.'
        - ''
        - '&cClique para acessar!'
    top:
      material: '351137e11443a8fbb05fcd3ccc1af9bd2303918f35448185e3ed96ef184da'
      name: '&aTOP Jogadores'
      lore:
        - '&7Visualize os jogadores que estão'
        - '&7se destacando em compras na loja.'
        - ''
        - '&aClique para acessar!'

# Menu de loja
shop:
  name: '&8Loja Virtual'
  size: 27
  back-slot: 9

# Menu de transações
transactions:
  name: '&8Loja Virtual'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 48
  # Seletor dos tops
  selector:
    slot: 50
    material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
    name: '&aSeletor de STATUS'
    # Tipos do seletor
    types:
      approved:
        enabled: true
        name: 'Aprovado'
      processing:
        enabled: true
        name: 'Processando'
      pending:
        enabled: true
        name: 'Pendente'
      canceled:
        enabled: true
        name: 'Cancelado'
      refunded:
        enabled: true
        name: 'Reembolsado'
      in-mediation:
        enabled: true
        name: 'Em mediação'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{name}'
      select: ' &f• &7{name}'

# Menu de histórico de compras
historic:
  name: '&8Loja Virtual'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu de correio
courier:
  name: '&8Loja Virtual'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
  previous-slot: 18
  next-slot: 26
  back-slot: 49

# Menu top
top:
  name: '&8TOP LOJA'
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
      spent:
        enabled: true
        name: 'Gasto na Loja'
    # Formatos do seletor
    formats:
      seeing: ' &f• &a{nome}'
      select: ' &f• &7{nome}'
  items:
    # Item do top mais gasto
    spent:
      material: '{player}'
      name: '&f{player}'
      lore:
        - ''
        - '&fGasto na Loja: &aR$ {amount}'
        - '&fPosição: &e{pos}º'
        - ''

# Menu de gateways
gateways:
  name: '&8Loja Virtual'
  size: 27
  back-slot: 9
  items:
    picpay-slot: 11
    mercadopago-slot: 12
    paypal-slot: 13
    coinbase-slot: 14
    stripe-slot: 15
    pix-slot: 16
    discount-slot: 17
    picpay:
      material: '9d98c8409ac195df33c6cf1b185c2a3959e03e61be22e4ca323c5e47d5dfa686'
      name: '&aPicPay'
      lore:
        - ''
        - '&fValor original: &aR$ {price_original}'
        - '&fDesconto: &aR$ {price_discount}'
        - '&fValor total: &aR$ {price}'
        - ''
        - '&6Clique para comprar com PicPay!'
    mercadopago:
      material: 'c0c9a3a4ffbee61d1ee1c3a533355bda9cdc377e07b0ff8bc618d3977b7f86cc'
      name: '&bMercadoPago'
      lore:
        - ''
        - '&fValor original: &aR$ {price_original}'
        - '&fDesconto: &aR$ {price_discount}'
        - '&fValor total: &aR$ {price}'
        - ''
        - '&6Clique para comprar com MercadoPago!'
    paypal:
      material: 'd4dcfcfaf770e563c0cfdcd306a185ea9423fe169ccacea6b9037f233a2bf5c'
      name: '&bPayPal'
      lore:
        - ''
        - '&fValor original: &aR$ {price_original}'
        - '&fDesconto: &aR$ {price_discount}'
        - '&fValor total: &aR$ {price}'
        - ''
        - '&6Clique para comprar com PayPal!'
    coinbase:
      material: '614d862b3a6a8e3989f294b208d45b663a8aede643292b05a349e2f46ac721eb'
      name: '&bCoinbase'
      lore:
        - ''
        - '&fValor original: &aR$ {price_original}'
        - '&fDesconto: &aR$ {price_discount}'
        - '&fValor total: &aR$ {price}'
        - ''
        - '&6Clique para comprar com Coinbase!'
    stripe:
      material: '60ffad33d293b61765fc86ab55602b955b9e1e757a8e885d502b3dbba5425517'
      name: '&bStripe'
      lore:
        - ''
        - '&fValor original: &aR$ {price_original}'
        - '&fDesconto: &aR$ {price_discount}'
        - '&fValor total: &aR$ {price}'
        - ''
        - '&6Clique para comprar com Stripe!'
    pix:
      material: '60ffad33d293b61765fc86ab55602b955b9e1e757a8e885d502b3dbba5425517'
      name: '&bPIX &7(MercadoPago)'
      lore:
        - ''
        - '&fValor original: &aR$ {price_original}'
        - '&fDesconto: &aR$ {price_discount}'
        - '&fValor total: &aR$ {price}'
        - ''
        - '&6Clique para comprar com PIX &7(MercadoPago)&6!'
    discount:
      material: 'GOLD_INGOT'
      name: '&6DESCONTO'
      lore:
        - ''
        - '&fAtual: &b{coupon} &f-> &b{discount}%'
        - ''
        - '&6Clique para digitar um cupom!'

# Menu principal
main-admin:
  name: '&8Loja Virtual - ADMIN'
  size: 27
  items:
    profile-slot: 10
    approved-slot: 12
    refunded-slot: 13
    mediation-slot: 14
    report-slot: 16
    profile:
      material: 'BOOK'
      name: '&eDados Gerais'
      lore:
        - '&7Confira detalhes do seu'
        - '&7faturamento da loja.'
        - ''
        - ' &8▶ &fValor GANHO: &aR$ {earned}'
        - ' &8▶ &fValor REEMBOLSADO: &cR$ {refunded}'
        - ''
    approved:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aAPROVADOS'
      lore:
        - '&7Confira detalhes das ordens'
        - '&7que foram aprovadas.'
        - ''
        - '&aClique para acessar'
    refunded:
      material: '548d7d1e03e1af145b0125ab841285672b421265da2ab915015f9058438ba2d8'
      name: '&cREEMBOLSADAS'
      lore:
        - '&7Confira detalhes das ordens'
        - '&7que foram reembolsadas.'
        - ''
        - '&aClique para acessar'
    mediation:
      material: '6f97b4bf51ce2b22d6eb5ecc154a7ab393f6a4b0b142c884615317d019d89639'
      name: '&5EM MEDIAÇÃO'
      lore:
        - '&7Confira detalhes das ordens'
        - '&7que estão sendo reembolsadas.'
        - ''
        - '&aClique para acessar'
    report:
      material: '4883d656e49c38c6b5378572f31c63c4c7a5dd4375b6ecbca43f5971c2cc4ff'
      name: '&eGerar Extrato'
      lore:
        - '&7Confira detalhes de todas as ordens'
        - '&7que foram realizadas no servidor.'
        - ''
        - '&aClique para gerar'

# Menu de transações
transactions-admin:
  name: '&8Loja Virtual - ADMIN'
  size: 54
  slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
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

    &a/shop &8- &7Abre o menu principal.
    &a/shop transacoes &8- &7Abre o menu de transações.
    &a/shop historico &8- &7Abre o menu de compras.
    &a/shop correio &8- &7Abre o menu de correio de produtos.
    &a/shop comprar [produto] &8- &7Abre o menu de comprar o produto.

  help-admin: |

    &a/shop &8- &7Abre o menu principal.
    &a/shop transacoes &8- &7Abre o menu de transações.
    &a/shop historico &8- &7Abre o menu de compras.
    &a/shop correio &8- &7Abre o menu de correio de produtos.
    &a/shop comprar [produto] &8- &7Abre o menu de comprar o produto.
    &a/shop admin &8- &7Abre o menu principal de ADM.
    &a/shop resetarcorreio &8- &7Ativa os produtos comprados novamente para todos.
    &a/shop criardesconto &8- &7Cria um cupom de desconto.
    &a/shop deletardesconto &8- &7Deletar um cupom de desconto.
    &a/shop descontos &8- &7Lista os descontos disponíveis.
    &a/shop setnpc &8- &7Seta o NPC.
    &a/shop delnpc &8- &7Deleta o NPC.
    &a/shop reload &8- &7Recarrega a configuração.

  pay: |

    &aSua cobrança foi gerada com sucesso no meio de pagamento &f{gateway}&a.
    &7Clique &a&l<click:open_url:{url}>AQUI</click> &7para realizar o pagamento.

  wait: '&cVocê precisa aguardar {time} para realizar essa operação.'
  courier-reset: '&aAs compras do jogador &f{player}&a foram liberadas para coleta novamente.'
  courier-reset-all: '&aAs compras de &f{amount} jogadores&a foram liberadas para coleta novamente.'
  discount-created: |

    &aInformações do CUPOM gerada:

    &7CUPOM: &f<click:suggest_command:{coupon}><hover:show_text:"<red>{coupon}<newline>Clique para copiar</red>">{coupon}</hover></click>
    &fDesconto: &f{discount}%

    &7Usos: &f{use}
    &7Expira em: &f{date} às {hour}
  discount-found: '&cEste cupom {coupon} já existe.'
  discount-not-found: '&cEste cupom {coupon} não existe.'
  discount-deleted: '&aEsta cupom {coupon} foi deletado.'
  discount-digit: |

    &aDigite o CUPOM que você quer.
    &7Para cancelar, digite &ncancelar&7.

  discount-max: '&cEste cupom {coupon} esgotou.'
  discount-expired: '&cEste cupom {coupon} expirou em {date} às {hour}.'
  discount-applied: '&cEste cupom {coupon} foi aplicado.'
  discount-format: '  &8(<click:suggest_command:{id}><hover:show_text:"<red>{coupon}<newline>Clique para copiar</red>">{coupon}</hover></click>)&f {coupon}&6 -> &7{discount}&6 -> &7{use}&6 -> &7{date} às {hour}'
  discount-none: '&cNão há nenhum cupom disponível.'
  discounts: |

    &aInformações sobre os CUPONS disponíveis:

    &f  CUPOM:            &fDESCONTO:            &fUSOS:            &fEXPIRA EM:

    {format}

  generating-report: '&aGerando relatório na pasta &f/report&a.'
  credentials: '&cCredenciais não configuradas.'
  npc-set: '&aNPC setado com sucesso.'
  npc-deleted: '&aNPC removido com sucesso.'
  npc-not-set: '&cNPC não está definido.'
  product-found: |
    &cProduto não encontrado.
    &7Disponíveis: {list}
  minimum-stripe: '&cA compra precisa ser de no mínimo 50 centavos.'
  alert-message: |

    &a&lLOJA
    &aVocê possui &f{amount}x compras &apara serem coletadas no &f/shop&a.

  already-map: '&cVocê já possui um mapa com QR-Code no inventário.'
]]>
</code-block>
</chapter>

<chapter title="products.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
products:
  diamond:
    # Nome nas mensagens
    name: '&bDiamantes!'
    # Nome no pagamento
    title: 'yStore - Diamantes'
    # Meio de pagamento
    # Disponível: MERCADOPAGO, PICPAY, PAYPAL, COINBASE, STRIPE, PIX
    gateways: ['PICPAY', 'MERCADOPAGO', 'PAYPAL', 'COINBASE', 'STRIPE', 'PIX']
    # Meios de pagamento que irão dar o mapa
    # Disponível: MERCADOPAGO, PICPAY, PAYPAL, COINBASE, STRIPE, PIX
    map-gateways: ['PICPAY', 'MERCADOPAGO', 'PAYPAL', 'COINBASE', 'STRIPE', 'PIX']
    # Em reais
    price: 0.01
    # Lista de descontos já aplicados
    # GATEWAY:PORCENTAGEM
    gateway-discount: [ 'PIX:10.0' ]
    # Lista de gateways que não será possível aplicar cupom
    # GATEWAY
    coupon-block: []
    # O que será dado ao player
    rewards:
      commands: []
      items:
        diamond:
          material: DIAMOND
          amount: 10
    discord:
      # exclusivo yDiscordHook
      # enviar o embed no privado
      discordhook:
        enable: true
        dm-bought-embed: 'bought'
        dm-mediation-embed: ''
        dm-refunded-embed: ''
      # enviar o embed em um chat
      webhook:
        enable: true
        chat-bought-embed: 'bought'
        chat-mediation-embed: ''
        chat-refunded-embed: ''
    # Comandos que serão executados quando o for reembolsado
    commands-refunded: ['give {player} barrier 1']
    # Comandos que serão executados quando o jogador contestar
    commands-mediation: ['give {player} stone 1']
    # Mensagens que serão executadas ao aprovar
    messages:
      broadcast:
        chat: ''
        actionbar: ''
        title: ''
      private:
        chat: |

          &a&lLOJA
          &aObrigado pela sua compra na nossa loja.
          &7Desfrute do seu novo item &bDiamantes!

        actionbar: ''
        title: ''
      refunded:
        chat: |

          &a&lLOJA
          &cSua compra de referência &f{reference} &7{gateway}&c foi reembolsada.
          &7Sanções serão aplicadas.

        actionbar: ''
        title: ''
      in-mediation:
        chat: |

          &a&lLOJA
          &cSua compra de referência &f{reference} &7{gateway}&c foi contestada.
          &7Sanções serão aplicadas.

        actionbar: ''
        title: ''
      collect:
        chat: |

          &a&lLOJA
          &bOs itens da sua compra foram adicionados ao seu inventário.

        actionbar: ''
        title: ''
    # Ícone no menu
    icons:
      sell:
        categories: ['11,items', '11,main-menu']
        material: DIAMOND
        name: '&bDiamantes'
        amount: 10
        lore: [ '&7Ostente esses belíssimos', '&7diamantes no servidor.', '', '&fPreço: &2R$ &a0,01', '', '&7Clique para comprar' ]
      historic:
        material: DIAMOND
        name: '&bDiamantes'
        amount: 10
        lore: [ '&7Ostente esses belíssimos', '&7diamantes no servidor.', '', '&fReferência: &b{reference}&f.', '&aComprado em &f{date} &aàs &f{hour}', '&aPreço pago: &fR$ {price}' ]
      transactions:
        material: DIAMOND
        name: '&bDiamantes'
        amount: 10
        lore: [ '&7Ostente esses belíssimos', '&7diamantes no servidor.', '', '&fReferência: &b{reference}&f.', '&fStatus: &e{status}&f.', '&fGateway: &b{gateway}', '', '&aAtualizado em &f{date} &aàs &f{hour}', '&aPreço pago: &fR$ {price}', '' ]
      transactions-admin:
        material: DIAMOND
        name: '&bDiamantes'
        amount: 10
        lore: [ '&7Ostente esses belíssimos', '&7diamantes no servidor.', '', '&fJogador: &6{owner}', '&fReferência: &b{reference}&f.', '&fStatus: &e{status}&f.', '&fGateway: &b{gateway}', '', '&aAtualizado em &f{date} &aàs &f{hour}', '&aPreço pago: &fR$ {price}', '' ]
      collect:
        material: DIAMOND
        name: '&bDiamantes'
        amount: 10
        lore: [ '&7Ostente esses belíssimos', '&7diamantes no servidor.', '', '&fReferência: &b{reference}&f.', '', '&aClique para recolher' ]
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/112-yPayments">Site do plugin yPayments</a>
    </category>
</seealso>