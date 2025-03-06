# yEnchants
<secondary-label ref="factions"/>

### Descrição
Deixe que nosso feiticeiro venda encantamentos em troca de XP, influencie o mercado de frascos de XP.

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
<video src="//www.youtube.com/watch?v=_x2grE5P4fI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/encantar - Abrir o menu principal
/encantar setnpc - Setar o NPC do mago
/encantar delnpc - Deletar o NPC do mago
/encantar givelivro&nbsp;- Dar livros para um jogador
/encantar darencantamento&nbsp;- Dar livros encantados para um jogador
/encantar givefrasco - Dar frascos de xp para um jogador
/encantar giveespecial - Dar livros especiais para um jogador
/encantar giveruna - Dar runas de extração para um jogador
/xp - Ver sua quantia de xp
/xp  - Ver a quantia de xp de um jogador
/xp set - Setar xp para um jogador
/xp add - Adicionar xp para um jogador
/xp remove - Remover xp de um jogador
/reciclar&nbsp;- Abrir o menu do reciclador
/reciclar setnpc&nbsp;- Setar o NPC do reciclador
/reciclar delnpc&nbsp;- Deletar o NPC do reciclador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yenchants.usar - Permissão para o /encantar
yenchants.reciclar - Permissão para o /reciclar
yenchants.setnpc - Permissão para o /encantar setnpc e /reciclador setnpc
yenchants.delnpc - Permissão para o /encantar delnpc e /reciclador setnpc
yenchants.givelivro - Permissão para o /encantar givelivro
yenchants.giveenchant - Permissão para o /encantar darencantamento
yenchants.giveespecial - Permissão para o /encantar giveespecial
yenchants.givefrasco - Permissão para o /encantar givefrasco
yenchants.giveruna - Permissão para o /encantar giveruna
yenchants.usar.xp - Permissão para o /xp
yenchants.setar - Permissão para o /xp setar
yenchants.adicionar - Permissão para o /xp adicionar
yenchants.remover - Permissão para o /xp remover
yenchants.olhar - Permissão para o /xp</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yEnchants/
    ├── menus/
    │    ├── encantar.yml
    │    ├── especial.yml
    │    ├── especialpreview.yml
    │    ├── preview.yml
    │    ├── principal.yml
    │    └── reciclador.yml
    ├── categorias.yml
    ├── config.yml
    ├── frascos.yml
    └── reciclador.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="encantar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Encantar item'
Tamanho: 45
Itens:
  LivroSlot: 31
  ItemSlot: 29
  BackSlot: 18
  Confirmar:
    Slot: 24
    CustomSkull: false
    URL: ''
    ID: 35
    Data: 5
    Name: '&aConfirmar'
    Lore: [ '&7Clique para comprar e encantar' ]
# Caso queira enfeitar seu menu, poderá criar itens nesta seção:
Itens custom:
  Livro:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: 340
    Data: 0
    Name: '&eColoque o livro abaixo'
    Lore: []
  Item:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: 276
    Data: 0
    Name: '&eColoque o item abaixo'
    Lore: []
  Enfeite1:
    Slot: 0
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite2:
    Slot: 1
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite3:
    Slot: 2
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite4:
    Slot: 3
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite5:
    Slot: 4
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite6:
    Slot: 5
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite7:
    Slot: 6
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite8:
    Slot: 7
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite9:
    Slot: 8
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite10:
    Slot: 9
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite11:
    Slot: 10
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite12:
    Slot: 12
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite13:
    Slot: 14
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite14:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite15:
    Slot: 16
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite16:
    Slot: 17
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite18:
    Slot: 19
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite19:
    Slot: 20
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite20:
    Slot: 21
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite21:
    Slot: 22
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite22:
    Slot: 23
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite23:
    Slot: 25
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite24:
    Slot: 26
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite25:
    Slot: 27
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite26:
    Slot: 28
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite27:
    Slot: 30
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite28:
    Slot: 32
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite29:
    Slot: 33
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite30:
    Slot: 34
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite31:
    Slot: 35
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite32:
    Slot: 36
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite33:
    Slot: 37
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite34:
    Slot: 38
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite35:
    Slot: 39
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite36:
    Slot: 40
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite37:
    Slot: 41
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite38:
    Slot: 42
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite39:
    Slot: 43
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []
  Enfeite40:
    Slot: 44
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Name: ''
    Lore: []

]]>
</code-block>
</chapter>

