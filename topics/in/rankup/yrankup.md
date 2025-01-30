# yRankup
<secondary-label ref="rankup"/>

### Descrição
Agora é possível evoluir de rank com cabeças e outros meios de economias.

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
<video src="//www.youtube.com/watch?v=TOYnlP6w7WI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/rank - Abre o menu principal
/rankup - Abre o menu de rankup
/prestigio - Dá prestígio
/heads - Abre o menu de heads
/rank top- Abre o menu de top
/rank [player] - Vê as informações de um jogador
/rank giverankup - Dar item rankup para um jogador
/rank giveprestigio - Dar item prestígio para um jogador
/rank setrank - Seta um rank para um jogador
/rank setprestigio - Seta um prestígio para um jogador
/fragmentos - Vê a quantia de fragmentos
/fragmentos [player] - Vê a quantia de fragmentos de um jogador
/fragmentos enviar - Envia seus fragmentos para um jogador
/fragmentos add - Adiciona fragmentos para um jogador
/fragmentos give - Dá fragmentos em forma de itens para um jogador
/fragmentos set - Seta fragmentos para um jogador
/fragmentos remove - Remove fragmentos de um jogador
/heads add - Adiciona heads para um jogador
/heads give - Dá heads em forma de itens para um jogador
/heads set - Seta heads para um jogador
/heads remove - Remove heads de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yrankup.use - Permissão para o /rank
yrankup.giverankup - Permissão para o /rank giverankup
yrankup.giveprestige - Permissão para o /rank giveprestige
yrankup.setrank - Permissão para o /rank setrank
yrankup.setprestige - Permissão para o /rank setprestige
yrankup.admin.reload - Permissão para o /rank reload
yrankup.look - Permissão para o /rank [player]
yrankup.rankup - Permissão para o /rankup
yrankup.rankup.max - Permissão para o /rankup max
yrankup.ranks - Permissão para o /ranks
yrankup.heads - Permissão para o /heads
yrankup.prestige - Permissão para o /prestigio
yrankup.autorankup - Permissão para o /autorankup
yrankup.coin.use - Permissão para o /fragmentos
yrankup.coin.look - Permissão para o /fragmentos [player]
yrankup.coin.send - Permissão para o /fragmentos enviar
yrankup.coin.help - Permissão para o /fragmentos ajuda
yrankup.coin.add - Permissão para o /fragmentos add
yrankup.coin.remove - Permissão para o /fragmentos remove
yrankup.coin.set - Permissão para o /fragmentos set
yrankup.coin.give - Permissão para o /fragmentos give
yrankup.head.help - Permissão para o /heads ajuda
yrankup.head.add - Permissão para o /heads add
yrankup.head.remove - Permissão para o /heads remove
yrankup.head.set - Permissão para o /heads set
yrankup.head.give - Permissão para o /heads give</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yrankup_rank_name% - Retorna o nome do rank
%yrankup_rank_tag% - Retorna a tag do rank
%yrankup_next_rank_name% - Retorna o nome do próximo rank
%yrankup_next_rank_tag% - Retorna a tag do próximo rank
%yrankup_prestige_tag% - Retorna a tag do prestígio
%yrankup_prestige% - Retorna o prestígio
%yrankup_prestige_raw% - Retorna o prestígio sem formatar
%yrankup_next_prestige% - Retorna o próximo prestígio
%yrankup_next_prestige_raw% - Retorna o próximo prestígio sem formatar
%yrankup_progressbar% - Retorna a barra de progresso do rank
%yrankup_percentage% - Retorna a porcentagem de rankup
%yrankup_percentage_raw% - Retorna a porcentagem de rankup (decimais claros)
%yrankup_heads% - Retorna a quantia de heads
%yrankup_heads_raw% - Retorna a quantia de heads sem formatar
%yrankup_head_[head]% - Retorna a quantia de uma head específica
%yrankup_head_[head]_raw% - Retorna a quantia de uma head específica sem formatar
%yrankup_autorankup% - Retorna o estado do auto-rankup
%yrankup_autorankup_raw% - Retorna o estado do auto-rankup sem formatar
%yrankup_coin% - Retorna a quantia de fragmentos
%yrankup_coin_raw% - Retorna a quantia de fragmentos sem formatar
%yrankup_next_price_[provider]% - Retorna a quantia necessária de tal economia para dar rankup
%yrankup_next_price_[provider]_nodiscount% - Retorna a quantia necessária de tal economia para dar rankup sem desconto
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{rank_name} - Retorna o nome do rank
{rank_tag} - Retorna a tag do rank
{next_rank_name} - Retorna o nome do próximo rank
{next_rank_tag} - Retorna a tag do próximo rank
{prestige} - Retorna o prestígio
{prestige_raw} - Retorna o prestígio sem formatar
{prestige_tag} - Retorna a tag do prestígio
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static RankupAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;RankupAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(RankupAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/32-yRankup">Site do plugin yRankup</a>
    </category>
</seealso>