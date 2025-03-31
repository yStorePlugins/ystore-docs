# yMinas
<secondary-label ref="rankup"/>

### Descrição
Crie minas com uma picareta customizável

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
<video src="https://www.youtube.com/watch?v=zoqq3USdhO4?start=3"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mina - Abre o menu principal
/mina ir - Vai até uma mina
/mina sair - Sai da mina
/mina lista - Abre o menu de minas
/mina skins - Abre o menu de skins
/mina classes - Abre o menu de classes
/mina evoluir - Abre o menu de evolução
/mina bombas - Abre o menu de bombas
/blocos - Vê a quantia de blocos
/blocos [player] - Vê a quantia de blocos de um jogador
/blocos enviar - Envia seus blocos para um jogador
/blocos add - Adiciona blocos para um jogador
/blocos give - Dá blocos em forma de itens para um jogador
/blocos set - Seta blocos para um jogador
/blocos remove - Remove blocos de um jogador
/minaadmin criar - Cria uma mina
/minaadmin editar - Abre o menu de gerenciamento da mina
/minaadmin deletar - Deleta uma mina
/minaadmin resetar - Reseta uma mina
/minaadmin resetarpicareta - Reseta a picareta de um jogador
/minaadmin darnivel - Dar nível de picareta para um jogador
/minaadmin removernivel - Remover nível da picareta de um jogador
/minaadmin darenergia - Dar energia da picareta para um jogador
/minaadmin removerenergia - Remover energia da picareta de um jogador
/minaadmin lista - Abre a lista de minas
/minaadmin setsaida - Seta a saída das minas
/minaadmin resetarclasse - Reseta a classe de um jogador
/minaadmin adicionarclasse - Adiciona classe para um jogador
/minaadmin removerclasse - Remove a classe de um jogador
/minaadmin setarclasse - Seta a classe de um jogador
/minaadmin givebooster - Dar booster a um jogador
/minaadmin manutencao - Define a mina em manutenção ou não
/minaadmin kickall - Expulsa todos os jogadores das minas
/minaadmin reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yminas.usar - Permissão para o /mina
yminas.ir - Permissão para o /mina ir
yminas.lista - Permissão para o /mina lista
yminas.sair - Permissão para o /mina sair
yminas.enchants - Permissão para o /mina evoluir
yminas.bombs - Permissão para o /mina bombas
yminas.classes - Permissão para o /mina classes
yminas.skins - Permissão para o /mina skins
yminas.blocos.usar - Permissão para o /blocos
yminas.blocos.look - Permissão para o /blocos [player]
yminas.blocos.send - Permissão para o /blocos enviar
yminas.blocos.help - Permissão para o /blocos ajuda
yminas.go.all - Permissão para ir à todas as minas
yminas.teleport.bypass - Permissão para não ter delay de teleporte
yminas.teleport.movebypass - Permissão para não cancelar o teleporte ao se mover
yminas.blocos.add - Permissão para o /blocos add
yminas.blocos.remove - Permissão para o /blocos remove
yminas.blocos.set - Permissão para o /blocos set
yminas.blocos.give - Permissão para o /blocos give
yminas.admin.criar - Permissão para o /minaadmin criar
yminas.admin.deletar - Permissão para o /minaadmin deletar
yminas.admin.editar - Permissão para o /minaadmin editar
yminas.admin.resetar - Permissão para o /minaadmin resetar
yminas.admin.resetarpicareta - Permissão para o /minaadmin resetarpicareta
yminas.admin.darnivel - Permissão para o /minaadmin darnivel
yminas.admin.removernivel - Permissão para o /minaadmin removernivel
yminas.admin.darenergia - Permissão para o /minaadmin darenergia
yminas.admin.removerenergia - Permissão para o /minaadmin removerenergia
yminas.admin.lista - Permissão para o /minaadmin lista
yminas.admin.setsaida - Permissão para o /minaadmin setsaida
yminas.admin - Permissão para ser reconhecido como admin
yminas.admin.reload - Permissão para o /minaadmin reload
yminas.admin.resetarclasse - Permissão para o /minaadmin resetarclasse
yminas.admin.adicionarclasse - Permissão para o /minaadmin adicionarclasse
yminas.admin.removerclasse - Permissão para o /minaadmin removerclasse
yminas.admin.setarclasse - Permissão para o /minaadmin setarclasse
yminas.givebooster - Permissão para o /minaadmin givebooster
yminas.admin.manutencao - Permissão para o /minaadmin manutencao
yminas.admin.kickall - Permissão para o /minaadmin kickall
yminas.manutencao.bypass - Permissão para entrar nas minas em manutenção</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yminas_blocos% - Retorna os blocos do jogador formatado (1K, 1M, 1T...)
%yminas_blocos_raw% - Retorna os blocos do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_quebrados% - Retorna os blocos quebrados do jogador formatado (1K, 1M, 1T...)
%yminas_quebrados_raw% - Retorna os blocos quebrados do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_nivel% - Retorna o nível da picareta do jogador
%yminas_energia% - Retorna a energia da picareta do jogador formatado (1K, 1M, 1T...)
%yminas_energia_raw% - Retorna a energia da picareta do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_proximo_energia% - Retorna a energia do próx nível da picareta do jogador formatado (1K, 1M, 1T...)
%yminas_proximo_energia_raw% - Retorna a energia&nbsp;do próx nível&nbsp;da picareta do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_classe% - Retorna a classe atual
%yminas_classe_proximo% - Retorna a próxima classe
%yminas_classe_progresso% - Retorna a barra de progresso de evolução da classe
%yminas_classe_porcentagem% - Retorna a porcentagem de progresso de evolução da classe
%yminas_bonus% - Retorna o bônus do jogador
%yminas_bonus_display% - Retorna o display do bônus do jogador
%yminas_energia_progresso% - Retorna a barra de progresso de evolução da picareta
%yminas_energia_porcentagem% - Retorna a porcentagem de progresso de evolução da picareta
%yminas_encantamento_[enchant]% - Retorna o nível atual do encantamento
%yminas_encantamento_porcentagem_[enchant]% - Retorna a porcentagem do nível atual do encantamento
%yminas_encantamento_multiplicador_[enchant]% - Retorna o multiplicador do nível atual do encantamento
%yminas_tag_blocos% - Retorna a tag para o jogador com mais blocos
%yminas_tag_quebrados% - Retorna a tag para o jogador que quebrou mais blocos
%yminas_tag_tempo% - Retorna a tag para o jogador com mais tempo de mineração
%yminas_mina% - Retorna o nome da mina
%yminas_mina_raw% - Retorna o nome da mina na config
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{yminas_blocos} - Tag do jogador com mais blocos
{yminas_quebrados} - Tag do jogador que quebrou mais blocos
{yminas_tempo} - Tag do jogador com mais tempo de mineração
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:k
└── yMinas/
    ├── menus/
    │    ├── bombs.yml
    │    ├── classes.yml
    │    ├── desencantador.yml
    │    ├── evoluir.yml
    │    ├── filtro.yml
    │    ├── lista.yml
    │    ├── principal.yml
    │    ├── skins.yml
    │    └── top.yml
    ├── bonus.yml
    ├── boosters.yml
    ├── bungeecord.yml
    ├── classes.yml
    ├── config.yml
    ├── custom_encantamentos.yml
    ├── economies.yml
    ├── encantamentos.yml
    ├── ferramentas.yml
    ├── messages.yml
    ├── mina_recompensas.yml
    ├── recompensas.yml
    ├── scoreboard.yml
    └── skins.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="bombs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Bombas'
