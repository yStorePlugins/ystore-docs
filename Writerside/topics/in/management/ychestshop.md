# yChestShop
<secondary-label ref="management"/>

### Descrição
Venda itens por placas usando diferentes economias

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
<video src="//www.youtube.com/watch?v=F9w_SIesY88"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/ychestshop setowner&nbsp;- Seta o dono da placa
/ychestshop reload&nbsp;- Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ychestshop.admin - Permissão para o /ychestshop reload e /ychestshop setowner
ychestshop.create - Permissão para criar placas normais
ychestshop.shop.hologram - Permissão para poder habilitar o holograma na loja
ychestshop.shop.name - Permissão para poder trocar o nome na loja
ychestshop.break.other - Permissão para quebrar placas de outros jogadores
ychestshop.break.admin - Permissão para quebrar placas de loja admin
ychestshop.create.admin - Permissão para criar placas de loja admin</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yChestShop/
    ├── commands.yml
    ├── config.yml
    ├── economies.yml
    ├── menus.yml
    ├── messages.yml
    └── plugin.yml
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
  ychestshop: 'ychestshop|chestshop|cs'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____ _                _    ____  _
#  _   _ / ___| |__   ___  ___ | |_ / ___|| |__   ___  _ __
# | | | | |   | '_ \ / _ \/ __|| __|\___ \| '_ \ / _ \| '_ \
# | |_| | |___| | | |  __/\__ \| |_  ___)| | | || (_)|| |_) |
#  \__, |\____|_| |_|\___||___/\__||____/|_| |_|\___/| .__/
#  |___/                                             |_|
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

# Ativar o sistema de menu para comprar na loja
sign-buy-menu: true

# Quantia máxima de caracteres do nome do item da loja
max-item-characters: 20

# Traduzir nome dos itens padrões para português
translate-names: true

# Ativar comercialização com o botão Q
button-q: true

# Vender o inv inteiro usando o shift
shift-sell-all: true

# Rodar a task de limpeza de placas inexistentes após 5 segundos do load do servidor
shop-clear-task: true

# Ativar o sistema de bolsa (yBolsa, NextEconomy, StormEconomy e HeroBolsa)
bolsa: false

# Tipo padrão da placa
# BUY - Players compram
# SELL - Players vendem
# BUYSELL - Playeres compram e vendem
default-type: 'SELL'

# Lore do ícone de selecionar item na configuração da placa
item-select-lore: [ '&aClique em um item do seu inventário para alterar' ]

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Sistema de holograma na loja de jogadores
sign-hologram:
  enabled: true
  hologram-buy:
    offset: 3.0
    lines:
      - '{item_name}'
      - '[item][shopitem]'
      - '&fLoja de &b{player}'
      - '&fQuantia comercializada: &b{amount}'
      - '&fEconomia utilizada: &b{provider}'
      - '&fPreço de compra: &b{price_buy} {provider_abbreviated}'
  hologram-sell:
    offset: 3.0
    lines:
      - '{item_name}'
      - '[item][shopitem]'
      - '&fLoja de &b{player}'
      - '&fQuantia comercializada: &b{amount}'
      - '&fEconomia utilizada: &b{provider}'
      - '&fPreço de venda: &b{price_sell} {provider_abbreviated}'
  hologram-buy-sell:
    offset: 3.5
    lines:
      - '{item_name}'
      - '[item][shopitem]'
      - '&fLoja de &b{player}'
      - '&fQuantia comercializada: &b{amount}'
      - '&fEconomia utilizada: &b{provider}'
      - '&fPreço de compra: &b{price_buy} {provider_abbreviated}'
      - '&fPreço de venda: &b{price_sell} {provider_abbreviated}'
  hologram-buy-admin:
    offset: 3.0
    lines:
      - '{item_name}'
      - '[item][shopitem]'
      - '&aLoja do Servidor'
      - '&fQuantia comercializada: &b{amount}'
      - '&fEconomia utilizada: &b{provider}'
      - '&fPreço de compra: &b{price_buy} {provider_abbreviated}'
  hologram-sell-admin:
    offset: 3.0
    lines:
      - '{item_name}'
      - '[item][shopitem]'
      - '&aLoja do Servidor'
      - '&fQuantia comercializada: &b{amount}'
      - '&fEconomia utilizada: &b{provider}'
      - '&fPreço de venda: &b{price_sell} {provider_abbreviated}'
  hologram-buy-sell-admin:
    offset: 3.5
    lines:
      - '{item_name}'
      - '[item][shopitem]'
      - '&aLoja do Servidor'
      - '&fQuantia comercializada: &b{amount}'
      - '&fEconomia utilizada: &b{provider}'
      - '&fPreço de compra: &b{price_buy} {provider_abbreviated}'
      - '&fPreço de venda: &b{price_sell} {provider_abbreviated}'

