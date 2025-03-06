# yGuerra
<secondary-label ref="utility"/>

### Descrição
Crie eventos pvp e agite seu servidor com itens setados ou não!

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
<video src="//www.youtube.com/watch?v=fWmaoeTu8Dg"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/guerra - Abre o menu principal
/guerra iniciar - Inicia um evento
/guerra parar - Para o evento atual
/guerra pvp - Ativa
/Desativa o PVP do evento
/guerra admin - Abre o menu principal do admin
/guerra kickplayer - Kicka o jogador do evento
/guerra kickclan - Kicka o clan do evento
/guerra banplayer - Ban um jogador de um evento específico
/guerra banclan - Ban um clan de um evento específico
/guerra unbanplayer - Desbane um jogador de um evento específico
/guerra unbanclan - Desbane um clan de um evento específico
/guerra apostar - Aposta em um clan
/jogador
/guerra camarote - Vai para o camarote
/guerra forcardm - Força o deathmatch da guerra.
/guerra sopa - Seta os itens da placa de sopa
/guerra ajuda - Mostra a mensagem de ajuda.
/guerra info - Mostra a mensagem do informativo.
/guerra add - Adiciona novos jogadores a guerra.
/guerra puxar - Puxa o jogador da guerra para sua localização.
/guerra reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yguerra.usar - Permissão para o /guerra
yguerra.admin - Permissão para o /guerra admin
yguerra.iniciar - Permissão para o /guerra iniciar
yguerra.parar - Permissão para o /guerra parar
yguerra.pvp - Permissão para o /guerra pvp
yguerra.kickplayer - Permissão para o /guerra kickplayer
yguerra.kickclan - Permissão para o /guerra kickclan
yguerra.banplayer - Permissão para o /guerra banplayer
yguerra.banclan - Permissão para o /guerra banclan
yguerra.unbanplayer - Permissão para o /guerra unbanplayer
yguerra.unbanclan - Permissão para o /guerra unbanclan
yguerra.apostar - Permissão para o /guerra apostar
yguerra.camarote - Permissão para o /guerra camarote
yguerra.forcardm - Permissão para o /guerra forcardm
yguerra.ajuda - Permissão para o /guerra ajuda
yguerra.info - Permissão para o /guerra info
yguerra.add - Permissão para o /guerra add
yguerra.pull - Permissão para o /guerra puxar
yguerra.sopa - Permissão para o /guerra sopa
yguerra.reload - Permissão para o /guerra reload
yguerra.vanish.bypass - Permissão para ver os jogadores no camarote</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yguerra_[nome_do_evento]% - Retorna a tag do evento.&nbsp;(Altere o nome_do_evento pelo nome do arquivo do tipo, exemplo: gladiador.)
%yguerra_clans% - Retorna as tags dos clans da guerra
%yguerra_clans_quantia% - Retorna a quantia de clans na guerra
%yguerra_jogadores% - Retorna a quantia de jogadores na guerra
%yguerra_jogadores_clan% - Retorna a quantia de jogadores do clan do player na guerra
%yguerra_fogoamigo% - Retorna o fogo amigo da guerra
%yguerra_duracao% - Retorna o tempo da guerra
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{nome_do_evento} - Retorna a tag do evento.&nbsp;(Altere o nome_do_evento pelo nome do arquivo do tipo, exemplo: gladiador.)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yGuerra/
    ├── menus/
    │    ├── clansbanidos.yml
    │    ├── clansparticipando.yml
    │    ├── informacoes.yml
    │    ├── jogadoresbanidos.yml
    │    ├── jogadoresparticipando.yml
    │    ├── ocorrendo.yml
    │    ├── principal.yml
    │    └── top.yml
    ├── tipos/
    │    └── gladiador.yml
    ├── config.yml
    └── discord.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="clansbanidos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Guerra - Clans Banidos'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
#
Item:
   Banner: true
   CustomSkull: false
   URL: ''
   ID: 0
   Data: 0
   Glow: false
   Name: '&f{clan}'
   Lore:
   - '&7Banido dos eventos: &f{eventos}&7.'

]]>
</code-block>
</chapter>