Tamanho: 54
]]>
</code-block>
</chapter>

<chapter title="classes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Mina - Classes'
Tamanho: 54
Slots: [ 11, 12,13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33]
BackSlot: 48
AnteriorSlot: 18
ProximoSlot: 26
# Item da classe atual
Classe:
  Slot: 50
  CustomSkull: false
  URL: ''
  ID: LEATHER_CHESTPLATE
  Data: 0
  Name: '&bClasses'
  Lore:
    - '&7Upando sua classe você irá ganhar'
    - '&7bônus na mineração, no ganho de'
    - '&7coins e gemas.'
    - ''
    - '&fSua classe: &7{classe}'
    - ''
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="desencantador.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Picareta - Desencatador'
Tamanho: 36
Slots: [11, 12, 13, 14, 15]
BackSlot: 29
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a picareta do jogador
PicaretaSlot: 31
# Configurações do enchant
Item:
  Nome: '&a{enchant}'
  Lore:
    - ''
    - '&fEncantamento: &7{enchant}'
    - '&fNíveis: &7{level}'
    - ''
    - '&fIrá ganhar &a{yminas} blocos &fe'
    - '&a{money} coins&f por nível.'
    - ''
    - '&aBotão &fESQUERDO &apara desencatar 1 nível'
    - '&aBotão &fDIREITO &apara desencatar {level} níveis'
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="evoluir.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Picareta - Evoluir'
Tamanho: 54
Slots: [11, 12, 13, 14, 15, 20, 21, 22, 23, 24, 29, 30, 31, 32, 33]
BackSlot: 45
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a picareta do jogador
PicaretaSlot: 47
# Item para ver adicionar mais blocos
Perfil:
  Slot: 50
  material: '{player}'
  name: '&a{player}'
  lore:
    - ''
    - '&fBlocos: &b{blocos}'
    - '&fBlocos quebrados: &b{blocos_quebrados}'
    - ''
Skin:
  Slot: 48
  material: '731f3279fc112b7f18bd0a2229934fcb5605c62823ce698b8b503ecccf0a3ac4'
  name: '&aSkins'
  lore:
    - '&7Configure a skin da sua picareta'
    - '&7e ganhe alguns bônus.'
    - ''
    - '&aClique para acessar'
# Item do filtro
Filtro:
  Slot: 52
  material: HOPPER
  glow: true
  name: '&aFiltro'
  lore:
    - '&7Desabilite encantamentos que não'
    - '&7queira utilizar no momento.'
    - ''
    - '&aClique para acessar'
# Item do desencantador
Desencantador:
  Slot: 53
  material: ANVIL
  glow: true
  name: '&aDesencantador'
  lore:
    - '&7Desencante encantamentos que não'
    - '&7queira utilizar e receba o valor'
    - '&7de volta.'
    - ''
    - '&aClique para acessar'
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="filtro.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Picareta - Filtro'
Tamanho: 36
Slots: [11, 12, 13, 14, 15]
BackSlot: 29
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a picareta do jogador
PicaretaSlot: 31
# Configurações do enchant
Item:
  Nome: '&a{enchant}'
  Lore:
    - ''
    - '&fEncantamento: &7{enchant}'
    - '&fDesativado: &7{status}'
    - ''
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="lista.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Mina - Lista'
Tamanho: 36
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
AnteriorSlot: 29
ProximoSlot: 33
# Este item será mostrado para cada mina que não estiver configurada na seção Minas.
Padrao:
  Name: '&e{nome}'
  Lore:
    - ''
    - '&7Clique para se teleportar'
    - '&7até esta mina.'
    - ''
# Configure as minas que irão aparecer
Minas:
  Mina1:
    # Nome da mina criada
    Mina: 'Mina1'
    Name: '&eMina 1'
    Lore:
      - '&7Essa mina comporta os seguintes'
      - '&7ranks:'
      - ''
      - '&f・&fPorcoIII &7-> &7PorcoI&7.'
      - ''
      - '&f・&7Permite Lucky Blocks.'
      - '&f・&7PVP &cOFF&7.'
      - ''
      - '&9&lyStore'

Itens: {}
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Mineração'
Tamanho: 27
Itens:
  Encantamentos:
    Slot: 10
    CustomSkull: true
    URL: 'b2f79016cad84d1ae21609c4813782598e387961be13c15682752f126dce7a'
    ID: AIR
    Data: 0
    Name: '&aEncantamentos'
    Lore:
      - '&7Gerencie os encantamentos da'
      - '&7sua picareta.'
      - ''
      - '&aClique para acessar.'
  Top:
    Slot: 11
    CustomSkull: false
    URL: ''
    ID: BOOK_AND_QUILL
    Data: 0
    Name: '&aTop'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacaram na mineração.'
      - ''
      - '&aClique para visualizar.'
  Minas:
    Slot: 12
    CustomSkull: false
    URL: ''
    ID: GOLD_INGOT
    Data: 0
    Name: '&aMinas'
    Lore:
      - '&7Veja as minas disponíveis no'
      - '&7nosso servidor.'
      - ''
      - '&aClique para visualizar.'
  Ir:
    Slot: 16
    CustomSkull: false
    URL: ''
    ID: DIAMOND_PICKAXE
    Data: 0
    Name: '&aIr minerar'
    Lore:
      - '&7Teleportar para sua mina e começar'
      - '&7a jornada de mineração.'
      - ''
      - ' &fSua mina: &b{mina}&f.'
      - ''
      - '&aClique para ir minerar'
  Sair:
    Slot: 16
    CustomSkull: true
    URL: '5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: AIR
    Data: 0
    Name: '&eSair da mineração'
    Lore:
      - '&7Terminar sua jornada de mineração'
      - '&7e sair da mina.'
      - ''
      - ' &fMina atual: &b{mina}&f.'
      - ''
      - '&aClique para sair da mineração'
  Classe:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: LEATHER_CHESTPLATE
    Data: 0
    Name: '&bClasses'
    Lore:
      - '&7Upando sua classe você irá ganhar'
      - '&7bônus na mineração, no ganho de'
      - '&7coins e gemas.'
      - ''
      - '&fSua classe: &7{classe}'
      - ''
      - '&aClique para gerenciar as classes'
  Bombs:
    Slot: 14
    CustomSkull: false
    URL: ''
    ID: FIREBALL
    Data: 0
    Name: '&bArsenal'
    Lore:
      - '&7Leve bombas no seu arsenal para'
      - '&7destruir a mina e ganhar muito'
      - '&7dinheiro.'
      - ''
      - '&aClique para abrir o arsenal'
  Booster-no:
    CustomSkull: false
    URL: ''
    ID: GLASS_BOTTLE
    Data: 0
    Name: '&aBooster'
    Lore:
      - '&cNenhum booster ativo'
  Booster:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: EXP_BOTTLE
    Data: 0
    Name: '&aBooster'
    Lore:
      - '&aSeu booster de drops está ativo!'
      - '&f> &bTempo: &7{time}&f.'
      - '&f> &bBônus venda: &7{bonus}%&f.'
      - '&f> &bBônus blocos: &7{bonus-block}%&f.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Sair:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="skins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Picareta - Skins'
