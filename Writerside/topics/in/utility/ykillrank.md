# yKillRank
<secondary-label ref="utility"/>

### Descrição
Evolua de rank matando jogadores e ganhe recompensa por isso!

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
<video src="//www.youtube.com/watch?v=E5eJ8GFjPUs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/kills - Abre o menu principal
/kills - Vê as informações de um jogador.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ykillrank.usar - Permissão para o /kills
ykillrank.olhar - Permissão para o /kills</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ykillrank_tag% - Mostra o rank do jogador.
%ykillrank_kills% - Mostra a quantia de kills do jogador.
%ykillrank_nome% - Mostra o nome do rank do jogador.
%ykillrank_needkills% - Mostra a quantia de kills necessária para o próx rank.
%ykillrank_nexttag% - Mostra a tag do próx rank.
%ykillrank_progressbar% - Mostra a progressbar do próx rank.
%ykillrank_percentage% - Mostra a porcentagem do próx rank.
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{killrank} - Mostra o rank do jogador.
{killrank_nome} - Mostra o nome do rank do jogador.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yKillRank/
    ├── menus/
    │    ├── principal.yml
    │    ├── ranks.yml
    │    ├── recompensas.yml
    │    └── top.yml
    ├── config.yml
    ├── data.yml
    ├── messages.yml
    ├── ranks.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8KillRank - Principal'
Tamanho: 27
Itens:
   Perfil: # primeiro
      Slot: 11
      Name: '&f{player}'
      Lore:
      - ''
      - '&7Você matou &f{kills} &ajogadores.'
      - '&7Rank: &f{rank}'
      - '&7Próximo rank: &f{nextrank}'
      - ''
   Recompensas: #segundo
      Slot: 13
      CustomSkull: false
      URL: ''
      ID: 54
      Data: 0
      Glow: false
      Name: '&aRecompensas'
      Lore:
      - '&7Clique para gerenciar as recompensas.'
   Ranks:
      Slot: 14
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aRanks'
      Lore:
      - '&7Clique para acessar o menu de ranks.'
   Top: #terceiro
      Slot: 15
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: false
      Name: '&aTOP'
      Lore:
      - '&7Clique para ver os jogadores mais matadores.'
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Informativo dos ranks'
Tamanho: 36
Slots: [10, 11, 12, 13, 14, 15]
BackSlot: 0
VoltarSlot: 27
ProximoSlot: 35

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cSem ranks'
   Lore:
   - '&cNão há nenhum rank cadastrado :c'
   
Itens: #se o Usar item rank estiver false, isso não irá funcionar
   item1:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4'
      ID: 0
      Data: 0
      Glow: true
      Name: '&6Rank Bronze'
      Lore:
      - '&7Informações deste rank:'
      - ''
      - '&6 Nenhum -> Bronze'
      - ' &f Preço: &71 kill'
      - ''

]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8KillRank recompensas'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Kills'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fKills: &6{kills}'
   - '&fPosição: &6{pos}'
   - ''

Item p:
   Slot: 32
   Name: '&7#&f{pos} - &aVocê &7({player})'
   Lore:
   - ''
   - '&fKills: &6{kills}'
   - '&fPosição: &6{pos}'
   - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
   Tipo: SQLITE #Tipos: MYSQL, SQLITE
   IP: localhost:3306
   DB: test
   User: admin
   Pass: ''
   Debug: true
   
Comando:
   Comando: 'kills'
   Aliases: {}

Anti freekill: true #so ira contabilizar uma kill, quando matar um jogador diferente do morto anteriormente.
Recompensa auto: true #quando o player atingir a quantia necessária de kills ele já recebe a recompensa automaticamente.

# Comandos que poderão ser dados ao matar um jogador
ComandosPorKill:
   - '25.0,give {player} STONE 1'

# Mundos onde não irá contar kills
Mundo blacklist:
   - 'none'

# Regiões onde irá contar kills
Region whitelist: []

Placeholders:
   Tag tem: '{tag}'
   Tag nao tem: ''
   Nome tem: '{nome}'
   Nome nao tem: '&7Sem rank'

# Configuração da barra de progresso
progress-bar:
   amount: 10
   symbol: ':'
   color-yes: '&a'
   color-no: '&7'

# Sistema de npc
npc:
   skin: 'Pitombaa'
   hologram:
      offset: 3.4
      hologram:
         - '&6&lRanking de Kills'
         - '&7Evolua seu rank com a matança!'
         - '[item]DIAMOND_SWORD'