<chapter title="clansparticipando.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Clans participando'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31

Item:
   Banner: true
   CustomSkull: false
   URL: ''
   ID: 0
   Data: 0
   Name: '&f{clan}'
   Lore:
   - '&7Kills: &a{kills}&7.'
]]>
</code-block>
</chapter>

<chapter title="informacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Guerra - Informações'
Tamanho: 45
Backslot: 40
Itens:
   Gladiador:
      Slot: 11
      CustomSkull: false
      URL: ''
      ID: 276
      Data: 0
      Glow: false
      Name: '&aGladiador'
      Lore:
      - ''
      - '&fFogo amigo: &cDesativado'
      - '&fItens setados: &aAtivado'
      - ''
      - '&7Horários:'
      - ' &fTodo dia'

]]>
</code-block>
</chapter>

<chapter title="jogadoresbanidos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Guerra - Jogadores Banidos'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
#
Item:
   CustomSkull: true
   URL: '{player}'
   ID: 0
   Data: 0
   Glow: true
   Name: '&f{player}'
   Lore:
   - '&7Banido dos eventos: &f{eventos}&7.'

]]>
</code-block>
</chapter>

<chapter title="jogadoresparticipando.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Jogadores participando'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31

Item:
   CustomSkull: true
   URL: '{player}'
   ID: 0
   Data: 0
   Name: '&7[{clan}&7] &f{player}'
   Lore:
   - '&fKills: &a{kills}&f.'

]]>
</code-block>
</chapter>

<chapter title="ocorrendo.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Guerra - Ocorrendo'
Tamanho: 27
Back slot: 18
EntrarSair slot: 16
Itens:
   Informacoes:
      Slot: 10
      CustomSkull: false
      URL: ''
      ID: 276
      Data: 0
      Glow: false
      Name: '&aInformações'
      Lore:
      - ''
      - '&7Fogo amigo: &f{fogoamigo}&7.'
      - '&7Itens setados: &f{setados}&7.'
      - '&7Tempo decorrido: &f{duracao}&7.'
      - ''
      - '&7Jogadores participando: &a{jogadores}&7.'
      - '&7Clans participando: &a{clans}&7.'
   Jogadores:
      Slot: 12
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/723863981895b104c1b29c9f5f427ae0a0ede464584587068fb1593a27d'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aJogadores'
      Lore:
      - '&7Clique para ver os jogadores participando.'
   Clans:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/4571b004409ae2d5b3b95f0bace50207eef9ece866f050540e293dbf632329fd'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aClans'
      Lore:
      - '&7Clique para ver os clans participando.'
   Entrar:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/2c9e601ed9198dbb34c51ddf323929f01a5f958ab11133e3e0407b698393b3f'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aEntrar'
      Lore:
      - '&fCusto para entrar &7(jogador)&f: &a{money}&f.'
      - '&fCusto para entrar &7(banco)&f: &a{banco}&f.'
      - ''
      - '&7Clique para participar.'
   Sair:
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/c532576b8bc9a876419a39ae4498c456fe9ee5bdc7ba91fd3b2f1b0a7eb91'
      ID: 1
      Data: 0
      Glow: true
      Name: '&cSair'
      Lore:
      - '&7Clique para sair.'
   Em andamento:
      CustomSkull: false
      URL: ''
      ID: 166
      Data: 0
      Glow: true
      Name: '&cEM ANDAMENTO'
      Lore:
      - '&7Você não pode mais entrar no evento.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> SAIR:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Guerra - Principal'
