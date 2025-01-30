# yFragmentosVirtuais
<secondary-label ref="utility"/>

### Descrição
Armazene pedaços de itens que podem ser utilizados como moeda de troca

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
<video src="//www.youtube.com/watch?v=aKlZuImwhWI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/fragmentos - Abre o menu de fragmentos
/fragmentos shop - Abre o menu de loja
/fragmentos enviar - Envia fragmentos para um jogador
/fragmentos give - Dar fragmentos à um jogador
/fragmentos reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yfragmentosvirtuais.use - Permissão para o /fragmentos
yfragmentosvirtuais.shop - Permissão para o /fragmentos shop
yfragmentosvirtuais.send - Permissão para o /fragmentos enviar
yfragmentosvirtuais.give - Permissão para o /fragmentos give
yfragmentosvirtuais.reload - Permissão para o /fragmentos reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yfragmentosvirtuais_amount% - Retorna a quantia de fragmentos que o jogador possui
%yfragmentosvirtuais_amount_raw% - Retorna a quantia de fragmentos que o jogador possui sem formatar
%yfragmentosvirtuais_[identificador_da_config]_amount% - Retorna a quantia de tal fragmentos do jogador
%yfragmentosvirtuais_[identificador_da_config]_amount_raw% - Retorna a quantia de tal fragmentos&nbsp;do jogador sem formatar
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static CrateHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;CrateHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(CrateHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/99-yFragmentosVirtuais">Site do plugin yFragmentosVirtuais</a>
    </category>
</seealso>