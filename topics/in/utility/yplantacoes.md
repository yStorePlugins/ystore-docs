# yPlantacoes
<secondary-label ref="utility"/>

### Descrição
Colha e replante automaticamente com chances de recompensas

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
<video src="//www.youtube.com/watch?v=L4xT_CWRY7k"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/farm - Abre o menu principal
/farm moedas - Vê suas moedas
/farm [player] - Vê as moedas de outro jogador
/farm enviar - Envia suas moedas para outro jogador
/farm ir - Ir para a área de farm
/farm darenxada - Dá enxada para um jogador
/farm add - Adicionada moedas para um jogador
/farm set - Seta moedas para um jogador
/farm remove - Remove moedas de um jogador
/farm setspawn - Seta o local de spawn da área de farm
/farm reload - Recarregar as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yplantacoes.usar - Permissão para o /farm e /farm moedas
yplantacoes.look - Permissão para o /farm [player]
yplantacoes.send - Permissão para o /farm enviar
yplantacoes.go - Permissão para o /farm ir
yplantacoes.givehoe - Permissão para o /farm givehoe
yplantacoes.add - Permissão para o /farm add
yplantacoes.remove - Permissão para o /farm remove
yplantacoes.set - Permissão para o /farm set
yplantacoes.setspawn - Permissão para o /farm setspawn
yplantacoes.help - Permissão para o /farm help
yplantacoes.reload - Permissão para o /farm reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yplantacoes_moedas% - Retorna os moedas do jogador formatado.
%yplantacoes_moedas_raw% - Retorna os moedas do jogador sem formatação.
%yplantacoes_time% - Retorna o tempo do jogador na farm.
%yplantacoes_time_raw% - Retorna o tempo do jogador na farm sem formatar.
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static PlantacaoAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;PlantacaoAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(PlantacaoAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/89-yPlantacoes">Site do plugin yPlantacoes</a>
    </category>
</seealso>