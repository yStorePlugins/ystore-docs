# yLojas
<secondary-label ref="utility"/>

### Descrição
Crie lojas para cada jogador, permitindo abrir e fechá-la, podendo ter sua loja em uma lista GUI.

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
<video src="//www.youtube.com/watch?v=ozmjwTEgipU"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/loja - Abre o menu principal. 
/loja anunciar - Anuncia sua loja. 
/loja [player] - Teleporta a loja de um jogador 
/loja remover - Deleta a loja de um jogador. 
/loja desfazer - Desfaz sua própria loja.
/loja setar - Seta o local da sua própria loja. 
/loja avaliar - Avalia uma outra loja 
/loja ajuda - Envia a mensagem de ajuda.
/loja reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ylojas.usar - Permissão para o /loja e /loja (player), /loja desfazer, /loja avaliar, /loja setar
ylojas.anunciar - Permissão para o /loja anunciar
ylojas.criar - Permissão para criar uma loja
ylojas.admin - Permissão para o /lojas remover
ylojas.reload - Permissão para o /lojas reload
ylojas.anuncio_delay_[delay] - Permissão para definir delay de anúncio por permissão</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLojas/
    ├── menus/
    │    ├── avaliar.yml
    │    ├── criarloja.yml
    │    ├── loja.yml
    │    ├── lojas.yml
    │    └── principal.yml
    └── config.yml
</code-block>
</chapter>

<chapter title="menus" collapsible="true">
<chapter title="avaliar.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja avaliar'
Tamanho: 27
Back slot: 9
Itens:
   Positiva:
      Slot: 11
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/e9e4bdcf172d5dc77c2bd4e37ad985399a9f2cdebf72463929ea4b666ef6f80'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aPositiva'
      Lore:
      - '&fNome: &a{nome}'
      - '&fDono: &f{dono}'
      - ''
      - '&7Clique para dar uma avaliação positiva'
      - ''
   Negativa:
      Slot: 15
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      ID: 0
      Data: 0
      Glow: true
      Name: '&cNegativa'
      Lore:
      - '&fNome: &a{nome}'
      - '&fDono: &f{dono}'
      - ''
      - '&7Clique para dar uma avaliação negativa'
      - ''
   Remover:
      Slot: 13
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/5fde3bfce2d8cb724de8556e5ec21b7f15f584684ab785214add164be7624b'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aRemover avaliação'
      Lore:
      - '&fNome: &a{nome}'
      - '&fDono: &f{dono}'
      - '&fSua avaliação: &b{nota}'
      - ''
      - '&7Clique para remover tua avaliação'
      - ''
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> LOJAS:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="criarloja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja criar'
Tamanho: 27
Back slot: 9
Itens:
  Criar:
    Slot: 13
    CustomSkull: true
    URL: 'http://textures.minecraft.net/texture/8169e179c314499fa837498a2626c6bbc9300a3d175813e29bd0c06401f5901a'
    ID: 0
    Data: 0
    Glow: true
    Name: '&aCriar Loja'
    Lore:
      - '&fPreço: &a{money} coins &7e &6{cash} cash&f.'
      - ''
      - '&7Clique para criar sua loja.'
    Lore gratis:
      - '&fVocê pode criar sua loja gratuitamente.'
      - '&7Clique para criar sua loja.'

## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> CRIAR:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="loja.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja config'
Tamanho: 27
Back slot: 9
Setar tp slot: 16
Itens:
   Perfil:
      Slot: 11
      CustomSkull: true
      URL: '{player}'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aInformações' #disponível a variável {player}
      Lore:
      - '&fAberta: &7{aberta}&f.'
      - '&fVisitas: &f{visitas}&f.'
      - ''
      - '&fAvalições positivas: &7{positivas}&f.'
      - '&fAvaliações negativas: &7{negativas}&f.'
      - ''
      - '&fNota total: {total}&f.'
      - ''
      - '&7Clique para abrir/fechar tua loja.'
      - '&7Clique com o botão do meio para deletar tua loja.'
   Nome:
      Slot: 13
      CustomSkull: false
      URL: ''
      ID: 339
      Data: 0
      Glow: true
      Name: '&aNome'
      Lore:
      - '&fNome atual: &7{nome}&f.'
      - '&7Clique para alterar o nome da loja.'
   Desc:
      Slot: 14
      CustomSkull: false
      URL: ''
      ID: 340
      Data: 0
      Glow: true
      Name: '&aDescrição'
      Lore:
      - '&fDescrição atual: &7{desc}&f.'
      - '&7Clique para alterar a descrição da loja.'
   Setar:
      CustomSkull: false
      URL: ''
      ID: 331
      Data: 0
      Glow: true
      Name: '&aSetar local'
      Lore:
      - '&7Clique para setar o local da tua loja.'
   Tp:
      CustomSkull: false
      URL: ''
      ID: 368
      Data: 0
      Glow: true
      Name: '&aTeleportar'
      Lore:
      - '&7Clique com botão esquerdo para ir a tua loja.'
      - '&7Clique com botão direito para remover o local da loja.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> LOJAS:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
]]>
</code-block>
</chapter>

<chapter title="lojas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Lojas'
Tamanho: 45
Slots: [10, 11, 12, 13, 14, 15, 16]
BackSlot: 31
Itens:
   Vazio:
      Slot: 13
      CustomSkull: false
      URL: ''
      ID: 328
      Data: 0
      Name: '&cOps...'
      Lore:
      - '&7Não há nenhuma loja aberta cadastrada :c'
   Item:
      CustomSkull: true
      URL: '{player}'
      ID: 0
      Data: 0
      Name: '&a{nome}' #variavel {player} disponivel
      Lore: #variavel {nome} disponivel
      - '&fDescrição: &7{desc}'
      - '&fDono: &7{player}'
      - ''
      - '&fVisitas: &a{visitas}'
      - '&fAvaliações: {nota}'
      - ''
      - '&7Clique com o botão esquerdo para ir até ela.'
      - '&7Clique com o botão direito para avaliar.'
      - ''
   Seletor:
      Slot: 32
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/22d145c93e5eac48a661c6f27fdaff5922cf433dd627bf23eec378b9956197'
      ID: 0
      Data: 0
      Name: '&aSeletor das Lojas'
   
Formato:
   Visualizando: ' &f• &a{nome}'
   Selecionar: ' &f• &7{nome}'
]]>
</code-block>
</chapter>

<chapter title="principal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Nome: '&8Loja principal'
Tamanho: 27
Itens:
   Minha:
      Slot: 12
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/182d36b973e57e4c0fe28c371a7f11fc04a2a342a88a7e5e5d83edbcab61770e'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aMinha Loja'
      Lore:
      - '&7Clique para gerenciar sua loja.'
   Lojas:
      Slot: 14
      CustomSkull: true
      URL: 'http://textures.minecraft.net/texture/152353641d287ce9ed30906f938ae9c517ec04caa8da71571954c81b09db454c'
      ID: 0
      Data: 0
      Glow: true
      Name: '&aLojas'
      Lore:
      - '&7Clique para acessar o menu de lojas.'
      
## CASO QUEIRA CRIAR OUTROS ITENS PARA ENFEITAR TEU MENU, ABAIXO DE ITENS: -> LOJAS:, COPIE E COLE E MUDE O NOME E AS INFORMAÇÕES :)
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
# Comandos e aliases do plugin
Comando:
  Comando: 'loja'
  Aliases: [ ]
  Anunciar:
    Comando: 'anunciar'
    Aliases: [ ]
#Coloque yPoints, PlayerPoints, JH_Shop, yCash, TGCash, AtlasEconomiaSecundaria ou MageCash
Plugin de Pontos: 'PlayerPoints'
# Tipo de formatos de quantia disponíveis: LETRA (K,M,B,T...) e NUMERO (100,00)
Formatacao: 'LETRA'
# Mundos em que poderá setar uma loja
Mundos permitidos:
  - 'world'
  - 'plot'
