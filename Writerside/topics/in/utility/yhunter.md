# yHunter
<secondary-label ref="utility"/>

### Descrição
Pague para matarem seu jogador inimigo

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
<video src="//www.youtube.com/watch?v=E7WjtAXuRXU"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/hunter - Abre o menu principal
/hunter setnpc - Seta o npc do hunter
/hunter delnpc - Deleta o npc do hunter</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yhunter.usar - Permissão para o /hunter
yhunter.admin - Permissão para o /hunter setnpc e /hunter delnpc
yhunter.staff - Permissão para ser reconhecido como staff (não podem pagar por sua cabeça)</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yHunter/
    ├── menus/
    │    ├── colocaram.yml
    │    ├── principal.yml
    │    ├── recompensas.yml
    │    └── top.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="colocaram.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caçador -> Colocaram'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
VoltarSlot: 27
ProximoSlot: 35

Item:
   CustomSkull: true
   URL: '{player}'
   ID: 0
   Data: 0
   Glow: true
   Name: '&e{player}'
   Lore:
   - '&7Este jogador já colocou &aR${money}&7 em sua cabeça.' #disponível variável {player}

]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caçador - Principal'
Tamanho: 27
Itens:
   Perfil: # primeiro
      Slot: 10
      CustomSkull: true
      URL: '{player}'
      ID: 0
      Data: 0
      Glow: true
      Name: '&f{player}'
      Lore:
      - ''
      - '&7Já colocaram um total de &aR${colocaram} &7em sua cabeça.'
      - '&7Você já coletou um total de &aR${coletou}&7.'
      - ''
      - '&7Clique para ver os jogadores que pagaram pela sua morte.'
   Adicionar: # segundo
      Slot: 12
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/3edd20be93520949e6ce789dc4f43efaeb28c717ee6bfcbbe02780142f716'
      ID: 0
      Data: 0
      Glow: true
      Name: '&cAdicionar recompensa'
      Lore:
      - '&7Clique para adicionar uma recompensa na cabeça de alguém.'
   Recompensas: #terceiro
      Slot: 14
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/1a696e152363ad477ed6cb5a518bfea84b036148fecac0581f32c5b5396958'
      ID: 0
      Data: 0
      Glow: false
      Name: '&aRecompensas'
      Lore:
      - '&7Clique para ver os players online com recompensas existentes.'
   Top: #quarto
      Slot: 16
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/15a7ee9a86de203674a93b570bc8992e500363dd32f2b9813daaeeabccf92151'
      ID: 0
      Data: 0
      Glow: false
      Name: '&aTop'
      Lore:
      - '&7Clique para ver os jogadores que mais coletaram recompensas.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> LOJAS:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Caçador -> Recompensas'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30
VoltarSlot: 27
ProximoSlot: 35

Item:
   CustomSkull: true
   URL: '{player}'
   ID: 0
   Data: 0
   Glow: true
   Name: '&e{player}'
   Lore:
   - '&7Mate e receba &aR${money}&7.' #disponível variável {player}
   
Seletor:
   Slot: 32
   CustomSkull: true
   URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
   ID: 0
   Data: 0
   Glow: true
   Name: '&aSeletor das Lojas'
   
Formato:
   Visualizando: ' &f• &a{nome}'
   Selecionar: ' &f• &7{nome}'
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Hunter'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fColetado: &aR${coletado}'
   - '&fPosição: &6{pos}'
   - ''

Item p:
   Slot: 32
   Name: '&7#&f{pos} - &aVocê &7({player})'
   Lore:
   - ''
   - '&fColetado: &aR${coletado}'
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

# Comando e aliases do plugin
Comando:
  Comando: 'hunter'
  Aliases: [ ]

