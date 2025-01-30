# ySpawners
<secondary-label ref="rankup"/>

### Descrição
Spawners com amigos e drops armazenados nele mesmo!

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
<video src="//www.youtube.com/watch?v=eZMcE03CywQ"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/spawnerbooster - Mostra o status do booster
/spawneradmin givebooster - Dar boosters a um jogador
/spawneradmin givespawner - Dar spawners a um jogador
/spawneradmin givelimitstack - Dar limites de stack a um jogador
/spawneradmin givelimitdrop - Dar limites de venda a um jogador
/spawneradmin reload - Recarrega as configurações
/limitdrop - Mostra seu limite de drops
/limitdrop [player] - Mostra o limite de drops de outro jogador
/limitdrop enviar - Envia limite de drops para outro jogador
/limitdrop ajuda - Envia a mensagem de ajuda
/limitdrop set - Seta limite de drops para um jogador
/limitdrop add - Adiciona limite de drops para um jogador
/limitdrop remove - Remove limite de drops de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yspawnersv2.booster - Permissão para o /spawnerboosteryspawnersv2.givespawner - Permissão para o /spawneradmin givespawneryspawnersv2.givebooster - Permissão para o /spawneradmin giveboosteryspawnersv2.givelimit - Permissão para o /spawneradmin givelimitstack e /spawneradmin givelimitdropyspawnersv2.use - Permissão para o /spawneradminyspawnersv2.admin.reload - Permissão para o /spawneradmin reloadyspawnersv2.admin - Permissão para ser reconhecido como um ADM
yspawners.limitdrop.use - Permissão para o /limitdrop
yspawners.limitdrop.others - Permissão para o /limitdrop [player]
yspawners.limitdrop.send - Permissão para o /limitdrop enviar
yspawners.limitdrop.help - Permissão para o /limitdrop ajuda
yspawners.limitdrop.set - Permissão para o /limitdrop set
yspawners.limitdrop.add - Permissão para o /limitdrop add
yspawners.limitdrop.remove - Permissão para o /limitdrop remove</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yspawners_limitdrop% - Retorna o limite de drops formatado (1K, 1M, 1T...)
%yspawners_limitdrop_raw% - Retorna o limite de drops sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static SpawnerV2APIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;SpawnerV2APIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(SpawnerV2APIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/72-ySpawners">Site do plugin ySpawners</a>
    </category>
</seealso>