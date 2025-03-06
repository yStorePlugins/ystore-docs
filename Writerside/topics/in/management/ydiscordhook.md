# yDiscordHook
<secondary-label ref="management"/>

### Descrição
Vincule seu discord para receber e remover cargos automaticamente

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
<video src="https://www.youtube.com/watch?v=DgYA0JW5-LM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/discord - Envia a mensagem de discord
/discord msg - Envia uma mensagem no discord do jogador
/discord reload - Recarrega as configurações
/vinculardc - Abre o menu de vinculação
/vinculardc [player] [id] - Vincula um ID a outro jogador
/desvinculardc - Desvincula seu discord
/desvinculardc [player] - Desvincula o discord de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ydiscordhook.usar - Permissão para o /discord e /vinculardc
ydiscordhook.msg - Permissão para o /discord msg
ydiscordhook.reload - Permissão para o /discord reload
ydiscordhook.vincular.outros - Permissão para o /vinculardc [player] [id]
ydiscordhook.desvincular - Permissão para o /desvinculardc
ydiscordhook.admin.desvincular - Permissão para o /desvinculardc [player]
ydiscordhook.bypass - Permissão para o bypass de cargos</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ydiscordhook_vinculado% - Retorna se o jogador está vinculado
%ydiscordhook_id% - Retorna o ID do discord
%ydiscordhook_name% - Retorna o nome no discord
%ydiscordhook_tag% - Retorna a tag caso vinculado
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yDiscordHook/
    ├── menus/
    │    └── principal.yml
    ├── cargos.yml
    ├── config.yml
    ├── discord.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Conta do Discord'
Tamanho: 27
VincularSlot: 12
Itens:
  Vincular:
    CustomSkull: true
    URL: '{player}'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aMinha conta'
    Lore:
      - ''
      - ' &fConta vinculada: &7Nenhuma'
      - ''
      - '&aClique para vincular sua conta'
  Vinculada:
    CustomSkull: true
    URL: '{player}'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aMinha conta'
    Lore:
      - ''
      - ' &fConta vinculada: &7{discord_tag}&f.'
      - ' &fID da conta: &7{discord_id}&f.'
      - ' &fServer Booster: {booster}&f.'
      - ''
      - ' &fData da vinculação: &7{data} às {hora}&f.'
      - ''
      - '&aClique para desvincular sua conta'
  Discord:
    Slot: 14
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/4d42337be0bdca2128097f1c5bb1109e5c633c17926af5fb6fc20000011aeb53'
    ID: AIR
    Data: 0
    Glow: true
    Name: '&aDiscord do servidor'
    Lore:
      - '&7Clique para entrar no discord'
      - '&7do nosso servidor.'
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> Discord:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

</chapter>

<chapter title="cargos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Cargo dado ao vincular o usuário
Vincular:
  # ID do cargo no discord
  ID: ''
  # Sincronizar o nick no discord
  Sincronizar:
    Ativar: false
    Nick: '[MEMBRO] {player}'

Cargos:
  vip:
    # Prioridade, quanto maior melhor
    Ordem: 1
    # ID do cargo no discord
    ID: ''
    # Permissão para receber o cargo
    Permissao: 'ydiscordhook.vip'
    # Sincronizar o nick no discord
    Sincronizar:
      Ativar: false
      Nick: '[VIP] {player}'
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
  Vincular:
    Comando: 'vinculardiscord'
    Aliases: [ vincular, vinculardc, dcvincular, discordvincular ]
  Desvincular:
    Comando: 'desvinculardiscord'
    Aliases: [ desvincular, desvinculardc, dcdesvincular, discorddesvincular ]
  Discord:
    Comando: 'discord'
    Aliases: [ ]

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Tag do vinculado
# %ydiscordhook_tag%
Tag: '&a&l[V]'

# Configurações do bot
Bot:
  # Token do bot
  Token: ''
  # ID do grupo (guilda) do discord
  Guild: ''
  # Status do bot
  # Deixe '' (vazio para não usar)
  Status: 'ystoreplugins.com.br'

# Sistema de aviso para vincular
Aviso:
  Ativar: true
  Mensagem:
    - ' '
    - ' &aVocê ainda não vinculou sua conta do discord.'
    - ' &7Utilize &f/vinculardiscord&7 para vincular.'
    - ' '

