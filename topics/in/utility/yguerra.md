# yGuerra
<secondary-label ref="utility"/>

### Descrição
Crie eventos pvp e agite seu servidor com itens setados ou não!

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
<video src="//www.youtube.com/watch?v=fWmaoeTu8Dg"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/guerra - Abre o menu principal
/guerra iniciar - Inicia um evento
/guerra parar - Para o evento atual
/guerra pvp - Ativa
/Desativa o PVP do evento
/guerra admin - Abre o menu principal do admin
/guerra kickplayer - Kicka o jogador do evento
/guerra kickclan - Kicka o clan do evento
/guerra banplayer - Ban um jogador de um evento específico
/guerra banclan - Ban um clan de um evento específico
/guerra unbanplayer - Desbane um jogador de um evento específico
/guerra unbanclan - Desbane um clan de um evento específico
/guerra apostar - Aposta em um clan
/jogador
/guerra camarote - Vai para o camarote
/guerra forcardm - Força o deathmatch da guerra.
/guerra sopa - Seta os itens da placa de sopa
/guerra ajuda - Mostra a mensagem de ajuda.
/guerra info - Mostra a mensagem do informativo.
/guerra add - Adiciona novos jogadores a guerra.
/guerra puxar - Puxa o jogador da guerra para sua localização.
/guerra reload - Recarrega as configurações.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yguerra.usar - Permissão para o /guerra
yguerra.admin - Permissão para o /guerra admin
yguerra.iniciar - Permissão para o /guerra iniciar
yguerra.parar - Permissão para o /guerra parar
yguerra.pvp - Permissão para o /guerra pvp
yguerra.kickplayer - Permissão para o /guerra kickplayer
yguerra.kickclan - Permissão para o /guerra kickclan
yguerra.banplayer - Permissão para o /guerra banplayer
yguerra.banclan - Permissão para o /guerra banclan
yguerra.unbanplayer - Permissão para o /guerra unbanplayer
yguerra.unbanclan - Permissão para o /guerra unbanclan
yguerra.apostar - Permissão para o /guerra apostar
yguerra.camarote - Permissão para o /guerra camarote
yguerra.forcardm - Permissão para o /guerra forcardm
yguerra.ajuda - Permissão para o /guerra ajuda
yguerra.info - Permissão para o /guerra info
yguerra.add - Permissão para o /guerra add
yguerra.pull - Permissão para o /guerra puxar
yguerra.sopa - Permissão para o /guerra sopa
yguerra.reload - Permissão para o /guerra reload
yguerra.vanish.bypass - Permissão para ver os jogadores no camarote</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yguerra_[nome_do_evento]% - Retorna a tag do evento.&nbsp;(Altere o nome_do_evento pelo nome do arquivo do tipo, exemplo: gladiador.)
%yguerra_clans% - Retorna as tags dos clans da guerra
%yguerra_clans_quantia% - Retorna a quantia de clans na guerra
%yguerra_jogadores% - Retorna a quantia de jogadores na guerra
%yguerra_jogadores_clan% - Retorna a quantia de jogadores do clan do player na guerra
%yguerra_fogoamigo% - Retorna o fogo amigo da guerra
%yguerra_duracao% - Retorna o tempo da guerra
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{nome_do_evento} - Retorna a tag do evento.&nbsp;(Altere o nome_do_evento pelo nome do arquivo do tipo, exemplo: gladiador.)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static GuerraAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;GuerraAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(GuerraAPIHolder.class);
        return rsp == null ? null : rsp.getProvider();
    } catch (Throwable var1) {
        return null;
    }
}
</code-block>

## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/20-yGuerra">Site do plugin yGuerra</a>
    </category>
</seealso>