<chapter title="especial.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Encantamentos - Especial'
Tamanho: 27
BackSlot: 9
Itens:
  Coins:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: 265
    Data: 0
    Glow: true
    Name: '&fCoins'
    Lore:
      - '&cVocê não pode realizar a compra'
      - '&cpor meio deste pagamento.'
  Cash:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: 266
    Data: 0
    Glow: true
    Name: '&aCash'
    Lore:
      - '&7Clique para comprar este livro'
      - '&7gastando &6100 cash&7.'
# Caso queira enfeitar seu menu, poderá criar itens nesta seção:
Itens custom: {}
  #Enfeite1:
  #  Slot: 0
  #  CustomSkull: false
  #  URL: ''
  #  ID: 1
  #  Data: 0
  #  Glow: true
  #  Name: ''
  #  Lore: []
]]>
</code-block>
</chapter>

<chapter title="especialpreview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Encantamentos - Preview'
Tamanho: 27
Slots: [ 10, 11, 12, 13, 14, 15 ]
BackSlot: 0
VoltarSlot: 18
ProximoSlot: 26
Itens:
  Item1:
    CustomSkull: false
    URL: ''
    ID: 1
    Data: 0
    Glow: true
    Name: '&aPedra preciosa'
    Lore:
      - '&fEsta é uma pedra preciosa.'
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Encantamentos - Preview'
Tamanho: 27
Slots: [ 10, 11, 12, 13, 14, 15 ]
BackSlot: 0
VoltarSlot: 18
ProximoSlot: 26
Item:
  CustomSkull: false
  URL: ''
  ID: BOOK
  Data: 0
  Name: '&eLivro encantado'
  Lore: []
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Encantamentos'
Tamanho: 45
Itens:
  Informacoes:
    Slot: 13
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSua experiência'
    Lore:
      - '&fXP atual: &7{xp}&f.'
  Frasco sim:
    Slot: 29
    CustomSkull: false
    URL: ''
    ID: 384
    Data: 0
    Glow: false
    Name: '&eFrasco de experiência'
    Lore:
      - '&fCusto: &a{xp} XP&f.'
      - ''
      - '&7Você receberá um frasco de'
      - '&7experiência com &n{xp} XP.'
  Frasco nao:
    Slot: 29
    CustomSkull: false
    URL: ''
    ID: 374
    Data: 0
    Glow: false
    Name: '&eFrasco de experiência'
    Lore:
      - '&cVocê não possui XP para'
      - '&cser coletado.'
  Especiais:
    Slot: 34
    CustomSkull: false
    URL: ''
    ID: 403
    Data: 0
    Glow: false
    Name: '&eLivro de encantamento'
    Lore:
      - '&fTipo: &6Especiais&f.'
      - ''
      - '&7Clique com &fbotão direito &7para'
      - '&7ver os encantamentos especiais.'
      - ''
      - '&fCusto: &a10.000 coins &7ou &6100 cash&f.'
  Encantar:
    Slot: 31
    CustomSkull: false
    URL: ''
    ID: 145
    Data: 0
    Glow: false
    Name: '&eForjar'
    Lore:
      - '&7Clique para abrir o menu e'
      - '&7forjar o encantamento no seu item.'
  Reciclar:
    Slot: 22
    CustomSkull: false
    URL: ''
    ID: HOPPER
    Data: 0
    Glow: false
    Name: '&eReciclar'
    Lore:
      - '&7Clique para abrir o menu e'
      - '&7reciclar os encantamentos do seu item.'
# Caso queira enfeitar seu menu, poderá criar itens nesta seção:
Itens custom: {}
  #Enfeite1:
  #  Slot: 0
  #  CustomSkull: false
  #  URL: ''
  #  ID: 1
  #  Data: 0
  #  Glow: true
  #  Name: ''
  #  Lore: []