# Permissão (ylojas.gratis)
# Ativar a permissão para criar lojas gratuitamente
Permissao gratis: true
# Preco para criacao da loja
Preco:
  Criar:
    Money: 100.0
    Points: 100.0
# Esta opção permite que carregue todas as lojas que estão abertas quando o servidor ligar
# tenha em mente que pode causar uma lotação excessiva de memória para servidores com muitos jogadores.
Carregar abertas: false
# Quantia de letras que o nome da loja pode ter.
Nome quantia: 15
# Quantia de letras que a descrição da loja pode ter.
Desc quantia: 20
# Em segundos ( delay para anunciar a loja )
Delay: 60
# Mensagens do plugin
Mensagens:
  Permissao: '&c&lERRO! &cVocê não tem permissão para isto.'
  Permissao criar: '&c&lERRO! &cVocê não tem permissão para criar uma loja.'
  Sem money: '&c&lERRO! &cVocê não tem money suficiente para isto &7( {preco} )&c.'
  Sem points: '&c&lERRO! &cVocê não tem pontos suficiente para isto &7( {preco} )&c.'
  Deletada: '&a&lSUCESSO! &aVocê deletou sua loja com sucesso.'
  Local setado: '&a&lSUCESSO! &aVocê setou o local da tua loja.'
  Local removido: '&a&lSUCESSO! &aVocê removeu o local da tua loja.'
  Teleportado: '&a&lSUCESSO! &aVocê foi teleportado.'
  Cancelou: '&cVocê cancelou a ação.'
  Nome quantia: '&c&lERRO! &cO nome da loja não pode ser menor que 1 caractere ou maior que 15 caracteres.'
  Desc quantia: '&c&lERRO! &cA descrição da loja não pode ser menor que 1 caractere ou maior que 20 caracteres.'
  Mudou nome: '&a&lSUCESSO! &aAgora o nome da tua loja é: &7{nome}&a.'
  Mudou desc: '&a&lSUCESSO! &aAgora a descrição da tua loja é: &7{desc}&a.'
  Local primeiro: '&c&lERRO! &cVocê deve setar o local da loja primeiro.'
  Removeu avaliacao: '&a&lSUCESSO! &aVocê removeu sua avaliação.'
  Avaliacao positiva: '&a&lSUCESSO! &aVocê avaliou positivamente a loja.'
  Avaliacao negativa: '&a&lSUCESSO! &aVocê avaliou negativamente a loja.'
  Avaliar si mesmo: '&c&lERRO! &cVocê não pode avaliar sua própria loja.'
  Nao encontrado: '&c&lERRO! &cJogador não encontrado.'
  Nao possui: '&c&lERRO! &cEste jogador não possui loja.'
  Fechada: '&c&lERRO! &cEsta loja está fechada.'
  Mundo: '&cMundo não permitido.'
  Terreno: '&cVocê não tem permissão neste terreno.'
  Delay: '&cVocê deve aguadar {tempo} para anunciar sua loja novamente.'
  Anunciar sem: '&cVocê não tem uma loja para anunciar.'
  Anunciar fechada: '&cVocê não pode anunciar sua loja estando fechada.'
  Nao tem: '&cVocê não possui uma loja.'
  Digite nome:
    - ''
    - '&aDigite o nome da loja.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Digite desc:
    - ''
    - '&aDigite o nome da descrição.'
    - '&7para cancelar digite &ncancelar&7.'
    - ''
  Help:
    - '&c-> Comandos disponíveis <-'
    - ''
    - ' &f> &c/loja'
    - ' &f> &c/loja anunciar'
    - ' &f> &c/loja desfazer'
    - ' &f> &c/loja avaliar'
    - ' &f> &c/loja setar'
    - ' &f> &c/loja <player>'
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
# Formatador booleano e de mensagens
Formatador:
  True f: '&aSim'
  False f: '&cNão'
  Sem nome: '&7Sem nome.'
  Sem desc: '&7Sem descrição.'
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

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/2-yLojas">Site do plugin yLojas</a>
    </category>
</seealso>