# Sistema de nomeação da placa
# Será identificado na primeira linha da placa
sign-definer:
  admin: 'lojaadmin'
  player: 'loja'

# Sistema de formatação da placa
sign-format:
  # Outras placeholder de preços: {price_buy_raw}, {price_sell_raw} (sem formatação de letra)
  buy: '&2C &r{price_buy} &7({provider_abbreviated})'
  sell: '&cV &r{price_sell} &7({provider_abbreviated})'
  buy-sell: '&2C &r{price_buy} | &cV &r{price_sell} &7({provider_abbreviated})'
  free: 'Grátis'
  sign:
    admin:
      line-1: '&aLoja Admin'
      line-2: '{format}'
      line-3: '{amount}'
      line-4: '&0Clique para ver' # placeholder {item_name} disponível
    player:
      line-1: '&a{owner}'
      line-2: '{format}'
      line-3: '{amount}'
      line-4: '&0Clique para ver' # placeholder {item_name} disponível

# Sistema de bônus
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender para a loja do servidor.
bonus:
  member:
    priority: 1
    # Permissão para ser reconhecido
    permission: 'ychestshop.bonus.member'
    # Quantia do bônus em %
    bonus: 10.0

# Sistema de descontos
# Você pode criar quantos descontos quiser
# Será dado o desconto ao comprar da loja do servidor.
discounts:
  member:
    priority: 1
    # Permissão para ser reconhecido
    permission: 'ychestshop.discount.member'
    # Quantia do desconto em %
    discount: 10.0

# Sistema de formatos de money e quantia
format:
  type: 'NUMBER' # Tipos: LETTER - NUMBER
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

# Economia padrão que irá vir na placa
# Deixe '' (vazio) para não usar
default: 'money'

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
    # Habilitar o sistema de bônus na economia
    bonus-allowed: true
    # Habilitar o sistema de desconto na economia
    discount-allowed: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'ychestshop.provider.money'
    # ‘Item’ que aparecerá para os jogadores ao interagir com a placa
    item:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &aEsta loja está comercializando com &fMoney&a.'
        - ''
    # ‘Item’ que aparecerá para o dono ao editar/criar a placa
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ''
        - '&aClique para alterar'
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

