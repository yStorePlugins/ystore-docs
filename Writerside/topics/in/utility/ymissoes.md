# yMissoes
<secondary-label ref="utility"/>

### Descrição
Deixe seu servidor mais interativo com nossas missões, são vários tipos para deixar seu server legal.

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
<video src="//www.youtube.com/watch?v=UUAFyqZQ1-g"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/missoes - Abrir o menu de missões.
/missoes info - Ver o progresso da missão do jogador.
/missoes set - Setar uma missão para um jogador.
/missoes setnpc - Setar o npc de entregar itens das missões.
/missoes delnpc - Deletar o npc de entregar itens das missões.
/missoes reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ymissoes.info - Permissão para o /missoes info
ymissoes.set - Permissão para o /missoes set
ymissoes.setnpc - Permissão para o /missoes setnpc
ymissoes.delnpc - Permissão para o /missoes delnpc
ymissoes.reload - Permissão para o /missoes reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ymissoes_nivel% - Retorna o nível em missões do jogador.
%ymissoes_info% - Retorna o dado necessário da missão atual.
%ymissoes_progressbar% - Retorna a barra de progresso da missão atual.
%ymissoes_porcentagem% - Retorna a porcentagem de progresso da missão atual.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMissoes/
    ├── menus/
    │    ├── atrasadas.yml
    │    ├── principal.yml
    │    └── top.yml
    ├── config.yml
    ├── desafios.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="atrasadas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Missoes - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cVazio'
   Lore:
   - ''
   - '&7Você não possui nenhuma recompensa atrasada.'
   - ''
   
Item:
   Lore pode:
   - ''
   - '&aClique para recolher as recompensas'
   - ''
   Lore nao pode:
   - ''
   - '&cVocê não tem permissão para recolher esta recompensa.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Missoes - desafios'
Tamanho: 54
Menu slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
AnteriorSlot: 36
ProximoSlot: 44
# Item das missões atrasadas
Atrasadas:
  Slot: 45
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/e9e4bdcf172d5dc77c2bd4e37ad985399a9f2cdebf72463929ea4b666ef6f80'
  ID: 0
  Data: 0
  Glow: false
  Name: '&aRecompensas atrasadas'
  Lore:
    - '&7Clique para recolher as recompensas'
    - '&7atrasadas.'
# Item do TOP
Top:
  Slot: 53
  CustomSkull: false
  URL: ''
  ID: 340
  Data: 0
  Glow: false
  Name: '&aTop'
  Lore:
    - '&7Clique para ver o Top missões.'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Missões'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17

# Item do top Missões
Item:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fNível: &7{nivel}'
    - '&fPosição: &e{pos}º'
    - ''

# Item do top quem realizou primeiro
Item primeiros:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fTerminou: &e{pos}º'
    - ''

# Seletor dos tops
Seletor:
  Slot: 32
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: 0
  Data: 0
  Name: '&aSeletor do TOP'

# Tipos do seletor
Tipos:
  Nivel:
    Ativar: true
    Nome: 'Nível'
  Primeiros:
    Ativar: true
    Nome: 'Primeiros'

# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome}'
  Selecionar: ' &f• &7{nome}'
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

# Comandos e aliases do plugin
Comando:
  Comando: 'missoes'
  Aliases: []

# Opções gerais
Opcoes:
  #se estiver false, o jogador terá q abrir o menu para coletar a recompensa.
  #se estiver true, no momento que ele atingir todas as metas, as recompensas serão dadas automaticamente.
  Recompensar ao terminar: false
  #Use TODOS para mesmo se a missão não necessitar de matar mobs por exemplo, resetar.
  #Use NENHUM para não resetar ao terminar.
  #Use APENAS_USADO para resetar só o que a missão utilizou.
  Resetar ao terminar: 'TODOS'
  #se estiver false, se a missão não requerir quebrar blocos por exemplo, não ira contabilizar + 1 pro player
  #se estiver true, mesmo se a missão não requerir quebrar blocos por exemplo, ira subir + 1 pro player
  Contabilizar nao tem: false
  # Metadata do plugin de mob-stack para multiplicar a missão de matar mobs
  # Deixe vazio '' para não usar
  Metadata: 'ySpawnersV2-MobStacked'
  # Ao matar com shift, não calcular a metadata
  Shift unitario: true
  # Ao matar em pé, não calcular a metadata
  SemShift unitario: false
  # Sobrepor as lores de coleta, já realizada e desbloqueie
  Lore sobrepor: true
  # Som ao terminar uma missão
  Som: 'LEVEL_UP'