# Itens das categorias
# configuradas na "categorias.yml"
Categorias:
  cat1:
    Categoria: 'basico'
    Slot: 24
    Item:
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: False
      Name: '&eLivro de encantamento'
      Lore:
        - '&fTipo: &7Básico.'
        - ''
        - '&7Clique com &fbotão direito &7para.'
        - '&7ver os encantamentos básicos.'
        - ''
        - '&fCusto: &a1000 XP&f.'
  cat2:
    Categoria: 'medio'
    Slot: 25
    Item:
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: False
      Name: '&eLivro de encantamento'
      Lore:
        - '&fTipo: &7Médio.'
        - ''
        - '&7Clique com &fbotão direito &7para.'
        - '&7ver os encantamentos médios.'
        - ''
        - '&fCusto: &a1500 XP&f.'
  cat3:
    Categoria: 'avancado'
    Slot: 33
    Item:
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: False
      Name: '&eLivro de encantamento'
      Lore:
        - '&fTipo: &7Avançado.'
        - ''
        - '&7Clique com &fbotão direito &7para.'
        - '&7ver os encantamentos avançados.'
        - ''
        - '&fCusto: &a2500 XP&f.'
# Itens dos frascos
# configuradas na "frascos.yml"
Frascos:
  frasco1:
    Frasco: 'frasco1'
    Slot: 19
    Item:
      CustomSkull: false
      URL: ''
      ID: 384
      Data: 0
      Glow: False
      Name: '&eFrasco de experiência'
      Lore:
        - '&fCusto: &a1000 XP&f.'
        - ''
        - '&7Você receberá um frasco de'
        - '&7experiência com &n1000 XP.'
  frasco2:
    Frasco: 'frasco2'
    Slot: 20
    Item:
      CustomSkull: false
      URL: ''
      ID: 384
      Data: 0
      Glow: False
      Name: '&eFrasco de experiência'
      Lore:
        - '&fCusto: &a3000 XP&f.'
        - ''
        - '&7Você receberá um frasco de'
        - '&7experiência com &n3000 XP.'
  frasco3:
    Frasco: 'frasco3'
    Slot: 28
    Item:
      CustomSkull: false
      URL: ''
      ID: 384
      Data: 0
      Glow: False
      Name: '&eFrasco de experiência'
      Lore:
        - '&fCusto: &a5000 XP&f.'
        - ''
        - '&7Você receberá um frasco de'
        - '&7experiência com &n5000 XP.'


]]>
</code-block>
</chapter>

<chapter title="reciclador.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Reciclador'
Tamanho: 45
FrascoSlot: 40
Itens:
  Cancelar:
    Slot: 39
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 14
    Glow: false
    Name: '&cCancelar'
    Lore:
      - '&7Clique para cancelar a reciclagem.'
  Confirmar:
    Slot: 41
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 5
    Glow: false
    Name: '&aConfirmar'
    Lore:
      - '&7Clique para reciclar todos'
      - '&7os itens selecionados.'
  Frasco sim:
    CustomSkull: false
    URL: ''
    ID: 384
    Data: 0
    Glow: false
    Name: '&eFrasco de experiência'
    Lore:
      - '&fValor total: &a{xp} XP'
      - ''
      - '&7Todos os seus itens serão transformados em'
      - '&7um frasco de experiência com &n{xp} XP&7.'
      - ''
  Frasco nao:
    CustomSkull: false
    URL: ''
    ID: 374
    Data: 0
    Glow: false
    Name: '&eExperiência reciclada'
    Lore:
      - '&fValor total: &a0 XP'
      - ''
      - '&7Todos os seus itens serão transformados em'
      - '&7um frasco de experiência com &n0 XP&7.'
# Caso queira enfeitar seu menu, poderá criar itens nesta seção:
Itens custom:
  Enfeite1:
    Slot: 36
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Glow: false
    Name: ''
    Lore: []
  Enfeite2:
    Slot: 37
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Glow: false
    Name: ''
    Lore: []
  Enfeite3:
    Slot: 38
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Glow: false
    Name: ''
    Lore: []
  Enfeite4:
    Slot: 42
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Glow: false
    Name: ''
    Lore: []
  Enfeite5:
    Slot: 43
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Glow: false
    Name: ''
    Lore: []
  Enfeite6:
    Slot: 44
    CustomSkull: false
    URL: ''
    ID: 160
    Data: 15
    Glow: false
    Name: ''
    Lore: []
]]>
</code-block>
</chapter>

</chapter>

