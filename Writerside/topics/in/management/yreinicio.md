# yReinicio
<secondary-label ref="management"/>

### Descrição
Reinicie seu servidor automaticamente e bloqueie ações

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
<video src="//www.youtube.com/watch?v=Pp1HeIrgqS4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/reinicio forcar - Forçar o início de um reinício
/reinicio editar - Editar um reinício
/reinicio cancelar - Cancelar um reinício
/reinicio reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yreinicio.usar - Permissão para o /reinicio
yreinicio.chat.bypass - Permissão para o bypass de falar no chat
yreinicio.colocar.bypass - Permissão para o bypass de colocar blocos
yreinicio.comando.bypass - Permissão para o bypass de enviar comandos
yreinicio.dropar.bypass - Permissão para o bypass de dropar itens
yreinicio.enderpearl.bypass - Permissão para o bypass de jogar enderpearl
yreinicio.interagir.bypass - Permissão para o bypass de interagir em blocos bloqueados
yreinicio.pegar.bypass - Permissão para o bypass de pegar itens
yreinicio.quebrar.bypass - Permissão para o bypass de quebrar blocos</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yReinicio/
    ├── menus/
    │    └── principal.yml
    ├── reinicios/
    │    └── manha.yml
    ├── config.yml
    └── discord.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Editar {reinicio}'
Tamanho: 36
Chat slot: 19
Colocar slot: 20
Quebrar slot: 21
Pegar slot: 22
Dropar slot: 23
Comandos slot: 24
Enderpearl slot: 25
Pvp slot: 28
Itens:
 Chat Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fChat'
  Lore:
  - '&7Estado: &aLigado'
 Chat Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fChat'
  Lore:
  - '&7Estado: &cDesligado'
 Colocar Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fColocar'
  Lore:
  - '&7Estado: &aLigado'
 Colocar Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fColocar'
  Lore:
  - '&7Estado: &cDesligado'
 Quebrar Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fQuebrar'
  Lore:
  - '&7Estado: &aLigado'
 Quebrar Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fQuebrar'
  Lore:
  - '&7Estado: &cDesligado'
 Pegar Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fPegar'
  Lore:
  - '&7Estado: &aLigado'
 Pegar Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fPegar'
  Lore:
  - '&7Estado: &cDesligado'
 Dropar Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fDropar'
  Lore:
  - '&7Estado: &aLigado'
 Dropar Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fDropar'
  Lore:
  - '&7Estado: &cDesligado'
 Comandos Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fComandos'
  Lore:
  - '&7Estado: &aLigado'
 Comandos Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fComandos'
  Lore:
  - '&7Estado: &cDesligado'
 Enderpearl Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fEnderpearl'
  Lore:
  - '&7Estado: &aLigado'
 Enderpearl Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fEnderpearl'
  Lore:
  - '&7Estado: &cDesligado'
 Pvp Ativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 5
  Glow: false
  Name: '&fPvP'
  Lore:
  - '&7Estado: &aLigado'
 Pvp Desativado:
  CustomSkull: false
  URL: ''
  ID: 160
  Data: 14
  Glow: false
  Name: '&fPvP'
  Lore:
  - '&7Estado: &cDesligado'
# Itens customizados
CustomItens: {}
#VOCÊ PODE ENFEITAR SEU MENU CRIANDO OUTROS ITENS EM CustomItens :)
]]>
</code-block>
</chapter>

</chapter>

<chapter title="reinicios" collapsible="true">
<chapter title="manha.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Habilitar comandos
Comandos: true
# Lista de comandos bloqueados
# coloque minúsculo
Comandos bloqueados:
  - '/pl'
