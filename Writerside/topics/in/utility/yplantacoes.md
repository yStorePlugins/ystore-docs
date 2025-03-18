# yPlantacoes
<secondary-label ref="utility"/>

### Descrição
Colha e replante automaticamente com chances de recompensas

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
<video src="//www.youtube.com/watch?v=L4xT_CWRY7k"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/farm - Abre o menu principal
/farm moedas - Vê suas moedas
/farm [player] - Vê as moedas de outro jogador
/farm enviar - Envia suas moedas para outro jogador
/farm ir - Ir para a área de farm
/farm darenxada - Dá enxada para um jogador
/farm add - Adicionada moedas para um jogador
/farm set - Seta moedas para um jogador
/farm remove - Remove moedas de um jogador
/farm setspawn - Seta o local de spawn da área de farm
/farm reload - Recarregar as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yplantacoes.usar - Permissão para o /farm e /farm moedas
yplantacoes.look - Permissão para o /farm [player]
yplantacoes.send - Permissão para o /farm enviar
yplantacoes.go - Permissão para o /farm ir
yplantacoes.givehoe - Permissão para o /farm givehoe
yplantacoes.add - Permissão para o /farm add
yplantacoes.remove - Permissão para o /farm remove
yplantacoes.set - Permissão para o /farm set
yplantacoes.setspawn - Permissão para o /farm setspawn
yplantacoes.help - Permissão para o /farm help
yplantacoes.reload - Permissão para o /farm reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yplantacoes_moedas% - Retorna os moedas do jogador formatado.
%yplantacoes_moedas_raw% - Retorna os moedas do jogador sem formatação.
%yplantacoes_time% - Retorna o tempo do jogador na farm.
%yplantacoes_time_raw% - Retorna o tempo do jogador na farm sem formatar.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPlantacoes/
    ├── addons/
    │    └── enchants.yml
    ├── menus/
    │    ├── evoluir.yml
    │    ├── ferramentas.yml
    │    ├── principal.yml
    │    ├── recompensas.yml
    │    ├── skins.yml
    │    └── top.yml
    ├── private/
    │    └── armors.yml
    ├── bonus.yml
    ├── config.yml
    ├── custom_encantamentos.yml
    ├── data.yml
    ├── economies.yml
    ├── encantamentos.yml
    ├── flowEnchants.yml
    ├── plantacoes.yml
    ├── recompensas.yml
    └── skins.yml
</code-block>
</chapter>

<chapter title="addons" collapsible="true">
<chapter title="enchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
linear:
  Ordem: 5
  Display: 'Linear'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aLinear<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

explosive:
  Ordem: 5
  Display: 'Explosão'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

laser:
  Ordem: 5
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&alaser<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

boomerang:
  Ordem: 5
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="evoluir.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Enxada - Evoluir'
Tamanho: 36
Slots: [11, 13, 15]
BackSlot: 27
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a enxada do jogador
EnxadaSlot: 29
# Item para ver adicionar mais blocos
Perfil:
  Slot: 31
  CustomSkull: true
  URL: '{player}'
  ID: AIR
  Data: 0
  Glow: true
  Name: '&a{player}'
  Lore:
    - ''
    - '&fMoedas: &b{moedas}'
    - ''
# Item para trocar a ferramenta
Ferramenta:
  Slot: 33
  CustomSkull: false
  URL: ''
  ID: DIAMOND_HOE
  Data: 0
  Glow: true
  Name: '&aFerramenta'
  Lore:
    - '&aClique para gerenciar a ferramenta'
Skin:
  Slot: 35
  material: '731f3279fc112b7f18bd0a2229934fcb5605c62823ce698b8b503ecccf0a3ac4'
  name: '&aSkins'
  lore:
    - '&7Configure a skin da sua ferramenta'
    - '&7e ganhe alguns bônus.'
    - ''
    - '&aClique para acessar'
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="ferramentas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Enxada - Ferramenta'
Tamanho: 36
Slots: [11, 13, 15]
BackSlot: 31
AnteriorSlot: 18
ProximoSlot: 26
Ferramentas:
  enxada:
    type: 'DIAMOND_HOE'
    material: 'DIAMOND_HOE'
    name: '&bMachado de Diamante'
    lore:
      - ''
      - '&eTroque sua ferramenta por uma'
      - '&ebelíssima enxada de diamante.'
      - ''
      - '&aClique para trocar.'
  machado:
    type: 'DIAMOND_AXE'
    material: 'DIAMOND_AXE'
    name: '&bMachado de Diamante'
    lore:
      - ''
      - '&eTroque sua ferramenta por um'
      - '&ebelíssimo machado de diamante.'
      - ''
      - '&aClique para trocar.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Sair:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Plantação'