# Opcoes de configuração do NPC
NPC:
  ID: 923287
  Skin: 'TheThunderGod063'
  Holograma:
    Altura: 3.1
    Holograma:
      - '&6Matador de aluguel'
      - '&7Veja as recompensas disponíveis.'

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Opções gerais do plugin
Opcoes:
  # Permissão para poder receber a recompensa de matar o jogador
  KillPerm: ''
  Minimo colocar: 1000.0 # minimo de money para pagar pela morte do jogador
  Minimo tirar: 10000.0 # minimo de money para o morto perder ( x % do seu money )
  Maximo tirar: 20000.0 # máximo de money para o morto perder ( x % do seu money )
  Porcentagem tirar: 10.0 # quando o jogador que estiver sendo caçado morrer, perder esta % de money
  Porcentagem adicionar: 5.0 # quando o jogador que estiver sendo caçado matar um jogador, aumentar essa % na recompensa
  # Mundos onde os eventos de matar e morrer não serão contabilizados
  Mundos blacklist:
    - 'guerra'
    - 'eventos'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Cancelou: '&cVocê cancelou a ação.'
  Nao encontrado: '&cJogador não encontrado.'
  Deslogou: '&cAparentemente este jogador deslogou.'
  Nao e numero: '&cO argumento não é um número.'
  Minimo: '&cO valor mínimo é &71K&c.'
  Nao possui: '&cVocê não possui esta quantia de dinheiro.'
  Si mesmo: '&cVocê não pode pagar pela sua própria morte.'
  Colocou: '&aVocê está agora pagando &eR${money} &apela cabeça do jogador &e{player}&a.'
  Colocou ativar: false #ativa a mensagem de cima
  Perdeu: '&cVocê perdeu 10% do seu money por morrer com uma recompensa pela sua morte.'
  Coletou: '&aVocê ganhou &eR${money} &aao matar o jogador &e{player}&a.'
  Coletou ativar: false #ativa a mensagem de cima
  Staff: '&cVocê não pode definir valores pela morte de um staff.'
  Setado: '&aNPC da pesca setado com sucesso.'
  Removido: '&aNPC da pesca removido com sucesso'
  Nao setado: '&cO NPC não está setado.'
  Digite:
    - ''
    - '&aDigite o nome do jogador.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite valor:
    - ''
    - '&aDigite o preço pela cabeça do jogador.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''

Anuncios:
  Colocou:
    Actionbar:
      Ativar: true
      Msg: '&aFoi colocado &e{money}&a pela morte do jogador &e{player}&a.'
    Title:
      Ativar: true
      Broadcast: false
      Title: '&aMate o &e{player}'
      Subtitle: '&ae ganhe &e{money}&a.'
    Chat:
      Ativar: true
      Broadcast: false
      Msg:
        - '&aFoi colocado &e{money}&a pela morte do jogador &e{player}&a.'
  Coletou:
    Actionbar:
      Ativar: true
      Msg: '&e{matou} &aganhou &e{money} &apor matar o jogador &e{morreu}&a.'
    Title:
      Ativar: true
      Broadcast: false
      Title: '&e{matou} &aganhou &e{money}'
      Subtitle: '&aao matar &e{morreu}&a.'
    Chat:
      Ativar: true
      Broadcast: false
      Msg:
        - '&e{matou} &aganhou &e{money} &apor matar o jogador &e{morreu}&a.'
  Somou:
    Actionbar: '&e{matou} &aaumentou em &e{money} &asua recompensa de procurado ao matar &e{morreu}&a.'
    Title: '&e{matou} &aaumentou em &e{money}<nl>&asua recompensa de procurado'
    Chat: [ '&e{matou} &aaumentou em &e{money} &asua recompensa de procurado ao matar &e{morreu}&a.' ]

Setas:
  Voltar:
    CustomSkull: false
    URL: ''
    ID: ARROW
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
    ID: ARROW
    Data: 0
    Glow: true
    Name: '&aPróximo'
    Lore:
      - ''
      - '&7Clique para ir à próxima página.'
      - ''

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

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/38-yHunter">Site do plugin yHunter</a>
    </category>
</seealso>