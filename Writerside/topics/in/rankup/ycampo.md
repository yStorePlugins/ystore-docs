# yCampo
<secondary-label ref="rankup"/>

### Descrição
Plantas agora dão dinheiro aos jogadores

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
<video src="//www.youtube.com/watch?v=E1e3fqp8GNM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/campo - Abre o menu principal
/tesoura - Recebe uma tesoura
/campo ajuda - Envia a mensagem de ajuda
/campo ir - Vai até a área de campo
/campo sair - Sai da área de campo
/campo flores - Abre o menu de flores
/campo armazem - Abre o menu de recompensas armazenadas
/campo top - Abre o menu de top
/fertilizantes - Vê a quantia de corais
/fertilizantes [player] - Vê a quantia de fertilizantes de um jogador
/fertilizantes enviar - Envia seus fertilizantes para um jogador
/fertilizantes add - Adiciona fertilizantes para um jogador
/fertilizantes give - Dá fertilizantes em forma de itens para um jogador
/fertilizantes set - Seta fertilizantes para um jogador
/fertilizantes remove - Remove fertilizantes de um jogador
/campo setspawn - Seta o local de spawn da área de campo
/campo setsaida - Seta a saída de campo
/campo givebooster - Dá um booster à um jogador
/campo give - Dá uma tesoura à um jogador
/campo reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ycampo.use - Permissão para o /campo, /campo flores, /campo armazem, /campo top
ycampo.tool - Permissão para o /tesoura
ycampo.go - Permissão para o /pesca ir
ycampo.exit - Permissão para o /pesca sair
ycampo.coin.use - Permissão para o /fertilizantes
ycampo.coin.look - Permissão para o /fertilizantes [player]
ycampo.coin.send - Permissão para o /fertilizantes enviar
ycampo.coin.help - Permissão para o /fertilizantes ajuda
ycampo.coin.add - Permissão para o /fertilizantes add
ycampo.coin.remove - Permissão para o /fertilizantes remove
ycampo.coin.set - Permissão para o /fertilizantes set
ycampo.coin.give - Permissão para o /fertilizantes give
ycampo.setspawn - Permissão para o /campo setspawn
ycampo.setexit - Permissão para o /campo setexit
ycampo.givebooster - Permissão para o /campo givebooster
ycampo.give - Permissão para o /campo give
ycampo.reload - Permissão para o /campo reload</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ycampo_time% - Retorna o tempo que o jogador ficou no campo
%ycampo_time_raw% - Retorna o tempo que o jogador ficou no campo sem formatar
%ycampo_broken% - Retorna a quantia de plantas que o jogador quebrou
%ycampo_broken_raw% - Retorna a quantia de plantas que o jogador quebrou sem formatar
%ycampo_pvp% - Retorna se o player está com o pvp ativo
%ycampo_pvp_raw% - Retorna se o player está com o pvp ativo sem formatar
%ycampo_coin% - Retorna a quantia de fertilizantes do jogador
%ycampo_coin_raw% - Retorna a quantia de fertilizantes&nbsp;do jogador sem formatar
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static CampoAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;CampoAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(CampoAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/107-yCampo">Site do plugin yCampo</a>
    </category>
</seealso>