Tamanho: 27
Itens:
  Encantamentos:
    Slot: 11
    CustomSkull: true
    URL: 'b2f79016cad84d1ae21609c4813782598e387961be13c15682752f126dce7a'
    ID: AIR
    Data: 0
    Name: '&aEncantamentos'
    Lore:
      - '&7Gerencie os encantamentos da'
      - '&7sua enxada.'
      - ''
      - '&aClique para acessar.'
  Top:
    Slot: 12
    ID: BOOK_AND_QUILL
    Name: '&aTop'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacaram ao plantar.'
      - ''
      - '&aClique para visualizar.'
  Recompensas:
    Slot: 13
    ID: CHEST
    Name: '&aRecompensas'
    Lore:
      - '&7Veja as recompensas que'
      - '&7você conseguiu na farm.'
      - ''
      - '&aClique para visualizar.'
  Enxada:
    Slot: 15
    ID: DIAMOND_HOE
    Name: '&aEnxada'
    Lore:
      - '&7Compre sua enxada e começe a farmar'
      - '&7para ganhar bastante dinheiro!'
      - ''
      - '&fValor: &a100 coins&f.'
      - ''
      - '&aClique para comprar.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Sair:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&8Plantacoes'
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
]]>
</code-block>
</chapter>

<chapter title="skins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Ferramenta - Skins'
Tamanho: 36
Slots: [11, 12, 13, 14, 15]
BackSlot: 29
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a picareta do jogador
FerramentaSlot: 31
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Plantação'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17
# Item do top Moedas
Item moedas:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fMoedas: &7{moedas}'
    - '&fPosição: &e{pos}º'
    - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="private" collapsible="true">
<chapter title="armors.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Armor encontrado: '&cEsta armadura não existe. Disponíveis: &7{list}'
Deu armor: '&bVocê deu uma armadura para o jogador &f{player}&b.'

Armors:
  basic:
    item:
      material: 'DIAMOND_HELMET'
      name: '&aCapacete Básico'
      lore: ['&7Você é pobre.', '', '&fBônus: &a10% (todos)']
    bonus-crops: 10.0
    bonus-coin: 10.0
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
    Permissao: 'yplantacoes.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
    BonusMoeda: 10.0
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

# Comandos e aliases do plugin
Comando:
  Farm:
    Comando: 'farm'
    Aliases: [ ]

