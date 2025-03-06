# yReports
<secondary-label ref="management"/>

### Descrição
Gerencie as denúncias em seu servidor

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
<video src="//www.youtube.com/watch?v=PEhLP4Rj1Ys"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/reportar - Reporta um jogador
/reportar reload - Recarrega as configurações
/reports - Ver a lista de reportes.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yreports.reportar - Permissão para o /reportar
yreports.reload - Permissão para o /reportar reload
yreports.staff - Permissão para ser reconhecido como staff e para o /reports</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yreports_quantia% - Retorna a quantia de reportes formatado (1K, 1M, 1T...)
%yreports_quantia_raw% - Retorna a quantia de reportes sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yReports/
    ├── menus/
    │    ├── gerenciar.yml
    │    ├── provas.yml
    │    ├── punir.yml
    │    ├── reportar.yml
    │    └── reportes.yml
    ├── config.yml
    ├── discord.yml
    ├── motivos.yml
    └── punicoes.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="gerenciar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Gerenciar reporte'
Tamanho: 27
BackSlot: 0
# Itens de gerenciamento
Itens:
  Punir:
    Slot: 11
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/8e2c18ab35949bf9f9e7d6a69b885ccd8cc2efb9475946d7d3fb5c3fef61'
    ID: 1
    Data: 0
    Name: '&cPunir'
    Lore:
      - '&7Clique para punir o jogador.'
  Deletar:
    Slot: 13
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/3ed1aba73f639f4bc42bd48196c715197be2712c3b962c97ebf9e9ed8efa025'
    ID: 1
    Data: 0
    Name: '&aDeletar'
    Lore:
      - '&7Clique para deletar o reporte.'
# Itens customizados
# Aqui você pode criar quantos quiser
Itens custom:
  Jail:
    Slot: 15
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/b00020b44357c1a51cb81c78a6f47e3fc97f0e9dd89ef4d3b9f710b4bd6a0e21'
    ID: 1
    Data: 0
    Name: '&cPrender'
    # Coloque '[console],cmd' para o console executar o comando
    # Coloque '[player],cmd' para o player executar o comando
    Comando: '[console],/tell {staff} Você clicou para prender {player}.'
    Lore:
      - '&7Clique para prender o jogador.'
]]>
</code-block>
</chapter>

<chapter title="provas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Informações do reporte'
Tamanho: 27
BackSlot: 0
VoltarSlot: 9
ProximoSlot: 17
Slots: [11, 12, 13, 14, 15]
# Item do jogador que reportou
Item:
 CustomSkull: true
 URL: '{player}'
 ID: 1
 Data: 0
 Glow: false
 Name: '&aReportador: {player}'
 Lore:
   - ''
   - '&fMotivo: &7{motivo}&f.'
   - '&fProva: &7{prova}&f.'
   - ''
   - '&7Clique para copiar a prova.'
# Itens para enfeitar o menu
Itens: {}
  #Enfeite1:
  #  Slot: 11
  #  CustomSkull: false
  #  URL: ''
  #  ID: 130
  #  Data: 0
  #  Glow: true
  #  Name: '&aEnfeite!'
  #  Lore: []
]]>
</code-block>
</chapter>

<chapter title="punir.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Punir &7{player}'
Tamanho: 27
BackSlot: 0
# Itens para enfeitar o menu
Itens: {}
  #Enfeite1:
  #  Slot: 11
  #  CustomSkull: false
  #  URL: ''
  #  ID: 130
  #  Data: 0
  #  Glow: true
  #  Name: '&aEnfeite!'
  #  Lore: []
]]>
</code-block>
</chapter>

<chapter title="reportar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Reportar &7{player}'
Tamanho: 27
# Itens para enfeitar o menu
Itens: {}
  #Enfeite1:
  #  Slot: 11
  #  CustomSkull: false
  #  URL: ''
  #  ID: 130
  #  Data: 0
  #  Glow: true
  #  Name: '&aEnfeite!'
  #  Lore: []
]]>
</code-block>
</chapter>