# Lista de blocos que você não poderá interagir
# Recomendados:
# TRAPPED_CHEST(baú com trap), CHEST(baú), ENDERCHEST(baú do fim), ANVIL(bigorna), WORKBENCH(mesa de trabalho),
# ENCHANTMENT_TABLE(mesa de encantamento), FURNACE(fornalha), DISPENSER, DROPPER, BEACON, LEVER(alavanca), STONE_BUTTON(botão de pedra), WOOD_BUTTON(botão de madeira)
Interagir bloqueados:
  - 'TRAPPED_CHEST'
  - 'CHEST'
  - 'ENDERCHEST'
  - 'ANVIL'
  - 'WORKBENCH'
  - 'ENCHANTMENT_TABLE'
  - 'FURNACE'
  - 'DISPENSER'
  - 'DROPPER'
  - 'BEACON'
  - 'LEVER'
  - 'STONE_BUTTON'
  - 'WOOD_BUTTON'
# Habilitar jogar enderpearl
Enderpearl: false
# Habilitar falar no chat
Chat: false
# Habilitar dropar itens
Dropar: false
# Habilitar pegar itens
Pegar: false
# Habilitar colocar blocos
Colocar: false
# Habilitar quebrar blocos
Quebrar: false
# Habilitar mexer no inventário
MexerInventario: true
# Lista de comandos que serão executados ao começar o reinicio
Comandos executar:
  - 'save-all'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
  Comando: 'reinicio'
  Aliases: [ reiniciar ]

# Opções gerais do plugin
Opcoes:
  # Tempo que o servidor irá demorar para reiniciar após o reinício começar
  # em segundos
  Tempo: 180
  # Ativar o modo enviar para outro servidor
  Bungeecord: true
  # Lista de lobbies
  Lobby list: [ 'lobby' ]
  # Comandos que serão executados ao ligar o servidor
  Comandos start: [ 'alerta Servidor ligado!' ]

# Autostart do restart
Autostart:
  horario1:
    # nome do arquivo da pasta reinicios sem o .yml
    Tipo: 'manha'
    # todos, segunda, terca, quarta, quinta, sexta, sabado, domingo
    # dia-hora-minuto-segundo
    Horario: 'todos-00:00:01'

# Mensagens gerais do plugin
Mensagens:
  Permissao: '&cVocê não tem permissão para isto.'
  Comandos: |
    &cComandos disponíveis:
    &f> &c/reinicio forcar <tipo>
    &f> &c/reinicio editar <tipo>
    &f> &c/reinicio cancelar
  Existe: '&cEste tipo não existe. Disponíveis: &7{tipos}&c.'
  Nao esta: '&cNão está ocorrendo nenhum reinício.'
  Ja esta: '&cJá está ocorrendo um reinício.'
  Enviado: '&cO servidor que você estava está reiniciando, por isso te enviamos ao lobby.'
  Kick: '&c&lyStore<nl><nl>&c&lSERVIDOR REINICIANDO<nl><nl>'
  Parou: '&cVocê parou o reinício.'
  Comecou: '&aVocê começou o reinício.'
  Quebrar: '&cVocê não pode quebrar blocos enquanto o servidor estiver em modo de reinício.'
  Colocar: '&cVocê não pode colocar blocos enquanto o servidor estiver em modo de reinício.'
  Pegar: '&cVocê não pode pegar itens enquanto o servidor estiver em modo de reinício.'
  Dropar: '&cVocê não pode dropar itens enquanto o servidor estiver em modo de reinício.'
  Enderpearl: '&cVocê não pode jogar enderpearls enquanto o servidor estiver em modo de reinício.'
  Comandos block: '&cVocê não pode executar comandos enquanto o servidor estiver em modo de reinício.'
  Comando: '&cVocê não pode executar este comando enquanto o servidor estiver em modo de reinício.'
  Interagir: '&cVocê não pode interagir com este bloco enquanto o servidor estiver em modo de reinício.'
  Chat: '&cVocê não pode enviar mensagens enquanto o servidor estiver em modo de reinício.'
  Pvp: '&cVocê não pode entrar em pvp enquanto o servidor estiver em modo de reinício.'
  MexerInventario: '&cVocê não pode mexer no inventário enquanto o servidor estiver em modo de reinício.'
  Cancelado:
    - ''
    - '&b[REINICIO] &fUm administrador cancelou o reinício.'
    - ''
  Iniciado:
    - ''
    - '&b[REINICIO] &fO servidor irá reiniciar em &b3 minutos&f.'
    - ''