# Opções gerais do plugin
Opcoes:
  # Pode conflitar com plugins de armazém
  AutoPickup: false
  # Subcomando de moedas
  Moedas subcomandos: ['moeda', 'moedas']
  # Mundos blacklistados
  MundoBlacklist:
    - 'nenhum'
  # Ao quebrar com uma enxada no shift não executar o evento do plugin
  ShiftEnxadaBypass: true
  # Ao quebrar no modo criativo não executar o evento do plugin
  CriativoBypass: true
  # Fazer com que a Enxada nunca quebre
  EnxadaUnbreakable: true
  # Valor da enxada no menu principal
  EnxadaValor: 100.0
  # Quebrar as plantações apenas com a enxada custom
  QuebrarSoCustom: false
  # Abrir menu de evolução ao interagir com a enxada (Shift+Botão direito)
  InteragirMenu: true
  # Somar um nível a mais na evolução
  # Padrão: true (versões anteriores)
  SomarEvolute: true
  # Máximo permitido para evoluir com Q
  QMax: 0
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Enviar recompensas para o menu de recompensas
  RecompensasMenu: true
  # Skill do herbalismo no seu mcMMO/AuraSkills
  Herbalismo: 'HERBALISM'
  # Formatador de mensagens
  Formatador:
    Bonus tem: '&a+{bonus}% por ser {display}&a.'
    Bonus nao tem: ''
  # Materiais que irão ser reconhecidos na skin
  Skin-materiais:
    - 'WOOD'
    - 'STONE'
    - 'IRON'
    - 'GOLD'
    - 'DIAMOND'
  # Item da enxada
  Enxada:
    CustomSkull: false
    URL: ''
    ID: DIAMOND_HOE
    Data: 0
    Name: '&bEnxada de farm'
    Lore:
      - '&7Inquebrável ∞'
      - '{enchants}'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Segurando: '&cVocê deve estar segurando sua enxada.'
  Evoluido: '&aO encantamento &f{encantamento}&a foi evoluido para o nível &f{nivel}&a.'
  Numero: '&cO argumento não é um número.'
  Jogador: '&cEste jogador não foi encontrado.'
  SiMesmo: '&cVocê não pode realizar esta ação à si mesmo.'
  Moedas: '&bVocê possui &f{moedas} moedas&b.'
  Moedas player: '&bO jogador &f{player}&b possui &f{moedas} moedas&b.'
  Adicionou: '&bVocê adicionou &f{moedas} moedas&b ao jogador &f{player}&b.'
  Removeu: '&bVocê removeu &f{moedas} moedas&b do jogador &f{player}&b.'
  Setou: '&bVocê setou &f{moedas} moedas&b para o jogador &f{player}&b.'
  Enviou: '&bVocê enviou &f{moedas} moedas&b para o jogador &f{player}&b.'
  Recebeu: '&bVocê recebeu &f{moedas} moedas&b do jogador &f{player}&b.'
  Possui: '&cVocê não possui a quantia de &f{moedas}&c moedas.'
  Deu: '&bVocê deu uma enxada para o jogador &f{player}&b.'
  Custo: '&cVocê não possui 100 coins.'
  Comprou: '&aVocê comprou uma enxada por 100 coins.'
  PermPlanta: '&cVocê não possui a permissão deste tipo de planta.'
  Enxada: '&cVocê deve quebrar esta plantação com uma enxada de farm.'
  Aguarde: '&cVocê precisa aguardar {time} para quebrar essa plantação novamente.'
  Cancelou: '&cOperação cancelada.'
  Excede: '&cEstes níveis excedem o nível máximo do encantamento.'
  Skin encontrada: '&cEsta skin não existe. Disponíveis: &7{list}'
  Deu skin: '&bVocê deu uma skin para o jogador &f{player}&b.'
  Skin possui: '&aA ferramenta já possui esta skin ativada.'
  Skin ativou: '&aSkin ativada com sucesso.'
  Skin nao possui: '&cA ferramenta não possui essa skin.'
  Skin removida: '&aSkin removida com sucesso.'
  Ja tem: '&cVocê já possui uma enxada no inventário.'
  NoBalance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  Digite encantamento:
    - ''
    - '&aDigite a quantia de níveis que você quer adquirir ao encantamento &f{encantamento}&a.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Farm help:
    - ''
    - '&a/farm &8- &7Abre o menu principal.'
    - '&a/farm moedas &8- &7Vê as suas moedas.'
    - '&a/farm <player> &8- &7Ver as moedas de alguém.'
    - '&a/farm enviar <player> <quantia> &8- &7Envia suas moedas para alguém.'
    - '&a/farm darenxada <player> &8- &7Dá enxada para um jogador.'
    - '&a/farm add <player> <quantia> &8- &7Adiciona moedas a alguém.'
    - '&a/farm set <player> <quantia> &8- &7Remove moedas de alguém.'
    - '&a/farm remove <player> <quantia> &8- &7Seta moedas a alguém.'
    - ''
  Reward-collected: '&eItem recolhido com sucesso.'
  Reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'

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
]]>
</code-block>
</chapter>

<chapter title="custom_encantamentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Encantamentos:
  Chaveiro:
    Ordem: 5
    Display: 'Chaveiro'
    Padrao: 0
    Maximo: -1
    BonusPorLevel: 10.0 # em porcentagem
    ChancePorLevel: 10.0 # em porcentagem
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    # Aparecer no menu de evolução
    MostrarMenu: true
    # chance,comando
    Comandos:
      - '20,give {player} quartz 1'
    # Economias que irá dár por nível ao executar o enchant
    Give-PerLevel:
      price1:
        provider: 'money'
        amount: 1.0
    Mensagens:
      Title: '&aChave<nl>&eencontrado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Bônus atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} moedas&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} moedas&f.'
          - ''
          - '&cVocê não tem moedas suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="data.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Não altere nada nesta config.
Data: {}
Locais: {}
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
    permission: 'ycampo.provider.money'
]]>
</code-block>
</chapter>

<chapter title="encantamentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Velocidade ao quebrar
Eficiencia:
  # Ordem do enchant no menu
  Ordem: 1
  Display: 'Eficiência'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: FEATHER
      Data: 0
      Name: '&aEficiência'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre mais rápido.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: FEATHER
      Data: 0
      Name: '&aEficiência'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre mais rápido.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: FEATHER
      Data: 0
      Name: '&aEficiência'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre mais rápido.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - ''
        - '&cVocê já está no máximo.'

# Bônus de drop
Fortuna:
  # Ordem do enchant no menu
  Ordem: 2
  Display: 'Bônus'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'

