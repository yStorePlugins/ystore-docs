# yTempoOnline
<secondary-label ref="utility"/>

### Descrição
Presenteie os jogadores que jogam por bastante tempo no teu servidor.

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

### Demonstração
<video src="//www.youtube.com/watch?v=0sKuB49BRGc"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/tempo - Abre o menu principal
/tempo [player]  - Vê o tempo de um jogador.
/tempo setnpc - Seta o NPC do tempo
/tempo delnpc - Deleta o NPC do tempo
/tempo reload - Recarrega as configurações
/tempo set - Seta um tempo específico para o jogador
/tempo add - Add um tempo específico para o jogador
/tempo remove - Remove um tempo específico para o jogador
/tempo reset - Reseta o tempo do jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytempoonline.usar - Permissão para o /tempo
ytempoonline.look.others - Permissão para o /tempo [player]
ytempoonline.veroff - Permissão para o /tempo [player] em jogadores offline
ytempoonline.setnpc - Permissão para o /tempo setnpc
ytempoonline.delnpc - Permissão para o /tempo delnpc
ytempoonline.reset - Permissão para o /tempo reset
ytempoonline.set - Permissão para o /tempo set
ytempoonline.add - Permissão para o /tempo add
ytempoonline.remove - Permissão para o /tempo remove
ytempoonline.reload - Permissão para o /tempo reload
ytempoonline.bypass - Permissão para não contar tempo</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ytempoonline_tempo% - Retorna o tempo online do jogador
%ytempoonline_tempo_raw% - Retorna o tempo online do jogador sem formatação (em segundos)
%ytempoonline_tag% - Retorna a tag do top tempo
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{ytempoonline} - Retorna a tag para o TOP 1
{ytempoonline_horas} - Retorna as horas do jogador
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static TempoAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;TempoAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(TempoAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/34-yTempoOnline">Site do plugin yTempoOnline</a>
    </category>
</seealso>