# Opções gerais do plugin
Opcoes:
  # Ativar a permissão de bypass para não receber cargos
  # Permissão: ydiscordhook.bypass
  Bypass: false
  # Tamanho mínimo do ID
  TamanhoMinimo: 18
  # Enviar mensagem no chat apenas se estiver vinculado
  ChatVinculado: false
  # Habilitar o jogador desvincular o discord
  Desvincular: true
  # Delay para carregar os dados depois do login
  # Necessário para usar em servidor de mina separado
  # Recomendado: 20 ticks
  Login delay: 20
  # Recompensas dadas ao vincular pela primeira vez
  # As recompensas são cadastradas na recompensas.yml
  # Use: chance,recompense
  Recompensas:
    - '100,Reco1'
  # Sistema de verificação do server booster
  Booster:
    Ativar: true
    # ID do cargo do booster
    CargoID: ''
    # Comandos que serão executados
    Comandos:
      # Ao virar booster
      Booster:
        # Executar o comando sempre ao logar
        # caso false, será executado apenas uma vez
        AoLogar: false
        Lista:
          - 'alert {player} virou server booster'
      # Ao não ser mais booster
      NaoBooster:
        Lista:
          - 'alert {player} não é mais server booster'
  # Sistema de verificação do mito (yMito pago)
  Mito:
    Ativar: true
    # ID do cargo do mito
    CargoID: ''

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Cancelou: '&cVocê cancelou a ação.'
  Valido: |
    &cVocê deve por um ID ou TAG válido.
    &7O ID é composto somente por números e com no mínimo 18 números.
    &7A sua tag deve possuir # e não pode conter letras especiais.
  Ja vinculado sua: '&cEste já está vinculado à sua conta.'
  Ja vinculado: '&cEste já está vinculado à {player}.'
  Privado: '&cSeu privado está bloqueado.'
  Errado: '&cO token está errado.'
  Encontrado: '&cO membro com este ID ou TAG não foi encontrado.'
  Enviando: '&aEnviando token...' # deixe '' para não usar
  Nao vinculado: '&cVocê não está vinculado.'
  Nao vinculado player: '&cO jogador &f{player}&c não está vinculado.'
  Jogador: '&cJogador não encontrado.'
  Chat: '&cVocê não pode enviar mensagens antes de se vincular. -> /vincular'
  DesvincularBooster: '&cVocê não pode desvincular enquanto for server-booster.'
  Ja vinculado player: '&cO jogador &f{player}&c já está vinculado.'
  Vinculou target:
    - ''
    - '&aVocê vinculou com sucesso o discord do jogador &f{player}&a.'
    - '&aConta: &f{discord_tag}&a.'
    - '&aID: &f{discord_id}&a.'
    - ''
  Digite:
    - ''
    - '&aDigite o ID do discord que deseja vincular.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Desvinculou:
    - ''
    - '&aVocê desvinculou com sucesso o discord.'
    - '&aConta: &f{discord_tag}&a.'
    - '&aID: &f{discord_id}&a.'
    - ''
  Vinculou:
    - ''
    - '&aVocê vinculou com sucesso o discord.'
    - '&aConta: &f{discord_tag}&a.'
    - '&aID: &f{discord_id}&a.'
    - ''
  Verifique:
    - ''
    - '&aDigite o código enviado à sua DM para completar a verificação.'
    - '&7A verificação irá expirar em 1 minuto.'
    - ''
  Info:
    - ''
    - '&aInformações do jogador &f{player}&a:'
    - '&aConta: &f{discord_tag}&a.'
    - '&aID: &f{discord_id}&a.'
    - ''
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Embeds:
  vincular:
    Title: 'Pedido de vinculação de conta'
    Thumbnail: ''
    Color: '#fff'
    Footer:
      Text: '{data} às {hora}'
      Image: ''
    Description: 'Para completar a verificação, digite o código a seguir no chat do servidor'
    Fields:
      jogador:
        Inline: false
        Header: 'Jogador'
        Content: '{player}'
      codigo:
        Inline: false
        Header: 'Código'
        Content: '{codigo}'
  vinculado:
    Title: 'Vinculação de conta'
    Thumbnail: ''
    Color: '#fff'
    Footer:
      Text: '{data} às {hora}'
      Image: ''
    Description: ''
    Fields:
      jogador:
        Inline: false
        Header: 'Jogador'
        Content: '{player}'
      estado:
        Inline: false
        Header: 'Estado'
        Content: 'Vinculado com sucesso.'
  naoVinculado:
    Title: 'Vinculação de conta'
    Thumbnail: ''
    Color: '#fff'
    Footer:
      Text: '{data} às {hora}'
      Image: ''
    Description: ''
    Fields:
      jogador:
        Inline: false
        Header: 'Jogador'
        Content: '{player}'
      estado:
        Inline: false
        Header: 'Estado'
        Content: 'Você não vinculou em tempo.'
  ystafflogin_verificacao:
    Title: 'Realize seu LoginStaff'
    Thumbnail: ''
    Color: '#fff'
    Content: ''
    Footer:
      Text: 'Todos os direitos reservados'
      Image: ''
    Description: ''
    Fields:
      usuario:
        Inline: false
        Header: 'Usuário'
        Content: '{player}'
      codigo:
        Inline: false
        Header: 'Código'
        Content: '{codigo}'
      ip:
        Inline: false
        Header: 'IP'
        Content: '{ip}'
      data:
        Inline: false
        Header: 'Data'
        Content: '{data} - {hora}'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
  Reco1:
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

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/84-yDiscordHook">Site do plugin yDiscordHook</a>
    </category>
</seealso>