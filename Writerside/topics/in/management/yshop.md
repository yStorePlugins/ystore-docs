# yShop
<secondary-label ref="management"/>

### Descrição
Venda itens e comandos por categorias e ações.

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
<video src="//www.youtube.com/watch?v=Ram2Shkpca0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/yshop setnpc - Setar o NPC
/yshop delnpc - Deletar o NPC
/yshop reload - Recarregar as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yshopv2.admin - Permissão para o /yshop</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yShop/
    ├── categorias/
    │    └── padrao.yml
    ├── menus/
    │    ├── confirmacao.yml
    │    └── confirmacao_venda.yml
    ├── bonus.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── descontos.yml
    ├── economies.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="categorias" collapsible="true">
<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Comandos: [ 'shop' ] #comandos para abrir (deixe [] para não usar)

Permissao: '' #permissao para abrir

# false = abre o shop se o comando começar com /shop -> exemplo: /shop aa
# true = só abre o shop se o comando for igual a /shop
ComandoIgual: false

Tamanho: 27 #tamanho do inventário

Nome: '&7Loja padrão' #nome do inventário

# Som ao abrir a loja
Som: ''

# Ativar a compra de uma quantia customizada via chat
# Só afeta esta categoria
Quantia chat: true

# Ativar a confirmação da compra no menu
Confirmacao: true
#
Itens:
   Item1:
      # Sistema de permissão para comercializar
      Permissao:
         Permissao: ''
         Mensagem: '&cVocê não tem permissão para comprar este item.'
      # necessário para verificar a quantia disponível no inv
      InvStackVerify: 64
      Slot: 10
      Display:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos' ]
      # Caso não queira usar, apague
      Display-Perm:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos', '', '&cVocê não tem permissão.' ]
      # Ação com botão esquerdo
      Acao:
      - '[abrir]blocos.yml'
      # Ação com botão direito
      Acao direito:
      - '[nenhuma]'
      ## Ações: [comprar], [cmd], [cmd_console], [abrir], [nenhuma]
      Comprar:
         # Permitir que os usuários comprem com desconto
         # Padrão: true, mesmo se não estiver definido na config
         # se quiser false, defina aqui.
         Permitir desconto: true
         Usar itens: true
         Usar comandos: true
         # Ao ativar, cada comando será 1 slot
         # Ele poderá comprar só a quantia de slots disponíveis.
         Contabilizar comandos: true
         # Se essa opção estiver true, ele irá executar o comando pela quantidade que o player escolheu na hora na compra, se estiver false, irá adicionar a placeholder {quantia} no comando.
         Repetir comandos: true
         # Executar os comandos após um delay
         # em ticks -> 20t = 1s
         Comandos delay: 0
         Comandos:
         - 'alerta {player} é bonito'
         # Mensagens customizadas ao comprar
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
   #
   Item2:
      Slot: 11
      InvStackVerify: 64
      Display:
         material: IRON_INGOT
         name: '&fAlerta de beleza'
         lore:
            - '&7Seu desconto: {desconto}&7.'
            - '&7Seu bônus: {bonus}&7.'
      # Sistema de comprar apenas 1x
      Onetime:
         Ativar: false
         Display:
            material: IRON_INGOT
            name: '&fAlerta de beleza'
            lore: [ '&cEste item já foi adquirido.' ]
      Custos:
         Custo1:
            Display: 'money'
            Tipo: 'money'
            Custo: 1000.0
         Custo2:
            Display: 'Pontos'
            Tipo: 'playerpoints'
            Custo: 10.0
      Custos fragmentos:
         - 'Fragmento1:32'
         - 'Fragmento2:10'
      Acao: '[comprar]'
      Comprar:
         Usar itens: false
         Usar comandos: true
         Contabilizar Comandos: true
         Comandos: ['alerta {player} é bonito']
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
      Vender:
         Quantia: 1
         Depositos:
            Deposito1:
               Tipo: 'money'
               Deposito: 100.0
         Item:
            material: STONE
            amount: 1
            name: '&cPedra preciosa'
            glow: true
            lore: [ '&aVocê é um mago' ]
   #

]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmacao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de compra'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser comprada: &a{quantia}&7.'
      - '&7Seu desconto: {desconto}&7.'
      - '&7Valor total: &c{playerpoints} pontos e {money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a compra.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a compra.'

]]>
</code-block>
</chapter>

