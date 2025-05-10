# yVender
<secondary-label ref="utility"/>

### Descrição
Venda itens ao agachar, manualmente ou automaticamente.

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
<video src="//www.youtube.com/watch?v=MoLaMSHABRE"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/vender - Abre o menu principal ou vende manualmente.
/vender menu - Abre o menu principal.
/vender reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yvender.usar - Permissão para o /vender e /vender menu
yvender.reload - Permissão para o /vender reload
yvender.bypass.vender - Dar bypass no delay da venda manual.
yvender.bypass.shift - Dar bypass no delay de venda por shift.Permissão para a venda manual, por shift e automática na config.yml</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yVender/
    ├── menus/
    │    ├── itens.yml
    │    └── principal.yml
    ├── new/
    │    └── itens_new.yml
    ├── bonus.yml
    ├── commands.yml
    ├── config.yml
    ├── delay.yml
    ├── economies.yml
    ├── messages.yml
    └── upgrades.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="itens.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Itens do vender'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 18
VoltarSlot: 27
ProximoSlot: 35
Item:
  Name: '&a{display}'
  Lore:
    - ''
    - ' &fPreço por unidade: &a{unidade_money}&f.'
    - ' &fPreço por pack: &a{pack_money}&f.'
    - ' &fSeu bônus: &b{bonus}%&f.'
    - ''
# Crie itens customizados
Itens custom: {}
#  Enfeite:
#    Slot: 11
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: true
#    Name: '&aEnfeite'
#    Lore: []
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Vender'
Tamanho: 27
Auto slot: 13
Shift slot: 15
Itens:
  Vender:
    Slot: 10
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/d883f946202bbdf25f8a1062e8c3317194333128207c89a474bde300c533dc3c'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aVender'
    Lore:
      - '&7Clique para vender seus itens.'
  Itens:
    Slot: 11
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/e2a46b04ebd3bef3bf77a2c624434945d34a0c947a2ab18a785e633bdceed90'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aItens'
    Lore:
      - '&7Clique para ver os itens do seu grupo.'
  Auto sim:
    CustomSkull: false
    URL: ''
    ID: 351
    Data: 10
    Glow: false
    Name: '&aVenda automática'
    Lore:
      - '&fEstado: &aAtivada&f.'
      - ''
      - '&7Você está vendendo seus itens'
      - '&7automaticamente a cada 1 segundo.'
  Auto nao:
    CustomSkull: false
    URL: ''
    ID: 351
    Data: 8
    Glow: false
    Name: '&aVenda automática'
    Lore:
      - '&fEstado: &cDesativada&f.'
      - ''
      - '&7Clique para vender seus itens'
      - '&7automaticamente a cada 1 segundo.'
  Shift sim:
    CustomSkull: false
    URL: ''
    ID: 351
    Data: 10
    Glow: false
    Name: '&aVenda por Shift'
    Lore:
      - '&fEstado: &aAtivada&f.'
      - ''
      - '&7Você está vendendo seus itens'
      - '&7ao agaixar.'
  Shift nao:
    CustomSkull: false
    URL: ''
    ID: 351
    Data: 8
    Glow: false
    Name: '&aVenda por Shift'
    Lore:
      - '&fEstado: &cDesativada&f.'
      - ''
      - '&7Clique para vender seus itens'
      - '&7ao agaixar.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Magnata:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

</chapter>

<chapter title="new" collapsible="true">
<chapter title="itens_new.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
itens:
  membro:
    # A ordem serve para pegar o maior caso
    # o jogador tenha permissão de vários grupos
    ordem: 1
    # Permissão para vender nesse grupo
    permissao: 'yvender.membro'
    itens:
      item1:
        # Ordenação do item no menu
        ordem: 1
        # Material da venda
        material: 'STONE:0'
        # Nome do item
        display-name: '&7Pedra'
        # Vender apenas os itens que estiverem renomeados com o display_name
        require-display-name: false
        # Permissão para vender esse item
        permissao: ''
        # Item no menu
        display:
          material: 'STONE:0'
          name: '&7Pedra'
          lore:
            - ''
            - ' &fPreço por unidade: &a{unidade_money}&f.'
            - ' &fPreço por pack: &a{pack_money}&f.'
            - ' &fSeu bônus: &b{bonus}%&f.'
            - ''
            - '&aBotão &fESQUERDO &apara vender 64.'
            - '&aSHIFT+Botão &fESQUERDO &apara vender tudo.'
        # Preços que a unidade irá dar
        prices:
          price1:
            provider: 'money'
            amount: 10.0
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Este bônus servirá na hora de vender drops.
# Você pode criar quantos quiser.
Bonus:
  VIP:
    Ordem: 1
    # O jogador que tiver várias permissões se bônus
    # será usada a de maior porcentagem
    #
    # Permissão do bônus
    Permissao: 'yvender.vip'
    # Bônus
    Bonus: 10.0
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
  sell: 'sell|vender'
]]>
</code-block>
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

