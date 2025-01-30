# yCorreio
<secondary-label ref="management"/>

### Descrição
Envie itens entre jogadores e dê recompensas dentro de eventos!

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
<video src="//www.youtube.com/watch?v=_wIU7Hv1U78"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/correio - Abre o menu principal
/correio ajuda - Envia a mensagem de ajuda
/correio enviar [player] - Envia itens à um jogador.
/correio enviartodos - Envia itens à todos os jogadores online.
/correio enviargrupo [grupo] - Envia itens à todos os jogadores online de um grupo.
/correio give [player] [categoria] [recompensa] [quantia] - Dá x recompensa(s) configurada à um jogador.
/correio giveall [categoria] [recompensa] [quantia] - Dá x recompensa(s) configurada à todos os jogadores online.
/correio givegrupo [grupo] [categoria] [recompensa] [quantia] - Dá x recompensa(s) configurada à todos os jogadores online de um grupo.
/correio recompensas - Vê a lista de recompensas configuradas.
/correio grupos - Vê a lista de grupos configurados.
/correio categorias - Vê a lista de categorias configuradas.
/correio setnpc - Seta o NPC do correio.
/correio delnpc - Deleta o NPC do correio.
/correio reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycorreio.usar - Permissão para o /correio
ycorreio.enviar - Permissão para o /correio enviar
ycorreio.admin - Permissão para ser reconhecido como admin
ycorreio.enviartodos - Permissão para o /correio enviartodos
ycorreio.enviargrupo - Permissão para o /correio enviargrupo
ycorreio.give - Permissão para o /correio give
ycorreio.giveall - Permissão para o /correio giveall
ycorreio.givegrupo - Permissão para o /correio givegrupo
ycorreio.recompensas - Permissão para o /correio recompensas
ycorreio.grupos - Permissão para o /correio grupos
ycorreio.categorias - Permissão para o /correio categorias
ycorreio.setnpc - Permissão para o /correio setnpc
ycorreio.delnpc - Permissão para o /correio delnpc
ycorreio.reload - Permissão para o /correio reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ycorreio_encomendas% - Retorna a quantia de encomendas que o jogador tem (formatado)
%ycorreio_recompensas% - Retorna a quantia de recompensas que o jogador tem (formatado)
%ycorreio_total% - Retorna a quantia de encomendas mais recompensas que o jogador tem (formatado)
%ycorreio_encomendas_raw% - Retorna a quantia de encomendas que o jogador tem (sem formatar)
%ycorreio_recompensas_raw% - Retorna a quantia de encomendas que o jogador tem (sem formatar)
%ycorreio_total_raw% - Retorna a quantia de encomendas que o jogador tem (sem formatar)
</code-block>



## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/81-yCorreio">Site do plugin yCorreio</a>
    </category>
</seealso>