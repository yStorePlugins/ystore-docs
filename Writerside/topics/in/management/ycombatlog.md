# yCombatLog
<secondary-label ref="management"/>

### Descrição
O plugin mais versátil de combatlog

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
<video src="//www.youtube.com/watch?v=tGgfJXG4SIU"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/combatlog toggle [player] - Alterna o estado do PVP
/combatlog reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycombatlog.use - Permissão para o /combatlog
ycombatlog.admin - Permissão para o /combatlog reload
ycombatlog.toggle - Permissão para o /combatlog toggle
ycombatlog.toggle.others - Permissão para o /combatlog toggle [player]
ycombatlog.staff - Permissão para ser reconhecido como staff</code-block>
</chapter>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static CombatAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;CombatAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(CombatAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/43-yCombatLog">Site do plugin yCombatLog</a>
    </category>
</seealso>