# Opcoes gerais do plugin
Opcoes:
  # Ao executar o comando /vender, abrir o menu
  # se estiver false, ele irá vender diretamente.
  Abrir menu: true
  # Ativar a multiplicação pela bolsa
  Bolsa: true
  # Vender itens renomeados
  Vender renomeado: true
  # Vender itens não renomeados
  Vender NaoRenomeado: true
  # Fechar o menu de venda ao vender
  Vender fecharMenu: false
  # Permissao para vender manualmente
  Vender perm: 'yvender.vender'
  # Permissao para vender pelo shift
  Shift perm: 'yvender.shift'
  # Permissao para ativar o autovender
  Auto perm: 'yvender.auto'
  # Pegar os itens das ordens anteriores
  # que ele tem permissão. Só irá pegar os itens
  # que a ordem maior não possuir.
  Anteriores: false
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Mundos que não funcionará a venda
  Mundos blacklist: []

# Setas dos menus
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
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'
]]>
</code-block>
</chapter>

<chapter title="delay.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Delays:
  membro:
    Ordem: 1
    Permissao: ''
    # Delay de venda do autovender
    # em ticks
    Auto delay: 20
    # Delay de venda do shift
    # em segundos
    Shift delay: 10
    # Delay de venda do vender normal
    # em segundos
    Vender delay: 10
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
    permission: 'yvender.provider.money'
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

actionbar:
  sell: '&aVocê vendeu &7{quantia}x {item} &apor &6{money}&a. Bolsa &b{bolsa}%&a &8(+{bonus}%).'
  wait: '&cAguarde &7{tempo} segundos &cpara vender novamente.'

chat:
  syntax: '&cUse: /{command} {syntax}'
  target: '&cJogador {player} não encontrado.'
  number: '&cO argumento não é um número.'
  permission: '&cVocê não tem permissão para fazer isto.'
  console: '&cApenas jogadores in-game podem realizar esta ação.'
  cancelled: '&cVocê cancelou a ação.'
  reload: '&aConfigurações recarregadas com sucesso.'
  help: |

    &a/vender &8- &7Vende seus itens.
    &a/vender menu &8- &7Abre o menu principal.
    &a/vender itens &8- &7Abre o menu de itens cadastrados.

  found: '&cVocê não possui nenhum dos grupos cadastrados.'
  sell: '&f > &aVocê vendeu &7{quantia}x {item} &apor &6{money}&a. Bolsa &b{bolsa}% &8(+{bonus}%)&a.'
  none: '&cVocê não possui nenhum item para vender.'
  world: '&cVocê não pode vender nesse mundo.'
]]>
</code-block>
</chapter>

<chapter title="upgrades.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Upgrade de redução de delay
delay:
  # Valor padrão
  default: 0
  # Valor máximo
  maximum: 3
  # Quanto irá reduzir de delay por nível
  per-level: 1
  # Aplicar na venda por shift
  shift-sell: true
  # Aplicar na venda automática
  automatic-sell: true
  # Aplicar na venda manual
  manual-sell: true
  # Mensagens
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  upgraded: '&aVocê adquiriu um upgrade de delay.'
  # Preços por nível
  # Cálculo: level * price-amount
  prices-per-level:
    price1:
      provider: 'money'
      amount: 1000.0
  # Ícones no menu
  icon:
    slot: -1
    material: FIREBALL
    name: '&aUpgrade de Delay'
    lore:
      - ''
      - ' &fAtual: &7{actual}/{maximum}&f.'
      - ' &fCusto para -{per-level}: &7{Money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  icon-maximum:
    material: FIREBALL
    name: '&aUpgrade de Delay'
    lore:
      - ''
      - ' &fAtual: &7{actual}/{maximum}&f.'
      - ''
      - '&cEste upgrade já está no máximo.'

# Upgrade de limite de venda
limit:
  # Ativar o sistema de limite
  enabled: false
  # Valor padrão
  default: 0
  # Valor máximo
  maximum: 3
  # Quanto irá adicionar de limite por nível
  per-level: 100
  # Mensagens
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  upgraded: '&aVocê adquiriu um upgrade de limite.'
  # Preços por nível
  # Cálculo: level * price-amount
  prices-per-level:
    price1:
      provider: 'money'
      amount: 1000.0
  # Ícones no menu
  icon:
    slot: -1
    material: SLIME_BALL
    name: '&aUpgrade de Limite'
    lore:
      - ''
      - ' &fAtual: &7{actual}/{maximum}&f.'
      - ' &fCusto para +{per-level}: &7{Money} coins&f.'
      - ''
      - '&aClique para evoluir.'
  icon-maximum:
    material: SLIME_BALL
    name: '&aUpgrade de Limite'
    lore:
      - ''
      - ' &fAtual: &7{actual}/{maximum}&f.'
      - ''
      - '&cEste upgrade já está no máximo.'
]]>
</code-block>
</chapter>

</chapter>
## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yvender_limite% - Retorna a quantia de limite do jogador formatado.
%yvender_limite_raw% - Retorna a quantia de limite do jogador sem formatar.&nbsp;
</code-block>



## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/52-yVender">Site do plugin yVender</a>
    </category>
</seealso>