# Mensagens do plugin
Mensagens:
  Title terminou: '&aMissão<nl>&eFinalizada!'
  Actionbar terminou: '&aMissão concluída com sucesso!'

# Lores para substituição
Lores:
  Ja realizada:
    - ''
    - '&aVocê já completou esta missão.'
    - ''
  Desbloqueie:
    - ''
    - '&cComplete a missão anterior para desbloquear esta.'
    - ''
  Coletar:
    - ''
    - '&aVocê completou essa missão, clique para coletar as recompensas.'
    - ''

# Flechas do menu
Flechas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: false
    Name: '&8Voltar'
    Lore:
      - ''
      - '&eClique para voltar.'
      - ''
  Proxima:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: false
    Name: '&8Próxima'
    Lore:
      - ''
      - '&eClique para ir para a próxima página.'
      - ''

# Itens gerais
Items:
  Completou:
    Usar: true
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/78d58a7651fedae4c03efebc226c03fd791eb74a132babb974e8d838ac6882'
    ID: 0
    Data: 0
    Glow: true
    Name: '{nome}'
  Bloqueada:
    Usar: true
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 0
    Data: 0
    Glow: true
    Name: '{nome}'

# Configuração do NPC
NPC:
  Skin: 'deliveryman'
  Altura: 3.1
  Holograma:
    - '&6&lEntregador'
    - '&7Clique para entregar seu item.'

# Configuração da barra de progresso
Progress bar:
  Quantia: 10
  Simbolo: ':'
  Cor sim: '&a'
  Cor nao: '&7'

# Local do NPC (não altere nada aqui)
NPC Local: 'none'

# Formatos de money e quantia
Formats:
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

<chapter title="desafios.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Desafios:
  Desafio01:
    Ordem: 1
    Permissao: '' #permissao para receber os itens da recompensa
    # Dado que a placeholder %ymissoes_info% irá retornar
    Placeholder: 'Quebre 2 blocos de terra'
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
    ID: 0
    Data: 0
    Glow: true
    Name: '&8#Desafio 1'
    Lore:
      - ''
      - '&7Quebre 2 blocos de terra, mate 1 player, '
      - '&7entregue 40 terras e pesque 1 peixe para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Info-message:
      - '&aInformações da missão de &f{player}&a:'
      - ''
      - '&7Coloque 2 blocos de terra para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Quebrar blocos:
      Ativar: true
      Ativar tipo especifico: true
      Tipo especifico: 'DIRT'
      Data: 0
      Quantia: 2
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Colocar blocos:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'CHEST'
      Data: 0
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Matar mobs:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'ZOMBIE'
      Quantia: 4000
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Matar players:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Entregador:
      Ativar: true
      Tipo: 'DIRT'
      Data: 0
      Nome: 'none' #deixe "none" para aceitar itens com qualquer nome
      Quantia: 40
    Pescar:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Andar:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Craftar:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'CHEST'
      Data: 0
      Quantia: 1
    Morrer:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
      Regioes: []
    Bosses:
      Ativar: true
      Quantia: 1
    Criticos:
      Ativar: true
      Quantia: 1
    Recompensas:
      - 'give {player} minecraft:diamond 1'
      - 'give {player} minecraft:gold_ingot 1'
      - 'give {player} minecraft:emerald 1'
  Desafio02:
    Ordem: 2
    Permissao: '' #permissao para receber os itens da recompensa
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
    ID: 0
    Data: 0
    Glow: true
    Name: '&8#Desafio 2'
    Lore:
      - ''
      - '&7Coloque 2 blocos de terra para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Info-message:
      - '&aInformações da missão de &f{player}&a:'
      - ''
      - '&7Coloque 2 blocos de terra para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Quebrar blocos:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'DIRT'
      Data: 0
      Quantia: 2
      Mundos:
        - 'Plot'
        - 'world'
    Colocar blocos:
      Ativar: true
      Ativar tipo especifico: true
      Tipo especifico: 'DIRT'
      Data: 0
      Quantia: 2
      Mundos:
        - 'Plot'
        - 'world'
    Matar mobs:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'ZOMBIE'
      Quantia: 4000
      Mundos:
        - 'Plot'
        - 'world'
    Matar players:
      Ativar: true
      Quantia: 40
      Mundos:
        - 'Plot'
        - 'world'
    Entregador:
      Ativar: true
      Tipo: 'DIRT'
      Data: 0
      Nome: 'none' #deixe "none" para aceitar itens com qualquer nome
      Quantia: 40
    Pescar:
      Ativar: true
      Quantia: 40
      Mundos:
        - 'Plot'
        - 'world'
    Andar:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Craftar:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'CHEST'
      Data: 0
      Quantia: 1
    Morrer:
      Ativar: false
      Quantia: 0
      Mundos:
        - 'Plot'
        - 'world'
    Bosses:
      Ativar: false
      Quantia: 0
    Criticos:
      Ativar: false
      Quantia: 0
    Recompensas:
      - 'give {player} minecraft:diamond 1'
      - 'give {player} minecraft:gold_ingot 1'
      - 'give {player} minecraft:emerald 1'
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

    &aMissoes comandos:

    &a> /missoes
    &a> /missoes set <player> <missao>
    &a> /missoes info <player>
    &a> /missoes setnpc
    &a> /missoes delnpc
    &a> /missoes reload

  finished-automatic: '&aVocê completou o desafio {desafio} e ganhou suas recompensas automaticamente.'
  finished-manual: '&aVocê completou o desafio {desafio}. Acesse /missoes e clique nela para receber as recompensas.'
  finished-permission: '&aVocê completou o desafio {desafio} mas não ganhou nem pode coletar as recompensas pois não possui a permissão.'
  hand-none: '&cVocê não está segurando nenhum item.'
  hand-found: '&cSua missão não requer entregas'
  hand-wrong: '&cVocê está entregando o item errado.'
  hand-delivered: '&aVocê entregou este item.'
  mission-collected: '&aVocê coleteu as recompensas do desafio {desafio}'
  mission-changed: '&aMissão alterada para o jogador &f{player}&a.'
  mission-found: '&cNenhuma missão encontrada para o jogador &f{player}&a.'
  npc-found: '&cNPC do entregador não encontrado.'
  npc-set: '&aNPC do entregador setado com sucesso.'
  npc-deleted: '&aNPC do entregador deletado com sucesso.'
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yMissoes/
    ├── menus/
    │    ├── atrasadas.yml
    │    ├── principal.yml
    │    └── top.yml
    ├── config.yml
    ├── desafios.yml
    └── messages.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="atrasadas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Missoes - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 18
