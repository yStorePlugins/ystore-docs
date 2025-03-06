# yKillSystem
<secondary-label ref="utility"/>

### Descrição
Dê um UP! no pvp do teu servidor.

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
<video src="//www.youtube.com/watch?v=EMlxHRfg3zM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/kills - Abre o menu principal
/kills [player]  - Ver as informações de um jogador
/kills help  - Ver todos os comandos disponíveis
/kills setxp - Seta xp para um ou todos os jogadores
/kills addxp  - Adicionar xp para um ou todos os jogadores
/kills delxp  - Remover xp de um ou todos os jogadores
/kills resetkdr - Resetar o kdr
/abates
/mortes de um ou todos os jogadores
/kills giveresetkdr - Dar o item de resetkdr para um jogador
/kills addrank - Adiciona rank para um jogador
/kills delrank -  Remove rank de um jogador
/kills setrank -  Seta rank para um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ykillsystem.usar - Permissão para o /kills
ykillsystem.ver - Permissão para o /kills</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ykillsystem_kills% - Retorna a quantia de kills do jogador.
%ykillsystem_deaths% - Retorna a quantia de mortes do jogador.
%ykillsystem_kdr% - Retorna o KDR do jogador.
%ykillsystem_xp% - Retorna a quantia de XP do jogador (formatado).
%ykillsystem_xp_raw% - Retorna a quantia de XP do jogador (sem formatar).
%ykillsystem_tag% - Retorna a tag do rank do jogador.
%ykillsystem_nome% - Retorna o nome do rank do jogador.
%ykillsystem_next% - Retorna a tag do próximo rank.
%ykillsystem_streak% - Retorna o killstreak do jogador.
%ykillsystem_progressbar% - Retorna a barra de progresso do jogador.
%ykillsystem_porcentagem% - Retorna a porcentagem de progresso do jogador.
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{kill_tag} - Retorna a tag do rank do jogador.
{kill_nome} - Retorna o nome do rank do jogador.
{kill_kills} - Retorna as kills do jogador.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yKillSystem/
    ├── menus/
    │    ├── informacoes.yml
    │    ├── missoes.yml
    │    ├── principal.yml
    │    ├── ranks.yml
    │    └── top.yml
    ├── bonus.yml
    ├── config.yml
    ├── loja.yml
    ├── matar.yml
    ├── missoes.yml
    ├── morrer.yml
    ├── ranks.yml
    └── roubar.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="informacoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8KillRank - Informacoes'
Tamanho: 27
Toggle slot: 11
Itens:
  Perfil:
    Slot: 10
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aInformações de {player}'
    Lore:
      - ''
      - '&fRank: {rank}&f.'
      - '&fPróximo rank: {proximo_rank}&f.'
      - '&fProgresso: {progressbar} &8({porcentagem})'
      - '&fK/D: &b{kdr} &7(&a{kills}&7/&c{deaths}&7)'
      - '&fCríticos: &7({criticos})&f / &bNormais: &7({hits})&f.'
      - ''
      - '&fBônus: &a{bonus}%&f.'
      - '&fXP: &a{xp}&f.'
      - ''
]]>
</code-block>
</chapter>