<chapter title="confirmacao_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de venda'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser vendida: &a{quantia}&7.'
      - '&7Seu bônus: {bonus}&7.'
      - '&7Valor total: &c{playerpoints} pontos e {money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a venda.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a venda.'

]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bonus:
   VIP:
      Permissao: 'yshopv2.vip'
      Bonus: 10.0
      Ordem: 1
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
  yshop: 'yshop'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____  _
#  _   _/ ___|| |__   ___  _ __
# | | | \___ \| '_ \ / _ \| '_ \
# | |_| |___) | | | | (_) | |_) |
#  \__, |____/|_| |_|\___/| .__/
#  |___/                  |_|
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

# Opções gerais
general:
  # Maximo de itens por compra
  max-buy: 64
  # Fechar o menu depois de confirmar
  close-confirm: false
  # Delay entre operações de compra e venda
  # em segundos
  delay: 3
  # Formato do desconto nas mensagens
  format-discount: ' &7( {desconto}% )'
  # Formato do bônus nas mensagens
  format-bonus: ' &7( {bonus}% )'

# Opcoes de configuração do NPC
npc:
  # Skin do NPC
  skin: 'TheThunderGod063'
  # Categoria que irá abrir ao clicar no NPC
  category: 'padrao.yml'
  # Configurações do holograma
  hologram:
    # Altura em relação ao NPC
    offset: 3.1
    # Linhas do holograma
    lines:
      - '&6Shop'
      - '&7Veja os itens à venda.'

# Sistema de bonus
# Será adicionado no próximo update. PORTANTO, DEIXE CONFIGURADO
bonus:
  VIP:
    # Ordem de reconhecimento da permissão
    order: 1
    # Permissão para ser reconhecido
    permission: 'yshop.vip'
    # Porcentagem do bônus
    bonus: 10.0

# Sistema de descontos
# Será adicionado no próximo update. PORTANTO, DEIXE CONFIGURADO
discount:
  VIP:
    # Ordem de reconhecimento da permissão
    order: 1
    # Permissão para ser reconhecido
    permission: 'yshop.vip'
    # Porcentagem do desconto
    discount: 10.0
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Npc local: 'none'

Data: {}
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Permissao: 'yshopv2.vip'
      Desconto: 10.0
      Ordem: 1
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
    # Símbolo para por nas mensagens
    symbol: '$'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yshop.provider.money'
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

    &a/yshop setnpc &8- &7Seta o NPC.
    &a/yshop delnpc &8- &7Deleta o NPC.
    &a/yshop reload &8- &7Recarrega as configurações.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  no-balance: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  action-found: '&cA ação não foi encontrada.'
  category-found: '&cA categoria não foi encontrada.'
  buy-max: '&cDesculpe, o valor máximo por compra é de 64.'
  inv-full: '&cSeu inventário não tem espaço suficiente.'
  bought: '&aVocê adquiriu produtos no shop.'
  fragment-has: '&cVocê não possui fragmentos suficientes.'
  sold: '&aVocê vendeu produtos no shop.' #deixe '' para não usar
  sell-has: '&aVocê não tem {amount} itens para vender.'
  delay: '&c&lERRO! &cAguarde &e{time} &cpara comercializar na loja novamente.'
  digit: |
    &r
    &aDigite a quantia que deseja comprar do item {item}&a.
    &r
    &7Preços:
    &7> &fMoney: &a{money}&7.
    &7> &fPoints: &a{playerpoints}&7.
    &r
    &7Seu desconto:{desconto}&7.
    &r
    &7para cancelar digite &ncancelar&7.
    &r
  digit-sell: |
    &r
    &aDigite a quantia que deseja vender do item {item}&a.
    &r
    &7Valor de cada:
    &7> &fMoney: &a{money}&7.
    &7> &fPoints: &a{playerpoints}&7.
    &r
    &7Seu bonus:{bonus}&7.
    &r
    &7para cancelar digite &ncancelar&7.
    &r
  npc-set: '&aNPC do shop setado com sucesso.'
  npc-removed: '&aNPC do shop removido com sucesso'
  npc-found: '&cO NPC não está setado.'
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yShop/
    ├── categorias/
    │    └── padrao.yml
    ├── menus/
    │    ├── confirmacao.yml
    │    └── confirmacao_venda.yml
    ├── bonus.yml
    ├── commands.yml
    ├── config.yml
    ├── data.yml
    ├── descontos.yml
    ├── economies.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="categorias" collapsible="true">