# Menu de configuração
settings:
  name: '&8Configuração da loja'
  size: 36
  items:
    item-slot: 11
    provider-slot: 13
    type-slot: 14
    price-slot: 15
    name-slot: 20
    amount-slot: 21
    open-close-slot: 22
    hologram-slot: 23
    warns-slot: 24
    item:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aItem que será comercializado'
      lore:
        - '&7Item que será utilizado no comércio'
        - '&7desta loja.'
        - ''
        - '&aClique em um item do seu inventário'
    provider:
      material: '61a8e6d27b96c0aa4df5b8347260eb051c56944c97d837f22655d8ecbc449137'
      name: '&aMoeda da loja'
      lore:
        - '&7Moeda que será utilizada no comércio'
        - '&7desta loja.'
        - ''
        - '&7Atual: &fNenhuma'
        - ''
        - '&aClique para alterar a moeda'
    name:
      material: 'NAME_TAG:0'
      name: '&aNome do item'
      lore:
        - '&7Nome do item que será comercializado'
        - '&7nesta loja.'
        - ''
        - '&7Atual: &f{item_name}'
        - ''
        - '&aClique para alterar o nome'
    amount:
      material: 'e146b765fca7d406de0079fe6a762fe439a418129d2395b5c6c5044be71c13d1'
      name: '&aQuantia do item'
      lore:
        - '&7Quantia do item que será comercializado'
        - '&7nesta loja.'
        - ''
        - '&7Atual: &f{amount}'
        - ''
        - '&aClique para alterar a quantia'
    type-buy:
      material: '7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      name: '&aTipo da loja'
      lore:
        - '&7Tipo da sua loja:'
        - ''
        - ' &f• &aComprar item &8(Jogadores vendem a você)'
        - ' &f• &7Vender item &8(Jogadores compram de você)'
        - ' &f• &7Comprar e vender item'
        - ''
        - '&aClique para alterar'
    type-sell:
      material: '7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      name: '&aTipo da loja'
      lore:
        - '&7Tipo da sua loja:'
        - ''
        - ' &f• &7Comprar item &8(Jogadores vendem a você)'
        - ' &f• &aVender item &8(Jogadores compram de você)'
        - ' &f• &7Comprar e vender item'
        - ''
        - '&aClique para alterar'
    type-buy-sell:
      material: '7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
      name: '&aTipo da loja'
      lore:
        - '&7Tipo da sua loja:'
        - ''
        - ' &f• &7Comprar item &8(Jogadores vendem a você)'
        - ' &f• &7Vender item &8(Jogadores compram de você)'
        - ' &f• &aComprar e vender item'
        - ''
        - '&aClique para alterar'
    price-buy:
      material: '945f47feb4d75cb333914bfdb999a489c9d0e320d548f310419ad738d1e24b9'
      name: '&aPreço do item'
      lore:
        - '&7Quantia que você vai oferecer por este item:'
        - ''
        - ' &fPreço atual: &7{price_buy}'
        - ''
        - '&aClique para alterar'
    price-sell:
      material: '945f47feb4d75cb333914bfdb999a489c9d0e320d548f310419ad738d1e24b9'
      name: '&aPreço do item'
      lore:
        - '&7Quantia que você vai ganhar por este item:'
        - ''
        - ' &fPreço atual: &7{price_sell}'
        - ''
        - '&aClique para alterar'
    price-buy-sell:
      material: '945f47feb4d75cb333914bfdb999a489c9d0e320d548f310419ad738d1e24b9'
      name: '&aPreço do item'
      lore:
        - '&7Quantia que o item será comercializado:'
        - ''
        - ' &fPreço de venda atual: &7{price_sell} &8(Você recebe pela venda do item)'
        - ' &fPreço de compra atual: &7{price_buy} &8(Você paga para comprar o item)'
        - ''
        - '&aBotão &fESQUERDO&a para alterar o preço de venda.'
        - '&aBotão &fDIREITO&a para alterar o preço de compra.'
    open:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aAbrir loja'
      lore:
        - '&7Esta loja está fechada no momento.'
        - '&7Jogadores não poderão comprar nem vender.'
        - ''
        - '&aClique para abrir a loja'
    close:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cFechar loja'
      lore:
        - '&7Esta loja está aberta no momento.'
        - '&7Jogadores poderão comprar e vender.'
        - ''
        - '&aClique para fechar a loja'
    hologram-enable:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aHabilitar holograma'
      lore:
        - '&7Esta loja está com o holograma'
        - '&7desabilitado no momento.'
        - ''
        - '&aClique para habilitar'
    hologram-disable:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cDesabilitar holograma'
      lore:
        - '&7Esta loja está com o holograma'
        - '&7habilitado no momento.'
        - ''
        - '&aClique para desabilitar'
    warns-enable:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aHabilitar avisos'
      lore:
        - '&7Esta loja está com os avisos'
        - '&7desabilitados no momento.'
        - ''
        - '&aClique para habilitar'
    warns-disable:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&cDesabilitar avisos'
      lore:
        - '&7Esta loja está com os avisos'
        - '&7habilitados no momento.'
        - ''
        - '&aClique para desabilitar'

# Menu de seleção de economias
providers:
  name: '&8Selecionar economia'
  size: 27
  previous: 9
  next: 17
  back: 18
  slots: [ 10, 11, 12, 13, 14, 15, 16 ]

# Menu de preview de uma placa admin
preview-admin:
  name: '&8Loja do servidor'
  size: 27
  items:
    provider-slot: 11
    display-slot: 13