<chapter title="missoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Missões de combate'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 0
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8KillRank - Principal'
Tamanho: 27
Toggle slot: 11
Itens:
  Perfil:
    Slot: 10
    CustomSkull: true
    URL: '{player}'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aSuas informações'
    Lore:
      - ''
      - '&fSeu rank: {rank}&f.'
      - '&fPróximo rank: {proximo_rank}&f.'
      - '&fProgresso: {progressbar} &8({porcentagem})'
      - '&fK/D: &b{kdr} &7(&a{kills}&7/&c{deaths}&7)'
      - '&fCríticos: &7({criticos})&f / &bNormais: &7({hits})&f.'
      - ''
      - '&fSeu bônus: &a{bonus}%&f.'
      - '&fXP: &a{xp}&f.'
      - ''
  Toggle on:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/8e9b27fccd80921bd263c91dc511d09e9a746555e6c9cad52e8562ed0182a2f'
    ID: 1
    Data: 0
    Glow: false
    Name: '&aProteção'
    Lore:
      - '&fEstado: &aAtivo&f.'
      - ''
      - '&7Você não poderá levar dano e bater em jogadores.'
  Toggle off:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
    ID: 1
    Data: 0
    Glow: false
    Name: '&aProteção'
    Lore:
      - '&fEstado: &cDesativado&f.'
      - ''
      - '&7Você poderá levar dano e bater em jogadores.'
  Top:
    Slot: 13
    CustomSkull: false
    URL: ''
    ID: 340
    Data: 0
    Glow: false
    Name: '&aTOP'
    Lore:
      - '&7Clique para ver o TOP Jogadores.'
  Loja:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/7e3deb57eaa2f4d403ad57283ce8b41805ee5b6de912ee2b4ea736a9d1f465a7'
    ID: 1
    Data: 0
    Glow: false
    Name: '&aLoja'
    Lore:
      - '&7Clique para acessar a loja.'
  Missoes:
    Slot: 15
    CustomSkull: false
    URL: ''
    ID: 54
    Data: 0
    Glow: false
    Name: '&aMissões'
    Lore:
      - '&7Clique para gerenciar as missões.'
  Ranks:
    Slot: 16
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aRanks'
    Lore:
      - '&7Clique para acessar o menu de ranks.'
  #Custom1:
  #  Slot: 17
  #  Comando: 'kill {player}'
  #  Material: '152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
  #  Name: '&aCustomizado'
  #  Lore: []
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Lista de ranks'
Tamanho: 27
Slots: [ 10, 11, 12, 13, 14, 15 ]
BackSlot: 0
VoltarSlot: 18
ProximoSlot: 26
# Quando não tiver nenhum rank cadastrado.
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
# Ranks que estarão visíveis no menu
Itens:
  item1:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/a54947de7f52598255d6afee9d77befad9b4f24c0c4663d28bcdf8a6457f34'
    ID: 0
    Data: 0
    Glow: true
    Name: '&6Rank Bronze'
    Lore:
      - '&7Informações deste rank:'
      - ''
      - '&7> &f Dado ao cadastrar.'
      - ''
  item2:
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/1ad5424d9903953843526a7c416866e7d79501c88ce7cdabeee5284ea39f'
    ID: 0
    Data: 0
    Glow: true
    Name: '&fRank Ferro'
    Lore:
      - '&7Informações deste rank:'
      - ''
      - '&6 Bronze -> &fFerro'
      - ' &f Preço: &750 XP&f.'
      - ''

]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Combate'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 30
AnteriorSlot: 9
ProximoSlot: 17
# Item do top XP
Item xp:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fXP: &7{xp}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top KDR
Item kdr:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fK/D: &7{kdr}'
    - '&fPosição: &e{pos}º'
    - ''
# Item do top Kills
Item kills:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&f{player}'
  Lore:
    - ''
    - '&fAbates: &7{kills}'
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
  XP:
    Ativar: true
    Nome: 'XP'
  KDR:
    Ativar: true
    Nome: 'KDR'
  Kills:
    Ativar: true
    Nome: 'Kills'
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
Bonus:
  membros:
    Ordem: 1
    Permissao: 'ykillsystem.membro'
    Display: '&7[Membro]'
    Bonus: 10.0 # em % do valor total
]]>
</code-block>
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
# Comandos e aliases do plugin
Comando:
  Comando: 'kills'
  Aliases: []
#Coloque Legendchat, OpeNChat (ou nChat), UltimateChat, NoxusChat ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'
# Mundos onde os sistemas não irão funcionar
# Sistemas: AntiFreeKill, Dominando, KillStreak, LostXp, Roubar, PvPToggle
Mundo blacklist:
  - 'nenhum'
# Configuração da barra de progresso
Progress bar:
  Quantia: 10
  Simbolo: ':'
  Cor sim: '&a'
  Cor nao: '&7'