Tamanho: 36
Slots: [11, 12, 13, 14, 15]
BackSlot: 29
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a picareta do jogador
PicaretaSlot: 31
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Mineração'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 30
AnteriorSlot: 9
ProximoSlot: 17
# Item do top Blocos
Item blocos:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fBlocos: &7{blocos}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top blocos quebrados
Item quebrados:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fBlocos Quebrados: &7{blocos}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top tempo
Item tempo:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fTempo de mineração: &7{tempo}'
    - '&fPosição: &e{pos}º'
    - ''
# Seletor dos tops
Seletor:
  Slot: 31
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: 0
  Data: 0
  Name: '&aSeletor do TOP'
# Tipos do seletor
Tipos:
  Blocos:
    Ativar: true
    Nome: 'Blocos'
  Quebrados:
    Ativar: true
    Nome: 'Blocos Quebrados'
  Tempo:
    Ativar: true
    Nome: 'Tempo de mineração'
# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome}'
  Selecionar: ' &f• &7{nome}'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="bonus.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos bônus quiser
# Será dado o bônus ao vender as platanções.
Bonus:
  membros:
    Ordem: 1
    # Permissão para ser reconhecido
    Permissao: 'yminas.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
    BonusBloco: 10.0
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
      # Bônus de venda
      bonus-block: 10.0
      # Item do booster
      item:
         material: EXP_BOTTLE
         glow: true
         name: '&aBônus de Mineração'
         lore: [ '', '&aTempo: &e{time}', '&aBônus de coins: &e{bonus}%', '&aBônus de blocos: &e{bonus-block}%', '' ]
]]>
</code-block>
</chapter>

<chapter title="bungeecord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Ativar o sistema de bungeecord
Ativar: false

# Modo deste servidor
# LOBBY (ex: servidor de RankUP)
# SERVER (ex: servidor que contém a mina)
Modo: 'LOBBY'

# Nome do servidor na config do BungeeCord em que o jogador vai ao sair da mina
Saida: 'rankup'

# Delay para enviar a picareta ao trocar para o servidor da mina
# em ticks
Delay: 3

# Bloquear ações neste servidor caso esteja fora da mina
# Somente caso o "Modo" for "SERVER"
# permissão de bypass: yminas.blocked.bypass
Block-actions: true
]]>
</code-block>
</chapter>

<chapter title="classes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
 Classes:
  class1:
    # O padrão é a ordem 0
    Ordem: 0
    Display: '&fQuartzo'
    # Cor da armadura
    # Formato: RED:GREEN:BLUE (255:255:255)
    # deixe RAINBOW para ser colorido
    Cor: '255:255:255'
    # Permissão para evoluir à esta classe
    # Deixe '' (vazio) para não usar
    Permissao: ''
    # Efeito:Nível
    Efeitos: ['SPEED:1']
    # Bônus que serão dados
    Bonus:
      Drops: 50
      Blocos: 30
    # Custos de evolução
    Custos:
      price1:
        provider: 'money'
        price: 1000.0
      price2:
        provider: 'yminas'
        price: 1000.0
    # Itens da armadura
    Armaduras:
      Capacete:
        Material: LEATHER_HELMET
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
      Peitoral:
        Material: LEATHER_CHESTPLATE
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
      Calca:
        Material: LEATHER_LEGGINGS
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
      Botas:
        Material: LEATHER_BOOTS
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
    # Itens do menu de classes
    Menu:
      Comprar:
        Material: LEATHER_CHESTPLATE
        Cor: '255:255:255'
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - '&7- &e{yminas} blocos'
          - ''
          - '&aClique para evoluir'
      Possui:
        Material: LEATHER_CHESTPLATE
        Cor: '255:255:255'
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&aClique para equipar.'
      Equipado:
        Material: LEATHER_CHESTPLATE
        Cor: '255:255:255'
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&aVocê está usando este.'
      Requisitos:
        Material: LEATHER_CHESTPLATE
        Cor: '255:255:255'
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - '&7- &e{yminas} blocos'
          - ''
          - '&cVocê não possui os custos para evoluir.'
      Anterior:
        Material: LEATHER_CHESTPLATE
        Cor: '255:255:255'
        Name: '&fClasse Quartzo'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&cVocê não possui a classe anterior.'
  class2:
    # O padrão é a ordem 0
    Ordem: 1
    Display: '&fBauxita'
    Cor: '238:0:255'
    Permissao: ''
    Efeitos: ['SPEED:2']
    Bonus:
      Drops: 80
      Blocos: 50
    Custos:
      price1:
        provider: 'money'
        price: 2000.0
      price2:
        provider: 'yminas'
        price: 2000.0
    Armaduras:
      Capacete:
        Material: LEATHER_HELMET
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
      Peitoral:
        Material: LEATHER_CHESTPLATE
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
      Calca:
        Material: LEATHER_LEGGINGS
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
      Botas:
        Material: LEATHER_BOOTS
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus adquiridos:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
    # Itens do menu de classes
    Menu:
      Comprar:
        Material: LEATHER_CHESTPLATE
        Cor: '238:0:255'
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - '&7- &e{yminas} blocos'
          - ''
          - '&aClique para evoluir'
      Possui:
        Material: LEATHER_CHESTPLATE
        Cor: '238:0:255'
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&aClique para equipar.'
      Equipado:
        Material: LEATHER_CHESTPLATE
        Cor: '238:0:255'
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&aVocê está usando este.'
      Requisitos:
        Material: LEATHER_CHESTPLATE
        Cor: '238:0:255'
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&fCusto para evoluir:'
          - '&7- &2$&f{money} coins'
          - '&7- &e{yminas} blocos'
          - ''
          - '&cVocê não possui os custos para evoluir.'
      Anterior:
        Material: LEATHER_CHESTPLATE
        Cor: '238:0:255'
        Glow: true
        Name: '&5Classe Bauxita'
        Lore:
          - ''
          - ' &7As classes irão te dar mais'
          - ' &7coins e blocos ao minerar!'
          - ''
          - '&fBônus habilitados:'
          - '&7- +{drops}% de coins'
          - '&7- +{blocos}% de blocos'
          - ''
          - '&cVocê não possui a classe anterior.'
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
  Tabela: 'yminas.players'
  Debug: true

# Comandos e aliases do plugin
Comando:
  MinaAdmin:
    Comando: 'Minaadmin'
    Aliases: [ minadmin ]
  Mina:
    Comando: 'mina'
    Aliases: [ minas, minerar, mine ]
  Blocos:
    Comando: 'blocos'
    Aliases: [ bloco, blocks, block ]

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Resetar as minas ao carregá-las da config
load-reset: true

# Quantidade do Y que vai teleportar ao spawn
# 1.19 usa-se -64
void-detect: 0

