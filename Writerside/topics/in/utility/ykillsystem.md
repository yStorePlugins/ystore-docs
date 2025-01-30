# yKillSystem
<secondary-label ref="utility"/>

### Descrição
Dê um UP! no pvp do teu servidor.

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
<video src="//www.youtube.com/watch?v=EMlxHRfg3zM"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/kills - Abre o menu principal
/kills [player]  - Ver as informações de um jogador
/kills help  - Ver todos os comandos disponíveis
/kills setxp - Seta xp para um ou todos os jogadores
/kills addxp  - Adicionar xp para um ou todos os jogadores
/kills delxp  - Remover xp de um ou todos os jogadores
/kills resetkdr - Resetar o kdr
/abates
/mortes de um ou todos os jogadores
/kills giveresetkdr - Dar o item de resetkdr para um jogador
/kills addrank - Adiciona rank para um jogador
/kills delrank -  Remove rank de um jogador
/kills setrank -  Seta rank para um jogador</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ykillsystem.usar - Permissão para o /kills
ykillsystem.ver - Permissão para o /kills</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ykillsystem_kills% - Retorna a quantia de kills do jogador.
%ykillsystem_deaths% - Retorna a quantia de mortes do jogador.
%ykillsystem_kdr% - Retorna o KDR do jogador.
%ykillsystem_xp% - Retorna a quantia de XP do jogador (formatado).
%ykillsystem_xp_raw% - Retorna a quantia de XP do jogador (sem formatar).
%ykillsystem_tag% - Retorna a tag do rank do jogador.
%ykillsystem_nome% - Retorna o nome do rank do jogador.
%ykillsystem_next% - Retorna a tag do próximo rank.
%ykillsystem_streak% - Retorna o killstreak do jogador.
%ykillsystem_progressbar% - Retorna a barra de progresso do jogador.
%ykillsystem_porcentagem% - Retorna a porcentagem de progresso do jogador.
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{kill_tag} - Retorna a tag do rank do jogador.
{kill_nome} - Retorna o nome do rank do jogador.
{kill_kills} - Retorna as kills do jogador.
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static KillSystemAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;KillSystemAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(KillSystemAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/44-yKillSystem">Site do plugin yKillSystem</a>
    </category>
</seealso>