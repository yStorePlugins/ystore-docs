# yTesouros
<secondary-label ref="rankup"/>

### Descrição
Crates virtuais, tesouros físicos e recompensas em menu!

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
<video src="//www.youtube.com/watch?v=yhoHfnX4L40"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/tesouro - Abre o menu de tesouros.
/tesouro give  - Dar tesouro à um jogador (apenas o virtual)
/tesouro recompensa - Abre o menu de recompensas.
/recompensas - Abre o menu de recompensas</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytesouros.tesouro - Permissão para o /tesouro
ytesouros.recompensa - Permissão para o /recompensas, /tesouro recompensa
ytesouros.give - Permissão para o /tesouro give</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTesouros/
    ├── menus/
    │    ├── preview.yml
    │    ├── principal.yml
    │    └── recompensas.yml
    ├── blocos.yml
    ├── config.yml
    ├── mobs.yml
    ├── recompensas.yml
    └── tesouros.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Tesouros - Preview'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 0
VoltarSlot: 9
ProximoSlot: 17
# Itens para customizar seu menu
Itens: {}
#  Enfeite:
#    Slot: 11
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: true
#    Name: '&aENFEITE!'
#    Lore: []
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Tesouros'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
VoltarSlot: 18
ProximoSlot: 26
# Item para recolher todas as recompensas
Recompensas:
  Slot: 49
  CustomSkull: false
  URL: ''
  ID: 342
  Data: 0
  Glow: false
  Name: '&aRecompensas'
  Lore:
    - '&7Clique para gerenciar'
    - '&7suas recompensas.'
# Item que irá mostrar quanto estiver vazio
Vazio:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: 30
  Data: 0
  Glow: false
  Name: '&cVazio!'
  Lore:
    - '&7Você não possui nenhum'
    - '&7tesouro armazenado.'
# Itens para customizar seu menu
Itens: {}
#  Enfeite:
#    Slot: 11
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: true
#    Name: '&aENFEITE!'
#    Lore: []
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Tesouros - Recompensas'
Tamanho: 54
Slots: [10, 11, 12, 13, 14, 15, 16, 19, 20, 21, 22, 23, 24, 25, 28, 29, 30, 31, 32, 33, 34, 37, 38, 39, 40, 41, 42, 43]
BackSlot: 9
VoltarSlot: 18
ProximoSlot: 26
# Item para recolher todas as recompensas
Recolher todos:
  Slot: 49
  CustomSkull: true
  URL: 'http://textures.minecraft.net/texture/1824d454e0508c57e3fe8337030a0bc52e2065e19f02e30b457d352d4a312537'
  ID: 1
  Data: 0
  Glow: false
  Name: '&6Recolher todos'
  Lore:
    - '&7Clique para recolher'
    - '&7todas as recompensas.'
# Item que irá mostrar quanto estiver vazio
Vazio:
  Slot: 22
  CustomSkull: false
  URL: ''
  ID: 30
  Data: 0
  Glow: false
  Name: '&cVazio!'
  Lore:
    - '&7Você não possui nenhuma'
    - '&7recompensa armazenada.'
# Itens para customizar seu menu
Itens: {}
#  Enfeite:
#    Slot: 11
#    CustomSkull: false
#    URL: ''
#    ID: 1
#    Data: 0
#    Glow: true
#    Name: '&aENFEITE!'
#    Lore: []
]]>
</code-block>
</chapter>

</chapter>

<chapter title="blocos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Blocos:
  ##
  ##
  ##
  blocoRecompensa:
    # ID:DATA
    ID: 'STONE:0'
    # Ativar apenas nas minas do yMinas e yMinasPackets
    Just-mine: false
    # Tesouros que serão dados
    # O nome dos tesouros é configurado na tesouros.yml
    # chance,tesouro
    Tesouros:
      - '100,recompensa'
    # Mundos permitidos
    Mundos:
      - 'world'
  ##
  ##
  ##
  blocoVirtual:
    ID: 'STONE:0'
    # Ativar apenas nas minas do yMinas e yMinasPackets
    Just-mine: false
    Tesouros:
      - '100,virtual'
    Mundos:
      - 'world'
  ##
  ##
  ##
  blocoBloco:
    ID: 'STONE:0'
    # Ativar apenas nas minas do yMinas e yMinasPackets
    Just-mine: false
    Tesouros:
      - '100,bloco'
    Mundos:
      - 'world'
  ##
  ##
  ##
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
  Tesouro:
    Comando: 'tesouro'
    Aliases: [ tesouros ]
  Recompensa:
    # Deixe '' para não usar
    Comando: 'recompensa'
    Aliases: [ recompensas ]

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
login-delay: 20

# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'

# Este limite serve para recolher recompensas
# Desativar ou aumentar o limite pode gerar lag
# e em alguns casos crashar o servidor.
Limite:
  Ativar: true
  # Máximo que irá recolher por vez
  Maximo: 40

# Mundos onde não pode coletar/abrir tesouros/recompensas
World blacklist:
  - 'none'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Inv cheio: '&cSeu inventário está cheio.'
  Deletou: '&aVocê deletou esta recompensa.'
  Cancelou: '&cVocê cancelou a operação.'
  Nao e numero: '&cO argumento não é um número.'
  Nao encontrado: '&cJogador não encontrado.'
  Suficiente: '&cVocê não possui tesouros suficiente.'
  Recolheu: '&aVocê recolheu &e{quantia}&a tesouros.'
  Deu: '&aVocê deu &e{quantia} &atesouros para o jogador &e{player}&a.'
  Armazenou: '&aVocê armazenou &e{quantia} &atesouros.'
  Pertence: '&cEste tesouro pertence à {player}.'
  Coletou: '&eVocê coletou uma recompensa.'
  ColetouTodas: '&eVocê coletou todas as suas recompensas.'
  Mundo: '&cVocê não pode fazer isto neste mundo.'
  Abriu:
    - '&aVocê abriu &e{quantia}&a tesouros. Para recolher suas recompensas digite &8/recompensas&e.'
  Recolher:
    - ''
    - '&aDigite a quantia que você quer recolher.'
    - ''
    - '&8| &fVocê possui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara recolher tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''
  Abrir:
    - ''
    - '&aDigite a quantia que você quer abrir.'
    - ''
    - '&8| &fVocê possui &6{quantia}&f disponível.'
    - '&8| &fDigite &8TUDO &fpara abrir tudo.'
    - ''
    - '&7Para cancelar digite &ncancelar&7.'
    - ''

# Setas dos menus.
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
    Name: '&cAnterior'
    Lore:
      - '&7Clique para ir à página anterior.'
  Proximo:
    CustomSkull: false
    URL: ''
    ID: 262
    Data: 0
    Glow: true
    Name: '&aPróximo'
    Lore:
      - '&7Clique para ir à próxima página.'

# Formatos de lores
Lores:
  Recompensa:
    # O sobrepor irá trocar a lore por esta
    Sobrepor: false
    Lore:
      - ''
      - '&fQuantia armazenada: &6{quantia}&f.'
      - ''
      - '&7Aperte o &fBotão Q&7 para &7deletar uma unidade deste item.'
      - '&7Aperte o &fBotão CTRL+Q&7 para &7deletar todos deste item.'

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

<chapter title="mobs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Só funcionam tesouros VIRTUAL ou RECOMPENSA
Entidades:
  entidadeRecompensa:
    # Entidade
    Entidade: 'CHICKEN'
    # Tesouros que serão dados
    # O nome dos tesouros é configurado na tesouros.yml
    # chance,tesouro
    Tesouros:
      - '100,recompensa'
    # Mundos permitidos
    Mundos:
      - 'world'
  entidadeVirtual:
    Entidade: 'PIG'
    Tesouros:
      - '100,virtual'
    Mundos:
      - 'world'
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
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEsta pedra vale muito dinheiro!'
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
      Name: '&8Pedra'
      Amount: 64
      Lore:
        - '&aEu valho muito!'
      # Caso não queira deixe:
      # Enchants:
      # - ''
      Enchants:
        - ''
    # Só será executado o comando se o "Use" estiver em true.
    # Comandos que serão executados no jogador.
    Command:
      Use: false
      List:
        - 'give {player} stone 1'
  Reco2:
    Preview:
      CustomSkull: false
      URL: ''
      ID: 264
      Data: 0
      Name: '&bDiamante'
      Amount: 1
      Lore:
        - '&bQuem não adora uma pedra preciosa?!'
      Enchants:
        - ''
    Command:
      Use: true
      List:
        - 'give {player} diamond 1'
  Reco3:
    # Item que aparecerá no preview.
    Preview:
      CustomSkull: false
      URL: ''
      ID: 388
      Data: 0
      Name: '&aEsmeralda'
      Amount: 64
      Lore:
        - '&aEsmeraldas valem muito?'
      Enchants:
        - ''
    Item:
      CustomSkull: false
      URL: ''
      ID: 388
      Data: 0
      Name: '&aEsmeralda'
      Amount: 64
      Lore:
        - '&aEu valho muito!'
      Enchants:
        - ''
]]>
</code-block>
</chapter>

