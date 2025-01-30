# yEconomias
<secondary-label ref="management"/>

### Descrição
Crie múltiplas novas economias no seu servidor

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
<video src="//www.youtube.com/watch?v=ifDtUaXUERw"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/currencies reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">/
yeconomias.use - Permissão para o /currencies reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yeconomias_[identificador_da_config]_amount% - Retorna a quantia do jogador na economia
%yeconomias_[identificador_da_config]_amount_raw% - Retorna a quantia do jogador na economia sem formatar
%yeconomias_[identificador_da_config]_rich% - Retorna a tag de top se o jogador for o mais rico na economia
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{identificador_da_config} - Tag do jogador mais rico&nbsp;
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static EconomiasAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;EconomiasAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(EconomiasAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/102-yEconomias">Site do plugin yEconomias</a>
    </category>
</seealso>