# Algumas opções gerais do plugin:
Opcoes:
  # Acumular os bônus que tiver permissão
  Acumular bonus: false
  # Caso for staff ficar com a tag no chat e no placeholderapi invisível
  # Permissão: (ykillsystem.staff)
  Staff invisivel: false
  # Ativar o sistema de ranks
  Ranks: true
  # Barra de corações abaixo do nome do jogador
  Healthbar:
    Ativar: true
    Icone: '&c❤'
  # Quando ativo, o jogador poderá ativar e usar até o tempo acabar.
  # Ele não poderá levar dano ou bater, mesmo em áreas de pvp on.
  Toggle:
    Ativar: true
    # Deixar o toggle com tempo infinito
    Infinito: false
    # Ativar o toggle ao registrar
    Registro: true
    # Comando para ativar o toggle (deixe '' para não usar)
    Cmd ativar: '/pvp on'
    # Comando para desativar o toggle (deixe '' para não usar)
    Cmd desativar: '/pvp off'
    Tempo: 20
    # Deixe '' para não usar
    Actionbar: '§cVocê ainda tem {tempo} de proteção.'
    # Deixe '' para não usar
    Actionbar infinito: '§cVocê está com a proteção contra pvp ativada.'
  # Evitar ganhar XP e Coins, killstreak ao matar o jogador 2x ou mais seguidas.
  AntiFreeKill: true
  # Quando um jogador matar outro por x vezes (minimo definido)
  # irá enviar a mensagem para o morto e para o matador.
  Dominar:
    Ativar: true
    Minimo: 1
  # Quando o jogador fizer x kills (minimo definido)
  # irá enviar mensagem para o broadcast e/ou para o jogador, informando
  # que ele está fazendo uma série de kills (matando muito)
  Killstreak:
    Ativar: true
    Minimo: 2
    # Deixe '' para não usar alguma das duas.
    Broadcast: '&aO jogador &f{player}&a está com um &nkillstreak&a de &6{kills} &a&nkills&a.'
    Player: '&aVocê está com um &nkillstreak&a de &6{kills} &a&nkills&a.'
    # Estes serão os efeitos dado para cada killstreak
    Efeitos:
      Ativar: true
      Lista:
        - 'SPEED:1-100' # Efeito:LEVEL-segundos
# Mensagens em actionbar do plugin
Actionbar:
  # Deixe vazio ( '' ) caso não queira usar alguma
  # A placeholder {bonus} irá usar a do formatador.
  Matou player: '&aVocê ganhou &7{xp} XP &apor matar &7{player}&a. {bonus}'
  Matou mob: '&aVocê matou um mob e ganhou &7{xp} &aXP. {bonus}'