ProximoSlot: 26

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cVazio'
   Lore:
   - ''
   - '&7Você não possui nenhuma recompensa atrasada.'
   - ''
   
Item:
   Lore pode:
   - ''
   - '&aClique para recolher as recompensas'
   - ''
   Lore nao pode:
   - ''
   - '&cVocê não tem permissão para recolher esta recompensa.'
   - ''
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Missoes - desafios'
Tamanho: 54
Menu slots: [ 10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43 ]
AnteriorSlot: 36
ProximoSlot: 44
# Item das missões atrasadas
Atrasadas:
  Slot: 45
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/e9e4bdcf172d5dc77c2bd4e37ad985399a9f2cdebf72463929ea4b666ef6f80'
  ID: 0
  Data: 0
  Glow: false
  Name: '&aRecompensas atrasadas'
  Lore:
    - '&7Clique para recolher as recompensas'
    - '&7atrasadas.'
# Item do TOP
Top:
  Slot: 53
  CustomSkull: false
  URL: ''
  ID: 340
  Data: 0
  Glow: false
  Name: '&aTop'
  Lore:
    - '&7Clique para ver o Top missões.'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Missões'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17

# Item do top Missões
Item:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fNível: &7{nivel}'
    - '&fPosição: &e{pos}º'
    - ''

# Item do top quem realizou primeiro
Item primeiros:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fTerminou: &e{pos}º'
    - ''

# Seletor dos tops
Seletor:
  Slot: 32
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
  ID: 0
  Data: 0
  Name: '&aSeletor do TOP'

# Tipos do seletor
Tipos:
  Nivel:
    Ativar: true
    Nome: 'Nível'
  Primeiros:
    Ativar: true
    Nome: 'Primeiros'

# Formatos do seletor
Formato:
  Visualizando: ' &f• &a{nome}'
  Selecionar: ' &f• &7{nome}'
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

# Comandos e aliases do plugin
Comando:
  Comando: 'missoes'
  Aliases: []

