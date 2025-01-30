# yBoosters
<secondary-label ref="utility"/>

### Descrição
Crie boosters para habilidades do mcmmo

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
<video src="//www.youtube.com/watch?v=nMREPQWK0LM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/booster - Abre o menu principal
/booster agradecer - Agradece o booster global
/booster removerglobal - Remove o booster global ativo
/booster removerplayer - Remove o booster global ativo
/booster givemcmmo - Dá um booster pessoal para um jogador
/booster givemcmmoglobal - Dá um booster global para um jogador
/booster ajuda - Mostra todos os comandos
/booster reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yboosters.agradecer - Permissão para o /booster agradecer
yboosters.removerglobal - Permissão para o /booster removerglobal
yboosters.removerplayer - Permissão para o /booster removerplayer
yboosters.givemcmmo - Permissão para o /booster givemcmmo
yboosters.givemcmmoglobal - Permissão para o /booster givemcmmoglobal
yboosters.ajuda - Permissão para o /booster ajuda
yboosters.usar - Permissão para o /booster
yboosters.pausar - Permissão para pausar um booster pessoal
yboosters.reload - Permissão para o /booster reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yboosters_pessoal_skill% - Retorna o nome da skill do booster pessoal
%yboosters_pessoal_multiplicador% - Retorna o multiplicador do booster pessoal
%yboosters_pessoal_tempo% - Retorna o tempo do booster pessoal
%yboosters_global_skill% - Retorna o nome da skill do booster global
%yboosters_global_multiplicador% - Retorna o multiplicador do booster global
%yboosters_global_tempo% - Retorna o tempo do booster global
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static BoosterAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;BoosterAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(BoosterAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/54-yBoosters">Site do plugin yBoosters</a>
    </category>
</seealso>