# Menu de preview de uma placa de um jogador
preview-player:
  name: '&8Loja de &a{player}'
  size: 27
  items:
    provider-slot: 11
    display-slot: 13
    owner-slot: 15
    owner:
      material: '{player}'
      name: '&aDono do comércio'
      lore:
        - ''
        - '&7Esta loja pertence ao jogador &f{player}&7.'
        - ''

# Menu de compra
buy:
  name: '&8Loja {player}'
  size: 27
  items:
    provider-slot: 11
    display-slot: 13
    confirm-slot: 15
    amount-slot: 16
    confirm:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aComprar'
      lore:
        - '&7Comprar o item à venda'
        - ''
        - ' &7Preço: &f{price} {provider_abbreviated}&7 a cada &f{amount}'
        - ' &7Preço: &f{price_unity} {provider_abbreviated}&7 a cada &f1 unidade'
        - ' &7Preço: &f{price_inv} {provider_abbreviated}&7 a cada &f1 inventário &7(2304)'
        - ''
        - ' &7Estoque atual: &f{stock}'
        - ''
        - '&aBotão &fESQUERDO&a para comprar &f{amount}'
    amount:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&aQuantia'
      lore:
        - '&7Configure a quantia que gostaria'
        - '&7de comercializar nessa loja.'
        - ''
        - ' &fAtual: &b{amount}'
        - ''
        - '&aClique para alterar'

# Menu de venda
sell:
  name: '&8Loja {player}'
  size: 27
  items:
    provider-slot: 11
    display-slot: 13
    confirm-slot: 15
    amount-slot: 16
    confirm:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aVender'
      lore:
        - '&7Vender seus itens à loja'
        - ''
        - ' &7Preço: &f{price} {provider_abbreviated}&7 a cada &f{amount}'
        - ' &7Preço: &f{price_unity} {provider_abbreviated}&7 a cada &f1 unidade'
        - ' &7Preço: &f{price_inv} {provider_abbreviated}&7 a cada &f1 inventário &7(2304)'
        - ''
        - '&aBotão &fESQUERDO&a para vender &f{amount}'
    amount:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&aQuantia'
      lore:
        - '&7Configure a quantia que gostaria'
        - '&7de comercializar nessa loja.'
        - ''
        - ' &fAtual: &b{amount}'
        - ''
        - '&aClique para alterar'

# Menu de compra e venda
buy-sell:
  name: '&8Loja {player}'
  size: 27
  items:
    provider-slot: 10
    display-slot: 12
    buy-slot: 14
    sell-slot: 15
    amount-slot: 17
    buy:
      material: '22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      name: '&aComprar'
      lore:
        - '&7Comprar o item à venda'
        - ''
        - ' &7Preço: &f{price} {provider_abbreviated}&7 a cada &f{amount}'
        - ' &7Preço: &f{price_unity} {provider_abbreviated}&7 a cada &f1 unidade'
        - ' &7Preço: &f{price_inv} {provider_abbreviated}&7 a cada &f1 inventário &7(2304)'
        - ''
        - ' &7Estoque atual: &f{stock}'
        - ''
        - '&aBotão &fESQUERDO&a para comprar &f{amount}'
    sell:
      material: 'c532576b8bc9a876419a39ae4498c456fe9ee5bdc7ba91fd3b2f1b0a7eb91'
      name: '&aVender'
      lore:
        - '&7Vender seus itens à loja'
        - ''
        - ' &7Preço: &f{price} {provider_abbreviated}&7 a cada &f{amount}'
        - ' &7Preço: &f{price_unity} {provider_abbreviated}&7 a cada &f1 unidade'
        - ' &7Preço: &f{price_inv} {provider_abbreviated}&7 a cada &f1 inventário &7(2304)'
        - ''
        - '&aBotão &fESQUERDO&a para vender &f{amount}'
    amount:
      material: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      name: '&aQuantia'
      lore:
        - '&7Configure a quantia que gostaria'
        - '&7de comercializar nessa loja.'
        - ''
        - ' &fAtual: &b{amount}'
        - ''
        - '&aClique para alterar'
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

