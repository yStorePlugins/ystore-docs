# yCrates
<secondary-label ref="utility"/>

### Descrição
Crie blocos que ao serem abertos lhe dará recompensas.

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
<video src="//www.youtube.com/watch?v=3qAwuCA9TxY"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/crate&nbsp;- Mostra os comandos disponíveis
/crate verconteudo&nbsp;- Abre o menu de preview de uma crate
/crate descompactar&nbsp;- Descompactar as keys que estão na mão
/crate givecrate - Dar crates para um jogador
/crate givekey - Dar keys para um jogador
/crate keyall&nbsp;- Dar keys para todos os jogadores
/crate reload&nbsp;- Recarrega os arquivos de configuração</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycrates.verconteudo - Permissão para o /crate verconteudo
ycrates.descompactar - Permissão para o /crate descompactar
ycrates.admin - Permissão para o /crate, /crate givecrate, /crate givekey, /crate keyall, /crate reload e remover as crates do chão</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yCrates/
    ├── crates/
    │    ├── esmeralda.yml
    │    └── padrao.yml
    ├── menus/
    │    ├── filter.yml
    │    └── preview.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="crates" collapsible="true">
<chapter title="esmeralda.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Holograma:
   ##
   # Esta opção serve para ajustar a altura do holograma
   Altura: 2.5
   # Ajustar a altura do holograma de recompensa ( apenas se tiver ativado )
   Altura recompensa: 0.5
   ##
   # O texto que irá aparecer no holograma
   Holograma:
   - '&fCrate &aesmeralda&f.'
   - '&7Consiga itens supremos ao abrí-la.'
   - ''
   - '&7Ver conteúdo: &fBotão esquerdo&7.'
   - '&7Abrir crate: &fBotão direito com a chave&7.'
#
##
# Este é o item que servirá para abrir a crate
Key:
   CustomSkull: false #se colocar true, coloque o URL
   URL: ''
   ID: TRIPWIRE_HOOK
   Data: 0
   Glow: true
   Name: '&fChave da caixa &aesmeralda&f.'
   Lore:
   - '&7Esta chave abre a caixa &aesmeralda&7,'
   - '&7com ela, você consegue itens supremos.'
   - ''
   - '&7Vá até a &f/warp crates&7 para abrir.'
   - ''
   - '&f Quantia: &b{amount}'
   - ''
#
##
# Este é o item que será dado para gerar a crate
Item:
   CustomSkull: false #se colocar true, coloque o URL
   URL: ''
   ID: CHEST
   Data: 0
   Glow: true
   Name: '&fCaixa &aesmeralda&f.'
   Lore:
   - '&7Coloque-a no chão para gerar a crate.'
#
##
# Os locais das caixas. Não altere nada aqui.
Locais: []
#
##
# Permissão para poder abrir a crate. Deixe vazio para não usar.
Permissao: ''
##
# Nome da crate
Display name: 'Esmeralda'
##
# Ativar a animação do item subir para cima do bloco (delay de 4 segundos)
# Funciona apenas na 1.8
Animacao: true
##
# Fireworks = Fogos de artifício
# Explode = Explosão ao redor
# Estas opções podem gerar um timings a mais.
Fireworks: true
Explode: true
##
# Ao clicar com shift, irá abrir a crate de acordo com a quantia de keys na mão
Shift tudo: false
#
#
Recompensas:
   #
   Reco1:
      Chance: 50.0
      Display:
         CustomSkull: false
         URL: ''
         ID: EMERALD
         Data: 0
         Glow: true
         Name: '&aEMERALDAS!'
         Amount: 64
         Lore:
         - '&7Chance: &f50%&7.'
      Recompensa:
         Usar itens: true
         Usar comandos: true
         Comandos:
         - 'alerta {player} é bonito'
         Itens:
            Esmeralda:
               CustomSkull: false
               URL: ''
               ID: EMERALD
               Data: 0
               Amount: 64
               Name: '&aESMERALDAS!'
               Glow: true
               Lore: []
               Enchants:
               - ''









]]>
</code-block>
</chapter>

<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Criar uma cabeça animada (que fica rodando) no lugar de um bloco
HeadAnimada: false
HAOptions:
  Velocidade: 4
  Altura: -1.2
  Particula:
    Ativar: true
    Particula: 'FLAME'
Holograma:
  # Esta opção serve para ajustar a altura do holograma
  # caso a crate seja uma cabeça animada, recomendamos 4.3
  Altura: 2.5
  # Ajustar a altura do holograma de recompensa ( apenas se tiver ativado )
  Altura recompensa: 0.5
  # O texto que irá aparecer no holograma
  Holograma:
    - '&fCrate &bdiamante&f.'
    - '&7Consiga itens raros ao abrí-la.'
    - ''
    - '&7Ver conteúdo: &fBotão esquerdo&7.'
    - '&7Abrir crate: &fBotão direito com a chave&7.'
    - ''
    - ''
    - '[item]DIAMOND_BLOCK' #use [item] para colocar um item
