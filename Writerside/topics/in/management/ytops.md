# yTops
<secondary-label ref="management"/>

### Descrição
Mostre para todos quem são os melhores do servidor

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
<video src="//www.youtube.com/watch?v=OG_8NdVB8-0"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/topentity - Gerencia os tops de entidades (NPC, ARMORSTAND)
/tophologram - Gerencia os tops de hologramas
/ytops reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ytops.topentity - Permissão para o /topentity
ytops.tophologram - Permissão para o /tophologram
ytops.admin - Permissão para o /ytops</code-block>
</chapter>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static TopAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;TopAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(TopAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/96-yTops">Site do plugin yTops</a>
    </category>
</seealso>