<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Comandos: [ 'shop' ] #comandos para abrir (deixe [] para não usar)

Permissao: '' #permissao para abrir

# false = abre o shop se o comando começar com /shop -> exemplo: /shop aa
# true = só abre o shop se o comando for igual a /shop
ComandoIgual: false

Tamanho: 27 #tamanho do inventário

Nome: '&7Loja padrão' #nome do inventário

# Som ao abrir a loja
Som: ''

# Ativar a compra de uma quantia customizada via chat
# Só afeta esta categoria
Quantia chat: true

# Ativar a confirmação da compra no menu
Confirmacao: true
#
Itens:
   Item1:
      # Sistema de permissão para comercializar
      Permissao:
         Permissao: ''
         Mensagem: '&cVocê não tem permissão para comprar este item.'
      # necessário para verificar a quantia disponível no inv
      InvStackVerify: 64
      Slot: 10
      Display:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos' ]
      # Caso não queira usar, apague
      Display-Perm:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos', '', '&cVocê não tem permissão.' ]
      # Ação com botão esquerdo
      Acao:
      - '[abrir]blocos.yml'
      # Ação com botão direito
      Acao direito:
      - '[nenhuma]'
      ## Ações: [comprar], [cmd], [cmd_console], [abrir], [nenhuma]
      Comprar:
         # Permitir que os usuários comprem com desconto
         # Padrão: true, mesmo se não estiver definido na config
         # se quiser false, defina aqui.
         Permitir desconto: true
         Usar itens: true
         Usar comandos: true
         # Ao ativar, cada comando será 1 slot
         # Ele poderá comprar só a quantia de slots disponíveis.
         Contabilizar comandos: true
         # Se essa opção estiver true, ele irá executar o comando pela quantidade que o player escolheu na hora na compra, se estiver false, irá adicionar a placeholder {quantia} no comando.
         Repetir comandos: true
         # Executar os comandos após um delay
         # em ticks -> 20t = 1s
         Comandos delay: 0
         Comandos:
         - 'alerta {player} é bonito'
         # Mensagens customizadas ao comprar
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
   #
   Item2:
      Slot: 11
      InvStackVerify: 64
      Display:
         material: IRON_INGOT
         name: '&fAlerta de beleza'
         lore:
            - '&7Seu desconto: {desconto}&7.'
            - '&7Seu bônus: {bonus}&7.'
      # Sistema de comprar apenas 1x
      Onetime:
         Ativar: false
         Display:
            material: IRON_INGOT
            name: '&fAlerta de beleza'
            lore: [ '&cEste item já foi adquirido.' ]
      Custos:
         Custo1:
            Display: 'Money'
            Tipo: 'Money'
            Custo: 1000.0
         Custo2:
            Display: 'Pontos'
            Tipo: 'PlayerPoints'
            Custo: 10.0
      Custos fragmentos:
         - 'Fragmento1:32'
         - 'Fragmento2:10'
      Acao: '[comprar]'
      Comprar:
         Usar itens: false
         Usar comandos: true
         Contabilizar Comandos: true
         Comandos: ['alerta {player} é bonito']
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
      Vender:
         Quantia: 1
         Depositos:
            Deposito1:
               Tipo: 'Money'
               Deposito: 100.0
         Item:
            material: STONE
            amount: 1
            name: '&cPedra preciosa'
            glow: true
            lore: [ '&aVocê é um mago' ]
   #

]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmacao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de compra'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser comprada: &a{quantia}&7.'
      - '&7Seu desconto: {desconto}&7.'
      - '&7Valor total: &c{PlayerPoints} pontos e {Money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a compra.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a compra.'

]]>
</code-block>
</chapter>

