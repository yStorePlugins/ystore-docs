# yPescaSimples
<secondary-label ref="rankup"/>

### Descrição
Recompense os jogadores com itens e comandos ao pescar

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
<video src="//www.youtube.com/watch?v=MaYkr59Ta2Q"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/simplepesca - Abre o menu principal
/simplepesca ajuda - Envia a mensagem de ajuda
/simplepesca desbugar - Desbugar uma vara
/simplepesca setloc - Setar o local da pesca
/simplepesca givevara - Dar uma vara de pesca à um jogador.
/simplepesca givebooster - Dar um booster à um jogador.
/simplepesca setnpc - Setar o local do NPC.
/simplepesca delnpc - Deleta o local do NPC.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ysimplepesca.usar - Permissão para o /simplepescaysimplepesca.ajuda - Permissão para o /simplepesca ajudaysimplepesca.admin - Permissão para o /simplepesca desbugar, /simplepesca givevara, /simplepesca setloc, /simplepesca setnpc, /simplepesca delnpc, /simplepesca giveboosterysimplepesca.afkbypass - Permissão para não ser detectado no anti - afk</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ysimplepesca_pescados% - Retorna formatado (1K, 1000,00...)
%ysimplepesca_pescados_raw% - &nbsp;Retorna o valor double sem formatação (1.0, 2.0...)
%ysimplepesca_pescados_rodada% - &nbsp;Retorna o valor de recompensas da última vez que começou a pescar, formatado.
%ysimplepesca_pescados_rodada_raw% - Retorna o valor de recompensas da última vez que começou a pescar, sem formatação.
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPescaSimples/
    ├── menus/
    │    ├── preview.yml
    │    ├── principal.yml
    │    └── top.yml
    ├── boosters.yml
    ├── config.yml
    ├── niveis.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Pesca - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 45
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Pesca principal'
Tamanho: 27
Itens:
  Vara:
    Slot: 10
    CustomSkull: false
    URL: ''
    ID: 346
    Data: 0
    Glow: true
    Name: '&aVara de pesca'
    Lore:
      - '&7Clique para pegar sua vara de pesca.'
  Local:
    Slot: 12
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4528ed45802400f465b5c4e3a6b7a9f2b6a5b3d478b6fd84925cc5d988391c7d'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aMundo pesca'
    Lore:
      - '&7Clique para ir ao mundo da pesca.'
  Top:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/15a7ee9a86de203674a93b570bc8992e500363dd32f2b9813daaeeabccf92151'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aTOP'
    Lore:
      - '&7Clique para o top pescadores.'
  Booster sim:
    Slot: 16
    CustomSkull: false
    URL: ''
    ID: 384
    Data: 0
    Glow: true
    Name: '&aBooster'
    Lore:
      - ''
      - '&fBônus: &a{bonus}%&f.'
      - '&fDuração: &b{tempo}&f.'
      - ''
  Booster nao:
    Slot: 16
    CustomSkull: false
    URL: ''
    ID: 374
    Data: 0
    Glow: true
    Name: '&cBooster'
    Lore:
      - '&cVocê não possui nenhum booster ativo.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> TOP:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Pesca'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fPescados: &6{pescados}'
   - '&fPosição: &6{pos}'
   - ''

Item p:
   Slot: 32
   Name: '&7#&f{pos} - &aVocê &7({player})'
   Lore:
   - ''
   - '&fPescados: &6{pescados}'
   - '&fPosição: &6{pos}'
   - ''
]]>
</code-block>
</chapter>

</chapter>

<chapter title="boosters.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Boosters:
   Booster1:
      Tempo: 60 #em segundos
      Bonus: 10.0 #porcentagem a mais
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
 Comando: 'simplepesca'
 Aliases: []

# Opcoes de configuração do NPC
NPC:
 ID: 923284
 Skin: 'TheThunderGod063'
 Holograma:
  Altura: 3.1
  Holograma:
   - '&6Pesca'
   - '&7Veja as informações da pesca.'

# Configurações gerais
Opcoes:
 Tempo pesca: 10 # Tempo para recompensar o jogador (em segundos)
 Raio agua: 10 # Raio de checagem de click na água
 # Verificar se há água por perto na task da pesca
 # pode gerar lag
 Verificar agua: false
 # Mundos onde a pesca é permitida
 Mundos permitidos:
 - 'world'

# Opções de compra
Compra:
 Preco: 100.0
 Mensagem: '&c&lERRO! &cVocê não &7100 &cem coins.'

# Formatar a lore da vara de pesca
# se estiver ativado ficará: 1K, 2K ...
Formatar vara: true

# Delay para comprar/pegar varas
Delay vara: 10 # Segundos

# Defina a NBTTAG das varas para caso queira resetá-las
NBTTag: 'ySimplePesca-Vara'

# Permissão para poder pescar
# deixe '' para não usar
Pescar perm: ''

# Sistema de anti-afk
Antiafk:
 Ativar: true
 Maximo rodadas: 5 # Irá pescar 2 vezes (tempo pesca * 2), ou seja, 20 segundos.