Upou:
   Msgs:
      Actionbar:
         Ativar: true
         Broadcast: false
         Msg: '&aVocê &7({player})&a upou seu rank de kills &ede {atual} &epara {rank} &7({nome})&a.'
      Title:
         Ativar: true
         Broadcast: false
         Title: '&aRank evoluido'
         Subtitle: '&e{rank} &7({nome})' # placeholder {atual} disponível
      Chat:
         Ativar: true
         Broadcast: false
         # placeholder {atual} disponível
         Msg:
         - ''
         - '&aVocê &7({player})&a evoluiu seu rank para &e{rank} &7({nome})&a.'
         - ''  
         
Setas:
   Voltar:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&cVoltar'
      Lore:
      - ''
      - '&7Clique para voltar.'
      - ''
   Proximo:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&aPróximo'
      Lore:
      - ''
      - '&7Clique para ir à próxima página.'
      - ''
      
Lores:
   Coletar:
      Sobrepor: false
      Lore:
      - ''
      - '&aClique para coletar essa recompensa'
   Ja coletou:
      Sobrepor: true
      Lore:
      - '&cVocê já coletou essa recompensa.'
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

    &aKill rank comandos:

    &a> /killrank
    &a> /killrank [player]
    &a> /killrank add
    &a> /killrank setnpc
    &a> /killrank delnpc
    &a> /killrank reload

  kill-changed: '&aKills do jogador &f{player}&a alterada para &f{kills}&a.'
  reward-collected: '&aVocê coletou a recompensa.'
  npc-set: '&aNPC setado com sucesso.'
  npc-deleted: '&aNPC removido com sucesso.'
  npc-not-set: '&cNPC não está definido.'
  look: |
    &r
    &7Informações do jogador &f{player}&7:
    &r
    &fKills: &b{kills}
    &fRank: &b{rank} &7({rank_nome})
    &r
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Ranks:
   Nenhum:
      Ordem: 0
      Tag: '&cNenhum'
      Kills: 0
   Broze:
      Ordem: 1
      Tag: '&7[&6Bronze&7]'
      Kills: 1
   Ferro:
      Ordem: 2
      Tag: '&7[&fFerro&7]'
      Kills: 2
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   1:
      Display:
         CustomSkull: false
         URL: ''
         ID: 388
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Lore: 
         - '&7Mate &f1 &7jogador e ganhe'
         - '&7 -> &a1 pedra.'
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         - '&aTu ganhou uma pedra.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Kills: 1
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'
   2:
      Display:
         CustomSkull: false
         URL: ''
         ID: 388
         Data: 0
         Glow: true
         Name: '&8Diamantes'
         Lore: 
         - '&7Mate &f2 &7jogadores e ganhe'
         - '&7 -> &a2 diamantes.'
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Kills: 2
      Command:
         Use: true
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} diamond 2'

]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yKillRank/
    ├── menus/
    │    ├── principal.yml
    │    ├── ranks.yml
    │    ├── recompensas.yml
    │    └── top.yml
    ├── config.yml
    ├── data.yml
    ├── ranks.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8KillRank - Principal'
Tamanho: 27
Itens:
   Perfil: # primeiro
      Slot: 11
      Name: '&f{player}'
      Lore:
      - ''
      - '&7Você matou &f{kills} &ajogadores.'
      - '&7Rank: &f{rank}'
      - '&7Próximo rank: &f{nextrank}'
      - ''
   Recompensas: #segundo
      Slot: 13
      CustomSkull: false
      URL: ''
      ID: 54
      Data: 0
      Glow: false
      Name: '&aRecompensas'
      Lore:
      - '&7Clique para gerenciar as recompensas.'
   Ranks:
      Slot: 14
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aRanks'
      Lore:
      - '&7Clique para acessar o menu de ranks.'
   Top: #terceiro
      Slot: 15
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: false
      Name: '&aTOP'
      Lore:
      - '&7Clique para ver os jogadores mais matadores.'
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Informativo dos ranks'
Tamanho: 36
Slots: [10, 11, 12, 13, 14, 15]
BackSlot: 0
VoltarSlot: 27
ProximoSlot: 35

Vazio:
   Slot: 22
   CustomSkull: false
   URL: ''
   ID: 408
   Data: 0
   Glow: true
   Name: '&cSem ranks'
   Lore:
   - '&cNão há nenhum rank cadastrado :c'
   
Itens: #se o Usar item rank estiver false, isso não irá funcionar
   item1:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/621668ef7cb79dd9c22ce3d1f3f4cb6e2559893b6df4a469514e667c16aa4'
      ID: 0
      Data: 0
      Glow: true
      Name: '&6Rank Bronze'
      Lore:
      - '&7Informações deste rank:'
      - ''
      - '&6 Nenhum -> Bronze'
      - ' &f Preço: &71 kill'
      - ''

]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8KillRank recompensas'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Kills'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fKills: &6{kills}'
   - '&fPosição: &6{pos}'
   - ''