<chapter title="confirmacao_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de venda'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser vendida: &a{quantia}&7.'
      - '&7Seu bônus: {bonus}&7.'
      - '&7Valor total: &c{PlayerPoints} pontos e {Money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a venda.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a venda.'

]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bonus:
   VIP:
      Permissao: 'yshopv2.vip'
      Bonus: 10.0
      Ordem: 1
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
  yshop: 'yshop'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____  _
#  _   _/ ___|| |__   ___  _ __
# | | | \___ \| '_ \ / _ \| '_ \
# | |_| |___) | | | | (_) | |_) |
#  \__, |____/|_| |_|\___/| .__/
#  |___/                  |_|
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

# Opções gerais
general:
  # Maximo de itens por compra
  max-buy: 64
  # Fechar o menu depois de confirmar
  close-confirm: false
  # Delay entre operações de compra e venda
  # em segundos
  delay: 3
  # Formato do desconto nas mensagens
  format-discount: ' &7( {desconto}% )'
  # Formato do bônus nas mensagens
  format-bonus: ' &7( {bonus}% )'

# Opcoes de configuração do NPC
npc:
  # Skin do NPC
  skin: 'TheThunderGod063'
  # Categoria que irá abrir ao clicar no NPC
  category: 'padrao.yml'
  # Configurações do holograma
  hologram:
    # Altura em relação ao NPC
    offset: 3.1
    # Linhas do holograma
    lines:
      - '&6Shop'
      - '&7Veja os itens à venda.'

# Sistema de bonus
# Será adicionado no próximo update. PORTANTO, DEIXE CONFIGURADO
bonus:
  VIP:
    # Ordem de reconhecimento da permissão
    order: 1
    # Permissão para ser reconhecido
    permission: 'yshop.vip'
    # Porcentagem do bônus
    bonus: 10.0

# Sistema de descontos
# Será adicionado no próximo update. PORTANTO, DEIXE CONFIGURADO
discount:
  VIP:
    # Ordem de reconhecimento da permissão
    order: 1
    # Permissão para ser reconhecido
    permission: 'yshop.vip'
    # Porcentagem do desconto
    discount: 10.0
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Npc local: 'none'

Data: {}
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Permissao: 'yshopv2.vip'
      Desconto: 10.0
      Ordem: 1
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
    permission: 'yshop.provider.money'
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

    &a/yshop setnpc &8- &7Seta o NPC.
    &a/yshop delnpc &8- &7Deleta o NPC.
    &a/yshop reload &8- &7Recarrega as configurações.

  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  no-balance: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  action-found: '&cA ação não foi encontrada.'
  category-found: '&cA categoria não foi encontrada.'
  buy-max: '&cDesculpe, o valor máximo por compra é de 64.'
  inv-full: '&cSeu inventário não tem espaço suficiente.'
  bought: '&aVocê adquiriu produtos no shop.'
  fragment-has: '&cVocê não possui fragmentos suficientes.'
  sold: '&aVocê vendeu produtos no shop.' #deixe '' para não usar
  sell-has: '&aVocê não tem {amount} itens para vender.'
  delay: '&c&lERRO! &cAguarde &e{time} &cpara comercializar na loja novamente.'
  digit: |
    &r
    &aDigite a quantia que deseja comprar do item {item}&a.
    &r
    &7Preços:
    &7> &fMoney: &a{Money}&7.
    &7> &fPoints: &a{PlayerPoints}&7.
    &r
    &7Seu desconto:{desconto}&7.
    &r
    &7para cancelar digite &ncancelar&7.
    &r
  digit-sell: |
    &r
    &aDigite a quantia que deseja vender do item {item}&a.
    &r
    &7Valor de cada:
    &7> &fMoney: &a{Money}&7.
    &7> &fPoints: &a{PlayerPoints}&7.
    &r
    &7Seu bonus:{bonus}&7.
    &r
    &7para cancelar digite &ncancelar&7.
    &r
  npc-set: '&aNPC do shop setado com sucesso.'
  npc-removed: '&aNPC do shop removido com sucesso'
  npc-found: '&cO NPC não está setado.'
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yShop/
    ├── categorias/
    │    └── padrao.yml
    ├── menus/
    │    ├── confirmacao.yml
    │    └── confirmacao_venda.yml
    ├── bonus.yml
    ├── config.yml
    ├── data.yml
    ├── descontos.yml
    └── economies.yml
