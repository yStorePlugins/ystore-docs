# yAntiGrief
<secondary-label ref="management"/>

### Descrição
Autenticação para uso de comandos

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
<video src="//www.youtube.com/watch?v=BhsVJ4UCrFI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/antigrief reload - Recarrega as configurações
/antigrief [senha] - Realiza o login</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yantigrief.staff - Permissão para ser reconhecido como staff</code-block>
</chapter>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static AntiGriefAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;AntiGriefAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(AntiGriefAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/77-yAntiGrief">Site do plugin yAntiGrief</a>
    </category>
</seealso>