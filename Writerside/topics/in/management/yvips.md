# yVips
<secondary-label ref="management"/>

### Descrição
Venda vantagens no seu servidor

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
<video src="//www.youtube.com/watch?v=lUqLHCAyvZ8"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/vip - Abre o menu principal
/vips [player] - Veja os vips ativos.
/keys [player
/admin] - Veja as chaves ativas.
/trocarvip [vip] - Trocqa o seu VIP atual por outro
/vip info [id-vip] - Vê as informações gerais do id selecionado.
/tempovip [jogador] - Mostra o seu tempo de vip ou de outro jogador
/usarkey [key] - Ativa um VIP a partir de uma KEY
/partyvip - Mostra o progresso atual do party-vip
/ativarvip [id] - Ativa um VIP a partir do ID do bônus
/bonusvip dar [player
/random] [vip] [duração] - Dar uma chave bônus para um jogador
/bonusvip enviar [id] [player] - Envia uma chave bônus para um jogador
/bonusvip ativar [id] - Ativa uma chave bônus
/vendervip [id] [economia] [preço] - Vende uma chave VIP
/comprarvip [id] - Compra uma chave VIP
/cancelarvendavip [id] - Cancela a venda de uma chave VIP
/congerlavip - Congela
/descongela o tempo dos vips
/darvip [jogador] [vip] [tempo] - Dá um determinado vip a um jogador
/darchave [jogador] [vip] [tempo] - Dá uma chave de um determinado vip a um jogador
/setarvip [jogador] [vip] [tempo] - Dá um determinado vip a um jogador, porém sem as mensagens e os comandos de ativação
/gerarkey [vip] [tempo] [tipo] [usos] - Cria uma key aleatória de um determinado vip
/criarkey [vip] [tempo] [tipo] [usos] [key] - Cria uma key customizada de um determinado vip
/editarkey [key] [vip] [tempo] [tipo] [usos] - Edita uma key
/deletarkey [key] - Deleta uma key
/removervip [id] - Remove um vip
/removervipplayer [player] - Remove todos os vips de um jogador
/removertempovip [id] [tempo] - Remove tempo de um vip</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yvips.use - Permissão para o /vip
yvips.freeze - Permissão para o /congelarvip
yvips.reload - Permissão para o /vip reload
yvips.bonusvip - Permissão para o /bonusvip
yvips.bonusvip.give - Permissão para o /bonusvip dar
yvips.bonusvip.active - Permissão para o /bonusvip ativar
yvips.bonusvip.send - Permissão para o /bonusvip enviar
yvips.bonusvip.list - Permissão para o /bonusvip lista
yvips.activevip - Permissão para o /ativarvip
yvips.buyvip - Permissão para o /comprarvip
yvips.givekey - Permissão para o /darchave
yvips.keys - Permissão para o /keys
yvips.keys.admin - Permissão para o /keys admin
yvips.keys.others - Permissão para o /keys [player]
yvips.sellcancelvip - Permissão para o /cancelarvendavip
yvips.sellvip - Permissão para o /vendervip
yvips.sellsvip - Permissão para o /vendasvip
yvips.sellsvip.others - Permissão para o /vendasvip [player]
yvips.usekey - Permissão para o /usarkey
yvips.createkey - Permissão para o /criarkey
yvips.editkey - Permissão para o /editarkey
yvips.generatekey - Permissão para o /gerarkey
yvips.removekey - Permissão para o /removerkey
yvips.infovip - Permissão para o /vip info
yvips.partyvip - Permissão para o /partyvip
yvips.timevip - Permissão para o /tempovip
yvips.timevip.others - Permissão para o /tempovip [player]
yvips.tradevip - Permissão para o /trocarvip
yvips.tradevip.others - Permissão para o /trocarvip [vip] [player]
yvips.vips - Permissão para o /vips
yvips.vips.others - Permissão para o /vips [player]
yvips.addvip - Permissão para o /darvip
yvips.setvip - Permissão para o /setarvip
yvips.removevip - Permissão para o /removervip
yvips.removevipplayer - Permissão para o /removervipplayer
yvips.removetime - Permissão para o /removertempovip
yvips.admin - Permissão para ser reconhecido como admin</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yvips_partyvip_has% - Retorna a quantia atual do party-vip
%yvips_partyvip_need% - Retorna a quantia necessária do party-vip
%yvips_partyvip_progressbar% - Retorna a barra de progresso do party-vip
%yvips_partyvip_percentage% - Retorna a porcentagem atual do party-vip
%yvips_credit% - Retorna a quantia de créditos VIP do jogador formatado
%yvips_credit_raw% - Retorna a quantia de créditos VIP do jogador sem formatar
%yvips_vip_raw% - Retorna o tipo do vip
%yvips_vip_tag% - Retorna a tag do vip
%yvips_vip_prefix% - Retorna o prefixo do vip
%yvips_start_raw% - Retorna o horário raw de ativação do vip
%yvips_expire_raw% - Retorna o horário raw de expiração do vip
%yvips_duration_raw% - Retorna o horário raw de duração do vip
%yvips_start_date% - Retorna a data de ativação do vip
%yvips_start_hour% - Retorna a hora de ativação do vip
%yvips_expire_date% - Retorna a data de expiração do vip
%yvips_expire_hour% - Retorna a hora de expiração&nbsp;&nbsp;do vip
%yvips_duration% - Retorna a duração do vip
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{vip_tag} - Retorna a tag do vip
{vip_prefix} - Retorna o prefixo do vip
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static VipAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;VipAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(VipAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/103-yVips">Site do plugin yVips</a>
    </category>
</seealso>