# Opções gerais
Opcoes:
  #se estiver false, o jogador terá q abrir o menu para coletar a recompensa.
  #se estiver true, no momento que ele atingir todas as metas, as recompensas serão dadas automaticamente.
  Recompensar ao terminar: false
  #Use TODOS para mesmo se a missão não necessitar de matar mobs por exemplo, resetar.
  #Use NENHUM para não resetar ao terminar.
  #Use APENAS_USADO para resetar só o que a missão utilizou.
  Resetar ao terminar: 'TODOS'
  #se estiver false, se a missão não requerir quebrar blocos por exemplo, não ira contabilizar + 1 pro player
  #se estiver true, mesmo se a missão não requerir quebrar blocos por exemplo, ira subir + 1 pro player
  Contabilizar nao tem: false
  # Metadata do plugin de mob-stack para multiplicar a missão de matar mobs
  # Deixe vazio '' para não usar
  Metadata: 'ySpawnersV2-MobStacked'
  # Ao matar com shift, não calcular a metadata
  Shift unitario: true
  # Ao matar em pé, não calcular a metadata
  SemShift unitario: false
  # Sobrepor as lores de coleta, já realizada e desbloqueie
  Lore sobrepor: true
  # Som ao terminar uma missão
  Som: 'LEVEL_UP'

# Mensagens do plugin
Mensagens:
  Title terminou: '&aMissão<nl>&eFinalizada!'
  Actionbar terminou: '&aMissão concluída com sucesso!'

# Lores para substituição
Lores:
  Ja realizada:
    - ''
    - '&aVocê já completou esta missão.'
    - ''
  Desbloqueie:
    - ''
    - '&cComplete a missão anterior para desbloquear esta.'
    - ''
  Coletar:
    - ''
    - '&aVocê completou essa missão, clique para coletar as recompensas.'
    - ''

# Flechas do menu
Flechas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: false
    Name: '&8Voltar'
    Lore:
      - ''
      - '&eClique para voltar.'
      - ''
  Proxima:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: false
    Name: '&8Próxima'
    Lore:
      - ''
      - '&eClique para ir para a próxima página.'
      - ''

# Itens gerais
Items:
  Completou:
    Usar: true
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/78d58a7651fedae4c03efebc226c03fd791eb74a132babb974e8d838ac6882'
    ID: 0
    Data: 0
    Glow: true
    Name: '{nome}'
  Bloqueada:
    Usar: true
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 0
    Data: 0
    Glow: true
    Name: '{nome}'

# Configuração do NPC
NPC:
  Skin: 'deliveryman'
  Altura: 3.1
  Holograma:
    - '&6&lEntregador'
    - '&7Clique para entregar seu item.'

# Configuração da barra de progresso
Progress bar:
  Quantia: 10
  Simbolo: ':'
  Cor sim: '&a'
  Cor nao: '&7'

# Local do NPC (não altere nada aqui)
NPC Local: 'none'

# Formatos de money e quantia
Formats:
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

