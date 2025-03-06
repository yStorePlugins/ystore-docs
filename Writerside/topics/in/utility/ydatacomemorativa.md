# yDataComemorativa
<secondary-label ref="utility"/>

### Descrição
Agora é possível dar presentes aos jogadores em datas especiais!

### Versões
<secondary-label ref="1.8"/>
<secondary-label ref="1.9"/>
<secondary-label ref="1.10"/>
<secondary-label ref="1.11"/>
<secondary-label ref="1.12"/>

### Demonstração
<video src="//www.youtube.com/watch?v=dKpcLJCOw44"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/datafesta setnpc - Seta o NPC do Citizens
/datafesta delnpc - Deleta o NPC do Citizens
/datafesta setarmor - Seta o ArmorStand
/datafesta delarmor - Deleta o ArmorStand
/datafesta reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ydatacomemorativa.admin - Permissão para todos os comandos</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yDataComemorativa/
    ├── datas/
    │    ├── natal.yml
    │    └── padrao.yml
    ├── comemoracoes.yml
    ├── config.yml
    └── recompensas.yml
</code-block>
</chapter>

<chapter title="datas" collapsible="true">
<chapter title="natal.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
NPC:
   Skin: 'yChusy'
   Altura: 3.1
   Holograma:
   - '&c&lNatal'
   - '&aClique para pegar seu presente de natal'
   Mensagens:
      Setado: '&a&lSUCESSO! &aNPC do data comemorativa setado com sucesso.'
      Removido: '&a&lSUCESSO! &aNPC do data comemorativa removido com sucesso.'
      Nao removido: '&c&lERRO! &aNPC do data comemorativa não está setado.'

ArmorStand:
   Altura: 3.1
   Holograma:
   - '&c&lNatal'
   - '&aClique para pegar seu presente de natal'
   Posicoes:
      Cabeca:
         Pos1: 0
         Pos2: 0
         Pos3: 0
      Corpo:
         Pos1: 0
         Pos2: 20
         Pos3: 0
      Braco esquerdo:
         Pos1: 261
         Pos2: 16
         Pos3: 0
      Braco direito:
         Pos1: 261
         Pos2: 345
         Pos3: 0
      Perna esquerda:
         Pos1: 9
         Pos2: 0
         Pos3: 0
      Perna direita:
         Pos1: 9
         Pos2: 180
         Pos3: 0
   Itens:
      Mao:
         Nulo: false
         CustomSkull: true
         URL: 'http://textures.minecraft.net/texture/f5612dc7b86d71afc1197301c15fd979e9f39e7b1f41d8f1ebdf8115576e2e'
         Colorida: false #armadura de couro colorida
         Red: 0
         Green: 0
         Blue: 0
         ID: 0
         Data: 0
         Glow: false
      Capacete:
         Nulo: false
         CustomSkull: true
         URL: 'http://textures.minecraft.net/texture/14e424b1676feec3a3f8ebade9e7d6a6f71f7756a869f36f7df0fc182d436e'
         Colorida: true #armadura de couro colorida
         Red: 0
         Green: 0
         Blue: 0
         ID: 0
         Data: 0
         Glow: false
      Peitoral:
         Nulo: false
         Colorida: true
         Red: 252
         Green: 3
         Blue: 23
         ID: 0
         Data: 0
         Glow: true
      Calca:
         Nulo: false
         Colorida: true
         Red: 0
         Green: 112
         Blue: 0
         ID: 0
         Data: 0
         Glow: true
      Bota:
         Nulo: false
         Colorida: true
         Red: 252
         Green: 3
         Blue: 23
         ID: 0
         Data: 0
         Glow: true
   Mensagens:
      Setado: '&a&lSUCESSO! &aNPC do data comemorativa setado com sucesso.'
      Removido: '&a&lSUCESSO! &aNPC do data comemorativa removido com sucesso.'
      Nao removido: '&c&lERRO! &aNPC do data comemorativa não está setado.'
]]>
</code-block>
</chapter>

<chapter title="padrao.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
NPC:
   Skin: 'ySpeed_'
   Altura: 3.1
   Holograma:
   - '&c&lAguardando'
   - '&7Esperando uma próxima data comemorativa.'
   Mensagens:
      Setado: '&a&lSUCESSO! &aNPC do data comemorativa setado com sucesso.'
      Removido: '&a&lSUCESSO! &aNPC do data comemorativa removido com sucesso.'
      Nao removido: '&c&lERRO! &aNPC do data comemorativa não está setado.'
   