</code-block>
</chapter>

<chapter title="categorias" collapsible="true">
<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Comandos: [ 'shop' ] #comandos para abrir (deixe [] para não usar)

Permissao: '' #permissao para abrir

# false = abre o shop se o comando começar com /shop -> exemplo: /shop aa
# true = só abre o shop se o comando for igual a /shop
ComandoIgual: false

Tamanho: 27 #tamanho do inventário

Nome: '&7Loja padrão' #nome do inventário

# Som ao abrir a loja
Som: ''

# Ativar a compra de uma quantia customizada via chat
# Só afeta esta categoria
Quantia chat: true

# Ativar a confirmação da compra no menu
Confirmacao: true
#
Itens:
   Item1:
      # Sistema de permissão para comercializar
      Permissao:
         Permissao: ''
         Mensagem: '&cVocê não tem permissão para comprar este item.'
      # necessário para verificar a quantia disponível no inv
      InvStackVerify: 64
      Slot: 10
      Display:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos' ]
      # Caso não queira usar, apague
      Display-Perm:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos', '', '&cVocê não tem permissão.' ]
      # Ação com botão esquerdo
      Acao:
      - '[abrir]blocos.yml'
      # Ação com botão direito
      Acao direito:
      - '[nenhuma]'
      ## Ações: [comprar], [cmd], [cmd_console], [abrir], [nenhuma]
      Comprar:
         # Permitir que os usuários comprem com desconto
         # Padrão: true, mesmo se não estiver definido na config
         # se quiser false, defina aqui.
         Permitir desconto: true
         Usar itens: true
         Usar comandos: true
         # Ao ativar, cada comando será 1 slot
         # Ele poderá comprar só a quantia de slots disponíveis.
         Contabilizar comandos: true
         # Se essa opção estiver true, ele irá executar o comando pela quantidade que o player escolheu na hora na compra, se estiver false, irá adicionar a placeholder {quantia} no comando.
         Repetir comandos: true
         # Executar os comandos após um delay
         # em ticks -> 20t = 1s
         Comandos delay: 0
         Comandos:
         - 'alerta {player} é bonito'
         # Mensagens customizadas ao comprar
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
   #
   Item2:
      Slot: 11
      InvStackVerify: 64
      Display:
         material: IRON_INGOT
         name: '&fAlerta de beleza'
         lore:
            - '&7Seu desconto: {desconto}&7.'
            - '&7Seu bônus: {bonus}&7.'
      Custos:
         Custo1:
            Display: 'Money'
            Tipo: 'Money'
            Custo: 1000.0
         Custo2:
            Display: 'Pontos'
            Tipo: 'PlayerPoints'
            Custo: 10.0
      Custos fragmentos:
         - 'Fragmento1:32'
         - 'Fragmento2:10'
      Acao: '[comprar]'
      Comprar:
         Usar itens: false
         Usar comandos: true
         Contabilizar Comandos: true
         Comandos: ['alerta {player} é bonito']
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
      Vender:
         Quantia: 1
         Depositos:
            Deposito1:
               Tipo: 'Money'
               Deposito: 100.0
         Item:
            material: STONE
            amount: 1
            name: '&cPedra preciosa'
            glow: true
            lore: [ '&aVocê é um mago' ]
   #

]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmacao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de compra'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser comprada: &a{quantia}&7.'
      - '&7Seu desconto: {desconto}&7.'
      - '&7Valor total: &c{PlayerPoints} pontos e {Money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a compra.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a compra.'

]]>
</code-block>
</chapter>