# Aumenta chance nas recompensas
Sortudo:
  Ordem: 3
  Display: 'Sortudo'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: true
      URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      ID: AIR
      Data: 0
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: true
      URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      ID: AIR
      Data: 0
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
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
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'

# Ganhar mais moedas de farm
Multiplicador:
  Ordem: 4
  Display: 'Multiplicador'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: true
      URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      ID: AIR
      Data: 0
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Multiplicador Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: true
      URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      ID: AIR
      Data: 0
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
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
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="flowEnchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
linear:
  Ordem: 5
  Display: 'Linear'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aLinear<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

explosive:
  Ordem: 5
  Display: 'Explosão'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

laser:
  Ordem: 5
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&alaser<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

boomerang:
  Ordem: 5
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="plantacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
## ESTE PLUGIN NÃO É COMPATÍVEL COM PLANTAÇÕES DIFERENTES DE CROPS E FUNGOS, OU SEJA,
## NÃO RECOMENDAMOS O USO COM CACTO, CANA DE AÇÚCAR, BAMBU E DERIVADOS QUE CRESCEM EM BLOCOS PARA CIMA

Plantacoes:
  fungo:
    # Tipo da plantação
    Plantacao: 'NETHER_WARTS'
    # Configurações do replante
    Replantar:
      Ativar: true
      # Replantar apenas se ter a planta no inventário
      ApenasTer: true
      # Planta que precisará ter no inventário para replantar
      Planta: 'NETHER_STALK'
    # Quebrar apenas se estiver crescido
    QuebrarCrescido: true
    # Estágio máximo que a planta pode chegar (fungos = 3; os outros crops normalmente são 7)
    NivelMaximo: 3
    # Delay para quebrar o mesmo bloco novamente
    # em segundos
    FarmDelay: 0
    # Bônus por cada nível de fortuna (enchant default)
    # Ex: 1.0 de bônus por nível = nivel*bonus (10 niveis * 1 = 10% a mais)
    FortunaBonus: 1.0
    # Permissão para quebrar este tipo de plantação
    # Deixe '' (vazio) para não usar
    Permissao: 'yplantacoes.fungo'
    # XP que será dado ao jogador
    XP:
      Vanilla: 1.0
      Mcmmo: 1.0 # skill HERBALISM
    # Configuração do drop
    Drops:
      membro:
        Ordem: 1
        Drop:
          material: 'NETHER_STALK'
        Permissao: 'yplantacoes.fungo.membro'
        Minimo: 10
        Maximo: 15
        Title: ''
        Actionbar: '&aVocê recebeu &e{quantia} fungos&a e &e{moedas} moedas&a.'
        Chat: ''
        # Moedas que serão ganhas
        Moedas:
          Min: 1
          Max: 5
        # Sistema de auto-sell do drop
        AutoSell:
          Ativar: false
          DarMoney: true
          BasePrice: 100.0 # preço por drop (para o comando)
          Currencies:
            preco1:
              Provider: 'money'
              Amount: 100.0
          Mensagem:
            Actionbar: '&aVocê vendeu &fx{quantia} Fungos&a por &6{money}&a e &e{moedas} moedas&a.'
            Chat: '&aVocê vendeu &fx{quantia} Fungos&a por &6{money}&a e &e{moedas} moedas&a.'
          # O Drop vai executar um comando ao ser vendido?
          Comando:
            Ativar: false
            UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
            MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
            InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
            Comandos:
              - 'give {player} NETHER_STALK {quantia}'
    # Configuração das recompensas
    # recompensa (recompensas.yml),chance
    Recompensas:
      - 'Reco1,50.0'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá para coletar.
    Collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Só será dado o item se os comandos estiverem em false.
    # Item que será dado ao jogador.
    Item:
      material: STONE
      name: ''
      amount: 1
      lore: []
    # Mensagens que serão enviadas ao receber a recompensa
    Mensagens:
      Title: '&a+100 coins' # deixe '' para não usar
      Actionbar: '&a+100 coins' # deixe '' para não usar
      Chat: |
        &a+100 coins
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: true
      # quantia padrão da placeholder {amount} no comando (valor base)
      Placeholder-amount: 100
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      Multiply-placeholder: true
      List:
        - 'money add {player} {amount}'

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
    custom-model-data: 0
    item:
      material: 'STONE'
      name: '&aSkin de Pedra'
      lore: ['&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&aClique na ferramenta para ativar']
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
        lore: [ '&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&cVocê não possui esta skin' ]
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - '&a+10% ( PEDRA )'
      - ''
    bonus: 10.0
]]>
</code-block>
</chapter>