# Opções gerais do plugin
Opcoes:
  # Abrir o menu ao digitar /mina
  Mina menu: true
  # Ativar o livro do yRankup
  RankupBook: true
  # Ativar o sistema de minas em bungeecord
  Bungeecord: false
  # Quantia que irá somar no nível da fortuna
  # essencial para definir valores a partir da fortuna 1
  Fortuna-Acrescer: 0.5
  # Ativar o sistema de reset do FastAsyncWorldEdit ou WorldEdit (inclui AsyncWorldEdit)
  FAWE: true
  # Opções do FastAsyncWorldEdit ou WorldEdit (inclui AsyncWorldEdit)
  FAWEOptions:
    Normal: false # apagar o bloco quebrado usando o FastAsyncWorldEdit ou WorldEdit (inclui AsyncWorldEdit) (recomendo deixar desativado)
    Destruidor: true # apagar os blocos do raio do destruidor
    Explosao: true # -- da explosão
    Furadeira: true # -- da furadeira
    Laser: true # -- do raio do laser
  # Opções da luckyblock
  Luckyblock:
    Nuclear: false # dar lucky block quando o nuclear for ativado
    Destruidor: true # dar lucky block quando o destruidor for ativado
    Explosao: true # dar lucky block quando a explosão for ativada
    Furadeira: true # dar lucky block quando a furadeira for ativada
    Laser: true # dar lucky block quando o laser for ativado
  # Opções da recompensa
  Recompensa:
    Nuclear: false # dar recompensa quando o nuclear for ativado
    Destruidor: true # dar recompensa quando o destruidor for ativado
    Explosao: true # dar recompensa quando a explosão for ativada
    Furadeira: true # dar recompensa quando a furadeira for ativada
    Laser: true # dar recompensa quando o laser for ativado
  # Opções dos custom-enchants
  Custom-Enchant:
    Nuclear: false # dar custom-enchants quando o nuclear for ativado
    Destruidor: true # dar custom-enchants quando o destruidor for ativado
    Explosao: true # dar custom-enchants quando a explosão for ativada
    Furadeira: true # dar custom-enchants quando a furadeira for ativada
    Laser: true # dar custom-enchants quando o laser for ativado
  # Esconder o encantamento na lore da picareta caso o player desative ele
  # caso esteja false, o encantamento ficará riscado na lore da picareta
  DesativadoEsconder: false
  # Evoluir a picareta com a ação do botão direito
  EvoluirDireito: true
  # Evoluir a picareta com a ação do botão Q
  EvoluirQ: true
  # Máximo permitido para evoluir com Q
  QMax: 0
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Bloquear de quebrar blocos da mina enquanto o inventário estiver cheio
  Bloquear InvCheio: true
  # Ativar a picareta custom
  CustomPickaxe: true
  # Fazer com que a CustomPickaxe nunca quebre
  PickaxeUnbreakable: true
  # Resetar a picareta ao morrer na mina pvp
  ResetPvpDeath: false
  # Slot em que será setada a picareta do jogador
  # Deixe -1 para setar no slot que o jogador está selecionado
  PickaxeSlot: 2
  # Slot em que será setada a classe do jogador
  # Deixe -1 para não usar
  ClassesSlot: 6
  # Habilitar o menu de evolução ao interagir com a picareta sem shift
  InteragirEvolucaoNoShift: true
  # Habilitar o menu de evolução ao interagir com a picareta com shift
  InteragirEvolucaoYesShift: true
  # Permitir mover itens do inventário com os números na mina
  # Ativar esta opção pode causar erros dependendo da versão
  Numkeys: false
  # Para evoluir as classes ele deverá seguir a ordem delas?
  Classe ordem: true
  # Checar outras minas ao quebrar o bloco
  # Ideal para fazer 2 minas no mesmo warp
  Checar outras: false
  # Valor padrão (sem contar o multiplicador) que irá dar de blocos ao quebrar na mina
  BlocosDefault: 1
  # Skin default da picareta
  Skin-default: ''
  # Materiais que irão ser reconhecidos na skin
  Skin-materiais:
    - 'WOOD'
    - 'STONE'
    - 'IRON'
    - 'GOLD'
    - 'DIAMOND'
  # Sistema de money da mina
  # Quando o jogador minerar e receber money
  Money:
    # Dar o money direto pelo vault
    VaultAtivar: true
    # Caso a opção acima esteja desativada
    # irá executar o comando abaixo
    # (pode gerar lag)
    ComandoDar: 'money give {player} {quantia}'
  # Sistema de tags
  Tags:
    Blocos: '&b[B]'
    Quebrados: '&b[BQ]'
    Tempo: '&b[T]'
  # Sistema de energia
  Energia:
    # Ativar o sistema de energia
    Ativar: true
    # Quantia de energia por bloco quebrado
    Quantia: 1
    # Quantia de energia que irá aumentar a cada nível
    PorNivel: 1000
    # Ativar o sistema de dar encantamento aleatório
    DarEnchant: true
    # Comandos que irá dar quando evoluir (com enchant)
    ComandosEnchant: []
    # Comandos que irá dar quando evoluir (sem enchant)
    ComandosSemEnchant: []
    # Enchants que poderão ser dados
    # chance,encantamento
    Enchants:
      - '10.0,Eficiencia'
      - '10.0,Nuclear'
      - '10.0,Destruidor'
      - '10.0,Explosao'
      - '10.0,Laser'
      - '10.0,Furadeira'
      - '10.0,DestruidorInvertido'
      - '10.0,Linear'
      - '10.0,Esfera'
      - '10.0,X'
      - '10.0,Fortuna'
      - '10.0,Sumonador'
      - '10.0,Velocidade'
      - '10.0,Pressa'
      - '10.0,Sortudo'
      - '10.0,Multiplicador'
      - '10.0,Eletricidade'
    # Mensagens
    EvoluiuEnchant:
      - ''
      - '&bSua picareta evoluiu de nível!'
      - '&bEncantamento adquirido: &f+1 nível de {encantamento}&b.'
      - ''
    EvoluiuSemEnchant:
      - ''
      - '&bSua picareta evoluiu de nível!'
      - '&cInfelizmente todos seus encantamentos estão no máximo.'
      - ''
  # Sistema de encantamento aleatório por chance
  AleatorioChance:
    Chance: 0
    Mensagem:
      - ''
      - '&bEncantamento adquirido: &f+1 nível de {encantamento}&b.'
      - ''
  # Item da custompickaxe
  Pickaxe:
    CustomSkull: false
    URL: ''
    ID: DIAMOND_PICKAXE
    Data: 0
    Name: '&bPicareta &6[{blocos_quebrados}]'
    Lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{nivel}'
      - ' &fEnergia: &7{energia}/{energia_proximo} &f({progressbar}&f)'
  # Item das classes
  Classes:
    CustomSkull: false
    URL: ''
    ID: LEATHER_CHESTPLATE
    Data: 0
    Name: '&bClasses'
    Lore:
      - '&7Upando sua classe você irá ganhar'
      - '&7bônus na mineração, no ganho de'
      - '&7coins e gemas.'
      - ''
      - '&fSua classe: &7{classe}'
      - ''
      - '&aClique para upar sua classe'
  # Configuração do sistema de livro (yRankup)
  Livro:
    Formatador:
      Tem: '&a✔ {precisa} {tipo} &7(Possui {possui} {tipo})'
      NaoTem: '&c✖ {precisa} {tipo} &7(Possui {possui} {tipo})'
    Tipos:
      MONEY: 'coins'
      CASH: 'cash'
      ALMAS: 'almas'
      FRAGMENTOS: 'fragmentos'
      KILLS: 'kills'
      BLOCOS: 'blocos'
      FENOS: 'fenos'
      TEMPO: 'tempo'
    Item:
      # Slot em que será setada a classe do jogador
      # Deixe -1 para não usar
      Slot: 4
      Titulo: '&1Checklist'
      Conteudo:
        - ''
        - '&0Requisitos para o'
        - '&0próximo rank:'
        - ''
        - '&0Progresso: &7{progressbar} &7{porcentagem}'
        - ''
        - '{requisitos}'
        - ''
  # Varinha de seleção da mina
  Wand:
    CustomSkull: false
    URL: ''
    ID: GOLD_AXE
    Data: 0
    Glow: true
    Name: '&eSelecionar região'
    Lore:
      - '&fMina: &7{mina}&f.'
      - ''
      - '&aBotão esquerdo para selecionar a POS1'
      - '&aBotão direito para selecionar a POS2'
  # Item de blocos ativável
  Bloco:
    CustomSkull: true
    URL: '1ba16c3890af39c3f2d576586cff443de07dad32b2315e2ff6f0d5d6a3c663dd'
    ID: 0
    Data: 0
    Glow: true
    Name: '&b+{quantia} Blocos'
    Lore:
      - ''
      - '&fQuantia: &b{quantia}'
      - ''
      - '&7Clique com botão direito para ativar.'
      - ''
      - '&7Clique com shift + botão direito para compactar'
      - '&7todos os seus blocos no inventário em 1 só.'
      - ''
  # Mensagens e ações ao entrar
  Entrar:
    Title: '&bBem vindo à<nl>&fMina: {mina}'
    Actionbar: '&bVocê entrou na mina &f{mina}&b.'
    Som: 'ORB_PICKUP'
    Chat:
      - ''
      - '&bBem vindo à área de mineração.'
      - '&bVocê está na mina &f{mina}&b.'
      - ''
  # Mensagens e ações ao sair
  Sair:
    Title: ''
    Actionbar: '&bVocê saiu da mina &f{mina}&b.'
    Som: 'ORB_PICKUP'
    Chat:
      - ''
      - '&bVocê saiu da mina &f{mina}&b.'
      - ''
  # Lista de comandos permitidos na mina
  Comandos permitidos:
    - '/g'
    - '/l'
    - '/mina'
    - '/minerar'
    - '/mine'
    - '/minas'
  # Lista de comandos para sair da mina
  Comandos saida:
    - '/sair'
    - '/spawn'
    - '/exit'