Tamanho: 27
Back slot: 18
Itens:
   Perfil:
      Slot: 10
      CustomSkull: true
      URL: '{player}'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aInformações'
      Lore:
      - ''
      - '&7Participou &f{participou} &7vezes do gladiador.'
      - '&7Ganhou &f{ganhou} &7vezes o gladiador.'
      - ''
      - '&7Kills: &a{kills}&7.'
      - '&7Mortes: &c{mortes}&7.'
      - ''
   Informacoes:
      Slot: 12
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: false
      Name: '&aInformações'
      Lore:
      - '&7Clique para ver as informações dos eventos.'
   Top:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/15a7ee9a86de203674a93b570bc8992e500363dd32f2b9813daaeeabccf92151'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aTop'
      Lore:
      - '&7Clique para ver o top clans e jogadores.'
   Jogadores banidos:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/744b887a2b5523916a8552fb536f740e173a35bca9b7ebac584b14c7f814a3db'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aJogadores banidos'
      Lore:
      - '&7Clique para ver os jogadores banidos e os'
      - '&7respectivos eventos.'
   Clans banidos:
      Slot: 16
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/e55227f2f99abf6155ea13f41fb3b0efb721d4bdcdff49478451809588277c6d'
      ID: 1
      Data: 0
      Glow: true
      Name: '&aClans banidos'
      Lore:
      - '&7Clique para ver os clans banidos e os'
      - '&7respectivos eventos.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> CLANS BANIDOS:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Guerra'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item player:
   CustomSkull: true
   URL: '{player}'
   ID: 0
   Data: 0
   Name: '&f{player}'
   Lore:
   - ''
   - '&fVitórias: &e{vitorias}'
   - '&fPosição: &e{pos}º'
   - ''
   
Item clan:
   Banner: true
   CustomSkull: false
   URL: ''
   ID: 0
   Data: 0
   Name: '&f{clan} &8- &7{pos}'
   Lore:
   - ''
   - '&fVitórias: &e{vitorias}'
   - '&fPosição: &e{pos}º'
   - ''

Seletor:
   Slot: 31
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
   ID: 0
   Data: 0
   Name: '&aSeletor do TOP'
   
Formato:
   Visualizando: ' &f• &a{nome}'
   Selecionar: ' &f• &7{nome}'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="tipos" collapsible="true">
<chapter title="gladiador.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Comando:
  Comando: 'gladiador'
  Aliases: [ gladiadores, gladiator ]

Minimo clans: 2
Minimo jogadores: 2

# Máximo de clans
# Deixe 0 para ser infinito
Maximo clan: 0

# Máximo de jogadores por clan
# Deixe 0 para ser infinito
Maximo jogador clan: 0

# Máximo de jogadores no evento
Maximo jogador: 0

# Precisa de clan pra entrar
Precisa de clan: true

# Deixa os jogadores apostarem
Aposta: true

# Ativar o teleporte para a sala de espera
Sala de espera: false

# O jogador perder os itens ao morrer/deslogar/sair
Perder itens: true

# Permitir o jogador de dropar itens do inventário no chão
Player drop: false

# comando para executar no jogador que mais matou
Comando mais matou: [ 'mito setar {player}' ]
#
Temporizador:
  Chamadas:
    Quantia: 3
    Tempo: 10
  Iniciado:
    Tempo: 20
  Finalizar:
    Tempo: 20
  Informativo: 20 # tempo entre cada anúncio
  Deathmatch:
    # Tempo para iniciar o deathmatch
    # Ele começa a contar o tempo quando o evento inicia.
    # Em segundos
    # deixe 0 para desativar
    Tempo: 600
    # Delay para começar o pvp do deathmatch
    # em segundos
    Delay: 5
    # Minimo de clans para iniciar automaticamente
    # deixe 0 para não usar
    Minimo clans: 0
    # Minimo de jogadores para iniciar automaticamente
    # deixe 0 para não usar
    Minimo jogadores: 0
#
Bloqueadores:
  SpawnMob: false # bloquear o spawn de mobs durante a guerra
  Chat: false # bloquear falar no chat durante a guerra
  Craft: false # bloquear craftar itens durante a guerra
  Fornalha: false # bloquear derreter itens na fornalha durante a guerra
  Funil: false # bloquear o funil transferir itens durante a guerra
#
ClansPermitidos:
  Ativar: false
  # Sempre em caixa alta
  Lista: [ 'YST' ]
#
AutoStart:
  Ativar: true
  Horarios:
    - 'segunda-09:10:1' #dia-hora:minuto:segundo
    - 'terca-09:10:01'
    - 'quarta-09:10:01'
    - 'quinta-09:10:01'
    - 'sexta-09:10:01'
    - 'sabado-09:10:01'
    - 'domingo-09:10:01'
    - 'todos-09:10:01'
