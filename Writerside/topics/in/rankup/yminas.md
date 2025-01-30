# yMinas
<secondary-label ref="rankup"/>

### Descrição
Crie minas com uma picareta customizável

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
<video src="https://www.youtube.com/watch?v=zoqq3USdhO4?start=3"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/mina - Abre o menu principal
/mina ir - Vai até uma mina
/mina sair - Sai da mina
/mina lista - Abre o menu de minas
/mina skins - Abre o menu de skins
/mina classes - Abre o menu de classes
/mina evoluir - Abre o menu de evolução
/mina bombas - Abre o menu de bombas
/blocos - Vê a quantia de blocos
/blocos [player] - Vê a quantia de blocos de um jogador
/blocos enviar - Envia seus blocos para um jogador
/blocos add - Adiciona blocos para um jogador
/blocos give - Dá blocos em forma de itens para um jogador
/blocos set - Seta blocos para um jogador
/blocos remove - Remove blocos de um jogador
/minaadmin criar - Cria uma mina
/minaadmin editar - Abre o menu de gerenciamento da mina
/minaadmin deletar - Deleta uma mina
/minaadmin resetar - Reseta uma mina
/minaadmin resetarpicareta - Reseta a picareta de um jogador
/minaadmin darnivel - Dar nível de picareta para um jogador
/minaadmin removernivel - Remover nível da picareta de um jogador
/minaadmin darenergia - Dar energia da picareta para um jogador
/minaadmin removerenergia - Remover energia da picareta de um jogador
/minaadmin lista - Abre a lista de minas
/minaadmin setsaida - Seta a saída das minas
/minaadmin resetarclasse - Reseta a classe de um jogador
/minaadmin adicionarclasse - Adiciona classe para um jogador
/minaadmin removerclasse - Remove a classe de um jogador
/minaadmin setarclasse - Seta a classe de um jogador
/minaadmin givebooster - Dar booster a um jogador
/minaadmin manutencao - Define a mina em manutenção ou não
/minaadmin kickall - Expulsa todos os jogadores das minas
/minaadmin reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">yminas.usar - Permissão para o /mina
yminas.ir - Permissão para o /mina ir
yminas.lista - Permissão para o /mina lista
yminas.sair - Permissão para o /mina sair
yminas.enchants - Permissão para o /mina evoluir
yminas.bombs - Permissão para o /mina bombas
yminas.classes - Permissão para o /mina classes
yminas.skins - Permissão para o /mina skins
yminas.blocos.usar - Permissão para o /blocos
yminas.blocos.look - Permissão para o /blocos [player]
yminas.blocos.send - Permissão para o /blocos enviar
yminas.blocos.help - Permissão para o /blocos ajuda
yminas.go.all - Permissão para ir à todas as minas
yminas.teleport.bypass - Permissão para não ter delay de teleporte
yminas.teleport.movebypass - Permissão para não cancelar o teleporte ao se mover
yminas.blocos.add - Permissão para o /blocos add
yminas.blocos.remove - Permissão para o /blocos remove
yminas.blocos.set - Permissão para o /blocos set
yminas.blocos.give - Permissão para o /blocos give
yminas.admin.criar - Permissão para o /minaadmin criar
yminas.admin.deletar - Permissão para o /minaadmin deletar
yminas.admin.editar - Permissão para o /minaadmin editar
yminas.admin.resetar - Permissão para o /minaadmin resetar
yminas.admin.resetarpicareta - Permissão para o /minaadmin resetarpicareta
yminas.admin.darnivel - Permissão para o /minaadmin darnivel
yminas.admin.removernivel - Permissão para o /minaadmin removernivel
yminas.admin.darenergia - Permissão para o /minaadmin darenergia
yminas.admin.removerenergia - Permissão para o /minaadmin removerenergia
yminas.admin.lista - Permissão para o /minaadmin lista
yminas.admin.setsaida - Permissão para o /minaadmin setsaida
yminas.admin - Permissão para ser reconhecido como admin
yminas.admin.reload - Permissão para o /minaadmin reload
yminas.admin.resetarclasse - Permissão para o /minaadmin resetarclasse
yminas.admin.adicionarclasse - Permissão para o /minaadmin adicionarclasse
yminas.admin.removerclasse - Permissão para o /minaadmin removerclasse
yminas.admin.setarclasse - Permissão para o /minaadmin setarclasse
yminas.givebooster - Permissão para o /minaadmin givebooster
yminas.admin.manutencao - Permissão para o /minaadmin manutencao
yminas.admin.kickall - Permissão para o /minaadmin kickall
yminas.manutencao.bypass - Permissão para entrar nas minas em manutenção</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%yminas_blocos% - Retorna os blocos do jogador formatado (1K, 1M, 1T...)
%yminas_blocos_raw% - Retorna os blocos do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_quebrados% - Retorna os blocos quebrados do jogador formatado (1K, 1M, 1T...)
%yminas_quebrados_raw% - Retorna os blocos quebrados do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_nivel% - Retorna o nível da picareta do jogador
%yminas_energia% - Retorna a energia da picareta do jogador formatado (1K, 1M, 1T...)
%yminas_energia_raw% - Retorna a energia da picareta do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_proximo_energia% - Retorna a energia do próx nível da picareta do jogador formatado (1K, 1M, 1T...)
%yminas_proximo_energia_raw% - Retorna a energia&nbsp;do próx nível&nbsp;da picareta do jogador sem formatar (1000.0, 100.0, 10000.0...)
%yminas_classe% - Retorna a classe atual
%yminas_classe_proximo% - Retorna a próxima classe
%yminas_classe_progresso% - Retorna a barra de progresso de evolução da classe
%yminas_classe_porcentagem% - Retorna a porcentagem de progresso de evolução da classe
%yminas_bonus% - Retorna o bônus do jogador
%yminas_bonus_display% - Retorna o display do bônus do jogador
%yminas_energia_progresso% - Retorna a barra de progresso de evolução da picareta
%yminas_energia_porcentagem% - Retorna a porcentagem de progresso de evolução da picareta
%yminas_encantamento_[enchant]% - Retorna o nível atual do encantamento
%yminas_encantamento_porcentagem_[enchant]% - Retorna a porcentagem do nível atual do encantamento
%yminas_encantamento_multiplicador_[enchant]% - Retorna o multiplicador do nível atual do encantamento
%yminas_tag_blocos% - Retorna a tag para o jogador com mais blocos
%yminas_tag_quebrados% - Retorna a tag para o jogador que quebrou mais blocos
%yminas_tag_tempo% - Retorna a tag para o jogador com mais tempo de mineração
%yminas_mina% - Retorna o nome da mina
%yminas_mina_raw% - Retorna o nome da mina na config
</code-block>

## Chat
<primary-label ref="chat"/>

Esta seção apresenta as placeholders disponíveis para utilização no chat. Consulte-as para compreender como aplicá-las de maneira eficaz.

<code-block lang="plain text">
{yminas_blocos} - Tag do jogador com mais blocos
{yminas_quebrados} - Tag do jogador que quebrou mais blocos
{yminas_tempo} - Tag do jogador com mais tempo de mineração
</code-block>

## API
<primary-label ref="api"/>

Configure nossa API para aproveitar todos os recursos oferecidos pelo plugin. Siga as instruções para garantir uma integração bem-sucedida.

<code-block lang="java">
public static MinaAPIHolder getAPI() {
    try {
        RegisteredServiceProvider&lt;MinaAPIHolder> rsp = Bukkit.getServer().getServicesManager()
            .getRegistration(MinaAPIHolder.class);
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
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/85-yMinas">Site do plugin yMinas</a>
    </category>
</seealso>