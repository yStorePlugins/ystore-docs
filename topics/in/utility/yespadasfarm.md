# yEspadasFarm
<secondary-label ref="utility"/>

### Descrição
Tenha espadas com looting infinito no teu servidor

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
<video src="//www.youtube.com/watch?v=uEwMPFPXmM4"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/espadas - Abre o menu principal
/espadas ajuda - Envia a mensagem de ajuda
/espadas give - Dá uma espada à um jogador
/espadas givebook - Dá um item ativável com looting à um jogador
/espadas reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yespadasfarm.use - Permissão para o /espadas
yespadasfarm.help - Permissão para o /espadas ajuda
yespadasfarm.give - Permissão para o /espadas give
yespadasfarm.givebook - Permissão para o /espadas givebook
yespadasfarm.reload - Permissão para o /espadas reload</code-block>
</chapter>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static EspadasFarmAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;EspadasFarmAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(EspadasFarmAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/95-yEspadasFarm">Site do plugin yEspadasFarm</a>
    </category>
</seealso>