#
Scoreboard:
  Ativar: true
  Title: '&b&lyStore'
  Linhas:
    - '&7           Gladiador'
    - ''
    - '&fClans: &b{clans}&f.'
    - '&fJogadores: &b{jogadores}&f.'
    - '&fJogadores do Clan: &b{jogadores_clan}&f.'
    - ''
    - '&fDuração: &b{duracao}&f.'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&b    ystoreplugins.com.br'
#
Borda:
  Ativar: false
  ## use /<tipo> setcentro
  Mundo: ''
  Centro:
    X: 0
    Z: 0
  Tamanho: 1000 # tamanho padrão em blocos
  Dano: 5 # dano da borda
  # tempo decorrido da guerra, tamanho que vai ficar a borda, duração da diminuição da borda (deixe 0 para diminuir instantaneamente)
  Zonas:
    - '10,100,10'
#
Display:
  CustomSkull: false
  URL: ''
  ID: 276
  Data: 0
  Glow: true
  Name: '&aGladiador'
  Lore:
    - '&7Clique para gerenciar o evento gladiador.'
#
Custo:
  Banco: 1000.0 #exclusivo yClans, obriga o player precisar de clan.
  Jogador: 100.0
  RemoverBanco: true # remover o dinheiro do banco ao entrar
  RemoverJogador: true # remover o dinheiro do jogador ao entrar
  Tempo online: 0 #em segundos (exclusivo yTempoOnline)
  #
  Skills: #exclusivo mcMMO, deixe ( Skills: [] ) para não usar
    - 'SWORDS:1' #nome:level
#
Fogo amigo: false #simpleclans é sempre desativado.
Itens setados: true
Dropar itens: false #ao morrer dropar os itens do inventário
#
Tag:
  Display: '&6[Gladiador]'
  Setar em:
    Apenas quem ganhou: false
    Cargos:
      Lider: true
      Capitao: true #exclusivo yClans
      Confiavel: true #exclusivo yClans
      Membro: true
      Sem clan: true
#
Comandos permitidos:
  - '/g'
  - '/l'
  - '/.'
#
Recompensas:
  Apenas quem ganhou: false
  Dar para todos: true #dar recompensas até para os que já haviam morrido, porém só para os que continuam online
  Cargos:
    Lider:
      - 'give {player} emerald 64'
    #
    Capitao: #exclusivo yClans
      - 'give {player} diamond 64'
    #
    Confiavel: #exclusivo yClans
      - 'give {player} gold_ingot 64'
    #
    Membro: [ ] #deixe [] para não usar
    #
    Sem clan:
      - 'give {player} wood 64'
#
#
Efeitos:
  Ativar: false
  Lista:
    - 'INVISIBILITY:1-100' #efeito:level-tempo