<chapter title="confirmacao_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de venda'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser vendida: &a{quantia}&7.'
      - '&7Seu bônus: {bonus}&7.'
      - '&7Valor total: &c{PlayerPoints} pontos e {Money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a venda.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a venda.'

]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bonus:
   VIP:
      Permissao: 'yshopv2.vip'
      Bonus: 10.0
      Ordem: 1
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Comando: 'yshop'
  Aliases: []

# Opcoes de configuração do NPC
NPC:
  ID: 9232744
  Skin: 'TheThunderGod063'
  Categoria: 'padrao.yml'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Shop'
      - '&7Veja os itens à venda.'

# Maximo de itens por compra
Maximo por compra: 64

# Fechar o menu depois de confirmar
Fechar confirmar: false

# Delay entre operações de compra e venda
# em segundos
Delay: 3

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Cancelou: '&cVocê cancelou a compra.'
  Nao e numero: '&cO argumento não é um número.'
  Acao inexistente: '&cA ação não foi encontrada.'
  Categoria inexistente: '&cA categoria não foi encontrada.'
  Nao tem pontos: '&cDesculpe, mas você não possui a quantia necessária de pontos, &7{quantia} pontos&c.'
  Nao tem money: '&cDesculpe, mas você não possui a quantia necessária de money, &7{quantia} money&c.'
  Maximo: '&cDesculpe, o valor máximo por compra é de 64.'
  Inv cheio: '&cSeu inventário não tem espaço suficiente.'
  Comprou: '&aVocê adquiriu produtos no shop.' #deixe '' para não usar
  Nao possui: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  Desabilitado: '&cEste plugin &f{plugin}&c não está ligado.'
  Setado: '&aNPC da pesca setado com sucesso.'
  Removido: '&aNPC da pesca removido com sucesso'
  Nao setado: '&cO NPC não está setado.'
  Fragmento suficiente: '&cVocê não possui fragmentos suficientes.'
  Vendeu: '&aVocê vendeu produtos no shop.' #deixe '' para não usar
  Vendeu suficiente: '&aVocê não tem {amount} itens para vender.'
  Delay: '&c&lERRO! &cAguarde &e{time} &cpara comercializar na loja novamente.'
  Digite:
    - ''
    - '&aDigite a quantia que deseja comprar do item {item}&a.'
    - ''
    - '&7Preços:'
    - '&7> &fMoney: &a{Money}&7.'
    - '&7> &fPoints: &a{PlayerPoints}&7.'
    - ''
    - '&7Seu desconto:{desconto}&7.'
    - ''
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite venda:
    - ''
    - '&aDigite a quantia que deseja vender do item {item}&a.'
    - ''
    - '&7Valor de cada:'
    - '&7> &fMoney: &a{Money}&7.'
    - '&7> &fPoints: &a{PlayerPoints}&7.'
    - ''
    - '&7Seu bonus:{bonus}&7.'
    - ''
    - '&7para cancelar digite &ncancelar&7.'
    - ''

# Formatador de mensagens
Formatador:
  Money: '&aMoney'
  Points: '&6Cash'
  Desconto: ' &7( {desconto}% )'
  Bonus: ' &7( {bonus}% )'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Npc local: 'none'

Data: {}
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Permissao: 'yshopv2.vip'
      Desconto: 10.0
      Ordem: 1
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
    permission: 'yshop.provider.money'
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yShop/
    ├── categorias/
    │    └── padrao.yml
    ├── menus/
    │    ├── confirmacao.yml
    │    └── confirmacao_venda.yml
    ├── bonus.yml
    ├── config.yml
    ├── descontos.yml
    └── economies.yml