<chapter title="categorias.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Categorias:
  basico:
    Nome: 'Básico'
    # Custo em XP
    Custo: 1000
    # Chance de vir algum livro encantado
    # ao abrir.
    Chance:
      Min: 50
      Max: 90
    # Encantamentos que poderá vir neste livro
    # encantamento,nível
    # Lista de nomes de encantamentos: https://helpch.at/docs/1.8.8/index.html?org/bukkit/enchantments/Enchantment.html
    Encantamentos:
      - PROTECTION_ENVIRONMENTAL,1
      - PROTECTION_ENVIRONMENTAL,2
      - PROTECTION_FIRE,1
      - PROTECTION_FIRE,2
      - OXYGEN,1
      - PROTECTION_FALL,1
      - PROTECTION_FALL,2
      - DEPTH_STRIDER,1
      - DAMAGE_ALL,1
      - DAMAGE_ALL,2
      - LOOT_BONUS_MOBS,1
      - DIG_SPEED,1
      - DIG_SPEED,2
      - DURABILITY,1
      - DURABILITY,2
      - LOOT_BONUS_BLOCKS,1
      - ARROW_DAMAGE,1
      - ARROW_DAMAGE,2
    # Item que o jogador irá abrir
    Item:
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: False
      Name: '&eLivro de encantamento'
      Lore:
        - '&fTipo: &7Básico.'
        - ''
        - '&7Clique com &fbotão direito &7para abrir.'
  medio:
    Nome: 'Médio'
    Custo: 1500
    Chance:
      Min: 40
      Max: 70
    Encantamentos:
      - PROTECTION_ENVIRONMENTAL,3
      - PROTECTION_ENVIRONMENTAL,4
      - PROTECTION_FIRE,3
      - OXYGEN,2
      - PROTECTION_FALL,3
      - DEPTH_STRIDER,2
      - DAMAGE_ALL,3
      - DAMAGE_ALL,4
      - LOOT_BONUS_MOBS,2
      - DIG_SPEED,3
      - DIG_SPEED,4
      - DURABILITY,3
      - DURABILITY,4
      - LOOT_BONUS_BLOCKS,2
      - ARROW_DAMAGE,3
      - ARROW_DAMAGE,4
      - FIRE_ASPECT,1
      - ARROW_KNOCKBACK,1
    Item:
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: False
      Name: '&eLivro de encantamento'
      Lore:
        - '&fTipo: &7Médio.'
        - ''
        - '&7Clique com &fbotão direito &7para abrir.'
  avancado:
    Nome: 'Avançado'
    Custo: 2500
    Chance:
      Min: 20
      Max: 40
    Encantamentos:
      - PROTECTION_ENVIRONMENTAL,4
      - PROTECTION_FIRE,4
      - OXYGEN,3
      - PROTECTION_FALL,4
      - DEPTH_STRIDER,3
      - DAMAGE_ALL,5
      - LOOT_BONUS_MOBS,3
      - DIG_SPEED,5
      - DURABILITY,4
      - LOOT_BONUS_BLOCKS,3
      - ARROW_DAMAGE,5
      - ARROW_INFINITE,1
      - FIRE_ASPECT,2
      - ARROW_KNOCKBACK,2
      - ARROW_FLAME,1
      - SILK_TOUCH,1
    Item:
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: False
      Name: '&eLivro de encantamento'
      Lore:
        - '&fTipo: &7Avançado.'
        - ''
        - '&7Clique com &fbotão direito &7para abrir.'
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Enchant:
    Comando: 'encantar'
    Aliases: [ enchant ]
  XP:
    Comando: 'xp'
    Aliases: [ exp ]
  Reciclar:
    Comando: 'reciclar'
    Aliases: [ reciclador, recycle, recycler ]

#Coloque yPoints, PlayerPoints, JH_Shop, yCash, TGCash, AtlasEconomiaSecundaria, MageCash, WheavelGems, LegendaryEconomy
Plugin de Pontos: 'PlayerPoints'

# Opcoes de configuração do NPC
NPC:
  ID: 9232856
  Skin: 'TheMage'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Feiticeiro'
      - '&7Encante seus itens.'

# Opcoes de configuração do NPC do reciclador
NPC reciclador:
  ID: 92328566
  Skin: 'TheMage'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Reciclador'
      - '&7Recicle seus itens.'