<chapter title="desafios.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Desafios:
  Desafio01:
    Ordem: 1
    Permissao: '' #permissao para receber os itens da recompensa
    # Dado que a placeholder %ymissoes_info% irá retornar
    Placeholder: 'Quebre 2 blocos de terra'
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
    ID: 0
    Data: 0
    Glow: true
    Name: '&8#Desafio 1'
    Lore:
      - ''
      - '&7Quebre 2 blocos de terra, mate 1 player, '
      - '&7entregue 40 terras e pesque 1 peixe para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Info-message:
      - '&aInformações da missão de &f{player}&a:'
      - ''
      - '&7Coloque 2 blocos de terra para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Quebrar blocos:
      Ativar: true
      Ativar tipo especifico: true
      Tipo especifico: 'DIRT'
      Data: 0
      Quantia: 2
      Mundos:
        - 'Plot'
        - 'world'
    Colocar blocos:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'CHEST'
      Data: 0
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Matar mobs:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'ZOMBIE'
      Quantia: 4000
      Mundos:
        - 'Plot'
        - 'world'
    Matar players:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Entregador:
      Ativar: true
      Tipo: 'DIRT'
      Data: 0
      Nome: 'none' #deixe "none" para aceitar itens com qualquer nome
      Quantia: 40
    Pescar:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Andar:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Craftar:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'CHEST'
      Data: 0
      Quantia: 1
    Morrer:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Bosses:
      Ativar: true
      Quantia: 1
    Criticos:
      Ativar: true
      Quantia: 1
    Recompensas:
      - 'give {player} minecraft:diamond 1'
      - 'give {player} minecraft:gold_ingot 1'
      - 'give {player} minecraft:emerald 1'
  Desafio02:
    Ordem: 2
    Permissao: '' #permissao para receber os itens da recompensa
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/24c22b8df0a853a49cb82e90a618d65012122361c8398062fcbaf74d5696c2a9'
    ID: 0
    Data: 0
    Glow: true
    Name: '&8#Desafio 2'
    Lore:
      - ''
      - '&7Coloque 2 blocos de terra para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Info-message:
      - '&aInformações da missão de &f{player}&a:'
      - ''
      - '&7Coloque 2 blocos de terra para completar,'
      - '&7a primeira missão do servidor'
      - ''
      - '&aRecompensas:'
      - ' &a• 1 diamante'
      - ' &a• 1 ouro'
      - ' &a• 1 esmeralda'
      - ''
      - '&8Blocos quebrados: &7({quebrarmin} &8[{quebrarbar}&8] &7{quebrarmax})'
      - '&8Blocos colocados: &7({colocarmin} &8[{colocarbar}&8] &7{colocarmax})'
      - '&8Mobs matados: &7({matarmin} &8[{matarbar}&8] &7{matarmax})'
      - '&8Players matados: &7({matarpmin} &8[{matarpbar}&8] &7{matarpmax})'
      - '&8Itens entregues: &7({entreguemin} &8[{entregarbar}&8] &7{entreguemax})'
      - '&8Peixes pescados: &7({pescamin} &8[{pescarbar}&8] &7{pescamax})'
      - '&8Blocos andados: &7({andarmin} &8[{andarbar}&8] &7{andarmax})'
      - '&8Itens craftados: &7({craftarmin} &8[{craftarbar}&8] &7{craftarmax})'
      - '&8Morrer: &7({morrermin} &8[{morrerbar}&8] &7{morrermax})'
      - '&8Bosses matados: &7({bossesmin} &8[{bossesbar}&8] &7{bossesmax})'
      - '&8Criticos: &7({criticosmin} &8[{criticosbar}&8] &7{criticosmax})'
      - ''
    Quebrar blocos:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'DIRT'
      Data: 0
      Quantia: 2
      Mundos:
        - 'Plot'
        - 'world'
    Colocar blocos:
      Ativar: true
      Ativar tipo especifico: true
      Tipo especifico: 'DIRT'
      Data: 0
      Quantia: 2
      Mundos:
        - 'Plot'
        - 'world'
    Matar mobs:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'ZOMBIE'
      Quantia: 4000
      Mundos:
        - 'Plot'
        - 'world'
    Matar players:
      Ativar: true
      Quantia: 40
      Mundos:
        - 'Plot'
        - 'world'
    Entregador:
      Ativar: true
      Tipo: 'DIRT'
      Data: 0
      Nome: 'none' #deixe "none" para aceitar itens com qualquer nome
      Quantia: 40
    Pescar:
      Ativar: true
      Quantia: 40
      Mundos:
        - 'Plot'
        - 'world'
    Andar:
      Ativar: true
      Quantia: 1
      Mundos:
        - 'Plot'
        - 'world'
    Craftar:
      Ativar: false
      Ativar tipo especifico: false
      Tipo especifico: 'CHEST'
      Data: 0
      Quantia: 1
    Morrer:
      Ativar: false
      Quantia: 0
      Mundos:
        - 'Plot'
        - 'world'
    Bosses:
      Ativar: false
      Quantia: 0
    Criticos:
      Ativar: false
      Quantia: 0
    Recompensas:
      - 'give {player} minecraft:diamond 1'
      - 'give {player} minecraft:gold_ingot 1'
      - 'give {player} minecraft:emerald 1'
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

    &aMissoes comandos:

    &a> /missoes
    &a> /missoes set <player> <missao>
    &a> /missoes info <player>
    &a> /missoes setnpc
    &a> /missoes delnpc
    &a> /missoes reload

  finished-automatic: '&aVocê completou o desafio {desafio} e ganhou suas recompensas automaticamente.'
  finished-manual: '&aVocê completou o desafio {desafio}. Acesse /missoes e clique nela para receber as recompensas.'
  finished-permission: '&aVocê completou o desafio {desafio} mas não ganhou nem pode coletar as recompensas pois não possui a permissão.'
  hand-none: '&cVocê não está segurando nenhum item.'
  hand-found: '&cSua missão não requer entregas'
  hand-wrong: '&cVocê está entregando o item errado.'
  hand-delivered: '&aVocê entregou este item.'
  mission-collected: '&aVocê coleteu as recompensas do desafio {desafio}'
  mission-changed: '&aMissão alterada para o jogador &f{player}&a.'
  mission-found: '&cNenhuma missão encontrada para o jogador &f{player}&a.'
  npc-found: '&cNPC do entregador não encontrado.'
  npc-set: '&aNPC do entregador setado com sucesso.'
  npc-deleted: '&aNPC do entregador deletado com sucesso.'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/17-yMissoes">Site do plugin yMissoes</a>
    </category>
</seealso>