<chapter title="tesouros.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Tipos de tesouro:
# BLOCO -> irá spawnar um bloco no lugar do quebrado.
# VIRTUAL -> irá dar tesouros para serem abertos no /tesouros
# RECOMPENSA -> irá dar as recompensas diretamente no /recompensas ou /tesouros recompensas
Tesouros:
  recompensa:
    Tipo: 'RECOMPENSA'

    #
    # Este bloco será o que irá spawnar
    #Bloco:
    #  ID: CHEST
    #  Data: 0
    #

    #
    # Item que aparecerá no menu de /tesouros.
    # Apenas se o tipo for virtual.
    #Item:
    #  CustomSkull: false
    #  URL: ''
    #  ID: 1
    #  Data: 0
    #  Name: '&eTesouro'
    #  Amount: 64
    #  Lore:
    #    - '&fTipo: &aRecompensa&f.'
    #

    #
    # Item que será ativável
    # Apenas se o tipo for virtual.
    #Ativavel:
    #  CustomSkull: false
    #  URL: ''
    #  ID: 1
    #  Data: 0
    #  Name: '&eTesouro'
    #  Amount: 64
    #  Lore:
    #    - '&fTipo: &aRecompensa&f.'
    #

    # Som de quando encontrar um tesouro
    Som: 'ORB_PICKUP'
    # Mensagens que serão enviadas:
    Mensagens:
      Chat:
        Broadcast: false
        Msg:
          - '&a[TESOURO] &eVocê encontrou uma recompensa. Digite &8/recompensas &epara reivindicar!'
      Actionbar: '&eVocê encontrou uma recompensa &aBásico&e!'
      Title: '&eRecompensa encontrada!<nl>&8/recompensas&e!'
    # Recompensas do tesouro
    # As recompensas são cadastradas na recompensas.yml
    # Use: chance,recompensa
    Recompensas:
      # Irá tentar dar todas as recompensas da lista.
      Passar todas: true
      Lista:
        - '100,Reco1'
  virtual:
    Tipo: 'VIRTUAL'
    Som: 'ORB_PICKUP'
    Item:
      CustomSkull: false
      URL: ''
      ID: 54
      Data: 0
      Name: '&eTesouro Virtual'
      Amount: 64
      Lore:
        - '&fRaridade: &6Raro&f.'
        - '&fQuantia armazenada: &b{quantia}&f.'
        - ''
        - '&7Clique com botão esquerdo para abrir.'
        - '&7Clique com botão direito para recolher.'
        - '&7Aperte o botão Q para ver as recompensas.'
    Ativavel:
      CustomSkull: false
      URL: ''
      ID: 54
      Data: 0
      Name: '&eTesouro virtual'
      Amount: 64
      Lore:
        - '&7Clique com &fbotão direito'
        - '&7para armazenar.'
    Mensagens:
      Chat:
        Broadcast: false
        Msg:
          - '&a[TESOURO] &eVocê encontrou um tesouro &aVirtual&e. Digite &8/tesouros &epara reivindicar!'
      Actionbar: '&eVocê encontrou um tesouro &aVirtual&e!'
      Title: '&eTesouro Virtual<nl>&8/tesouros&e!'
    Recompensas:
      Passar todas: true
      Lista:
        - '100,Reco2'
  bloco:
    Tipo: 'BLOCO'
    Bloco:
      ID: CHEST
      Data: 0
    Holograma:
      Altura: 2.5
      Holograma:
        - '[item]DIAMOND'
        - ''
        - ''
        - '&6&lTesouro'
        - '&7Clique para pegar as recompensas.'
    Som: 'ORB_PICKUP'
    Mensagens:
      Chat:
        Broadcast: true
        Msg:
          - '&a[TESOURO] &eO jogador &7{player} &eencontrou um tesouro &aFísico&e!'
      Actionbar: '&eVocê encontrou um tesouro &aFísico&e!'
      Title: '&eTesouro encontrado<nl>&aFísico&e!'
    Recompensas:
      Passar todas: true
      Lista:
        - '100,Reco3'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/50-yTesouros">Site do plugin yTesouros</a>
    </category>
</seealso>