#
#
Mensagens:
  Chamada:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fChamada para participar'
    - ''
    - '&fDigite &b/guerra &7para entrar.'
    - '&fClans participando: &b({clans_quantia}) &8- &7{clans}&f.'
    - '&fJogadores participando: &b{jogadores}'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&7Chamada &f{min} &7de &f{max}&7 ({tempo}).'
    - ''
    - '&b----------------------------------------------'
  Iniciado:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento iniciado'
    - ''
    - '&fClans participando: &b({clans_quantia}) &8- &7{clans}&f.'
    - '&fJogadores participando: &b{jogadores}'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&7Os clans tem &f{tempo} &7para se prepararem.'
    - ''
    - '&b----------------------------------------------'
  Liberado:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento Liberado'
    - ''
    - '&fClans participando: &b({clans_quantia}) &8- &7{clans}&f.'
    - '&fJogadores participando: &b{jogadores}'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&7Os clans podem se matar.'
    - ''
    - '&b----------------------------------------------'
  Insuficiente:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento cancelado'
    - ''
    - '&fClans insuficientes ou jogadores insuficientes.'
    - ''
    - '&b----------------------------------------------'
  Deu errado clan:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento cancelado'
    - ''
    - '&fAlgo deu errado ao premiar, ao que parece'
    - '&ftodos os clans morreram.'
    - ''
    - '&b----------------------------------------------'
  Deu errado jogador:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento cancelado'
    - ''
    - '&fAlgo deu errado ao premiar, ao que parece'
    - '&ftodos os jogadores morreram.'
    - ''
    - '&b----------------------------------------------'
  Operador:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento cancelado'
    - ''
    - '&cCancelado por um operador.'
    - ''
    - '&b----------------------------------------------'
  Ganhar clan:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento finalizado'
    - ''
    - '&fClan ganhador: &b{clan}&f.'
    - '&fAbates do clan: &b{abates}&f.'
    - '&fJogadores do clan: &b{jogadores}&f.'
    - '&fA guerra durou: &b{duracao}&f.'
    - ''
    - '&fOs jogadores têm &b{tempo} &fsegundos para'
    - '&fse organizar e abrir espaço no inv para as'
    - '&frecompensas.'
    - ''
    - '&b----------------------------------------------'
  Ganhar player:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fEvento finalizado'
    - ''
    - '&fJogador ganhador: &b{player}&f.'
    - '&fAbates do jogador: &b{abates}&f.'
    - '&fA guerra durou: &b{duracao}&f.'
    - ''
    - '&fO jogador tem &b{tempo} &fsegundos para'
    - '&fse organizar e abrir espaço no inv para as'
    - '&frecompensas.'
    - ''
    - '&b----------------------------------------------'
  Teleportado dm:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador | &fDeathmatch'
    - ''
    - '&fClans participando: &b({clans_quantia}) &8- &7{clans}&f.'
    - '&fJogadores participando: &b{jogadores}'
    - '&fTempo decorrido: &b{duracao}&f.'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&7Todos os jogadores foram teleportados para o deathmatch.'
    - ''
    - '&b----------------------------------------------'
  Informativo:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador'
    - ''
    - '&fClans participando: &b({clans_quantia}) &8- &7{clans}&f.'
    - '&fJogadores participando: &b{jogadores}'
    - '&fTempo decorrido: &b{duracao}&f.'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&cAlgumas funções foram desativadas!'
    - ''
    - '&b----------------------------------------------'
  InfoComando:
    - '&b----------------------------------------------'
    - ''
    - '&b&lGladiador'
    - ''
    - '&fClans participando: &b({clans_quantia}) &8- &7{clans}&f.'
    - '&fJogadores participando: &b({jogadores_quantia}) &8- &7{jogadores}&f.'
    - '&fTempo decorrido: &b{duracao}&f.'
    - ''
    - '&fFogo Amigo: {fogoamigo}'
    - '&fItens setados: {setados}'
    - ''
    - '&cAlgumas funções foram desativadas!'
    - ''
    - '&b----------------------------------------------'
#
#
Actionbar:
  Iniciando: '&fIniciando gladiador em &b{tempo}&f.' #deixe '' para não usar
  Entrar: '&fDigite &b/guerra &7para &aentrar&f.' #deixe '' para não usar
  Morreu: '&7{morreu} &celiminado por &7{matou}&c, kills: &7{kills}&c. Restam: &7{vivos}&c.' #deixe '' para não usar
#
# os locais são setados in-game, não altere nada aqui
Locais:
  Saida: 'none'
  Entrada: 'none'
  Espera: 'none'
  Camarote: 'none'
  Deathmatch: 'none'
#
# os itens são setados in-game, não altere nada aqui
Itens:
Capacete:
Peitoral:
Calca:
Botas:
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
#
#
#
#Use: yClans, AtlasClans, SimpleClans, AtlasFactions, AtlasFactionsV2, UltimateClans, StormClans ou Factions
Plugin de clan: 'yClans'
# Ativar o hook com o Vault para usar um plugin de economia
VaultHook: true
# Bloquear o teleporte se estiver no evento
BlockTp: true
# Teleportar ao centro quando sair da borda enquanto ela estiver se movendo
TeleportOutside: false
#
#
Comando:
   Comando: 'guerra'
   Aliases: [ war ]