</chapter>
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Sair:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Plantação'
Tamanho: 27
Itens:
  Encantamentos:
    Slot: 11
    CustomSkull: true
    URL: 'b2f79016cad84d1ae21609c4813782598e387961be13c15682752f126dce7a'
    ID: AIR
    Data: 0
    Name: '&aEncantamentos'
    Lore:
      - '&7Gerencie os encantamentos da'
      - '&7sua enxada.'
      - ''
      - '&aClique para acessar.'
  Top:
    Slot: 12
    ID: BOOK_AND_QUILL
    Name: '&aTop'
    Lore:
      - '&7Veja os jogadores que'
      - '&7se destacaram ao plantar.'
      - ''
      - '&aClique para visualizar.'
  Recompensas:
    Slot: 13
    ID: CHEST
    Name: '&aRecompensas'
    Lore:
      - '&7Veja as recompensas que'
      - '&7você conseguiu na farm.'
      - ''
      - '&aClique para visualizar.'
  Enxada:
    Slot: 15
    ID: DIAMOND_HOE
    Name: '&aEnxada'
    Lore:
      - '&7Compre sua enxada e começe a farmar'
      - '&7para ganhar bastante dinheiro!'
      - ''
      - '&fValor: &a100 coins&f.'
      - ''
      - '&aClique para comprar.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Sair:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&8Plantacoes'
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
]]>
</code-block>
</chapter>

<chapter title="skins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Ferramenta - Skins'
Tamanho: 36
Slots: [11, 12, 13, 14, 15]
BackSlot: 29
AnteriorSlot: 18
ProximoSlot: 26
# Slot onde ficará a picareta do jogador
FerramentaSlot: 31
Itens: {}
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Plantação'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17
# Item do top Moedas
Item moedas:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fMoedas: &7{moedas}'
    - '&fPosição: &e{pos}º'
    - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="private" collapsible="true">
<chapter title="armors.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Armor encontrado: '&cEsta armadura não existe. Disponíveis: &7{list}'
Deu armor: '&bVocê deu uma armadura para o jogador &f{player}&b.'

Armors:
  basic:
    item:
      material: 'DIAMOND_HELMET'
      name: '&aCapacete Básico'
      lore: ['&7Você é pobre.', '', '&fBônus: &a10% (todos)']
    bonus-crops: 10.0
    bonus-coin: 10.0
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
    Permissao: 'yplantacoes.bonus.membro'
    # Nome que irá aparecer nas mensagens
    Display: '&7[Membro]'
    # Quantia do bônus em %
    Bonus: 10.0
    BonusMoeda: 10.0
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

# Comandos e aliases do plugin
Comando:
  Farm:
    Comando: 'farm'
    Aliases: [ ]