actionbar:
  owner-stock: '&cSua loja de &7{item}&c está sem estoque.'
  owner-space: '&cSua loja de &7{item}&c está sem espaço.'
  owner-buy: '&aO jogador &f{player}&a comprou &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na sua loja.'
  owner-sell: '&aO jogador &f{player}&a vendeu &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na sua loja.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  chest: '&cVocê precisa definir a placa em um baú.'
  permission-create-admin: '&cVocê não tem permissão para criar este tipo de loja.'
  permission-create: '&cVocê não tem permissão para criar lojas.'
  price-low: '&cO preço deve ser maior ou igual a 0.'
  price-buy-changed: '&aVocê alterou o preço que você quer receber pelo item para &f{price}&a.'
  price-sell-changed: '&aVocê alterou o preço que você quer pagar pelo item para &f{price}&a.'
  amount-changed: '&aVocê alterou a quantia que quer comercializar do item para &f{amount}&a.'
  name-changed: '&aVocê alterou o nome que quer comercializar do item para &f{name}&a.'
  price-buy-digit: |
    <nl>
    &aDigite o preço que você quer pagar pelo item.
    &7para cancelar digite &ncancelar&7.
    <nl>
  price-sell-digit: |
    <nl>
    &aDigite o preço que você quer receber pelo item.
    &7para cancelar digite &ncancelar&7.
    <nl>
  amount-digit: |
    <nl>
    &aDigite a quantia que você quer comercializar do item.
    &7para cancelar digite &ncancelar&7.
    <nl>
  name-digit: |
    <nl>
    &aDigite o nome que você quer por no item do comércio.
    &7para cancelar digite &ncancelar&7.
    <nl>
  amount-buy-digit: |
    <nl>
    &aDigite a quantia que você quer comprar do item.
    &7para cancelar digite &ncancelar&7.
    <nl>
  amount-sell-digit: |
    <nl>
    &aDigite a quantia que você quer vender do item.
    &7para cancelar digite &ncancelar&7.
    <nl>
  provider-permission: '&cVocê não tem permissão para comercializar com esta economia.'
  not-configured: '&cEssa loja ainda não foi totalmente configurada.'
  provider-not-configured: '&cA economia provedora desta loja está desconfigurada.'
  stock: '&cEsta loja está sem estoque.'
  player-stock: '&cVocê não possui este item para vender.'
  space: '&cEsta loja está sem espaço no baú.'
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  no-balance-owner: '&cO jogador {player} não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  buy-admin: '&aVocê comprou com sucesso &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na loja do servidor. &7Desconto: {discount}%'
  buy-player: '&aVocê comprou com sucesso &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na loja de &f{player}&a.'
  sell-admin: '&aVocê vendeu com sucesso &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na loja do servidor. &7Bônus: {bonus}%'
  sell-player: '&aVocê vendeu com sucesso &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na loja de &f{player}&a.'
  owner-offline: '&cEsta loja possui uma economia que não permite que o dono esteja offline e o dono desta loja está offline.'
  amount-low: '&cA quantia deve ser maior ou igual a 1.'
  inv-full: '&cSeu inventário está cheio.'
  closed: '&cEsta loja está fechada no momento.'
  owner-stock: '&cSua loja de &7{item}&c está sem estoque.'
  owner-space: '&cSua loja de &7{item}&c está sem espaço.'
  owner-buy: '&aO jogador &f{player}&a comprou &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na sua loja.'
  owner-sell: '&aO jogador &f{player}&a vendeu &f{amount}x {item}&a por &f{price} {provider_display_abbreviated}&a na sua loja.'
  set-owner-admin: '&cVocê não pode mudar o dono da placa ADMIN.'
  set-owner-found: '&cNenhum shop encontrado.'
  set-owner: '&aVocê mudou o dono da placa para &f{player}&a.'
]]>
</code-block>
</chapter>

<chapter title="plugin.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: yChestShop
version: '${project.version}'
main: com.ystoreplugins.ychestshop.Main
authors: [ yChusy ]
website: https://ystoreplugins.com.br
api-version: 1.13
depend: [ Vault ]
softdepend: [ HolographicDisplays, DecentHolograms, Multiverse-Core, MultiverseCore, My_Worlds ]
load: POSTWORLD
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/91-yChestShop">Site do plugin yChestShop</a>
    </category>
</seealso>