#
#
# Sistema de sopas
Sopa:
   # Vai funcionar apenas dentro do evento
   Ativar: true
   # quantia de vida que irá curar, o jogador possui 20 por padrão
   Curar: 3
   # Mundos em que ao interagir com botão direito em uma sopa, irá reparar vida
   Mundos:
      - 'world'
   # Configuração da placa
   # digite [sopa] na primeira linha da placa e salva
   Linha1: ''
   Linha2: '&1Pegue aqui'
   Linha3: '&1sua sopa'
   Linha4: ''
#
#
Mensagens:
   Permissao: '&cVocê não tem permissão para isto.'
   Itens configurados: '&aItens do evento &7{tipo} &aconfigurados.'
   Item configurado: '&aItem &7{item}&a do evento &7{tipo} &aconfigurado.'
   Sopa configurado: '&aItens da placa de sopa configurados.'
   Item nao setado: '&cEste item &7({item})&c não foi setado.'
   Pegou item: '&aVocê pegou o item.'
   Item nao compativel: '&cVocê não está segurando um {tipo}.'
   Local configurado: '&aLocal &7{local}&a do evento &7{tipo} &aconfigurado.'
   Local nao setado: '&cEste local &7({local}) &cnão foi setado.'
   Teleportado: '&aVocê foi teleportado.'
   Saiu: '&cVocê saiu do evento.'
   Nao ativo: '&cO evento não está ativo.'
   Nao pode: '&cVocê não pode mais entrar no evento.'
   Esvazie: '&cEsvazie seu inventário.'
   Leve: '&cVocê deve levar itens.'
   Sem money: '&cSem money suficiente: &f{money}&c.'
   Sem clan: '&cVocê não possui clan.'
   Sem money banco: '&cSeu clan não tem money no banco suficiente: &f{money}&c.'
   Entrou: '&aVocê entrou no evento.'
   Ja ocorrendo: '&cJá há um evento ocorrendo.'
   Local nulo: '&cAlgum dos principais locais (Saída, Espera, Entrada) estão nulos.'
   Iniciado: '&aEvento &7{tipo}&a iniciado.'
   Esta banido: '&cVocê está banido deste evento.'
   Clan banido: '&cSeu clan está banido deste evento.'
   Nao encontrado: '&cClan ou jogador não encontrado.'
   Kickado: '&cVocê foi kickado do evento.'
   Kickado clan: '&cSeu clan foi kickado do evento.'
   Kickado staff: '&aJogador &7{player} &akickado do evento.'
   Kickado staff clan: '&aClan &7{clan} &akickado do evento.'
   Banido: '&cVocê foi banido do evento.'
   Banido clan: '&cSeu clan foi banido do evento.'
   Banido staff: '&aJogador &7{player} &abanido do evento &7{tipo}&a.'
   Ja banido: '&cEste jogador/clan já está banido deste evento.'
   Banido staff clan: '&aClan &7{clan} &abanido do evento &7{tipo}&a.'
   Nao banido: '&cEste jogador/clan não está banido deste evento.'
   Desbanido: '&aJogador &7{player}&a desbanido do evento &7{tipo}&a.'
   Desbanido clan: '&aClan &7{clan}&a desbanido do evento &7{tipo}&a.'
   Aposta devolvida: '&aSua aposta no valor de &7{money}&a foi devolvida.'
   Aposta player nao: '&cEste player não está participando do evento.'
   Aposta clan nao: '&cEste clan não está participando do evento.'
   Aposta nao si: '&cVocê não pode apostar nem em você nem em teu clan.'
   Nao e numero: '&cO argumento não é um número.'
   Aposta realizada: '&aAposta realizada com sucesso.'
   Comando: '&cVocê não pode utilizar este comando no evento.'
   Camarote nao setado: '&cO camarote deste evento não está setado.'
   Teleportado camarote: '&aTeleportado ao camarote.'
   Tempo erro: '&cVocê deve estar online por pelo menos {tempo} antes de participar desse evento.'
   Mcmmo erro: '&cVocê deve ter &7{level}&c na skill &7{skill}&c para participar desse evento.'
   Nao pode apostar: '&cVocê não pode apostar nesse evento.'
   Apostas encerradas: '&cAs apostas já foram encerradas.'
   Lotou jogador: '&cA quantia de jogadores participando já chegou no limite.'
   Lotou jogador clan: '&cA quantia de jogadores participando do seu clan já chegou no limite.'
   Lotou clan: '&cA quantia de clans participando já chegou no limite.'
   Deathmatch setado: '&cO local do deathmatch não foi setado.'
   Deathmatch ja: '&cO deathmatch já está ocorrendo.'
   Deathmatch forcado: '&aVocê forçou o start do deathmatch.'
   Craft: '&cO craft de itens está desabilitado durante o evento.'
   Chat: '&cFalar no chat está desabilitado durante o evento.'
   Borda: '&aMundo e centro da borda do evento definida com sucesso.'
   ClanPermitido: '&cSeu clan não está permitido de participar.'
   Pvp-on: '&aVocê ativou o PVP no evento.'
   Pvp-off: '&aVocê desativou o PVP no evento.'
   Pvp-info: '&aO evento está com o PVP desativado.'
   Add-able: '&cO evento ainda pode ser acessado.'
   Add-already: '&cEste jogador {player} já está no evento.'
   Add-added: '&aEste jogador {player} foi adicionado no evento.'
   Pull-all: '&aTodos os jogadores foram puxados.'
   Pull-player: '&aJogador {player} puxado.'
   Ajuda:
      - '&b-> Comandos do guerra <-'
      - ''
      - '&b > &f/guerra'
      - '&b > &f/guerra apostar'
      - '&b > &f/guerra camarote'
      - '&b > &f/guerra admin'
      - '&b > &f/guerra iniciar'
      - '&b > &f/guerra parar'
      - '&b > &f/guerra forcardm'
      - '&b > &f/guerra kickplayer'
      - '&b > &f/guerra kickclan'
      - '&b > &f/guerra banplayer'
      - '&b > &f/guerra banclan'
      - '&b > &f/guerra unbanplayer'
      - '&b > &f/guerra unbanclan'
   Ja apostou player:
   - ''
   - '&cVocê ja realizou sua aposta.'
   - ''
   - '&7Apostou no jogador: &f{player}&7.'
   - '&7Valor da aposta: &f{money}&7.'
   - ''
   Ja apostou clan:
   - ''
   - '&cVocê ja realizou sua aposta.'
   - ''
   - '&7Apostou no clan: &f{clan}&7.'
   - '&7Valor da aposta: &f{money}&7.'
   - ''
