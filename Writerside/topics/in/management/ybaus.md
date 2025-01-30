# yBaus
<secondary-label ref="management"/>

### Descrição
Armazene itens virtualmente

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
<video src="//www.youtube.com/watch?v=A7cCeDaPFzo"/>


<chapter title="Comandos" id="commands" collapsible="true">
<code-block lang="plain text">/bau - Abre o menu principal
/bau [numero]  - Abre um baú específico
/bau gerenciar [numero]  - Gerencia um baú específico
/bau ajuda - Vê todos os comandos
/bau   - Vê um baú específico do player (ADMIN)
/bau darbau   - Dá um baú extra para um jogador (ADMIN)
/bau setnpc - Seta o NPC do bau (ADMIN)
/bau delnpc - Deleta o NPC do bau (ADMIN)
/bau reload - Recarrega as configurações</code-block>
</chapter>

<chapter title="Permissões" id="permissions" collapsible="true">
<code-block lang="plain text">ybaus.usar - Permissão para o /bau, /bau gerenciar [numero]
ybaus.usar.numero - Permissão para o /bau [numero]
ybaus.ajuda - Permissão para o /bau ajuda
ybaus.outros - Permissão para o /bau [numero] [player]
ybaus.darbau - Permissão para o /bau darbau
ybaus.setnpc - Permissão para o /bau setnpc
ybaus.delnpc - Permissão para o /bau delnpc
ybaus.reload - Permissão para abrir o /bau reload
ybaus.enderchest - Permissão para abrir o enderchest
ybaus.quantia.[numero] - Permissão para limitar a quantia de baús que um jogador pode ter (respeitando o limite máximo da config.yml)
ybaus.default_quantia.[numero] - Permissão para dar baús por padrão ao logar</code-block>
</chapter>

## Placeholders
<primary-label ref="placeholders"/>

Aqui estão as placeholders disponíveis para utilização com este plugin. Consulte-as para entender como utilizá-las corretamente.

<code-block lang="plain text" ignore-vars="true">
%ybaus_amount% - Retorna a quantidade de baús do jogador formatado (1K, 1M, 1T...)
%ybaus_amount_raw% - Retorna a quantidade de baús do jogador&nbsp;sem formatar (1000.0, 100.0, 10000.0...)
</code-block>



## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/76-yBaus">Site do plugin yBaus</a>
    </category>
</seealso>