# Mensagens no chat do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Suficiente xp: '&cVocê não tem XP suficiente &6{xp}&c.'
  Suficiente money: '&cVocê não tem money suficiente &6{money}&c.'
  Inv cheio: '&cSeu inventário está cheio. Necessário &f{quantia}&c de espaço.'
  Comprou: '&aVocê adquiriu item(ns) na loja de combate.'
  Loja rank: '&cEste item requer um rank que ainda não foi cadastrado.'
  Rank necessario: '&cVocê precisa estar no rank &f{tag}&c para poder comprar este item.' # Disponível variável {tag} e {rank}
  Esgotou: '&cSua proteção do toggle esgotou. Agora você está apto a levar dano de outros jogadores.'
  Ativou toggle: '&aVocê ativou a proteção.'
  Desativou toggle: '&aVocê desativou a proteção.'
  Nao ativar: '&cVocê já usou todo o tempo da proteção.'
  Toggle player: '&cVocê está com a proteção ativa.'
  Toggle target: '&cEste jogar está com a proteção ativa.'
  Coletou: '&aVocê coletou a recompensa da missão.'
  # Deixe vazio ( '' ) caso não queira usar alguma ( Apenas as: Matou player e Matou mob ).
  # A placeholder {bonus} irá usar a do formatador.
  Matou player: '&aVocê matou o jogador &7{player}&a e ganhou &6{money}&a coins! {bonus}'
  Matou mob: '&aVocê ganhou &6{money}&a coins por matar este mob! {bonus}'
  Morreu: '&cVocê perdeu &6{xp}&c XP por ter morrido.'
  Dominando: '&aVocê está dominando o jogador &7{player}&a.'
  Dominado: '&aVocê está sendo dominado pelo jogador &7{player}&a.'
  Nao encontrado: '&cJogador não encontrado.'
  Ja ativo: '&cO toggle já está ativo.'
  Ja desativado: '&cO toggle já está desativado.'
  Nao e numero: '&cO argumento não é um número.'
  Add todos: '&aVocê adicionou &7{quantia} xp&a para todos os jogadores online.'
  Add: '&aVocê adicionou &7{quantia} xp&a para o jogador &7{player}&a.'
  Del todos: '&aVocê removeu &7{quantia} xp&a de todos os jogadores online.'
  Del: '&aVocê removeu &7{quantia} xp&a do jogador &7{player}&a.'
  Set todos: '&aVocê setou &7{quantia} xp&a para todos os jogadores online.'
  Set: '&aVocê setou &7{quantia} xp&a para o jogador &7{player}&a.'
  Help staff: |
    &b-> Comandos disponíveis <-
    &f > &b/kills
    &f > &b/kills &7<player>
    &f > &b/kills &7addxp
    &f > &b/kills &7setxp
    &f > &b/kills &7delxp
    &f > &b/kills &7resetkdr
    &f > &b/kills &7giveresetkdr
    &f > &b/kills &7setrank
    &f > &b/kills &7delrank
    &f > &b/kills &7addrank
    &f > &b/kills &reload
  Help: |
    &b-> Comandos disponíveis <-
    &f > &b/kills
    &f > &b/kills &7<player>
  Reset abates: '&aVocê resetou os abates do jogador &f{player}&a.'
  Reset mortes: '&aVocê resetou as mortes do jogador &f{player}&a.'
  Reset kdr: '&aVocê resetou o kdr do jogador &f{player}&a.'
  Reset abates all: '&aVocê resetou os abates de todos os jogadores.'
  Reset mortes all: '&aVocê resetou as mortes de todos os jogadores.'
  Reset kdr all: '&aVocê resetou o kdr de todos os jogadores.'
  Deu resetkdr: '&aVocê deu x{quantia} ResetKDR para o jogador &7{player}&a.'
  Recebeu resetkdr: '&aVocê recebeu x{quantia} ResetKDR&a.'
  Ativou resetkdr: '&aVocê resetou seu KDR.'
  NaoRank: '&cNão há essa quantia de ranks disponíveis.'
  Definiu: '&aVocê definiu o rank de &f{player}&a para &f{rank}&a.'
# Item para o resetkdr
Resetkdr:
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/1ad6c81f899a785ecf26be1dc48eae2bcfe777a862390f5785e95bd83bd14d'
  ID: 0
  Data: 0
  Glow: false
  Name: '&aReset KDR'
  Lore:
    - '&7Ative para resetar seu KDR.'
# Formatador de mensagens
Formatador:
  Bonus tem: '&7Bônus: &f{bonus}%&7 ({display}&7).'
  Bonus nao tem: ''
  Tag tem: '{tag}'
  Tag nao tem: ''
  Nome tem: '{nome}'
  Nome nao tem: '&7Sem rank'
  Porcentagem: ''
  Progressbar: ''
# Lores das missões
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

<chapter title="loja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Loja:
  Nome: '&8Loja de combate'
  Tamanho: 54
  Back slot: 27
  Items:
    Pedra preciosa:
      Slot: 10
      Preco xp: 10.0
      Preco money: 100.0
      Rank minimo: 0
      CustomSkull: false
      URL: ''
      Name: '&fFerros!'
      Glow: true
      ID: 1
      Data: 0
      Quantia: 64
      Usar lore: false
      Lore:
        - '&fEstes ferros são usados para construir pontes.'
      Usar lore preco: true
      Lore preco:
        - ''
        - '&fPreço:'
        - ' &8> &710 XP&f; &7100 coins&f.'
      Encantamentos: #( deixe - '' caso não queira usar )
        - 'DAMAGE_ALL:1'
      Usar comandos: false
      Comandos:
        - ''
    Diamante:
      Slot: 11
      Preco xp: 20.0
      Preco money: 200.0
      Rank minimo: 1
      CustomSkull: false
      URL: ''
      Name: '&bDiamantes!'
      Glow: true
      ID: 56
      Data: 0
      Quantia: 64
      Usar lore: true
      Lore:
        - '&bEstas são as pedras preciosas mais caras do mundo!'
      Usar lore preco: true
      Lore preco:
        - ''
        - '&fPreço:'
        - ' &8> &720 XP&f; &7200 coins&f.'
      Encantamentos: #( deixe - '' caso não queira usar )
        - ''
      Usar comandos: true
      Comandos:
        - 'give {player} diamond 64'
]]>
</code-block>
</chapter>