# Anuncios de restart de acordo aos segundos
Anuncios:
  - '120,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b2 minutos&f.<nl>&r'
  - '60,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b1 minuto&f.<nl>&r'
  - '30,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b30 segundos&f.<nl>&r'
  - '15,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b15 segundos&f.<nl>&r'
  - '5,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b5 segundos&f.<nl>&r'
  - '4,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b4 segundos&f.<nl>&r'
  - '3,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b3 segundos&f.<nl>&r'
  - '2,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b2 segundos&f.<nl>&r'
  - '1,<nl>&b[REINICIO] &fO servidor irá reiniciar em &b1 segundo&f.<nl>&r'

# Anuncios de restart de acordo aos segundos (na actionbar)
Actionbar:
  - '120,&b[REINICIO] &fO servidor irá reiniciar em &b2 minutos&f.&r'
  - '60,&b[REINICIO] &fO servidor irá reiniciar em &b1 minuto&f.&r'
  - '30,&b[REINICIO] &fO servidor irá reiniciar em &b30 segundos&f.&r'
  - '15,&b[REINICIO] &fO servidor irá reiniciar em &b15 segundos&f.&r'
  - '5,&b[REINICIO] &fO servidor irá reiniciar em &b5 segundos&f.&r'
  - '4,&b[REINICIO] &fO servidor irá reiniciar em &b4 segundos&f.&r'
  - '3,&b[REINICIO] &fO servidor irá reiniciar em &b3 segundos&f.&r'
  - '2,&b[REINICIO] &fO servidor irá reiniciar em &b2 segundos&f.&r'
  - '1,&b[REINICIO] &fO servidor irá reiniciar em &b1 segundo&f.&r'

# Sons que serão enviados de acordo aos segundos
Sons:
  - '120,NOTE_STICKS'
  - '60,NOTE_STICKS'
  - '30,NOTE_STICKS'
  - '15,NOTE_STICKS'
  - '5,NOTE_STICKS'
  - '4,NOTE_STICKS'
  - '3,NOTE_STICKS'
  - '2,NOTE_STICKS'
  - '1,NOTE_PLING'

# Anúncios que serão enviados ao discord de acordo aos segundos
Discord:
  - '60,aviso1'

# Comandos que serão executados de acordo aos segundos
Comandos:
  - '5,alerta Reiniciando em 5s...'
]]>
</code-block>
</chapter>

<chapter title="discord.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Options:
  URL: ''
  Username: 'yReinicio'
  Ativar: false
  # Enviar um webhook no discord assim que o plugin ligar
  LoadWebhook:
    Ativar: false
    Anuncio: 'online'
Embeds:
  aviso1:
    Title: 'Servidor reiniciando em 1 minuto...'
    Thumbnail: ''
    Color: '#fff'
    Content: '@everyone'
    Footer:
      Text: 'Todos os direitos reservados'
      Image: ''
    Fields:
      reiniciando:
        Inline: false
        Header: 'Reiniciando em'
        Content: '1 minuto'
      server:
        Inline: false
        Header: 'Servidor'
        Content: 'RankUP'
      data:
        Inline: false
        Header: 'Data'
        Content: '{data} - {hora}'
  online:
    Title: 'Servidor online!'
    Thumbnail: ''
    Color: '#fff'
    Content: 'Estamos online novamente!\n@everyone'
    Footer:
      Text: 'Todos os direitos reservados'
      Image: ''
    Fields:
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


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/80-yReinicio">Site do plugin yReinicio</a>
    </category>
</seealso>