</code-block>
</chapter>

<chapter title="categorias" collapsible="true">
<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Comandos: [ 'shop' ] #comandos para abrir (deixe [] para não usar)

Permissao: '' #permissao para abrir

# false = abre o shop se o comando começar com /shop -> exemplo: /shop aa
# true = só abre o shop se o comando for igual a /shop
ComandoIgual: false

Tamanho: 27 #tamanho do inventário

Nome: '&7Loja padrão' #nome do inventário

# Som ao abrir a loja
Som: ''

# Ativar a compra de uma quantia customizada via chat
# Só afeta esta categoria
Quantia chat: true

# Ativar a confirmação da compra no menu
Confirmacao: true
#
Itens:
   Item1:
      # Sistema de permissão para comercializar
      Permissao:
         Permissao: ''
         Mensagem: '&cVocê não tem permissão para comprar este item.'
      # necessário para verificar a quantia disponível no inv
      InvStackVerify: 64
      Slot: 10
      Display:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos' ]
      # Caso não queira usar, apague
      Display-Perm:
         material: BRICK
         name: '&cCategoria de blocos'
         lore: [ '&7Clique para comprar blocos', '', '&cVocê não tem permissão.' ]
      # Ação com botão esquerdo
      Acao:
      - '[abrir]blocos.yml'
      # Ação com botão direito
      Acao direito:
      - '[nenhuma]'
      ## Ações: [comprar], [cmd], [cmd_console], [abrir], [nenhuma]
      Comprar:
         # Permitir que os usuários comprem com desconto
         # Padrão: true, mesmo se não estiver definido na config
         # se quiser false, defina aqui.
         Permitir desconto: true
         Usar itens: true
         Usar comandos: true
         # Ao ativar, cada comando será 1 slot
         # Ele poderá comprar só a quantia de slots disponíveis.
         Contabilizar comandos: true
         # Se essa opção estiver true, ele irá executar o comando pela quantidade que o player escolheu na hora na compra, se estiver false, irá adicionar a placeholder {quantia} no comando.
         Repetir comandos: true
         Comandos:
         - 'alerta {player} é bonito'
         # Mensagens customizadas ao comprar
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
   #
   Item2:
      Slot: 11
      InvStackVerify: 64
      Display:
         material: IRON_INGOT
         name: '&fAlerta de beleza'
         lore:
            - '&7Seu desconto: {desconto}&7.'
            - '&7Seu bônus: {bonus}&7.'
      Custos:
         Custo1:
            Display: 'Money'
            Tipo: 'Money'
            Custo: 1000.0
         Custo2:
            Display: 'Pontos'
            Tipo: 'PlayerPoints'
            Custo: 10.0
      Custos fragmentos:
         - 'Fragmento1:32'
         - 'Fragmento2:10'
      Acao: '[comprar]'
      Comprar:
         Usar itens: false
         Usar comandos: true
         Contabilizar Comandos: true
         Comandos: ['alerta {player} é bonito']
         Messages:
            Chat: '&aObrigado &f{player}&a por comprar!'
            Actionbar: '&aObrigado &f{player}&a por comprar!'
            Title: ''
         Itens:
            Pedra preciosa:
               material: STONE
               amount: 64
               name: '&cPedra preciosa'
               glow: true
               lore: [ '&aVocê é um mago' ]
      Vender:
         Quantia: 1
         Depositos:
            Deposito1:
               Tipo: 'Money'
               Deposito: 100.0
         Item:
            material: STONE
            amount: 1
            name: '&cPedra preciosa'
            glow: true
            lore: [ '&aVocê é um mago' ]
   #

]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="confirmacao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de compra'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser comprada: &a{quantia}&7.'
      - '&7Seu desconto: {desconto}&7.'
      - '&7Valor total: &c{PlayerPoints} pontos e {Money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a compra.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a compra.'

]]>
</code-block>
</chapter>