# Opções gerais do plugin
Opcoes:
  # Pode conflitar com plugins de armazém
  AutoPickup: false
  # Subcomando de moedas
  Moedas subcomandos: ['moeda', 'moedas']
  # Mundos blacklistados
  MundoBlacklist:
    - 'nenhum'
  # Ao quebrar com uma enxada no shift não executar o evento do plugin
  ShiftEnxadaBypass: true
  # Ao quebrar no modo criativo não executar o evento do plugin
  CriativoBypass: true
  # Fazer com que a Enxada nunca quebre
  EnxadaUnbreakable: true
  # Valor da enxada no menu principal
  EnxadaValor: 100.0
  # Quebrar as plantações apenas com a enxada custom
  QuebrarSoCustom: false
  # Abrir menu de evolução ao interagir com a enxada (Shift+Botão direito)
  InteragirMenu: true
  # Somar um nível a mais na evolução
  # Padrão: true (versões anteriores)
  SomarEvolute: true
  # Máximo permitido para evoluir com Q
  QMax: 0
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Enviar recompensas para o menu de recompensas
  RecompensasMenu: true
  # Formatador de mensagens
  Formatador:
    Bonus tem: '&a+{bonus}% por ser {display}&a.'
    Bonus nao tem: ''
  # Materiais que irão ser reconhecidos na skin
  Skin-materiais:
    - 'WOOD'
    - 'STONE'
    - 'IRON'
    - 'GOLD'
    - 'DIAMOND'
  # Item da enxada
  Enxada:
    CustomSkull: false
    URL: ''
    ID: DIAMOND_HOE
    Data: 0
    Name: '&bEnxada de farm'
    Lore:
      - '&7Inquebrável ∞'
      - '{enchants}'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Segurando: '&cVocê deve estar segurando sua enxada.'
  Evoluido: '&aO encantamento &f{encantamento}&a foi evoluido para o nível &f{nivel}&a.'
  Numero: '&cO argumento não é um número.'
  Jogador: '&cEste jogador não foi encontrado.'
  SiMesmo: '&cVocê não pode realizar esta ação à si mesmo.'
  Moedas: '&bVocê possui &f{moedas} moedas&b.'
  Moedas player: '&bO jogador &f{player}&b possui &f{moedas} moedas&b.'
  Adicionou: '&bVocê adicionou &f{moedas} moedas&b ao jogador &f{player}&b.'
  Removeu: '&bVocê removeu &f{moedas} moedas&b do jogador &f{player}&b.'
  Setou: '&bVocê setou &f{moedas} moedas&b para o jogador &f{player}&b.'
  Enviou: '&bVocê enviou &f{moedas} moedas&b para o jogador &f{player}&b.'
  Recebeu: '&bVocê recebeu &f{moedas} moedas&b do jogador &f{player}&b.'
  Possui: '&cVocê não possui a quantia de &f{moedas}&c moedas.'
  Deu: '&bVocê deu uma enxada para o jogador &f{player}&b.'
  Custo: '&cVocê não possui 100 coins.'
  Comprou: '&aVocê comprou uma enxada por 100 coins.'
  PermPlanta: '&cVocê não possui a permissão deste tipo de planta.'
  Enxada: '&cVocê deve quebrar esta plantação com uma enxada de farm.'
  Aguarde: '&cVocê precisa aguardar {time} para quebrar essa plantação novamente.'
  Cancelou: '&cOperação cancelada.'
  Excede: '&cEstes níveis excedem o nível máximo do encantamento.'
  Skin encontrada: '&cEsta skin não existe. Disponíveis: &7{list}'
  Deu skin: '&bVocê deu uma skin para o jogador &f{player}&b.'
  Skin possui: '&aA ferramenta já possui esta skin ativada.'
  Skin ativou: '&aSkin ativada com sucesso.'
  Skin nao possui: '&cA ferramenta não possui essa skin.'
  Skin removida: '&aSkin removida com sucesso.'
  Ja tem: '&cVocê já possui uma enxada no inventário.'
  NoBalance: '&cVocê não tem {provider_display} suficiente para isto. Disponível: {provider_balance}&c.'
  Digite encantamento:
    - ''
    - '&aDigite a quantia de níveis que você quer adquirir ao encantamento &f{encantamento}&a.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Farm help:
    - ''
    - '&a/farm &8- &7Abre o menu principal.'
    - '&a/farm moedas &8- &7Vê as suas moedas.'
    - '&a/farm <player> &8- &7Ver as moedas de alguém.'
    - '&a/farm enviar <player> <quantia> &8- &7Envia suas moedas para alguém.'
    - '&a/farm darenxada <player> &8- &7Dá enxada para um jogador.'
    - '&a/farm add <player> <quantia> &8- &7Adiciona moedas a alguém.'
    - '&a/farm set <player> <quantia> &8- &7Remove moedas de alguém.'
    - '&a/farm remove <player> <quantia> &8- &7Seta moedas a alguém.'
    - ''
  Reward-collected: '&eItem recolhido com sucesso.'
  Reward-collected-all: '&eTodas as recompensas possíveis foram recolhidas com sucesso.'

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
]]>
</code-block>
</chapter>

<chapter title="custom_encantamentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Encantamentos:
  Chaveiro:
    Ordem: 5
    Display: 'Chaveiro'
    Padrao: 0
    Maximo: -1
    BonusPorLevel: 10.0 # em porcentagem
    ChancePorLevel: 10.0 # em porcentagem
    Preco:
      Padrao: 100.0
      PerLevel: 200.0
    Prices-Default:
      price1:
        provider: 'money'
        price: 10000.0
    Prices-PerLevel:
      price1:
        provider: 'money'
        price: 10000.0
    # Aparecer no menu de evolução
    MostrarMenu: true
    # chance,comando
    Comandos:
      - '20,give {player} quartz 1'
    # Economias que irá dár por nível ao executar o enchant
    Give-PerLevel:
      price1:
        provider: 'money'
        amount: 1.0
    Mensagens:
      Title: '&aChave<nl>&eencontrado' # deixe '' para não usar
      Actionbar: '' # deixe '' para não usar
      Chat: [ ]
    Displays: # Item que aparecerá no menu de evolução
      Pode: # quando puder evoluir
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Bônus atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} moedas&f.'
          - ''
          - '&aBotão &fesquerdo &apara evoluir'
      NaoPode: # quando não puder evoluir
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&f > Custo: &a{moedas} moedas&f.'
          - ''
          - '&cVocê não tem moedas suficientes.'
      Maximo: # quando já estiver no máximo
        CustomSkull: false
        URL: ''
        ID: GOLD_INGOT
        Data: 0
        Name: '&aChaveiro'
        Lore:
          - '&7Este encantamento permite que você'
          - '&7encontre chaves ao colher.'
          - ''
          - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
          - '&f > Chance atual: &b{porcentagem}%&f.'
          - ''
          - '&cVocê já está no máximo.'
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
    permission: 'ycampo.provider.money'
]]>
</code-block>
</chapter>