# Opções gerais do plugin
Opcoes:
  # Para encantar, deve-se ter o nível anterior do encantamento.
  Anterior: true
  # Ao clicar numa mesa de encantamentos, abrir o menu do plugin
  Mesa menu: true
  # "Somar" encantamentos iguais ao encantar
  # Por exemplo: o peitoral tem protection 3 e o usuário tenta encantar
  # com um livro protection 3; o item vai ser encantado com o protection 4
  Somar iguais: false
  # Metadatas que o bloco tiver não irá abrir o menu do plugin
  Metadata blacklist:
    - 'yMultiAltar'
  # Lista de itens que a runa de extração não irá funcionar
  # id:data
  Runa blacklist:
    - '403:0'
  # Encantamentos máximos
  # Necessário para definir um máximo para não somar
  Max enchants:
    - 'DURABILITY:10'
  Especial:
    # Executar um comando ao invés de dar o livro
    Comando-executar: false
    # Comando que será executado caso a opção acima esteja ativada
    Comando: 'give {player} stone {quantia}'
    # Ao abrir um livro, irá escolher um dos comandos abaixo
    Comandos:
      - 'give {player} stone 1'
    Custos:
      custo1:
        Tipo: 'yPoints'
        Display: 'Pontos'
        Preco: 1000.0
    Coins:
      Ativar: true
      Custo: 1000

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não possui permissão para isto.'
  Setado: '&aNPC setado com sucesso.'
  Removido: '&aNPC removido com sucesso'
  Nao setado: '&cO NPC não está setado.'
  Suficiente: '&cVocê não possui XP suficiente.'
  Comprou frasco: '&aVocê adquiriu um frasco de &7{xp} XP&a.'
  Comprou livro: '&aVocê adquiriu um livro de encantamentos por &7{xp} XP&a.'
  Nao e numero: '&cO argumento não é um número.'
  Nao encontrado: '&cJogador não encontrado.'
  Setou: '&aVocê setou &7{xp} XP &apara o jogador &7{player}&a.'
  Adicionou: '&aVocê adicionou &7{xp} XP &apara o jogador &7{player}&a.'
  Removeu: '&aVocê removeu &7{xp} XP &ado jogador &7{player}&a.'
  Olhar: '&aXP do jogador &7{player}&a: &7{xp} XP&a.'
  Deu: '&aVocê deu um frasco de &7{xp} XP&a para o jogador &7{player}&a.'
  Deu runa: '&aVocê deu &7{quantia}x Runas de Extração&a para o jogador &7{player}&a.'
  Deu livro: '&aVocê deu &7{quantia}x Livros de Encantamento {livro}&a para o jogador &7{player}&a.'
  Deu especial: '&aVocê deu &7{quantia}x Livros de Encantamento &6Especial&a para o jogador &7{player}&a.'
  Ativou frasco: '&aVocê ativou um frasco de &7{xp} XP&a.'
  Nao pode: '&cEste encantamento não é para esse item.'
  Anterior: '&cVocê precisa ter o level anterior deste encantamento.'
  Superior: '&cO item já está encantado com um level superior.'
  Igual: '&cO item já contem este encantamento no mesmo level.'
  Falhou: '&cInfelizmente o encantamento falhou.'
  Encantou: '&aItem encantado com sucesso.'
  Sem: '&cEste item não contém encantamentos.'
  Extraido: '&aEncantamentos extraidos com sucesso.'
  Money suficiente: '&cVocê não possui money suficiente.'
  Cash suficiente: '&cVocê não possui cash suficiente.'
  Comprou especial: '&aVocê comprou um livro especial com sucesso.'
  Abriu especial: '&aVocê abriu um livro especial.'
  Cancelado: '&cReciclagem cancelada.'
  Reciclado: '&aVocê reciclou seus itens com sucesso.'
  Proibido: '&cVocê só pode reciclar itens ou livros com encantamentos.'
  Maximo: '&cEste item já possui o nível máximo deste encantamento.'
  Inserir: '&cVocê deve inserir o item e o livro.'
  No-has: '&cVocê não possui &f{value} {type}&c.'
  Deu encantamento: '&aVocê deu &71x Livros de Encantamento {encantamento} LVL.{level} &8({chance}%) &a para o jogador &7{player}&a.'

# Item do encantamento que será aplicado
Aplicavel:
  CustomSkull: false
  URL: ''
  ID: 403
  Data: 0
  Name: '&eLivro encantado'
  Lore:
    - ''
    - '&aChances: &e{chance}%&a.'

# Item da runa de extração
Runa:
  CustomSkull: false
  URL: ''
  ID: 154
  Data: 0
  Name: '&aRuna de extração'
  Glow: true
  Lore:
    - ''
    - '&7Clique em um item encantando para'
    - '&7extrair os seus encantamentos.'
    - ''