<chapter title="confirmacao_venda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Confirmação de venda'
Tamanho: 27
Item slot: 13
Itens:
   Confirmar:
      Slot: 11
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 5
      Glow: false
      Name: '&aConfirmar'
      Lore:
      - '&7Quantia a ser vendida: &a{quantia}&7.'
      - '&7Seu bônus: {bonus}&7.'
      - '&7Valor total: &c{PlayerPoints} pontos e {Money} coins&7.'
      - ''
      - '&7Clique para &aconfirmar&7 a venda.'
   Cancelar:
      Slot: 15
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: 35
      Data: 14
      Glow: false
      Name: '&cCancelar'
      Lore:
      - '&7Clique para &ccancelar&7 a venda.'

]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Bonus:
   VIP:
      Permissao: 'yshopv2.vip'
      Bonus: 10.0
      Ordem: 1
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Comando: 'yshop'
  Aliases: []

# Opcoes de configuração do NPC
NPC:
  ID: 9232744
  Skin: 'TheThunderGod063'
  Categoria: 'padrao.yml'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Shop'
      - '&7Veja os itens à venda.'

# Maximo de itens por compra
Maximo por compra: 64

# Fechar o menu depois de confirmar
Fechar confirmar: false

# Delay entre operações de compra e venda
# em segundos
Delay: 3

# Mensagens do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Cancelou: '&cVocê cancelou a compra.'
  Nao e numero: '&cO argumento não é um número.'
  Acao inexistente: '&cA ação não foi encontrada.'
  Categoria inexistente: '&cA categoria não foi encontrada.'
  Nao tem pontos: '&cDesculpe, mas você não possui a quantia necessária de pontos, &7{quantia} pontos&c.'
  Nao tem money: '&cDesculpe, mas você não possui a quantia necessária de money, &7{quantia} money&c.'
  Maximo: '&cDesculpe, o valor máximo por compra é de 64.'
  Inv cheio: '&cSeu inventário não tem espaço suficiente.'
  Comprou: '&aVocê adquiriu produtos no shop.' #deixe '' para não usar
  Nao possui: '&cVocê não possui a quantia &7{quantia} em &7{tipo}&c.'
  Desabilitado: '&cEste plugin &f{plugin}&c não está ligado.'
  Setado: '&aNPC da pesca setado com sucesso.'
  Removido: '&aNPC da pesca removido com sucesso'
  Nao setado: '&cO NPC não está setado.'
  Fragmento suficiente: '&cVocê não possui fragmentos suficientes.'
  Vendeu: '&aVocê vendeu produtos no shop.' #deixe '' para não usar
  Vendeu suficiente: '&aVocê não tem {amount} itens para vender.'
  Delay: '&c&lERRO! &cAguarde &e{time} &cpara comercializar na loja novamente.'
  Digite:
    - ''
    - '&aDigite a quantia que deseja comprar do item {item}&a.'
    - ''
    - '&7Preços:'
    - '&7> &fMoney: &a{Money}&7.'
    - '&7> &fPoints: &a{PlayerPoints}&7.'
    - ''
    - '&7Seu desconto:{desconto}&7.'
    - ''
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite venda:
    - ''
    - '&aDigite a quantia que deseja vender do item {item}&a.'
    - ''
    - '&7Valor de cada:'
    - '&7> &fMoney: &a{Money}&7.'
    - '&7> &fPoints: &a{PlayerPoints}&7.'
    - ''
    - '&7Seu bonus:{bonus}&7.'
    - ''
    - '&7para cancelar digite &ncancelar&7.'
    - ''

# Formatador de mensagens
Formatador:
  Money: '&aMoney'
  Points: '&6Cash'
  Desconto: ' &7( {desconto}% )'
  Bonus: ' &7( {bonus}% )'
]]>
</code-block>
</chapter>

<chapter title="descontos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Descontos:
   VIP:
      Permissao: 'yshopv2.vip'
      Desconto: 10.0
      Ordem: 1
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
    permission: 'yshop.provider.money'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/40-yShop">Site do plugin yShop</a>
    </category>
</seealso>