<chapter title="encantamentos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Velocidade ao quebrar
Eficiencia:
  # Ordem do enchant no menu
  Ordem: 1
  Display: 'Eficiência'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: FEATHER
      Data: 0
      Name: '&aEficiência'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre mais rápido.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: FEATHER
      Data: 0
      Name: '&aEficiência'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre mais rápido.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: FEATHER
      Data: 0
      Name: '&aEficiência'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebre mais rápido.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - ''
        - '&cVocê já está no máximo.'

# Bônus de drop
Fortuna:
  # Ordem do enchant no menu
  Ordem: 2
  Display: 'Bônus'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aFortuna'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais drops.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Bônus atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'

# Aumenta chance nas recompensas
Sortudo:
  Ordem: 3
  Display: 'Sortudo'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: true
      URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      ID: AIR
      Data: 0
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: true
      URL: 'd8188345dc6a1bf08663385b99f2bd1551a49292a93b84e0a97b917b565bf41a'
      ID: AIR
      Data: 0
      Name: '&aSortudo'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
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
        - '&7tenha mais sorte para ganhar recompensas.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{porcentagem}%&f.'
        - ''
        - '&cVocê já está no máximo.'

# Ganhar mais moedas de farm
Multiplicador:
  Ordem: 4
  Display: 'Multiplicador'
  Padrao: 0
  Maximo: -1
  BonusPorLevel: 10.0 # em porcentagem
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: true
      URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      ID: AIR
      Data: 0
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Multiplicador Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: true
      URL: '5d8604b9e195367f85a23d03d9dd503638fcfb05b0032535bc43734422483bde'
      ID: AIR
      Data: 0
      Name: '&aMultiplicador'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
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
        - '&7ganhe mais moedas ao farmar.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Porcentagem Atual: &b{multiplicador}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="flowEnchants.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
linear:
  Ordem: 5
  Display: 'Linear'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aLinear<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aLinear'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma linha reta.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

explosive:
  Ordem: 5
  Display: 'Explosão'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aExplosão<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aExplosão'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

laser:
  Ordem: 5
  Display: 'Laser'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&alaser<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&alaser'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'

boomerang:
  Ordem: 5
  Display: 'Boomerang'
  Padrao: 0
  Maximo: -1
  ChancePorLevel: 10.0 # em chance
  Preco:
    Padrao: 100.0
    PerLevel: 200.0
  Prices-Default:
    price1:
      provider: 'money'
      price: 10000.0
  Prices-PerLevel:
    price1:
      provider: 'money'
      price: 10000.0
  # Aparecer no menu de evolução
  MostrarMenu: true
  Mensagens:
    Title: '&aBoomerang<nl>&eativada' # deixe '' para não usar
    Actionbar: '' # deixe '' para não usar
    Chat: [ ]
  Displays: # Item que aparecerá no menu de evolução
    Pode: # quando puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&aBotão &fesquerdo &apara evoluir'
    NaoPode: # quando não puder evoluir
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&f > Custo: &a{moedas} moedas&f.'
        - ''
        - '&cVocê não tem moedas suficientes.'
    Maximo: # quando já estiver no máximo
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Name: '&aBoomerang'
      Lore:
        - '&7Este encantamento permite que você'
        - '&7quebra uma esfera.'
        - ''
        - '&f > Nível: &b{atual}&f/&b{maximo}&f.'
        - '&f > Chance atual: &b{chance}%&f.'
        - ''
        - '&cVocê já está no máximo.'
]]>
</code-block>
</chapter>

<chapter title="plantacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
## ESTE PLUGIN NÃO É COMPATÍVEL COM PLANTAÇÕES DIFERENTES DE CROPS E FUNGOS, OU SEJA,
## NÃO RECOMENDAMOS O USO COM CACTO, CANA DE AÇÚCAR, BAMBU E DERIVADOS QUE CRESCEM EM BLOCOS PARA CIMA