<chapter title="reportes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Jogadores reportados'
Tamanho: 27
VoltarSlot: 9
ProximoSlot: 17
Slots: [11, 12, 13, 14, 15]
# Formato do motivo
Formato: '&f > {motivo}: &7{quantia}'
# Item do jogador reportado
Item:
 CustomSkull: true
 URL: '{player}'
 ID: 1
 Data: 0
 Glow: false
 Name: '&a{player}'
 Lore:
   - '&7Informações do jogador reportado:'
   - ''
   - '&7Motivos:'
   - '{motivos}'
   - ''
   - '&7Quantia de reportes: &a{quantia}'
   - '&7Último reporte em: &b{data} &8- &b{hora}'
   - ''
   - '&fBotão esquerdo &8- &7teleportar ao jogador.'
   - '&fBotão direito &8- &7ver quem reportou e as provas.'
   - '&fBotão Q &8- &7gerenciar o reporte.'
# Itens para enfeitar o menu
Itens: {}
  #Enfeite1:
  #  Slot: 11
  #  CustomSkull: false
  #  URL: ''
  #  ID: 130
  #  Data: 0
  #  Glow: true
  #  Name: '&aEnfeite!'
  #  Lore: []
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

# Comandos e aliases do plugin
Comando:
  Reportar:
    Comando: 'reportar'
    Aliases: [report, denunciar]
  Reports:
    Comando: 'reports'
    Aliases: [reports, denuncias]

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

# Opções gerais de configuração do plugin
Opcoes:
  # Remover o reporte quando for aplicada uma punição
  # pelo menu de gerenciamento
  Remover punido: true
  # Bloquear de reportar staff
  # Permissão para ser reconhecido como staff: yreports.staff
  Bloquear staff: true
  # Habilitar o sistema de provas para reportar
  Provas: true
  # Sempre exigir uma prova para reportar
  Exigir prova: false
  # Lista de links permitidos para a prova de reporte.
  Links:
    - 'https://youtu.be'
    - 'https://youtube'
    - 'https://imgur'

# Mensagens que serão enviadas para
# quem tiver a permissão: yreports.staff
Staff mensagens:
  # Quando o jogador for reportado pela primeira vez
  Novo reporte:
    - ''
    - '&aUma denúncia foi registrada contra o jogador &7{player}&a.'
    - ''
  # Quando o jogador for reportado 2x ou mais
  Reportado novamente:
    - ''
    - '&aO jogador &7{player}&a foi denunciado novamente.'
    - ''
  # Quando o jogador que estiver sido reportado entrar
  Reportado entrou:
    - ''
    - '&aO jogador &7{player}&a foi denúnciado anteriormente e logou novamente no servidor.'
    - ''

# Mensagens gerais do plugin
Mensagens:
  Use: '&c/reportar <player>'
  Permissao: '&cVocê não tem permissão para isto.'
  Nao encontrado: '&cJogador não encontrado.'
  Cancelou: '&cVocê cancelou o report.'
  Ja reportou: '&cVocê já reportou este jogador.'
  Link nao: '&cEste link não é permitido. &7Digite &ncancelar&7 para cancelar.'
  Reportou: '&aVocê reportou o jogador &7{player} &apor &7{motivo}&a.'
  Teleportado: '&aVocê foi teleportado ao jogador &7{player}&a.'
  Deletado: '&aDenúncia deletada.'
  Punicao permissao: '&cVocê não tem permissão para aplicar esta punição.'
  Reportar staff: '&cVocê não pode reportar staff.'
  Si mesmo: '&cVocê não pode reportar a si mesmo.'
  Puniu: '&aVocê puniu o jogador &7{player}&a.'
  Acrescentar:
    - ''
    - '&aVocê deseja inserir alguma prova?'
    - '&7Digite &nSIM&7 ou &nNAO&7.'
    - ''
  Adicionar:
    - ''
    - '&aDigite abaixo o link da prova da denúncia.'
    - '&7Digite &ncancelar&7 para cancelar.'
    - ''
  Prova:
    - '&7Prova: &b{prova}&7.'

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