ArmorStand:
   Altura: 3.1
   Holograma:
   - '&c&lAguardando'
   - '&7Esperando uma próxima data comemorativa.'
   Posicoes:
      Cabeca:
         Pos1: 0
         Pos2: 0
         Pos3: 0
      Corpo:
         Pos1: 0
         Pos2: 0
         Pos3: 0
      Braco esquerdo:
         Pos1: 0
         Pos2: 0
         Pos3: 0
      Braco direito:
         Pos1: 0
         Pos2: 0
         Pos3: 0
      Perna esquerda:
         Pos1: 0
         Pos2: 0
         Pos3: 0
      Perna direita:
         Pos1: 0
         Pos2: 0
         Pos3: 0
   Itens:
      Mao:
         Nulo: false
         CustomSkull: true
         URL: 'http://textures.minecraft.net/texture/f5612dc7b86d71afc1197301c15fd979e9f39e7b1f41d8f1ebdf8115576e2e'
         Colorida: false #armadura de couro colorida
         Red: 0
         Green: 0
         Blue: 0
         ID: 0
         Data: 0
         Glow: false
      Capacete:
         Nulo: false
         CustomSkull: true
         URL: 'http://textures.minecraft.net/texture/40bd1ea6b264b7a1cebf47fbede13558c7d1e1b168608e65b652a9147cf7f125'
         Colorida: false #armadura de couro colorida
         Red: 0
         Green: 0
         Blue: 0
         ID: 0
         Data: 0
         Glow: false
      Peitoral:
         Nulo: false
         Colorida: false
         Red: 0
         Green: 0
         Blue: 0
         ID: 303
         Data: 0
         Glow: true
      Calca:
         Nulo: false
         Colorida: false
         Red: 0
         Green: 0
         Blue: 0
         ID: 304
         Data: 0
         Glow: true
      Bota:
         Nulo: false
         Colorida: false
         Red: 0
         Green: 0
         Blue: 0
         ID: 305
         Data: 0
         Glow: true
   Mensagens:
      Setado: '&a&lSUCESSO! &aArmorStand do data comemorativa setado com sucesso.'
      Removido: '&a&lSUCESSO! &aArmorStand do data comemorativa removido com sucesso.'
      Nao removido: '&c&lERRO! &aArmorStand do data comemorativa não está setado.'
]]>
</code-block>
</chapter>

</chapter>

<chapter title="comemoracoes.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Datas:
   natal:
      Nome arquivo: 'natal'
      Inicio: '25/12/2020-12:48'
      Fim: '25/12/2020-12:50'
      # Recompensas da data comemorativa
      # As recompensas são cadastradas na recompensas.yml
      # Use: chance,recompense
      Recompensas:
         - '100,Reco1'
]]>
</code-block>
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

Comando:
   Comando: 'datafesta'
   Aliases: {}
   
Mensagens:
   Permissao: '&c&lERRO! &cVocê não tem permissão para isto.'
   Ja coletou: '&c&lERRO! &cVocê já coletou a recompensa desta data comemorativa.'
]]>
</code-block>
</chapter>

<chapter title="recompensas.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Recompensas:
   Reco1:
      Msgs:
         Actionbar:
            Ativar: true
            Msg: '&cGanhou carvão por sel mal :c'
         Title:
            Ativar: false
            Title: ''
            Subtitle: ''
         Chat:
            Ativar: true
            Msg:
            - ''
            - '&cProcure se comportar melhor para ganhar coisas boas!'
            - ''
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 263
         Data: 0
         Glow: true
         Name: '&cCarvão'
         Amount: 1
         Lore:
         - '&cVocê se comportou mal, por isto'
         - '&cganhou um carvão.'
         Enchants: #se não desejar, deixe assim:
         - ''
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
         - 'give {player} stone 1'
   Reco2:
      Msgs:
         Actionbar:
            Ativar: true
            Msg: '&aVocê foi ótimo(a) esse ano.'
         Title:
            Ativar: false
            Title: ''
            Subtitle: ''
         Chat:
            Ativar: true
            Msg:
            - ''
            - '&aParabéns por se comportar bem, te dei diamantes.'
            - ''
      Item: #se o ( Command -> Use ) tiver true, isso não vai funcionar
         CustomSkull: false
         URL: ''
         ID: 264
         Data: 0
         Glow: true
         Name: '&bDiamantes!'
         Amount: 64
         Lore:
         - '&bVocê foi um ótimo garoto(a)!'
         Enchants: #se não desejar, deixe assim:
         - ''
      Command:
         Use: false
         List: #se o ( Use ) tiver false, isso não funcionar.
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/36-yDataComemorativa">Site do plugin yDataComemorativa</a>
    </category>
</seealso>