# Este é o item que servirá para abrir a crate
Key:
  CustomSkull: false #se colocar true, coloque o URL
  URL: ''
  ID: TRIPWIRE_HOOK
  Data: 0
  Glow: true
  Name: '&fChave da caixa &bdiamante&f.'
  Lore:
    - '&7Esta chave abre a caixa &bdiamante&7,'
    - '&7com ela, você consegue itens raros.'
    - ''
    - '&7Vá até a &f/warp crates&7 para abrir.'
    - ''
    - '&f Quantia: &b{amount}'
    - ''
# Este é o item que será dado para gerar a crate
Item:
  CustomSkull: false #se colocar true, coloque o URL
  URL: ''
  ID: CHEST
  Data: 0
  Glow: true
  Name: '&fCaixa &bdiamante&f.'
  Lore:
    - '&7Coloque-a no chão para gerar a crate.'
# Os locais das caixas. Não altere nada aqui.
Locais: [ ]
# Permissão para poder abrir a crate. Deixe vazio para não usar.
Permissao: ''
# Nome da crate
Display name: 'Diamante'
# Ativar a animação do item subir para cima do bloco (delay de 4 segundos)
# Funciona apenas na 1.8
Animacao: false
# Fireworks = Fogos de artifício
# Explode = Explosão ao redor
# Estas opções podem gerar um timings a mais.
Fireworks: false
Explode: false
# Ao clicar com shift, irá abrir a crate de acordo com a quantia de keys na mão
Shift tudo: true
# Recompensas da crate
Recompensas:
  #
  Reco1:
    # Chance para conseguir a recompensa
    Chance: 50.0
    # Opção para não vir nada ao receber esta recompensa
    Nada: false
    # Mensagens que serão enviadas
    # Broadcast envia para todos do servidor
    Mensagens:
      # Enviar a mensagem quando ativar no shift (uma para cada recompensa)
      Shift: true
      Actionbar:
        Ativar: true
        Broadcast: true
        Msg: '&aO jogador &7{player} &aabriu uma caixa.'
      Chat:
        Ativar: true
        Broadcast: false
        Msg:
          - '&aVocê &7({player}) &aabriu uma caixa.'
      Title: '&eVocê abriu<nl>&auma caixa!'
    # Item que irá aparecer na pré-visualização
    Display:
      CustomSkull: false #se colocar true, coloque o URL
      URL: ''
      ID: DIAMOND
      Data: 0
      Glow: true
      Name: '&bDIAMANTES!'
      Amount: 64
      Lore:
        - '&7Chance: &f50%&7.'
      Enchants:
        - '' #deixe vazio para não usar
    #
    Recompensa:
      # Ativar o give de itens
      Usar itens: true
      # Ativar o give de comandos
      Usar comandos: true
      # Comandos a serem dados
      Comandos:
        - 'alerta {player} é bonito'
      # Itens a serem dados
      Itens:
        #
        Diamante:
          CustomSkull: false
          URL: ''
          ID: DIAMOND
          Data: 0
          Amount: 64
          Name: '&bDIAMANTES!'
          Glow: true
          Lore: [ ]
          Enchants:
            - '' #deixe vazio para não usar









]]>
</code-block>
</chapter>

</chapter>

<chapter title="menus" collapsible="true">
<chapter title="filter.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
name: '&8Crates'
size: 45
slots: [ 11, 12, 13, 14, 15, 20, 21, 22, 23, 24 ]
previous-slot: 18
next-slot: 26
back-slot: 40
facing:
  e0:
    slot: 11
    material: 'BARRIER'
    name: ' '
    lore: []
  e1:
    slot: 12
    material: 'BARRIER'
    name: ' '
    lore: []
  e2:
    slot: 13
    material: 'BARRIER'
    name: ' '
    lore: []
  e3:
    slot: 14
    material: 'BARRIER'
    name: ' '
    lore: []
  e4:
    slot: 15
    material: 'BARRIER'
    name: ' '
    lore: []
  e5:
    slot: 20
    material: 'BARRIER'
    name: ' '
    lore: []
  e6:
    slot: 21
    material: 'BARRIER'
    name: ' '
    lore: []
  e7:
    slot: 22
    material: 'BARRIER'
    name: ' '
    lore: []
  e8:
    slot: 23
    material: 'BARRIER'
    name: ' '
    lore: []
  e9:
    slot: 24
    material: 'BARRIER'
    name: ' '
    lore: []
]]>
</code-block>
</chapter>

<chapter title="preview.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Crate {crate}'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
VoltarSlot: 27
ProximoSlot: 35
filter:
  slot: 40
  material: 'HOPPER'
  name: '&eItens filtrados'
  lore: [ '&7Clique para gerenciar', '&7os itens filtrados.' ]
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Modo de depuração para correção de problemas no plugin.
debug-mode: false