# Configuração das outras mensagens
OutrasMensagens:
  LuckyBlock Encontrou:
    Title: '' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: []
  LuckyBlock Nada:
    Title: '' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat:
      - '&e&lLuckyBlock: &cInfelizmente você não ganhou nada :c'
  Vendeu:
    Title: '' # deixe '' para não usar
    Actionbar: '&a+{money} coins adicionados ┃ &r{bonus}&a.' # deixe '' para não usar
    Chat: []
  VendeuNegativo:
    Title: '' # deixe '' para não usar
    Actionbar: '&c-{money}' # deixe '' para não usar
    Chat: []
  Resetou: # envia apenas para quem está na mina
    Title: '&a{mina}<nl>&aResetada!' # deixe '' para não usar
    Actionbar: '&a{mina} &aresetada com sucesso.' # deixe '' para não usar
    Chat: []
  Evoluiu: # envia quando a picareta evolui de nível
    Title: '&aPicareta evoluída<nl>&apara &e{nivel}!' # deixe '' para não usar
    Actionbar: '&aSua picareta evoluiu para o nível &e{nivel}!' # deixe '' para não usar
    Chat: []
  InvCheio: # envia quando o jogador quebra um bloco com o inv cheio
    Title: '&cInventário cheio!' # deixe '' para não usar
    Actionbar: '&cSeu inventário está cheio!' # deixe '' para não usar
    Chat: []

# Itens padrões definidos para o jogador.
#items:
  # Siga o exemplo abaixo para criar itens custom
  #custom:
  #  material: BARRIER:0
  #  slot: 0
  #  name: ''
  #  lore: []
  #  left-command: ''
  #  right-command: ''
  #  left-perm: 'yminas.left-perm.custom'
  #  right-perm: 'yminas.right-perm.custom'

# Setas dos menus
Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&cVoltar'
    Lore:
      - '&7Clique para voltar ao menu anterior.'
  Anterior:
    CustomSkull: false
    URL: ''
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&cAnterior'
    Lore:
      - '&7Clique para voltar à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&aPróxima'
    Lore:
      - '&7Clique para ir à próxima página.'

# Formatador de mensagens
Formatador:
  Bonus tem: '&a+{bonus}% por ser {display}&a.'
  Bonus nao tem: ''

# Configuração da barra de progresso
Progress bar:
  Quantia: 10
  Simbolo: ':'
  Cor sim: '&a'
  Cor nao: '&7'

# Enviar a mensagem de recompensas ganhas a cada x tempo
Luckyblock mensagem:
  ativar: true
  # delay para enviar a mensagem
  # em segundos
  delay: 60
  mensagem:
    - ''
    - '&eLuckyBlock'
    - '&7Suas recompensas do último minuto.'
    - ''
    - '{chat}'
    - ''
]]>
</code-block>
</chapter>

<chapter title="custom_encantamentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode criar quantos quiser
Encantamentos:
  Chaveiro:
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: TRIPWIRE_HOOK
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem A+ Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: TRIPWIRE_HOOK
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem A+ Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: TRIPWIRE_HOOK
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem A+ Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Chaveiro'
    # Nível da picareta necessário para poder evoluir o encantamento
    NivelPicareta: 0
    Ordem: 13
    MostrarMenu: true
    PodeComprar: true
    # chance,comando
    Comandos:
      - '20,give {player} tripwire_hook 1'
    Mensagens:
      Title: '&aChave<nl>&eencontrada' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
    Nivel:
      Padrao: 1.0
      Maximo: 1.0 # Use -1 para ser infinito
      Porcentagem: 0.0 # porcentagem adquirida por nível (ele acrescenta na chance do comando)
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Aventureiro:
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: QUARTZ
        Data: 0
        Name: '&aAventureiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre limites ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem A+ Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: QUARTZ
        Data: 0
        Name: '&aAventureiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre limites ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem A+ Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: QUARTZ
        Data: 0
        Name: '&aAventureiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre limites ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem A+ Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Aventureiro'
    # Nível da picareta necessário para poder evoluir o encantamento
    NivelPicareta: 0
    Ordem: 14
    MostrarMenu: true
    PodeComprar: true
    # chance,comando
    Comandos:
      - '20,give {player} quartz 1'
    Mensagens:
      Title: '&aLimite<nl>&eencontrado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
    Nivel:
      Padrao: 1.0
      Maximo: 1.0 # Use -1 para ser infinito
      Porcentagem: 0.0 # porcentagem adquirida por nível (ele acrescenta na chance do comando)
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
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
  Money:
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
    permission: 'yminas.provider.money'
    # ‘Item’ que aparecerá
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fMoney&7.'
        - ' &7Valor atual: &f{value}&7.'
        - ''
        - '&aClique para alterar'
  yMinas:
    # Coloque o nome do plugin
    # Para money deixe Money
    provider: 'yMinas'
    # Formato inteiro
    display: 'Blocos'
    # Formato abreviado
    abbreviated: 'blocos'
    # Permitir que comercializem na loja com o jogador offline
    allow-offline: true
    # Permissão para o usuário conseguir definir esta economia
    permission: 'yminas.provider.yminas'
    # ‘Item’ que aparecerá
    item-settings:
      material: '209299a117bee88d3262f6ab98211fba344ecae39b47ec848129706dedc81e4f'
      name: '&aEconomia'
      lore:
        - ''
        - ' &7Tipo de economia: &fBlocos&7.'
        - ' &7Valor atual: &f{value}&7.'
        - ''
        - '&aClique para alterar'
]]>
</code-block>
</chapter>

