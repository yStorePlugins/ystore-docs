# yLootingStack
<secondary-label ref="rankup"/>

### Descrição
Agora é possível stackar a looting tanto em um item quanto na sua arma!

### Versões
<secondary-label ref="1.8"/>
<secondary-label ref="1.9"/>
<secondary-label ref="1.12"/>
<secondary-label ref="1.16"/>

### Demonstração
<video src="//www.youtube.com/watch?v=92lLS3b_VCg"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/givelooting - Dá um item custom de looting para um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ylootingstack.admin - Permissão para o /givelooting</code-block>
</chapter>

## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yLootingStack/
    ├── blocos.yml
    ├── config.yml
    └── mobs.yml
</code-block>
</chapter>

<chapter title="blocos.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Blocos:
   bloco1:
      ID: 1
      Data: 0
      Chance: 100.0
      Quantia: 100 #quantia de looting
]]>
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Maximo: 0 #o máximo do minecraft é 30k
Ativar blocos: true
Ativar mobs: true
Ativar pesca: true
Ativar tradutor: false #ele irá remover o nome dos outros enchants e irá mostrar apenas do looting

Comando:
   Comando: 'givelooting'
   Aliases: {}

Pesca:
   Chance: 100.0
   Quantia: 100 #quantia de looting

# Mundos onde não receberá looting
Mundo blacklist:
   - 'none'

Permitidos:
- 'DIAMOND_SWORD'
- 'IRON_SWORD'
- 'GOLD_SWORD'
- 'STONE_SWORD'
- 'WOOD_SWORD'

Item:
   CustomSkull: false
   URL: ''
   ID: 388
   Data: 0
   Glow: true
   Name: '&eLooting'
   Lore:
   - '&7Looting: {lvl}'
   - ''
   - '&7Este encantamento permite multiplicar seus drops.'
   - '&7Clique no seu item para encantar.'
   - '&7Compatível com Espadas.'
   - ''
   - '&7Shift+Botão direito junta suas lootings em 1.'

Mensagens:
   Encantou: '&a&lSUCESSO! &aVocê encantou seu item com looting &7{lvl}&a.'
   Nao compativel: '&c&lERRO! &cEste item não é compatível com este encantamento.'
   Maximo: '&c&lERRO! &cSeu item já alcançou o máximo de looting.'
   Permissao: '&c&lERRO! &cVocê não tem permissão para usar isto.'
   Numero: '&c&lERRO! &cA quantia deve ser um número.'
   Numero max: '&c&lERRO! &cO máximo permitido é &7{max}&c.'
   Nao encontrado: '&c&lERRO! &cJogador não encontrado.'
   Deu: '&a&lSUCESSO! &aVocê deu &7{lvl} &ade looting para o jogador &7{player}&a.'
   Recebeu: '&a&lSUCESSO! &aVocê recebeu &7{lvl} &ade looting.'
   Converteu: '&a&lSUCESSO! &aVocê converteu seus lootings em &71&a.'
   Title:
      Ativar: true
      Title: '&aVocê ganhou'
      Subtitle: '&7{lvl}&a de looting'
   Chat:
      Ativar: true
      Msg:
      - ''
      - '&aVocê ganhou &7{lvl} &aem looting.'
      - ''
      
Formats:
 - ''
 - ''
 - 'K'
 - 'M'
 - 'B'
]]>
</code-block>
</chapter>

<chapter title="mobs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Mobs:
   mob1:
      Entidade: 'ZOMBIE'
      Chance: 100.0
      Quantia: 100 #quantia de looting
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/31-yLootingStack">Site do plugin yLootingStack</a>
    </category>
</seealso>