Item p:
   Slot: 32
   Name: '&7#&f{pos} - &aVocê &7({player})'
   Lore:
   - ''
   - '&fKills: &6{kills}'
   - '&fPosição: &6{pos}'
   - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Database:
   Tipo: SQLITE #Tipos: MYSQL, SQLITE
   IP: localhost:3306
   DB: test
   User: admin
   Pass: ''
   Debug: true
   
Comando:
   Comando: 'kills'
   Aliases: {}

Anti freekill: true #so ira contabilizar uma kill, quando matar um jogador diferente do morto anteriormente.
Recompensa auto: true #quando o player atingir a quantia necessária de kills ele já recebe a recompensa automaticamente.

# Comandos que poderão ser dados ao matar um jogador
ComandosPorKill:
   - '25.0,give {player} STONE 1'

# Mundos onde não irá contar kills
Mundo blacklist:
   - 'none'

# Regiões onde irá contar kills
Region whitelist: []

Placeholders:
   Tag tem: '{tag}'
   Tag nao tem: ''
   Nome tem: '{nome}'
   Nome nao tem: '&7Sem rank'

# Configuração da barra de progresso
progress-bar:
   amount: 10
   symbol: ':'
   color-yes: '&a'
   color-no: '&7'

# Sistema de npc
npc:
   skin: 'Pitombaa'
   hologram:
      offset: 3.4
      hologram:
         - '&6&lRanking de Kills'
         - '&7Evolua seu rank com a matança!'
         - '[item]DIAMOND_SWORD'

Mensagens:
   Permissao: '&cVocê não tem permissão para isto.'
   Coletou: '&aVocê coletou a recompensa.'
   Nao encontrado: '&c&lERRO! &cJogador não encontrado.'
   Npc-set: '&aNPC setado com sucesso.'
   Npc-deleted: '&aNPC removido com sucesso.'
   Npc-not-set: '&cNPC não está definido.'
   Olhar:
   - ''
   - '&7Informações do jogador &f{player}&7:'
   - ''
   - '&fKills: &b{kills}'
   - '&fRank: &b{rank} &7({rank_nome})'
   - ''
   
Upou:
   Msgs:
      Actionbar:
         Ativar: true
         Broadcast: false
         Msg: '&aVocê &7({player})&a upou seu rank de kills &ede {atual} &epara {rank} &7({nome})&a.'
      Title:
         Ativar: true
         Broadcast: false
         Title: '&aRank evoluido'
         Subtitle: '&e{rank} &7({nome})' # placeholder {atual} disponível
      Chat:
         Ativar: true
         Broadcast: false
         # placeholder {atual} disponível
         Msg:
         - ''
         - '&aVocê &7({player})&a evoluiu seu rank para &e{rank} &7({nome})&a.'
         - ''  
         
Setas:
   Voltar:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&cVoltar'
      Lore:
      - ''
      - '&7Clique para voltar.'
      - ''
   Proximo:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&aPróximo'
      Lore:
      - ''
      - '&7Clique para ir à próxima página.'
      - ''
      
Lores:
   Coletar:
      Sobrepor: false
      Lore:
      - ''
      - '&aClique para coletar essa recompensa'
   Ja coletou:
      Sobrepor: true
      Lore:
      - '&cVocê já coletou essa recompensa.'
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

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Ranks:
   Nenhum:
      Ordem: 0
      Tag: '&cNenhum'
      Kills: 0
   Broze:
      Ordem: 1
      Tag: '&7[&6Bronze&7]'
      Kills: 1
   Ferro:
      Ordem: 2
      Tag: '&7[&fFerro&7]'
      Kills: 2
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   1:
      Display:
         CustomSkull: false
         URL: ''
         ID: 388
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Lore: 
         - '&7Mate &f1 &7jogador e ganhe'
         - '&7 -> &a1 pedra.'
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         - '&aTu ganhou uma pedra.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Kills: 1
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'
   2:
      Display:
         CustomSkull: false
         URL: ''
         ID: 388
         Data: 0
         Glow: true
         Name: '&8Diamantes'
         Lore: 
         - '&7Mate &f2 &7jogadores e ganhe'
         - '&7 -> &a2 diamantes.'
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Kills: 2
      Command:
         Use: true
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} diamond 2'

]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/28-yKillRank">Site do plugin yKillRank</a>
    </category>
</seealso>