<chapter title="encantamentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Apague apenas os encantamentos que não for usar
Encantamentos:
  Eficiencia: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: DIAMOND_PICKAXE
        Data: 0
        Name: '&aEficiencia'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: DIAMOND_PICKAXE
        Data: 0
        Name: '&aEficiencia'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: DIAMOND_PICKAXE
        Data: 0
        Name: '&aEficiencia'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7minere com mais agilidade.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Eficiência'
    # Nível da picareta necessário para poder evoluir o encantamento
    NivelPicareta: 0
    # Ordem do ícone no menu
    Ordem: 1
    # Aparecer no menu de evolução
    MostrarMenu: true
    # Poder evoluir pagando no menu de evolução
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Fortuna: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aFortuna'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aFortuna'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aFortuna'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Fortuna'
    NivelPicareta: 0
    Ordem: 2
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Nuclear: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        ID: AIR
        Data: 0
        Name: '&aNuclear'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        ID: AIR
        Data: 0
        Name: '&aNuclear'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: '7faf3efbff6d7ef465ecacbc517f4dad5cc1a2261ea7a609f216aae48784'
        ID: AIR
        Data: 0
        Name: '&aNuclear'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a mina inteira.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Nuclear'
    NivelPicareta: 0
    Ordem: 2
    Animacao: true
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.00015 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
    Mensagens:
      Title: '&cNuclear<nl>&cativado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
  Destruidor: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        ID: AIR
        Data: 0
        Name: '&aDestruidor'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de blocos.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        ID: AIR
        Data: 0
        Name: '&aDestruidor'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de blocos.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: '8da332abde333a15a6c6fcfeca83f0159ea94b68e8f274bafc04892b6dbfc'
        ID: AIR
        Data: 0
        Name: '&aDestruidor'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar a camada inteira.'
          - '&7de blocos.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Destruidor'
    NivelPicareta: 0
    Ordem: 3
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Animacao: true
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.0015 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
    Mensagens:
      Title: '&cDestruidor<nl>&cativado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
  Sumonador: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: NETHER_STAR
        Data: 0
        Name: '&aSumonador'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de transformar um bloco.'
          - '&7em LuckyBlock ao quebrá-lo.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: NETHER_STAR
        Data: 0
        Name: '&aSumonador'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de transformar um bloco.'
          - '&7em LuckyBlock ao quebrá-lo.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: NETHER_STAR
        Data: 0
        Name: '&aSumonador'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de transformar um bloco.'
          - '&7em LuckyBlock ao quebrá-lo.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Sumonador'
    NivelPicareta: 0
    Ordem: 4
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.01 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Velocidade: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: FEATHER
        Data: 0
        Name: '&aVelocidade'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: FEATHER
        Data: 0
        Name: '&aVelocidade'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: FEATHER
        Data: 0
        Name: '&aVelocidade'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de velocidade na mina.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Velocidade'
    NivelPicareta: 0
    Ordem: 5
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 1.0 # Use -1 para ser infinito
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Pressa: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        ID: AIR
        Data: 0
        Name: '&aPressa'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        ID: AIR
        Data: 0
        Name: '&aPressa'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: 'ae77ae4f3652f671203cf45ff3c7f7e6328e921c374a7a311b3e48444fd892'
        ID: AIR
        Data: 0
        Name: '&aPressa'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha o efeito de pressa na mina.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Pressa'
    NivelPicareta: 0
    Ordem: 6
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 1.0 # Use -1 para ser infinito
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Sortudo: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        ID: AIR
        Data: 0
        Name: '&aSortudo'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte ao quebrar uma LuckyBlock.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        ID: AIR
        Data: 0
        Name: '&aSortudo'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte ao quebrar uma LuckyBlock.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
        ID: AIR
        Data: 0
        Name: '&aSortudo'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha mais sorte ao quebrar uma LuckyBlock.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Sortudo'
    NivelPicareta: 0
    Ordem: 7
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.01 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Explosao: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        ID: AIR
        Data: 0
        Name: '&aExplosao'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        ID: AIR
        Data: 0
        Name: '&aExplosao'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: '713b78b520781b5970c4e117274e9363e66721efd7bbe1959e266b98e37759ce'
        ID: AIR
        Data: 0
        Name: '&aExplosao'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um buraco.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Explosao'
    NivelPicareta: 0
    Ordem: 8
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Animacao: true
    Raio: 2
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.01 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
    Mensagens:
      Title: '&cExplosão<nl>&cativada' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
  Laser: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        ID: AIR
        Data: 0
        Name: '&aLaser'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        ID: AIR
        Data: 0
        Name: '&aLaser'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: 'f073d84d6fda6a3404e77ad8d0f190893ae66d195fbb44d3c4607a6b71d9b9d5'
        ID: AIR
        Data: 0
        Name: '&aLaser'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de quebrar um +.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Laser'
    NivelPicareta: 0
    Ordem: 9
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Animacao: true
    Raio: -1 # em blocos para cada lado (4 lados) -1 = tamanho da mina
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.01 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
    Mensagens:
      Title: '&cLaser<nl>&cativado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
  Furadeira: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        ID: AIR
        Data: 0
        Name: '&aFuradeira'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        ID: AIR
        Data: 0
        Name: '&aFuradeira'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: 'b59a2e83f20260e9caac53b4b3a6566b92d7dda3c42313363fa25443052b93d'
        ID: AIR
        Data: 0
        Name: '&aFuradeira'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7tenha chances de varar a mina a partir'
          - '&7do bloco que você quebrou.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Furadeira'
    NivelPicareta: 0
    Ordem: 10
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Animacao: true
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.01 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
    Mensagens:
      Title: '&cFuradeira<nl>&cativado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
  Multiplicador: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        ID: AIR
        Data: 0
        Name: '&aMultiplicador'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Multiplicador Atual: &b{multiplicador}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        ID: AIR
        Data: 0
        Name: '&aMultiplicador'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
        ID: AIR
        Data: 0
        Name: '&aMultiplicador'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais blocos ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Multiplicador'
    NivelPicareta: 0
    Ordem: 11
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Multiplicador: 0.01 # multiplicador adquirido por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
  Eletricidade: # Não mude este nome, ou o encantamento não será reconhecido
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: true
        URL: '9ac52419b99025828c89fa825945e6948e45bb5a22e4425a59e9096e4c1ac38'
        ID: AIR
        Data: 0
        Name: '&aEletricidade'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais energia ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir 1x'
          - '&aBotão &fdireito &apara escolher a quantia de evolução'
          - '&aBotão &fQ &apara evoluir o possível'
      NaoPode: # quando não puder evoluir
        CustomSkull: true
        URL: '9ac52419b99025828c89fa825945e6948e45bb5a22e4425a59e9096e4c1ac38'
        ID: AIR
        Data: 0
        Name: '&aEletricidade'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7ganhe mais energia ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{blocos} blocos&f.'
          - '&f > Nível necessário: &a{nivel}&f.'
          - ''
          - '&cVocê não tem blocos ou nível suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: true
        URL: '9ac52419b99025828c89fa825945e6948e45bb5a22e4425a59e9096e4c1ac38'
        ID: AIR
        Data: 0
        Name: '&aEletricidade'
        Lore:
          - '&7Este encantamento permite que você'
          - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
          - '&7ganhe mais energia ao minerar.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - ''
          - '&cVocê já está no máximo.'
    Nome: 'Eletricidade'
    NivelPicareta: 0
    Ordem: 12
    MostrarMenu: true
    PodeComprar: true
    # Mostrar um ícone de infinito no lugar do nível
    # do encantamento na lore
    MostrarInfinito: false
    Nivel:
      Padrao: 0.0
      Maximo: 10.0 # Use -1 para ser infinito
      Porcentagem: 0.01 # porcentagem adquirida por nível
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
      Multiplicador: 1.00
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-Desencantador:
      price1:
        provider: 'money'
        price: 9000.0
      price2:
        provider: 'yminas'
        price: 100.0
]]>
</code-block>
</chapter>