Plantacoes:
  fungo:
    # Tipo da plantação
    Plantacao: 'NETHER_WARTS'
    # Configurações do replante
    Replantar:
      Ativar: true
      # Replantar apenas se ter a planta no inventário
      ApenasTer: true
      # Planta que precisará ter no inventário para replantar
      Planta: 'NETHER_STALK'
    # Quebrar apenas se estiver crescido
    QuebrarCrescido: true
    # Estágio máximo que a planta pode chegar (fungos = 3; os outros crops normalmente são 7)
    NivelMaximo: 3
    # Delay para quebrar o mesmo bloco novamente
    # em segundos
    FarmDelay: 0
    # Bônus por cada nível de fortuna (enchant default)
    # Ex: 1.0 de bônus por nível = nivel*bonus (10 niveis * 1 = 10% a mais)
    FortunaBonus: 1.0
    # Permissão para quebrar este tipo de plantação
    # Deixe '' (vazio) para não usar
    Permissao: 'yplantacoes.fungo'
    # XP que será dado ao jogador
    XP:
      Vanilla: 1.0
      Mcmmo: 1.0 # skill HERBALISM
    # Configuração do drop
    Drops:
      membro:
        Ordem: 1
        Drop:
          material: 'NETHER_STALK'
        Permissao: 'yplantacoes.fungo.membro'
        Minimo: 10
        Maximo: 15
        Title: ''
        Actionbar: '&aVocê recebeu &e{quantia} fungos&a e &e{moedas} moedas&a.'
        Chat: ''
        # Moedas que serão ganhas
        Moedas:
          Min: 1
          Max: 5
        # Sistema de auto-sell do drop
        AutoSell:
          Ativar: false
          DarMoney: true
          BasePrice: 100.0 # preço por drop (para o comando)
          Currencies:
            preco1:
              Provider: 'money'
              Amount: 100.0
          Mensagem:
            Actionbar: '&aVocê vendeu &fx{quantia} Fungos&a por &6{money}&a e &e{moedas} moedas&a.'
            Chat: '&aVocê vendeu &fx{quantia} Fungos&a por &6{money}&a e &e{moedas} moedas&a.'
          # O Drop vai executar um comando ao ser vendido?
          Comando:
            Ativar: false
            UsarQuantia: true # usar a placeholder {quantia} para ter a quantia de drops e executar o comando só 1x
            MultiplicarQuantiaPreco: true # multiplica a quantia pelo preço e o bônus (essencial para dar em outras economias)
            InvBypass: true # não checar se o inv está cheio (apenas quando os comandos tiverem ativos)
            Comandos:
              - 'give {player} NETHER_STALK {quantia}'
    # Configuração das recompensas
    # recompensa (recompensas.yml),chance
    Recompensas:
      - 'Reco1,50.0'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
    # Item que aparecerá para coletar.
    Collect:
      material: 'STONE:0'
      name: '&8Pedra'
      amount: 64
      lore: [ '&aEsta pedra vale muito dinheiro!', '', ' &7> &fQuantidade: &7{amount}', '', '&eClique esquerdo para receber', '&eClique direito para deletar' ]
      enchants: []
    # Só será dado o item se os comandos estiverem em false.
    # Item que será dado ao jogador.
    Item:
      material: STONE
      name: ''
      amount: 1
      lore: []
    # Mensagens que serão enviadas ao receber a recompensa
    Mensagens:
      Title: '&a+100 coins' # deixe '' para não usar
      Actionbar: '&a+100 coins' # deixe '' para não usar
      Chat: |
        &a+100 coins
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: true
      # quantia padrão da placeholder {amount} no comando (valor base)
      Placeholder-amount: 100
      # multiplicar a placeholder {amount} pela quantia de recompensas do mesmo tipo
      Multiply-placeholder: true
      List:
        - 'money add {player} {amount}'

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
    custom-model-data: 0
    item:
      material: 'STONE'
      name: '&aSkin de Pedra'
      lore: ['&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&aClique na ferramenta para ativar']
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
        lore: [ '&7Esta é a skin de pedra. Você é pobre.', '', '&fBônus: &a10%', '&fPrioridade: &a1', '', '&cVocê não possui esta skin' ]
    lore:
      - '&7Inquebrável ∞'
      - '{enchants}'
      - ''
      - '&a+10% ( PEDRA )'
      - ''
    bonus: 10.0
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static PlantacaoAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;PlantacaoAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(PlantacaoAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/89-yPlantacoes">Site do plugin yPlantacoes</a>
    </category>
</seealso>