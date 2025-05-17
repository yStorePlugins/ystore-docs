# yAutoClick
<secondary-label ref="utility"/>

### Descrição
Mate entidades automaticamente

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
<secondary-label ref="1.20.2"/>

### Demonstração
<video src="//www.youtube.com/watch?v=e67cRclGGDY"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/autoclick - Ativa
/desativa o autoclick</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yautoclick.usar - Permissão para o /autoclick
yautoclick.all - Permissão para conseguir matar todos os mobs</code-block>
</chapter>



## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yAutoClick/
    ├── config.yml
    └── mobs.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
# Comandos e aliases do plugin
Comando:
   Autoclick:
      Comando: 'autoclick'
      Aliases: [ ac ]

# Opções gerais do plugin
Opcoes:
   Delay: 30 #em ticks, ex: 20 ticks = 1 segundo, 30 ticks = 1,5 segundos.
   RaioX: 3
   RaioY: 3
   RaioZ: 3
   # Mundos onde será permitido o uso do AutoClick
   Mundos permitidos:
      - 'world'
   # Permitir somente na plot (PlotSquared)
   Somente plot: false
   # Não quebrar a espada ao usar o AutoClick
   Inquebravel: true
   # Acréscimo de XP do mcMMO para quando o jogador tiver poção de força
   Mcmmo forca:
      Espadas: 20.0
      Machados: 20.0
      Unarmed: 20.0

# Mensagens gerais do plugin
Mensagens:
   Permissao: '&cVocê não tem permissão para isto!'
   Ativado: '&aO Auto-Click foi &eATIVADO&a com sucesso!'
   Desativado: '&aO Auto-Click foi &eDESATIVADO&a com sucesso!'

# Nomes das skills do mcMMO
Skills:
   Desarmado: 'UNARMED'
   Espadas: 'SWORDS'
   Machados: 'AXES'
]]>
</code-block>
</chapter>

<chapter title="mobs.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
Mobs:
   COW:
      Permissao: 'yautoclick.vaca'
      XP: 1
      Mcmmo espadas: 1
      Mcmmo machados: 1
      Mcmmo unarmed: 1
   SHEEP:
      Permissao: 'yautoclick.ovelha'
      XP: 1
      Mcmmo espadas: 1
      Mcmmo machados: 1
      Mcmmo unarmed: 1
]]>
</code-block>
</chapter>

</chapter>
## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/87-yAutoClick">Site do plugin yAutoClick</a>
    </category>
</seealso>