<chapter title="ferramentas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Itens que poderão ser usados no lugar na Pickaxe default
Ferramentas:
  Spade:
    CustomSkull: false
    URL: ''
    ID: DIAMOND_SPADE
    Data: 0
    Name: '&bPá &6[{blocos_quebrados}]'
    Lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{nivel}'
      - ' &fEnergia: &7{energia}/{energia_proximo} &f({progressbar}&f)'
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
  no-balance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  mine-exists: '&cEssa mina já existe.'
  mine-found: |
    &cEssa mina não existe.
    &cDisponiveis: {minas}
  mine-created: '&aMina &f{mina}&a criada com sucesso.'
  mine-deleted: '&aMina &f{mina}&a deletada com sucesso.'
  mine-admin-help: |
    &cComandos disponíveis:
    &c> /minaadmin criar <mina>
    &c> /minaadmin editar <mina>
    &c> /minaadmin resetar <mina>
    &c> /minaadmin resetarpicareta <player>
    &c> /minaadmin darnivel <player> <quantia>
    &c> /minaadmin removernivel <player> <quantia>
    &c> /minaadmin darenergia <player> <quantia>
    &c> /minaadmin removerenergia <player> <quantia>
    &c> /minaadmin lista
    &c> /minaadmin setsaida
    &c> /minaadmin reload
  change-name: '&aVocê alterou o nome da arena mina &e{nome}&a.'
  change-time: '&aVocê alterou o tempo de reset da mina para &e{tempo} segundos&a.'
  change-percentage: '&aVocê alterou a porcentagem de reset da mina para &e{porcentagem}%&a.'
  change-chance: '&aVocê alterou a chance para {chance}.'
  change-price: '&aVocê alterou o preço para {preco}.'
  change-xp: '&aVocê alterou o xp para {xp}.'
  change-mcmmo: '&aVocê alterou o xp do mcMMO para {xp}.'
  change-priority: '&aVocê alterou a prioridade para {prioridade}.'
  change-order: '&aVocê alterou a ordem para {ordem}.'
  change-level: '&aVocê alterou o nível para {nivel}.'
  change-permission: '&aVocê alterou a permissao para {permissao}.'
  change-server: '&aVocê alterou o servidor para {server}.'
  change-icon: '&aÍcone alterado com sucesso.'
  item-no: '&cO item não pode ser nulo.'
  local-set: '&aLocal definido com sucesso.'
  local-deleted: '&aLocal deletado com sucesso.'
  local-not-set: '&cO local não foi definido ainda.'
  teleported: '&aTeleportado para a mina com sucesso.'
  pos1-set: '&aPosição 1 da mina &f{mina}&a setada.'
  pos2-set: '&aPosição 2 da mina &f{mina}&a setada.'
  chance: '&cA chance não pode ser maior que 100 nem menor que 0.'
  block: '&cVocê deve inserir um bloco.'
  block-already: '&cEsta mina já possui este bloco.'
  block-add: '&aBloco adicionado com sucesso.'
  invalid-percentage: '&cA porcentagem deve ser maior que 0% e menor que 100%.'
  reward-added: '&aRecompensa adicionada com sucesso.'
  none: '&cNenhuma mina foi encontrada disponível para você.'
  spawn: '&cO spawn da mina &f{mina}&c não foi setado.'
  exit: '&cA saída das minas não foi setada.'
  exit-set: '&aA saída das minas foi setada com sucesso.'
  slot-empty: '&cO slot {slot} deve estar vazio para poder receber a picareta. Por favor, re-entre na mina.'
  inv-full: '&cSeu inventário está cheio!'
  not-in: '&cVocê não está em uma mina.'
  command: '&cVocê não pode usar este comando na mina. Utilize /mina para sair dela.'
  evolved: '&aO encantamento &f{encantamento}&a foi evoluido para o nível &f{nivel}&a.'
  mine-permission: '&cVocê não tem permissão para ir até a mina {mina}.'
  mine-level: '&cSua picareta não tem nível suficiente para ir até a mina {mina}.'
  exceeds: '&cEstes níveis excedem o nível máximo do encantamento.'
  has: '&cVocê não possui a quantia de &f{blocos}&c blocos.'
  has-level: '&cVocê não possui a quantia de &f{nivel}&c níveis necessários.'
  already-in: '&cVocê já está em uma mina. Utilize /mina para sair dela.'
  blocks: '&bVocê possui &f{blocos} blocos&b.'
  blocks-player: '&bO jogador &f{player}&b possui &f{blocos} blocos&b.'
  blocks-added: '&bVocê adicionou &f{blocos} blocos&b ao jogador &f{player}&b.'
  blocks-removed: '&bVocê removeu &f{blocos} blocos&b do jogador &f{player}&b.'
  blocks-set: '&bVocê setou &f{blocos} blocos&b para o jogador &f{player}&b.'
  blocks-give: '&bVocê deu &f{blocos} &bblocos para o jogador &f{player}&b.'
  blocks-converted: '&bVocê compactou todos seus blocos em 1.'
  blocks-activated: '&bVocê ativou &f{blocos} blocos&b.'
  blocks-sent: '&bVocê enviou &f{blocos} blocos&b para o jogador &f{player}&b.'
  blocks-received: '&bVocê recebeu &f{blocos} blocos&b do jogador &f{player}&b.'
  yourself: '&cVocê não pode realizar esta ação à si mesmo.'
  reset-mine: '&aVocê resetou a mina &f{mina}&a.'
  reset-tool: '&aVocê resetou a picareta do jogador &f{player}&a.'
  give-level: '&aVocê deu &f{nivel}&a níveis para o jogador &f{player}&a.'
  removed-level: '&aVocê removeu &f{nivel}&a níveis do jogador &f{player}&a.'
  give-energy: '&aVocê deu &f{energia}&a em energia para o jogador &f{player}&a.'
  removed-energy: '&aVocê removeu &f{energia}&a de energia do jogador &f{player}&a.'
  clear: '&cVocê deve esvaziar seu inventário.'
  classe-bought: '&aVocê evoluiu para a classe &7{classe}&a.'
  classe-permission: '&cVocê não tem permissão para evoluir para esta classe.'
  classe-previous: '&cVocê deve possuir a classe anterior primeiro.'
  classe-reset: '&aVocê resetou a classe do jogador &f{player}&a.'
  classe-set: '&aVocê definiu a classe {classe} ao jogador &f{player}&a.'
  classe-found: '&aEsta classe não existe. Disponíveis: {classes}'
  added-all: '&bVocê adicionou &f{blocos} blocos&b para todos os jogadores online.'
  give-all: '&bO usuário &f{player}&b deu &f{blocos} &bblocos para todos os jogadores online&b.'
  bomb-shift: '&cVocê não pode usar shift no arsenal.'
  bomb-numkeys: '&cVocê não pode usar as teclas numéricas no arsenal.'
  bomb-creative: '&cVocê não pode usar clicar no arsenal estando no criativo.'
  bomb-blocked: '&cVocê pode colocar apenas bombas no arsenal.'
  cant-buy: '&cVocê não pode comprar esse encantamento.'
  wait: '&aVocê será teletransportado em {quantia} segundos... Não se mova.'
  desenchanted: '&aVocê desencantou &f{level} níveis &ado encantamento &f{enchant}&a.'
  skin-found: '&cEsta skin não existe. Disponíveis: &7{list}'
  skin-give: '&bVocê deu uma skin para o jogador &f{player}&b.'
  skin-has: '&aVocê já possui esta skin ativada.'
  skin-activated: '&aSkin ativada com sucesso.'
  skin-no-has: '&cA ferramenta não possui essa skin.'
  skin-removed: '&aSkin removida com sucesso.'
  skin-has-player: '&aO jogador já possui esta skin.'
  digit-name: |

    &aDigite o nome para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-time: |

    &aDigite o tempo (em seg) para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-percentage: |

    &aDigite a porcentagem para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-chance: |

    &aDigite a chance para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-price: |

    &aDigite o preço para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-xp: |

    &aDigite o xp para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-mcmmo: |

    &aDigite o xp do mcMMO para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-priority: |

    &aDigite a prioridade para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-order: |

    &aDigite a ordem para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-level: |

    &aDigite o nivel para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-permission: |

    &aDigite a permissão para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-server: |

    &aDigite o servidor para qual deseja alterar.
    &7para cancelar digite &ncancelar&7.

  digit-enchant: |

    &aDigite a quantia de níveis que você quer adquirir ao encantamento &f{encantamento}&a.
    &7para cancelar digite &ncancelar&7.

  blocks-help: |

    &a/blocos &8- &7Ver os seus blocos.
    &a/blocos <player> &8- &7Ver os blocos de alguém.
    &a/blocos enviar <player> <quantia> &8- &7Envia seus blocos para alguém.
    &a/blocos add <player> <quantia> &8- &7Adiciona blocos a alguém.
    &a/blocos give <player> <quantia> &8- &7Dá blocos em forma de item a alguém.
    &a/blocos set <player> <quantia> &8- &7Remove blocos de alguém.
    &a/blocos remove <player> <quantia> &8- &7Seta blocos a alguém.

  mine-help: |

    &a/mina &8- &7Abre o menu principal.
    &a/mina ir &8- &7Vai até a sua maior mina.
    &a/mina ir <mina> &8- &7Vai até uma mina específica.
    &a/mina sair &8- &7Sai da mina.
    &a/mina lista &8- &7Abre o menu de minas.
    &a/mina bombas &8- &7Abre o menu do arsenal.
    &a/mina skins &8- &7Abre o menu de skins.
    &a/mina classes &8- &7Abre o menu de classes.
    &a/mina evoluir &8- &7Abre o menu de evolução.

  booster-give: '&aVocê deu &7{amount}x Booster(s)&a para o jogador &7{player}&a.'
  booster-received: '&aVocê recebeu &7{amount}x Booster(s)&a.'
  booster-list: |
    &cBooster não encontrado.
    &cBooster disponíveis: &f{list}
  booster-finished: '&cSeu booster de mineração acabou.'
  booster-already: '&cVocê já está usando um booster.'
  booster-activated: '&aVocê ativou um booster de mineração. Multiplicador: &e{bonus}% coins &ae &e{bonus-block}% blocos&a. Tempo: &e{time}&a.'
  mine-maintenance: '&cEsta mina {mina} &cestá em manutenção.'
  mine-maintenance-on: '&aA mina {mina} &aestá agora em manutenção.'
  mine-maintenance-off: '&cA mina {mina} &cnão está mais em manutenção.'
  mine-kick-all: '&aVocê expulsou todos os jogadores das minas.'
]]>
</code-block>
</chapter>