# Mensagens do plugin
Mensagens:
 Permissao: '&c&lERRO! &cVocê não tem permissão para fazer isto.'
 Permissao pescar: '&cVocê não tem permissão para pescar.'
 Setado: '&aNPC da pesca setado com sucesso.'
 Removido: '&aNPC da pesca removido com sucesso'
 Nao setado: '&cO NPC não está setado.'
 Nao cadastrada: '&c&lERRO! &cSua vara de pesca não está cadastrada.'
 Recebeu: '&a&lINFORMATIVO! &aVocê recebeu uma vara de pesca.'
 Desativado automaticamente: '&a&lINFORMATIVO! &aVocê parou de pescar por conta do Anti-AFK.'
 Delay: '&c&lERRO! &cAguarde &e{time} &cpara adquirir uma vara novamente.'
 Local nulo: '&c&lERRO! &cO local ainda não foi setado.'
 Teleportado: '&a&lSUCESSO! &aTeleportado para o mundo pesca.'
 # Deixe : '' para não usar.
 # Enviada o no actionbar
 # Disponível: {recompensas_rodadas} para puxar as que ele pescou em uma rodada de pesca.
 Pescando: '&aVocê está pescando... Recompensas pescadas: &c{recompensas}&a.'
 # Title que irá enviar quando começar a pesca
 # deixe : '' para não usar
 Comecou title: '&ePesca<nl>&aVocê começou a pescar'
 # Title que irá enviar quando paror de pesca
 # deixe : '' para não usar
 Parou title: '&ePesca<nl>&cVocê parou de pescar'
 Nao encontrado: '&cEste jogador não foi encontrado.'
 Nao e numero: '&cO argumento não é um número.'
 Booster recebeu: '&aVocê recebeu &7{quantia} &a booster(s) de drops.'
 Booster deu: '&aVocê deu &7{quantia} &a booster(s) de drops para o jogador &7{player}&a.'
 Acabou booster: '&cSeu booster de drops acabou.'
 Ja esta booster: '&cVocê já está usando um booster.'
 Ativou booster: '&aVocê ativou um booster de drops. Multiplicador: &e{bonus}&a. Tempo: &e{tempo}&a.'
 Comecou:
 - ''
 - '&a&lINFORMATIVO: &aVocê começou a pescar!'
 - ''
 Parou:
 - ''
 - '&c&lINFORMATIVO: &cVocê parou de pescar!'
 - ''
 Ajuda:
 - ''
 - '&bComandos disponíveis:'
 - '&b-> /simplepesca &7- &fAbre o menu principal'
 - '&b-> /simplepesca setnpc &7- &fSeta o local do NPC'
 - '&b-> /simplepesca delnpc &7- &fDeleta o local do NPC'
 - '&b-> /simplepesca setloc &7- &fSeta o local da pesca'
 - '&b-> /simplepesca givevara &7- &fDá uma vara para um jogador'
 - '&b-> /simplepesca givebooster &7- &fDá um booster para um jogador'
 - ''

Booster:
 CustomSkull: false
 URL: ''
 ID: 384
 Data: 0
 Glow: true
 Name: '&aBônus de pesca'
 Lore:
  - ''
  - '&aTempo: &e{tempo}'
  - '&aPorcentagem: &e{bonus}%'
  - ''

# Configurações da recompensa
Ganhar recompensa:
 Passar todas: true #tentar givar todas as recompensas, mesmo quando ele já ganhar 1
 Msgs:
  Actionbar:
   Ativar: true
   Msg: '&aVocê pescou uma recompensa.'
  Title:
   Ativar: true
   Title: '&aRecompensa encontrada'
   Subtitle: '&epescando.'
  Chat:
   Ativar: true
   Msg:
   - ''
   - '&aVocê encontrou uma recompensa pescando.'
   - ''

# Opções da evolução
Evoluiu:
 Msgs:
  Actionbar:
   Ativar: true
   Msg: '&aVocê evoluiu o nível da tua vara de pesca.'
  Title:
   Ativar: true
   Title: '&aVara de pesca'
   Subtitle: '&eevoluída!'
  Chat:
   Ativar: true
   Msg:
   - ''
   - '&aVocê evoluiu o nível da vara de pesca.'
   - ''

# Configuração da vara de pesca
Vara:
 Glow: false
 Name: '&eVara de Pesca &7(Nível {nivel})'
 Lore:
 - '&eEXP: &a{tem}&7/&c{precisa}'
 - ''
 - '&7Clique com botão shift+direito para ver as'
 - '&7possíveis recompensas.'

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

# Local do npc (NÃO MEXER AQUI)
Local: 'none'
]]>
</code-block>
</chapter>

<chapter title="niveis.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Niveis:
   nivel1:
      # A ordem das varas começa em 0
      Ordem: 0
      # Preco para evoluir para esse nivel
      XP: 0.0
      # XP do AuraSkills que será dado ao pescar
      AuraSkills-XP: 1.0
      # Habilitar aparecer no menu de preview
      Preview: false
      # Recompensas cadastradas
      # Chance,recompensa-xp
      Recompensas:
      - '100.0,Reco1-10.0'
      - '50.0,Reco2-20.0'
   nivel2:
      Ordem: 1
      XP: 70.0
      AuraSkills-XP: 1.0
      Preview: true
      Recompensas:
      - '100.0,Reco2-40.0'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   Reco1:
      Preview:
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         - '&aTu vais ganhar uma pedra.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
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
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'
   Reco2:
      Preview:
         CustomSkull: false
         URL: ''
         ID: 1
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Amount: 64
         Lore:
         - ''
         - '&aTu vais ganhar uma pedra 2.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
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
         - '&aTu ganhou uma pedra 2.'
         - ''
         Enchants: #se não desejar, deixe assim:
         - ''
      Command:
         Use: true
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/33-yPescaSimples">Site do plugin yPescaSimples</a>
    </category>
</seealso>