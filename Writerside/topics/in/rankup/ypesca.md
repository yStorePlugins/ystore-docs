# yPesca
<secondary-label ref="rankup"/>

### Descrição
Sistema de pesca completo com torneios

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
<video src="//www.youtube.com/watch?v=Qk9F2Vl8ZPI"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/pesca - Abre o menu principal
/pesca top - Abre o menu de top
/pesca ajuda - Envia a mensagem de ajuda
/pesca ir - Vai até a área de pesca
/pesca sair - Sai da área de pesca
/pesca peixes - Abre o menu de armazém de peixes
/corais - Vê a quantia de corais
/corais [player] - Vê a quantia de corais de um jogador
/corais enviar - Envia seus corais para um jogador
/corais add - Adiciona corais para um jogador
/corais give - Dá corais em forma de itens para um jogador
/corais set - Seta corais para um jogador
/corais remove - Remove corais de um jogador
/pesca setspawn - Seta o local de spawn da área de pesca
/pesca setsaida - Seta a saída da pesca
/pesca iniciartorneio - Inicia um torneio
/pesca parartorneio - Finaliza um torneio
/pesca givebooster - Dá um booster à um jogador
/pesca giveclasse - Dá uma classe à um jogador
/pesca givefish - Dá um peixe à um jogador
/pesca resetrod - Reseta a vara de um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ypesca.use - Permissão para o /pesca
ypesca.top - Permissão para o /pesca top
ypesca.go - Permissão para o /pesca ir
ypesca.exit - Permissão para o /pesca sair
ypesca.sell - Permissão para o /pesca peixes
ypesca.sellall - Permissão para o sell - all
ypesca.coin.use - Permissão para o /corais
ypesca.coin.look - Permissão para o /corais [player]
ypesca.coin.send - Permissão para o /corais enviar
ypesca.coin.help - Permissão para o /corais ajuda
ypesca.coin.add - Permissão para o /corais add
ypesca.coin.remove - Permissão para o /corais remove
ypesca.coin.set - Permissão para o /corais set
ypesca.coin.give - Permissão para o /corais give
ypesca.setspawn - Permissão para o /pesca setspawn
ypesca.setexit - Permissão para o /pesca setexit
ypesca.tournament.start - Permissão para o /pesca iniciartorneio
ypesca.tournament.stop - Permissão para o /pesca parartorneio
ypesca.givebooster - Permissão para o /pesca givebooster
ypesca.giveclasse - Permissão para o /pesca giveclasse
ypesca.givefish - Permissão para o /pesca givefish
ypesca.resetrod - Permissão para o /pesca resetrod</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ypesca_time% - Retorna o tempo que o jogador ficou pescando
%ypesca_time_raw% - Retorna o tempo que o jogador ficou pescando sem formatar
%ypesca_best_weight% - Retorna o maior peso que o jogador já pescou
%ypesca_fished% - Retorna a quantia de peixes que o jogador pescou
%ypesca_fished_raw% - Retorna a quantia de peixes que o jogador pescou sem formatar
%ypesca_fished_round% - Retorna a quantia de peixes que o jogador pescou em uma rodada
%ypesca_fished_round_raw% - Retorna a quantia de peixes que o jogador pescou em uma rodada sem formatar
%ypesca_coin% - Retorna a quantia de corais do jogador
%ypesca_coin_raw% - Retorna a quantia de corais do jogador sem formatar
%ypesca_tag% - Retorna a tag para o ganhador do torneio
%ypesca_level% - Retorna a o level atual do jogador (formatado)
%ypesca_level_raw% - Retorna a o level atual do jogador (sem formatar)
%ypesca_classe% - Retorna a classe atual
%ypesca_classe_next% - Retorna a próxima classe
%ypesca_classe_progress% - Retorna a barra de progresso de evolução da classe
%ypesca_classe_percentage% - Retorna a porcentagem de progresso de evolução da classe
%ypesca_progress% - Retorna a barra de progresso de evolução da vara
%ypesca_percentage% - Retorna a porcentagem de progresso de evolução da vara
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{ypesca} - Tag do jogador que ganhou o torneio
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static PescaAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;PescaAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(PescaAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/92-yPesca">Site do plugin yPesca</a>
    </category>
</seealso>