<chapter title="mina_recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  reco1:
    Mina: 'sim'
    Chance: 20.0
    Recompensa: 'Reco1'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá no preview.
    Preview:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: '&a+100 Blocos'
      Amount: 64
      Lore:
        - '&aVocê irá ganhar blocos de mineração!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será dado o item se os comandos estiverem em false.
    # Item que será dado ao jogador.
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: ''
      Amount: 1
      Lore: []
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Mensagens que serão enviadas ao receber a recompensa
    Mensagens:
      Title: '&a+100 Blocos' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: []
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: true
      List:
        - 'blocos add {player} 100'
  Reco2:
    Preview:
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&6+10 Cash'
      Amount: 64
      Lore:
        - '&6Você irá ganhar cash!'
      Enchants:
        - ''
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Name: ''
      Amount: 1
      Lore: []
      Enchants:
        - ''
    Mensagens:
      Title: '' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat:
        - '&e&lLuckyBlock: &fVocê encontrou &610 cash&f.'
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: true
      List:
        - 'points add {player} 10'

]]>
</code-block>
</chapter>

<chapter title="scoreboard.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Ativar: true
Title: '&b&lyStore'
Linhas:
  - '&7     Área de mineração'
  - ''
  - '&f Mina: &7{mina}'
  - '&f B. quebrados: &7{blocos_quebrados}'
  - ''
  - '&e Picareta'
  - '&8  ❘&f Nível: &7{nivel}'
  - '&8  ❘&f Energia: &7{energia}/{energia_proximo}'
  - ''
  - '&f Blocos: &e⛃{blocos}'
  - '&f Coins: &2$&a{money}'
  - '&f Cash: &6✪%playerpoints_points%'
  - ''
  - '&b    ystoreplugins.com.br'
]]>
</code-block>
</chapter>

<chapter title="skins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Skins:
  stone:
    order: 1
    type: 'STONE'
    custom-model-data: 1
    item:
      material: 'STONE'
      name: '&aSkin de Pedra'
      lore: ['&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&aClique para ativar']
    buy:
      enabled: true
      message: '&aVocê comprou a skin &&Pedra&a por &f{money}&a.'
      prices:
        price1:
          provider: 'money'
          amount: 100.0
    menu:
      equip:
        material: 'STONE'
        name: '&aSkin de Pedra'
        lore: [ '&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&aClique para equipar' ]
      equipped:
        material: 'STONE'
        name: '&aSkin de Pedra'
        lore: [ '&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&aJá está equipada' ]
      has:
        material: 'STONE'
        name: '&aSkin de Pedra'
        lore: [ '&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', ' &fPreço: &2$ &a{money} coins', '', '&aClique para comprar.' ]
    name: '&fPicareta de Pedra &6[{blocos_quebrados}]'
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - ' &fNível: &7{nivel}'
      - ' &fEnergia: &7{energia}/{energia_proximo} &f({progressbar}&f)'
      - ''
      - '&a+10% ( PEDRA )'
      - ''
    bonus: 10.0
    bonus-blocks: 10.0
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static MinaAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;MinaAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(MinaAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/85-yMinas">Site do plugin yMinas</a>
    </category>
</seealso>