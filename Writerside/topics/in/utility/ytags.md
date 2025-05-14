# yTags
<secondary-label ref="utility"/>

### Descrição
Dê uma cara nova ao chat, crie tags que podem ser compradas com CASH e MONEY.

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
<video src="https://www.youtube.com/watch?v=VyXm4z1iC8s"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/tags - Abrir o menu de tags.
/tags cash - Abrir o menu de tag por cash
/tags money - Abrir o menu de tags por money
/tags info - Vê as informações de um jogador.
/tags add - Adiciona uma tag à um jogador.
/tags del - Remove uma tag de um jogador.
/tags dar - Dar uma tag em forma de item à um jogador.
/tags darpacote - Dar um pacote de tags em forma de item à um jogador.
/tags setar - Setar uma tag própria para um jogador.
/tags limpar - Limpa a tag própria de um jogador.
/tags forcar - Força o player a abrir o menu de tags.
/tags reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytags.usar - Permissão para o /tags, /tags cash e /tags money
ytags.info - Permissão para o /tags info
ytags.add - Permissão para o /tags add
ytags.del - Permissão para o /tags del
ytags.dar - Permissão para o /tags dar
ytags.darpacote - Permissão para o /tags darpacote
ytags.setar - Permissão para o /tags setar
ytags.limpar - Permissão para o /tags limpar
ytags.forcar - Permissão para o /tags forcar
ytags.reload - Permissão para o /tags reload
ytags.help - Permissão para visualizar a mensagem de ajuda</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yTags/
    ├── menus/
    │    ├── cash.yml
    │    ├── coins.yml
    │    ├── naoCompravel.yml
    │    ├── possui.yml
    │    └── principal.yml
    ├── config.yml
    ├── pacotes.yml
    └── tags.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="cash.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Tags > Cash'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 18
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="coins.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Tags > Coins'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 18
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="naoCompravel.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Tags > Não comprável'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 18
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="possui.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Tags > Suas tags'
Tamanho: 27
Slots: [11, 12, 13, 14, 15]
BackSlot: 9
VoltarSlot: 18
ProximoSlot: 17
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&7Tags > Principal'
Tamanho: 27
Itens:
   Perfil:
      Slot: 10
      CustomSkull: true
      URL: '{player}'
      ID: AIR
      Data: 0
      Glow: false
      Name: '&aSuas Informações'
      Lore:
         - ''
         - '&f Tags Adquiridas: &b{tags}&f.'
         - '&f Tag Equipada: &c{equipada}&f.'
         - '&f Tag Customizada: &c{custom}&f.'
         - ''
         - '&aClique para ver suas tags adquiridas.'
   Coins:
      Slot: 12
      CustomSkull: false
      URL: ''
      ID: IRON_INGOT
      Data: 0
      Glow: false
      Name: '&fMoney'
      Lore:
         - '&7Clique para ver as tags que podem ser'
         - '&7compradas usando money.'
   Cash:
      Slot: 14
      CustomSkull: false
      URL: ''
      ID: GOLD_INGOT
      Data: 0
      Glow: false
      Name: '&6Cash'
      Lore:
         - '&7Clique para ver as tags que podem ser'
         - '&7compradas usando cash.'
   Nao compravel:
      Slot: 16
      CustomSkull: false
      URL: ''
      ID: EMERALD
      Data: 0
      Glow: false
      Name: '&aNão comprável'
      Lore:
         - '&7Clique para ver as tags que não podem'
         - '&7ser compradas.'
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
   Comando: 'tags'
   Aliases: [tag]

#Coloque Legendchat, OpeNChat (ou nChat), UltimateChat, NoxusChat ou deixe Automatico para o auto-detect
Plugin de chat: 'Automatico'

Tag propria:
   Chat: true
   Placeholder: true
   
Mensagens:
   Permissao: '&c&lERRO! &cVocê não tem permissão para isto.'
   Nao tem pontos: '&cDesculpe, mas você não possui a quantia necessária de pontos, &7{pontos} pontos&c.'
   Nao tem money: '&cDesculpe, mas você não possui a quantia necessária de money, &7{money} money&c.'
   Comprou: '&aObrigado pela sua compra, você adquiriu 1x &7Tag ( {tag} &7)&a com sucesso.'
   Nao encontrado: '&c&lERRO! &cJogador não encontrado.'
   Setada: '&a&lSUCESSO! &aVocê setou a tag do jogador &7{player} &apara &7{tag}&a.'
   Limpa: '&a&lSUCESSO! &aVocê limpou a tag do jogador &7{player}&a.'
   Recebeu: '&aVocê recebeu um vale-tag da tag &7{tag}&a.'
   Ativou: '&aVocê ativou um vale-tag da tag &7{tag}&a.'
   Ja tem: '&c&lERRO! &cVocê já possui esta tag.'
   Ja tem player: '&c&lERRO! &cEste jogador já possui esta tag.'
   Deu: '&aVocê deu um vale-tag da tag &7{tag}&a para o jogador &7{player}&a.'
   Adicionou: '&aVocê adicionou a tag &7{tag}&a para o jogador &7{player}&a.'
   Deu pacote: '&aVocê deu um pacote de tags &7{pacote}&a para o jogador &7{player}&a.'
   Recebeu pacote: '&aVocê recebeu um pacote de tags &7{pacote}&a.'
   Ja tem todas: '&c&lERRO! &cVocê já possui todas as tags deste pacote.'
   Ativou pacote: '&aVocê ativou um pacote de tags &7{pacote}&a.'
   Permissao tag: '&cVocê não pode usar esta tag.'
   Nao tem player: '&c&lERRO! &cEste jogador não possui esta tag.'
   Removeu: '&aVocê removeu a tag &7{tag}&a do jogador &7{player}&a.'
   Info:
   - ''
   - '&aInformações do jogador &7{player}&a:'
   - '&f > &bTag equipada: &7{tag}&f.'
   - '&f > &bTag própria: &7{owntag}&f.'
   - ''
   Comandos:
   - ''
   - '&aLista de comandos:'
   - '&f > /tag &8&l- &7Abre o menu principal.'
   - '&f > /tag cash &8&l- &7Abre o menu de tags por cash.'
   - '&f > /tag money &8&l- &7Abre o menu de tags por money.'
   - '&f > /tag info &f<player> &8&l- &7Vê as informações de um jogador.'
   - '&f > /tag setar &f<player> <tag> &8&l- &7Seta uma tag customizada à um jogador.'
   - '&f > /tag limpar &f<player> &8&l- &7Limpa a tag customizada de um jogador.'
   - '&f > /tag add &f<player> <tag> &8&l- &7Adiciona uma tag à um jogador.'
   - '&f > /tag dar &f<player> <tag> &8&l- &7Da uma tag em forma de item à um jogador.'
   - '&f > /tag darpacote &f<player> <pacote> &8&l- &7Da um pacote de tags em forma de item à um jogador.'
   - ''
   
