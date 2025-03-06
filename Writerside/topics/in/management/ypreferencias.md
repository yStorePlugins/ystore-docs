# yPreferencias
<secondary-label ref="management"/>

### Descrição
Pare de ser chateado por outros jogadores

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
<video src="//www.youtube.com/watch?v=fLPjyKBLbXQ"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/preferencias - Abre o menu principal
/preferencias reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ypreferencias.usar - Permissão para o /preferencias
ypreferencias.reload - Permissão para o /preferencias reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yPreferencias/
    ├── menus/
    │    └── principal.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Preferências'
Tamanho: 36
ChatGlobal slot: 19
ChatLocal slot: 20
ChatPrivado slot: 21
Coins slot: 22
Teleporte slot: 23
Coletar slot: 24
Clan slot: 25 # apenas compatível com o yClans (só aparece com ele ligado)
Sell-Message slot: 26 # apenas compatível com o yVender (só aparece com ele ligado)
Itens:
 ChatGlobal Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fChat global'
  Lore:
  - '&7Estado: &aLigado'
 ChatGlobal Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fChat global'
  Lore:
  - '&7Estado: &cDesligado'
 ChatLocal Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fChat local'
  Lore:
  - '&7Estado: &aLigado'
 ChatLocal Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fChat local'
  Lore:
  - '&7Estado: &cDesligado'
 ChatPrivado Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fMensagens privadas'
  Lore:
  - '&7Estado: &aLigado'
 ChatPrivado Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fMensagens privadas'
  Lore:
  - '&7Estado: &cDesligado'
 Coins Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fRecebimento de coins'
  Lore:
  - '&7Estado: &aLigado'
 Coins Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fRecebimento de coins'
  Lore:
  - '&7Estado: &cDesligado'
 Teleporte Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fPedidos de teleporte'
  Lore:
  - '&7Estado: &aLigado'
 Teleporte Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fPedidos de teleporte'
  Lore:
  - '&7Estado: &cDesligado'
 Coletar Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fColetar itens dropados'
  Lore:
  - '&7Estado: &aLigado'
 Coletar Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fColetar itens dropados'
  Lore:
  - '&7Estado: &cDesligado'
 Clan Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fConvite de clans'
  Lore:
  - '&7Estado: &aLigado'
 Clan Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fConvite de clans'
  Lore:
  - '&7Estado: &cDesligado'
 Sell-Message Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fMensagem de Venda (chat)'
  Lore:
  - '&7Estado: &aLigado'
 Sell-Message Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fMensagem de Venda (chat)'
  Lore:
  - '&7Estado: &cDesligado'
# Itens customizados
CustomItens:
 Global:
  Slot: 10
  CustomSkull: false
  URL: ''
  ID: 386
  Data: 0
  Glow: true
  Name: '&aChat global'
  Lore:
  - '&7Deseja receber mensagens do chat global?'
 Local:
  Slot: 11
  CustomSkull: false
  URL: ''
  ID: 358
  Data: 0
  Glow: true
  Name: '&aChat local'
  Lore:
  - '&7Deseja receber mensagens do chat local?'
 Privado:
  Slot: 12
  CustomSkull: false
  URL: ''
  ID: 339
  Data: 0
  Glow: true
  Name: '&aChat privado'
  Lore:
  - '&7Deseja receber mensagens no chat privado?'
 Coins:
  Slot: 13
  CustomSkull: false
  URL: ''
  ID: 371
  Data: 0
  Glow: true
  Name: '&aCoins'
  Lore:
  - '&7Deseja receber coins de outros jogadores?'
 Teleporte:
  Slot: 14
  CustomSkull: false
  URL: ''
  ID: 368
  Data: 0
  Glow: true
  Name: '&aTeleporte'
  Lore:
  - '&7Deseja receber solicitações de teleporte de outros jogadores?'
 Coletar:
  Slot: 15
  CustomSkull: false
  URL: ''
  ID: 154
  Data: 0
  Glow: true
  Name: '&aColetar itens dropados'
  Lore:
  - '&7Deseja coletar os itens dropados no chão?'
 Clans:
  Slot: 16
  CustomSkull: false
  URL: ''
  ID: 276
  Data: 0
  Glow: true
  Name: '&aConvite de clans'
  Lore:
  - '&7Deseja receber convites para integrar clans?'
 Sell-Message:
  Slot: 17
  CustomSkull: false
  URL: ''
  ID: EMERALD
  Data: 0
  Glow: true
  Name: '&aMensagem de Venda (chat)'
  Lore:
  - '&7Deseja receber mensagens de venda de itens?'
#VOCÊ PODE ENFEITAR SEU MENU CRIANDO OUTROS ITENS EM CustomItens :)
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

# Comando e aliases do plugin
Comando:
 Comando: 'preferencias'
 Aliases: [toggle, opcoes]

#Coloque Legendchat, OpeNChat (ou nChat) ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'

# Delay para carregar os dados depois do login
# Necessário para usar em servidor de mina separado
# Recomendado: 20 ticks
Login delay: 20

# Mensagens do plugin
Mensagens:
 Permissao: '&c&lERRO! &cVocê não tem permissão para isto.'
 Desativou tell: '&cEste jogador desativou o recebimento de mensagens privadas.'
 Desativou coins: '&cEste jogador desativou o recebimento de coins.'
 Desativou teleporte: '&cEste jogador desativou o recebimento de solicitações de teleporte.'
 Desativou global: '&cVocê desativou seu chat global.'
 Desativou local: '&cVocê desativou seu chat local.'
 Nao encontrado: '&cJogador não encontrado.'

# Configurações do chat
Chat global nome: 'global'
Chat local nome: 'local'

# Comandos de teleporte
# Deixe sempre o espaço " " no comando antes do nick
Comandos tp:
 - '/tpa '
 - '/etpa '
 - '/tpahere '
 - '/etpahere '

# Comandos de money
# Deixe sempre o espaço " " no comando antes do nick
Comandos coin:
 - '/pay '
 - '/money pay '
 - '/eco pay '
 - '/bal pay '
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/39-yPreferencias">Site do plugin yPreferencias</a>
    </category>
</seealso>