<chapter title="matar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Lista dos mobs: https://helpch.at/docs/1.8.8/org/bukkit/entity/EntityType.html
# Você pode configurar quantos mobs quiser.
# Use PLAYER para configurar um player.
Mobs:
  PLAYER:
    # Quantia de money que será dada ao jogador ao matar um PLAYER.
    # Será dado um valor entre o min e max (sem contar o bônus)
    # Só será dado se o jogador tiver a chance. Deixe 100.0 para dar sempre.
    Money:
      Chance: 100.0
      Min: 20.0
      Max: 70.0
    # Quantia de xp que será dada ao jogador ao matar um PLAYER (usado para upar de rank).
    # Será dado um valor entre o min e max (sem contar o bônus)
    # Só será dado se o jogador tiver a chance. Deixe 100.0 para dar sempre.
    Xp:
      Chance: 100.0
      Min: 5.0
      Max: 10.0
  PIG:
    Money:
      Chance: 100.0
      Min: 10.0
      Max: 50.0
    Xp:
      Chance: 50.0
      Min: 1.0
      Max: 5.0
  SKELETON:
    Money:
      Chance: 100.0
      Min: 12.0
      Max: 52.0
    Xp:
      Chance: 100.0
      Min: 2.0
      Max: 6.0
  ZOMBIE:
    Money:
      Chance: 100.0
      Min: 13.0
      Max: 53.0
    Xp:
      Chance: 100.0
      Min: 3.0
      Max: 7.0
]]>
</code-block>
</chapter>

<chapter title="missoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Estas são as missões que poderão ser configuradas.
# Você pode criar quantas quiser
# Os tipos são: Mate x jogadores, Dê x hits críticos em jogadores e Dê x hits em jogadores.
Missoes:
  1:
    Display:
      CustomSkull: false
      URL: ''
      ID: 388
      Data: 0
      Glow: true
      Name: '&8Pedra'
      Lore:
        - '&7Mate &f1 &7jogador&f; &7Dê &f1 &7hit crítico&f; &7Dê &f5 &7hits normais e ganhe'
        - '&7 -> &a1 pedra.'
    # Se o ( Command -> Use ) tiver true, isso não vai funcionar
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Glow: true
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEsta pedra não é apenas uma pedra comum.'
      Enchants: #se não desejar, deixe assim:
        - ''
    Kills: 1
    Criticos: 1
    Hits: 5
    Command:
      Use: false
      # Se o ( Use ) tiver false, isso não funcionar.
      List: []
  2:
    Display:
      CustomSkull: false
      URL: ''
      ID: 388
      Data: 0
      Glow: true
      Name: '&aEsmeralda'
      Lore:
        - '&7Mate &f2 &7jogadores e ganhe'
        - '&7 -> &a1 pedra.'
    # Se o ( Command -> Use ) tiver true, isso não vai funcionar
    Item:
      CustomSkull: false
      URL: ''
      ID: 1
      Data: 0
      Glow: true
      Name: 'Nada'
      Amount: 0
      Lore: []
      Enchants: #se não desejar, deixe assim:
        - ''
    Kills: 2
    Criticos: 0
    Hits: 0
    Command:
      Use: true
      # Se o ( Use ) tiver false, isso não funcionar.
      List:
        - 'give {player} emerald 1'
]]>
</code-block>
</chapter>