Vale tag:
   CustomSkull: false
   URL: ''
   ID: NAME_TAG
   Data: 0
   Glow: true
   Name: '&aVale Tag &8&l- &7{tag}'
   Lore:
   - '&7Tag: &f{tag}&7.'
   - ''
   - '&7Clique com botão direito para ativar.'
         
Setas:
   Voltar:
      CustomSkull: false
      URL: ''
      ID: ARROW
      Data: 0
      Glow: true
      Name: '&cVoltar'
      Lore:
      - '&7Clique para voltar ao menu ou página anterior.'
   Proximo:
      CustomSkull: false
      URL: ''
      ID: ARROW
      Data: 0
      Glow: true
      Name: '&aPróxima'
      Lore:
      - '&7Clique para ir à próxima página.'
      
Lores:
   Equipar:
      Sobrepor: true
      Lore:
      - '&7Clique para equipar esta tag.'
   Desequipar:
      Sobrepor: true
      Lore:
      - '&7Clique para desequipar esta tag.'
      
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

<chapter title="pacotes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Pacotes:
   Genero:
      Display: '&7Gênero'
      Item:
         CustomSkull: false
         URL: ''
         ID: NAME_TAG
         Data: 0
         Glow: true
         Name: '&ePacote de Tags'
         Lore:
            - '&7Ao ativar, você irá ganhar as tags'
            - '&7de gênero.'
            - ''
            - '&fEste pacote inclui:'
            - '&f > &b[Homem]'
            - '&f > &d[Mulher]'
      Tags:
         - 'Homem'
         - 'Mulher'
]]>
</code-block>
</chapter>

<chapter title="tags.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Tags:
   Homem:
      Tag: '&b[Homem]'
      Descricao: '&7Esta tag foi dada somente para homens.'
      Chat: true
      Placeholder: true
      # Deixe '' para não usar
      Permissao: ''
      # Permitir equipar a tag (mesmo sem comprar) apenas por ter a permissão
      Equipar-Permissao: false
      Preco:
         Compravel: true
         Tipo: 'MONEY'
         Preco: 100.0
      Item:
         CustomSkull: false
         URL: ''
         ID: NAME_TAG
         Data: 0
         Glow: true
         Name: '&b[Homem]'
         Lore:
         - '&fPreço: &6100 money.'
         - ''
         - '&7Clique para comprar esta tag.'
   Mulher:
      Tag: '&d[Mulher]'
      Descricao: '&7Esta tag foi dada somente para mulheres.'
      Chat: true
      Placeholder: true
      Permissao: ''
      Equipar-Permissao: false
      Preco:
         Compravel: true
         Tipo: 'yPoints'
         Preco: 100.0
      Item:
         CustomSkull: false
         URL: ''
         ID: NAME_TAG
         Data: 0
         Glow: true
         Name: '&d[Mulher]'
         Lore:
         - '&fPreço: &6100 pontos.'
         - ''
         - '&7Clique para comprar esta tag.'
   Beta:
      Tag: '&e[Beta]'
      Descricao: '&7Esta tag foi dada para aqueles que participaram da beta.'
      Chat: true
      Placeholder: false
      Permissao: 'ytags.beta'
      Equipar-Permissao: true
      Preco:
         # Mostrar no menu de NaoCompravel
         Menu: true
         Compravel: false
         Tipo: 'yPoints'
         Preco: 100.0
      Item:
         CustomSkull: false
         URL: ''
         ID: NAME_TAG
         Data: 0
         Glow: true
         Name: '&e[Beta]'
         Lore:
         - '&7Esta tag não é compravel.'
]]>
</code-block>
</chapter>

</chapter>
## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ytags_tag% - Retorna a tag adquirida
%ytags_owntag% - Retorna a tag própria
%ytags_desc% - Retorna a descrição da tag
%ytags_[tag_key]% - Retorna a tag pelo nome da config
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{ytags} - Retorna a tag adquirida
{ytags_own} - Retorna a tag própria
</code-block>



## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/5-yTags">Site do plugin yTags</a>
    </category>
</seealso>