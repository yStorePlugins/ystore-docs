# yClansColorsAddon
<secondary-label ref="addons"/>

### Descrição
Dê uma cor diferente aos seus aliados e inimigos

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
<video src="https://i.imgur.com/d8t9Ed8.png"/>


## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yClansColorsAddon/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
#         ____ _                  ____      _                   _       _     _
#  _   _ / ___| | __ _ _ __  ___ / ___|___ | | ___  _ __ ___   / \   __| | __| | ___  _ __
# | | | | |   | |/ _` | '_ \/ __| |   / _ \| |/ _ \| '__/ __| / _ \ / _` |/ _` |/ _ \| '_ \
# | |_| | |___| | (_| | | | \__ \ |__| (_) | | (_) | |  \__ \/ ___ \ (_| | (_| | (_) | | | |
#  \__, |\____|_|\__,_|_| |_|___/\____\___/|_|\___/|_|  |___/_/   \_\__,_|\__,_|\___/|_| |_|
#  |___/
#

# Formatação da placeholder (RELATIVE)
# Para testes, use o comando "/papi parserel <player> <player> %rel_yclanscolorsaddon_color%TESTE"
#
# PLACEHOLDER: %rel_yclanscolorsaddon_color%
#
placeholders:
  no-clan: '&7'
  same-clan: '&a'
  clan-ally: '&2[A] &a'
  clan-neutral: '&c'
  clan-rival: '&4[R] &c'
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/153-yClansColorsAddon">Site do plugin yClansColorsAddon</a>
    </category>
</seealso>