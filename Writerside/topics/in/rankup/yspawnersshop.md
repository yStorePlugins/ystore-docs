# ySpawnersShop
<secondary-label ref="rankup"/>

### Descrição
Simples e eficaz, gerencie a compra de spawners no seu servidor.

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
<video src="//www.youtube.com/watch?v=uiy9j4a3Gfs"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/spawners - Abre o menu principal.
/spawners reload - Recarrega as configurações
/spawners givelimite - Dá limite para um jogador.
/limite - Mostra a quantia de limite do jogador.
/limite top - Abre o top limite.
/limite - Mostra a quantia de limite de um jogador.
/limite help - Mostra a quantia de limite de um jogador.
/limite setar - Setar uma quantia de limite para o jogador.
/limite add - Adicionar uma quantia de limite para o jogador.
/limite remove - Remover uma quantia de limite do jogador.
/limite enviar - Enviar uma quantia de limite para um jogador.
/redutor give - Dá um redutor de tempo para um jogador.</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yspawnersshop.usar - Permissão para o /spawners e /limite top
yspawnersshop.givelimite - Permissão para o /spawners givelimite
yspawnersshop.reload - Permissão para o /spawners reload
yspawnersshop.limite - Permissão para o /limite
yspawnersshop.limite.outros - Permissão para o /limite
yspawnersshop.limite.setar - Permissão para o /limite setar
yspawnersshop.limite.add - Permissão para o /limite add
yspawnersshop.limite.help - Permissão para o /limite help
yspawnersshop.limite.remove - Permissão para o /limite remove
yspawnersshop.limite.enviar - Permissão para o /limite enviar
yspawnersshop.multiplicador.[quantia] - Permissão para ter uma x quantia de multiplicador
yspawnersshop.giveredutor - Permissão para o /redutor give</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yspawnersshop_limite% - Retorna o limite do jogador formatado (1K, 1M, 1T...)
%yspawnersshop_limite_raw% - Retorna o limite do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yspawnersshop_gasto% - Retorna o valor gasto do jogador formatado (1K, 1M, 1T...)
%yspawnersshop_gasto_raw% - Retorna o valor gasto do jogador sem formatar (1000.0, 100.0, 10000.0...)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static SpawnersShopAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;SpawnersShopAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(SpawnersShopAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/46-ySpawnersShop">Site do plugin ySpawnersShop</a>
    </category>
</seealso>