#
#
#
Setas:
   Voltar:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&cVoltar'
      Lore:
      - '&7Clique para voltar ao menu ou página anterior.'
   Proximo:
      CustomSkull: false
      URL: ''
      ID: 262
      Data: 0
      Glow: true
      Name: '&aPróxima'
      Lore:
      - '&7Clique para ir à próxima página.'
#
#
#
Formatador:
   B true: '&aSim'
   B false: '&cNão'
#
#
#
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

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Options:
  URL: ''
  Username: 'yGuerra'
  Ativar: false
Embeds:
  evento_glad:
    Tipo: 'gladiador.yml'
    Title: 'Evento iniciando...'
    Thumbnail: ''
    Color: '#fff'
    Content: 'Está começando o evento gladiador!\n@everyone'
    Image: ''
    Footer:
      Text: 'Todos os direitos reservados'
      Image: ''
    Fields:
      evento:
        Inline: false
        Header: 'Evento'
        Content: 'Gladiador'
      comecando:
        Inline: false
        Header: 'Começa em'
        Content: '30 segundos'
      server:
        Inline: false
        Header: 'Servidor'
        Content: 'RankUP'
      data:
        Inline: false
        Header: 'Data'
        Content: '{data} - {hora}'
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static GuerraAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;GuerraAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(GuerraAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/20-yGuerra">Site do plugin yGuerra</a>
    </category>
</seealso>