# Formatos de quantia e money
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
  Username: 'yReports'
  Ativar: false
#
# Placeholders:
# {motivo} - motivo do report
# {reportado} - player que foi reportado
# {reportador} - player que reportou
# {prova} - prova do report
# {data} - data do report
# {hora} - hora do report
#
Embeds:
  newReport: # não mude este nome
    Title: 'Novo report'
    Thumbnail: ''
    Color: '#fff'
    Content: 'Um novo report foi registrado!\n@everyone'
    Footer:
      Text: 'Todos os direitos reservados'
      Image: ''
    Fields:
      server:
        Inline: true
        Header: 'Servidor'
        Content: 'RankUP'
      data:
        Inline: true
        Header: 'Data'
        Content: '{data} - {hora}'
      reportador:
        Inline: false
        Header: 'Denunciante'
        Content: '{reportador}'
      reportado:
        Inline: false
        Header: 'Reportado'
        Content: '{reportado}'
      motivo:
        Inline: false
        Header: 'Motivo'
        Content: '{motivo}'
]]>
</code-block>
</chapter>

<chapter title="motivos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Motivos:
  1:
    Display:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/3c0dae47a7675ba073d7ef55741f0fa5cce8b634e00ace65451c5576c27acc78'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aUso de Hack'
      Lore:
        - '&7Clique para reportar o jogador'
        - '&f{player} &7por Uso de Hack.'
    Motivo: 'Uso de Hack'
    # Ações que são executadas com um mínimo de reporte
    # deste mesmo motivo
    # quantia,comando
    Acoes:
      - '1,alerta O jogador {player} foi reportado. Este é um exemplo de ação com mínimo'
  2:
    Display:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/a33f4875e72e0e40f3968ba5ad3246417ce7129d0862e65661310511e3d5e654'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aOfensa à Jogador'
      Lore:
        - '&7Clique para reportar o jogador'
        - '&f{player} &7por Ofensa à Jogador.'
    Motivo: 'Ofensa à Jogador'
    Acoes: []
  3:
    Display:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/14a37e5e3a5dae6d2781faef7cd4ee98b01f0d0a4293432ab3bcba5a3bced19b'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aAnti-Jogo'
      Lore:
        - '&7Clique para reportar o jogador'
        - '&f{player} &7por Anti-Jogo.'
    Motivo: 'Anti-Jogo'
    Acoes: []
]]>
</code-block>
</chapter>

<chapter title="punicoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Punicoes:
  1:
    Display:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/3c0dae47a7675ba073d7ef55741f0fa5cce8b634e00ace65451c5576c27acc78'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aUso de Hack'
      Lore:
        - '&7Clique para punir o jogador'
        - '&f{player} &7por Uso de Hack.'
    # Permissão para executar a punição
    Permissao: 'yreports.punicao.usodehack'
    # Comandos que serão executados pelo console
    Comandos:
      - 'alerta O jogador {player} foi punido por uso de hack'
  2:
    Display:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/a33f4875e72e0e40f3968ba5ad3246417ce7129d0862e65661310511e3d5e654'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aOfensa à Jogador'
      Lore:
        - '&7Clique para punir o jogador'
        - '&f{player} &7por Ofensa à Jogador.'
    # Permissão para executar a punição
    Permissao: 'yreports.punicao.ofensaajogador'
    # Comandos que serão executados pelo console
    Comandos:
      - 'alerta O jogador {player} foi punido por ofensa à jogador'
  3:
    Display:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/14a37e5e3a5dae6d2781faef7cd4ee98b01f0d0a4293432ab3bcba5a3bced19b'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aAnti-Jogo'
      Lore:
        - '&7Clique para punir o jogador'
        - '&f{player} &7por Anti-Jogo.'
    # Permissão para executar a punição
    Permissao: 'yreports.punicao.antijogo'
    # Comandos que serão executados pelo console
    Comandos:
      - 'alerta O jogador {player} foi punido por anti-joho'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/49-yReports">Site do plugin yReports</a>
    </category>
</seealso>