<chapter title="morrer.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Quando um jogador com um dos grupos definidos abaixo morrer,
# irá perder entre o Min e o Max de xp
Mortes:
  membro:
    # Permissão para ser reconhecido
    Permissao: 'ykillsystem.morrer'
    # Chance de perder o Xp
    Chance: 100.0
    # Mínimo que poderá ser perdido
    Min: 5
    # Máximo que poderá ser perdido
    Max: 10
]]>
</code-block>
</chapter>

<chapter title="ranks.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Você pode configurar quantos ranks quiser.
# Quando cair de rank, serão enviadas as mensagens e executados
# os comandos do rank para qual ele caiu. Por exemplo:
# se ele caiu de Ferro para Bronze, serão executadas as ações de cair do Bronze.
Ranks:
  bronze:
    # O jogador começa na ordem 0
    Ordem: 0
    # Este será o nome do rank
    Display: 'Bronze'
    # Esta é a tag que irá aparecer no chat e na placeholder do papi
    Tag: '&7[&cBronze&7]'
    # Este é o custo em XP (do plugin) para upar à este rank
    Custo xp: 0.0
    # Comandos a serem executados pelo console quando um jogador evoluir seu rank.
    # Se a ordem for 0, ao se registrar, também serão executados.
    # Deixe - 'none' para não usar
    Comandos evoluiu:
      - 'give {player} grass 1'
    Comandos caiu:
      - 'give {player} diamond 1'
    # Essas mensagens são executadas quando o jogador upar ou cair de rank
    # São executadas também ao registrar.
    Mensagens:
      Actionbar:
        Ativar: true
        Msg evoluiu: '&aO jogador &f{player} &ase registrou.'
        Msg caiu: '&cO jogador &f{player} &ccaiu para o rank &6Bronze&c.'
      Chat:
        Ativar: true
        Msg evoluiu:
          - '&aVocê se registrou.'
        Msg caiu:
          - '&cVocê caiu para o rank &6Bronze&c.'
  ferro:
    Ordem: 1
    Tag: '&7[&fFerro&7]'
    Display: 'Ferro'
    Custo xp: 50.0
    Comandos evoluiu:
      - 'give {player} stone 1'
    Comandos caiu:
      - 'give {player} coal 1'
    Mensagens:
      Actionbar:
        Ativar: true
        Msg evoluiu: '&aO jogador &f{player} &aupou para &fFerro&a.'
        Msg caiu: '&cO jogador &f{player} &ccaiu para o rank &fFerro&c.'
      Chat:
        Ativar: true
        Msg evoluiu:
          - '&aVocê upou para o rank &6Ferro&a.'
        Msg caiu:
          - '&cVocê caiu para o rank &fFerro&c.'
]]>
</code-block>
</chapter>

<chapter title="roubar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Quando um jogador matar outro e o que matou estiver em algum dos grupos
# configurados abaixo, irá roubar uma % de dinheiro do morto.
# Sem ultrapassar o limite máximo.
Roubos:
  vip:
    # Permissão para ser reconhecido
    Permissao: 'ykillsystem.roubar'
    # Chance de conseguir roubar. Deixe 100.0 para sempre conseguir
    Chance: 100.0
    # Porcentagem que será roubada
    Porcentagem: 10.0
    # Maximo que pode roubar de um jogador, deixe 0 para ser infinito.
    Maximo: 100.0
    # Deixe Mensagem roubou: [] para não usar
    Mensagem roubou:
      - ''
      - '&aVocê roubou &6{money} &7( {porcentagem}% ) &ado money do jogador &7{player}&a.'
      - ''
    # Deixe Mensagem roubado: [] para não usar
    Mensagem roubado:
      - ''
      - '&aVocê perdeu &6{money} &7( {porcentagem}% ) &ado money por morrer para o jogador &7{player}&a.'
      - ''
]]>
</code-block>
</chapter>

</chapter>
## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static KillSystemAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;KillSystemAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(KillSystemAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/44-yKillSystem">Site do plugin yKillSystem</a>
    </category>
</seealso>