# Item do livro especial
Especial:
  CustomSkull: false
  URL: ''
  ID: 403
  Data: 0
  Name: '&aLivro de encantamentos'
  Lore:
    - ''
    - '&7Clique para abrir este livro &6especial&7.'
    - ''

# As setas dos menus
Setas:
  # Voltar ao menu anterior
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
  # Voltar a página anterior
  Anterior:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar à página anterior.'
  # Ir para a próxima página
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

<chapter title="frascos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Item:
  CustomSkull: false
  URL: ''
  ID: 384
  Data: 0
  Glow: False
  Name: '&eFrasco de experiência'
  Lore:
    - '&fXP: &a{xp}&f.'
Frascos:
  frasco1:
    # Custo em XP
    Custo: 1000
  frasco2:
    Custo: 3000
  frasco3:
    Custo: 5000
]]>
</code-block>
</chapter>

<chapter title="reciclador.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# quantia de xp para qualquer item encantado
XP base: 200
# lista de encantamentos
Encantamentos:
  enc1:
    # nome do encantamento
    # lista: https://helpch.at/docs/1.8.8/org/bukkit/enchantments/Enchantment.html
    Encantamento: 'ARROW_DAMAGE'
    # quantia de XP pelo nível 1
    Padrao: 100
    # quantia de XP acrescida aos outros níveis
    PorLevel: 10
  enc2:
    Encantamento: 'ARROW_FIRE'
    Padrao: 100
    PorLevel: 10
  enc3:
    Encantamento: 'ARROW_INFINITE'
    Padrao: 100
    PorLevel: 10
  enc4:
    Encantamento: 'ARROW_KNOCKBACK'
    Padrao: 100
    PorLevel: 10
  enc5:
    Encantamento: 'DAMAGE_ALL'
    Padrao: 100
    PorLevel: 10
  enc6:
    Encantamento: 'DAMAGE_ARTHROPODS'
    Padrao: 100
    PorLevel: 10
  enc7:
    Encantamento: 'DAMAGE_UNDEAD'
    Padrao: 100
    PorLevel: 10
  enc8:
    Encantamento: 'DEPTH_STRIDER'
    Padrao: 100
    PorLevel: 10
  enc9:
    Encantamento: 'DIG_SPEED'
    Padrao: 100
    PorLevel: 10
  enc10:
    Encantamento: 'DURABILITY'
    Padrao: 100
    PorLevel: 10
  enc11:
    Encantamento: 'FIRE_ASPECT'
    Padrao: 100
    PorLevel: 10
  enc12:
    Encantamento: 'KNOCKBACK'
    Padrao: 100
    PorLevel: 10
  enc13:
    Encantamento: 'LOOT_BONUS_BLOCKS'
    Padrao: 100
    PorLevel: 10
  enc14:
    Encantamento: 'LOOT_BONUS_MOBS'
    Padrao: 100
    PorLevel: 10
  enc15:
    Encantamento: 'LUCK'
    Padrao: 100
    PorLevel: 10
  enc16:
    Encantamento: 'LURE'
    Padrao: 100
    PorLevel: 10
  enc17:
    Encantamento: 'OXYGEN'
    Padrao: 100
    PorLevel: 10
  enc18:
    Encantamento: 'PROTECTION_ENVIRONMENTAL'
    Padrao: 100
    PorLevel: 10
  enc19:
    Encantamento: 'PROTECTION_EXPLOSIONS'
    Padrao: 100
    PorLevel: 10
  enc20:
    Encantamento: 'PROTECTION_FALL'
    Padrao: 100
    PorLevel: 10
  enc21:
    Encantamento: 'PROTECTION_FIRE'
    Padrao: 100
    PorLevel: 10
  enc22:
    Encantamento: 'PROTECTION_PROJECTILE'
    Padrao: 100
    PorLevel: 10
  enc23:
    Encantamento: 'SILK_TOUCH'
    Padrao: 100
    PorLevel: 10
  enc24:
    Encantamento: 'THORNS'
    Padrao: 100
    PorLevel: 10
  enc25:
    Encantamento: 'WATER_WORKER'
    Padrao: 100
    PorLevel: 10
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/12-yEnchants">Site do plugin yEnchants</a>
    </category>
</seealso>