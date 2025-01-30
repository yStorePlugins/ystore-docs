# yEventos
<secondary-label ref="utility"/>

### Descrição
Crie interações e competições entre os jogadores, vários eventos para divertir seus players.

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
<video src="//www.youtube.com/watch?v=GoJAAM4Hc8s"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/eventos - Abre o menu principal
/eventos top - Abre o menu do top
/eventos info - Abre o menu de eventos
/eventos entrar - Entra no evento presencial que está ocorrendo
/eventos camarote - Entra no camarote do evento presencial que está ocorrendo
/eventos sair - Sair do evento presencial que está ocorrendo
/eventos setexitall - Seta a saída de todos os eventos
/eventos reload - Recarrega as configurações
/[name] - Para participar do evento
/[name] [resposta] - Para responder um evento chat
/[name] camarote - Para ir ao camarote do evento
/[name] apostar - Para apostar em alguém no evento
/[name] sair - Para sair do evento
/[name] iniciar - Para iniciar o evento
/[name] parar - Para parar o evento
/[name] setloc - Para setar um local do evento
/[name] addloc - Para adicionar multiplas entradas ao evento
/[name] delloc - Para deletar um local do evento
/[name] wand - Para pegar a ferramenta de seleção do evento
/[name] define - Para definir a área do evento
/[name] addwall - Para adicionar uma parede ao evento
/[name] clearwalls - Para limpar as paredes do evento
/[name] addsafezone - Para adicionar uma safezone ao evento
/[name] clearsafezones - Para limpar as safezones do evento
/[name] forcestart - Para forçar a inicialização do evento
/[name] ajuda - Mostra todos os comandos daquele evento</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yeventos.use - Permissão para o /eventos
yeventos.top - Permissão para o /eventos top
yeventos.info - Permissão para o /eventos info
yeventos.enter - Permissão para o /eventos entrar
yeventos.exit - Permissão para o /eventos exit
yeventos.reload - Permissão para o /eventos reload
yeventos.setexitall - Permissão para o /eventos setexitall
yeventos.[name].participate - Permissão para o /[name] e /[name] [resposta]
yeventos.[name].camarote - Permissão para o /[name] camarote
yeventos.[name].bet - Permissão para o /[name] apostar
yeventos.[name].exit - Permissão para o /[name] sair
yeventos.[name].start - Permissão para o /[name] iniciar
yeventos.[name].stop - Permissão para o /[name] parar
yeventos.[name].forcestart - Permissão para o /[name] forcestart
yeventos.[name].setloc - Permissão para o /[name] setloc
yeventos.[name].addloc - Permissão para o /[name] addloc
yeventos.[name].delloc - Permissão para o /[name] delloc
yeventos.[name].wand - Permissão para o /[name] wand
yeventos.[name].define - Permissão para o /[name] define
yeventos.[name].addwalls - Permissão para o /[name] addwalls
yeventos.[name].clearwalls - Permissão para o /[name] clearwalls
yeventos.[name].addsafezone - Permissão para o /[name] addsafezone
yeventos.[name].clearsafezones - Permissão para o /[name] clearsafezones
yeventos.staff - Permissão para ser reconhecido como staff
yeventos.command.bypass - Permissão para executar comandos nos eventos
yeventos.vanish.bypass - Permissão para não ficar invisível no camarote
yeventos.blockplace.bypass - Permissão para colocar blocos nos eventos</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yeventos_wins% - Retorna a quantia de eventos que o player ganhou com formatação (1K, 1000,00...)
%yeventos_wins_raw% - Retorna a quantia de eventos que o player ganhou sem formatação.
%yeventos_wins_[name]% - Retorna a quantia de vezes que o player ganhou o evento, com formatação (1K, 1000,00...)
%yeventos_wins_[name]_raw% - Retorna a quantia de vezes que o player ganhou o evento, sem formatação.
%yeventos_[name]&nbsp;- Retorna se o evento está ativo% - yeventos_[name]_tag
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{[name]} - Retorna a tag (se possuir)
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static EventAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;EventAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(EventAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/29-yEventos">Site do plugin yEventos</a>
    </category>
</seealso>