# yRecomendar
<secondary-label ref="utility"/>

### Descrição
Permita que jogadores recomendem outros e ganhe recompensas por isso!

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
<video src="//www.youtube.com/watch?v=p8acQkIITWM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/recomendar - Abre o menu principal
/recomendar reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yrecomendar.usar - Permissão para o /recomendar
yrecomendar.reload - Permissão para o /recomendar reload</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yRecomendar/
    ├── menus/
    │    ├── principal.yml
    │    ├── recomendados.yml
    │    ├── recompensas.yml
    │    └── top.yml
    ├── config.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Recomendar - Principal'
Tamanho: 27
Itens:
   Recomendar slot: 15
   Perfil: # primeiro
      Slot: 10
      Name: '&f{player}'
      Lore:
      - ''
      - '&7Você foi recomendado &f{vezes} &avezes.'
      - ''
   Recompensas: #segundo
      Slot: 11
      CustomSkull: false
      URL: ''
      ID: 54
      Data: 0
      Glow: false
      Name: '&aRecompensas'
      Lore:
      - '&7Clique para gerenciar as recompensas de ser recomendado.'
   Top: #terceiro
      Slot: 12
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: false
      Name: '&aTOP'
      Lore:
      - '&7Clique para ver os jogadores mais recomendados.'
   Recomendar sim: #quarto
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      ID: 0
      Data: 0
      Glow: false
      Name: '&aRecomendar'
      Lore:
      - '&7Clique para recomendar um jogador.'
   Recomendar nao: #quarto
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aRecomendar'
      Lore:
      - '&cVocê já recomendou um jogador: &7{player}&c.'

]]>
</code-block>
</chapter>

<chapter title="recomendados.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Quem recomendou'
Tamanho: 36
Slots: [ 10, 11, 12, 13, 14, 15, 16 ]
BackSlot: 31
AnteriorSlot: 9
ProximoSlot: 17
Item:
  CustomSkull: true
  URL: '{player}'
  ID: 0
  Data: 0
  Name: '&a{player}'
  Lore:
    - ''
    - '&fVocê foi recomendado 1x por: &a{player}&f.'
    - ''
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Recomendar recompensas'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 9
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="top.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8TOP Recomendacoes'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 30

Item:
   Name: '&7#&f{pos} - &e{player}'
   Lore:
   - ''
   - '&fRecomendações: &6{recomendacoes}'
   - '&fPosição: &6{pos}'
   - ''

Item p:
   Slot: 32
   Name: '&7#&f{pos} - &aVocê &7({player})'
   Lore:
   - ''
   - '&fRecomendações: &6{recomendacoes}'
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
   Tipo: SQLITE #Tipos: MYSQL, SQLITE, MYSQL_FAST
   IP: localhost:3306
   DB: test
   User: admin
   Pass: ''
   Debug: true

Comando:
   Comando: 'recomendar'
   Aliases: []

# Ativar a troca do sistema de chat quando estiver no mohist
# compatível apenas com: UltimateChat, nChat e Legendchat
mohist-chat: false

Msg coleta: true
# Permissão para poder ser recomendado
# Deixe '' para não usar
Permissao recomendado: ''

# Recomendar apenas se estiver vinculado (yDiscordHook)
Vinculado: false

Tempo: #exclusivo yTempoOnline
   Minimo: 60 #em segundos
   Msg: '&c&lERRO! &cVocê deve estar online por pelo menos 1 minuto antes de recomendar alguém.'

Mensagens:
   Cancelou: '&cVocê cancelou a ação.'
   Recomendou: '&aVocê recomendou o jogador &7{player}&a, ele já foi recomendado &7{vezes}&a vezes.'
   Nao encontrado: '&cJogador não encontrado.'
   Permissao: '&cVocê não tem permissão para isto.'
   Coletou: '&aVocê coletou a recompensa.'
   Si mesmo: '&cVocê não pode recomendar a si mesmo.'
   Nao pode: '&cEste jogador não pode ser recomendado.'
   Ja recomendou: '&cVocê já recomendou um jogador.'
   Chat vinculado: '&cVocê precisa vincular seu discord primeiro. /discord para vincular.'
   Ajuda: |
      &cComandos disponíveis:
      &c -> /recomendar
      &c -> /recomendar <player>
      &c -> /recomendar ajuda
   Digite:
   - ''
   - '&aDigite o nome do jogador que deseja recomendar.'
   - '&7para cancelar digite &ncancelar&7.'
   - ''
   
Setas:
   Voltar:
      CustomSkull: false
      URL: ''
      ID: 262
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
      ID: 262
      Data: 0
      Glow: true
      Name: '&aPróximo'
      Lore:
      - ''
      - '&7Clique para ir à próxima página.'
      - ''
      
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
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   1:
      Display:
         CustomSkull: false
         URL: ''
         ID: 388
         Data: 0
         Glow: true
         Name: '&8Pedra'
         Lore: 
         - '&7Seja recomendado por &f1 &7jogador e ganhe'
         - '&7 -> &a1 pedra.'
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
      Recomendacoes: 1
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'
   2:
      Display:
         CustomSkull: false
         URL: ''
         ID: 388
         Data: 0
         Glow: true
         Name: '&8Diamantes'
         Lore: 
         - '&7Seja recomendado por &f2 &7jogadores e ganhe'
         - '&7 -> &a2 diamantes.'
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
         Enchants: #se não desejar, deixe assim:
         - ''
      Recomendacoes: 2
      Command:
         Use: true
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} diamond 2'

]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/26-yRecomendar">Site do plugin yRecomendar</a>
    </category>
</seealso>