#      ___      _        _
#     /   \__ _| |_ __ _| |__   __ _ ___  ___
#    / /\ / _` | __/ _` | '_ \ / _` / __|/ _ \
#   / /_// (_| | || (_| | |_) | (_| \__ \  __/
#  /___,' \__,_|\__\__,_|_.__/ \__,_|___/\___|
#
# Configurações do banco de dados.

database:
   # Determina o tipo de banco de dados. Valores válidos: [SQLITE, MYSQL, HIKARI (recomendado)]
   storage-type: SQLITE

   # Dados para conexão ao banco de dados MYSQL.
   data:
      # Endereço de conexão do banco de dados. [EX: 127.0.0.1]
      host: localhost
      # Porta de conexão do banco de dados. [EX: 3306]
      port: 3306
      # Nome do banco de dados a ser conectado. [EX: minecraft]
      database: ''
      # Usuário de conexão. [EX: root]
      username: ''
      # Senha do usuário de conexão: [EX: 123]
      password: ''

Comando:
   Comando: 'crate'
   Aliases: [crates, caixa, caixas]

# Carregar as crates depois de x tempo que o server ligar
Carregar depois: 20 # Em ticks (20 ticks = 1 segundo)

# Ativar o sistema de filtro
Filtro: true

# Ativar o menu de preview
Preview: true

# Usar as partículas do Packet-Events
# Caso false, usará as do ProtocolLIB
packet-events-particles: false

# Limite máximo de abertura de keys por click
all-limit: 100

# Sistema de lores
lore:
   filter-remove: ['&cClique para remover do filtro']

# Sistema de limpar as possíveis caixas "bugadas"
crate-cleaner:
   enable: false
   # em segundos
   time: 300

Mensagens:
   Segurando: '&cVocê deve estar segurando uma key para abrir a crate &7{crate}&c.'
   Key nao: '&cEsta key não abre a crate &7{crate}&c.'
   Ja abrindo: '&cAlguém já está abrindo a crate &7{crate}&c neste local.'
   Mal configurada: '&cEsta crate não existe ou está mal configurada.'
   Setada: '&aCrate &7{crate} &asetada.'
   Removida: '&aCrate &7{crate} &aremovida.'
   Inv cheio: '&cSeu inventário está cheio.'
   Permissao: '&cVocê não tem permissão para isso.'
   Nao encontrado: '&cJogador não encontrado.'
   Nao e numero: '&cO argumento não é um número.'
   Deu crate: '&aVocê deu &7{quantia}x {crate} &apara o jogador &7{player}&a.'
   Recebeu crate: '&aVocê recebeu &7{quantia}x {crate}&a.'
   Deu key: '&aVocê deu &7{quantia}x &akey(s) da crate &7{crate} &apara o jogador &7{player}&a.'
   Recebeu key: '&aVocê recebeu &7{quantia}x &a key(s) da crate &7{crate}&a.'
   Deu todos: '&aVocê deu &7{quantia}x &akey(s) da crate &7{crate}&a para &7({players}) &ajogadores online.'
   AdicionadoFiltro: '&aEste item foi adicionado ao filtro.'
   RemovidoFiltro: '&aEste item foi removido do filtro.'
   Descompactar-Segurando: '&cVocê precisa estar segurando keys compactadas.'
   Descompactar-Encontrado: '&cA crate vinculada nesta key não foi encontrada.'
   Descompactar-Minimo: '&cA sua key já está no mínimo possível.'
   Descompactar: '&a{amount} Keys descompactadas.'
   Recebeu todos:
      - ''
      - '&aTodos os jogadores receberam &7{quantia}x &akey(s) da crate &7{crate}&a.'
      - ''
   Help:
      - '&c&lERRO! &cComandos disponíveis:'
      - '&c-> /crate givecrate'
      - '&c-> /crate givekey'
      - '&c-> /crate keyall'
      - '&c-> /crate reload'
      - ''
#
#
Sons:
   Erro:
      Ativar: true
      Som: 'CAT_MEOW'
   Ganhou:
      Ativar: true
      Som: 'ORB_PICKUP'
#
#
##
# Lista de efeitos da 1.8: https://helpch.at/docs/1.8.8/org/bukkit/Effect.html
# Lista de efeitos da 1.16: https://helpch.at/docs/1.16.1/org/bukkit/Effect.html
#
# Lista de sons da 1.8: https://helpch.at/docs/1.8.8/org/bukkit/Sound.html
# Lista de sons da 1.16: https://helpch.at/docs/1.16.1/org/bukkit/Sound.html
#
Explode:
   Som: 'EXPLODE'
   Efeitos:
   - 'LAVADRIP:40' # Efeito:intensidade
   - 'VILLAGER_THUNDERCLOUD:300' # Efeito:intensidade
   - 'CLOUD:230' # Efeito:intensidade
   - 'EXPLOSION_HUGE:20' # Efeito:intensidade
#
#
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
      Name: '&cVoltar'
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

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/42-yCrates">Site do plugin yCrates</a>
    </category>
</seealso>