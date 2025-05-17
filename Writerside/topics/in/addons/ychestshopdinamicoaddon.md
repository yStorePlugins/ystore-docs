# yChestShopDinamicoAddon
<secondary-label ref="addons"/>

### Descrição
Deixe os preços das placas administrativas de modo dinâmico

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
<video src="//www.youtube.com/watch?v=kOyNlWjuemM"/>


## Configuração
<primary-label ref="config"/>
Confira os arquivos de configuração deste plugin e revise os detalhes para garantir uma implementação correta.

<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yChestShopDinamicoAddon/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
maximum:
  # Máximo que o preço poderá subir
  # em porcentagem
  add: 100.0
  # Máximo que o preço poderá diminuir (cair)
  # em porcentagem
  remove: -90.0
  # Máximo que o preço poderá flutuar a cada operação de compra e venda
  # em porcentagem
  adjust: 5.0

# Tempo em segundos para normalizar o preço do shop aos poucos
# deixe 0 para não ter normalização sem novas transações
time-reduce: 60

# Atualizar a placa e o holograma na mudança de preços
# PODE CAUSAR LAG
update-sign: false
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yChestShopDinamicoAddon/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
maximum:
  # Máximo que o preço poderá subir
  # em porcentagem
  add: 100.0
  # Máximo que o preço poderá diminuir (cair)
  # em porcentagem
  remove: -90.0
  # Máximo que o preço poderá flutuar a cada operação de compra e venda
  # em porcentagem
  adjust: 5.0

# Tempo em segundos para normalizar o preço do shop aos poucos
# deixe 0 para não ter normalização sem novas transações
time-reduce: 60
]]>
</code-block>
</chapter>

</chapter>
<chapter title="Arquivos de Configuração" collapsible="true">
<chapter title="Estrutura do diretório" collapsible="false">
<code-block lang="plain text" ignore-vars="true">
Estrutura do diretório:
└── yChestShopDinamicoAddon/
    └── config.yml
</code-block>
</chapter>

<chapter title="config.yml" collapsible="true">
<code-block lang="yaml" ignore-vars="true">
<![CDATA[
maximum:
  # Máximo que o preço poderá subir
  # em porcentagem
  add: 100.0
  # Máximo que o preço poderá diminuir (cair)
  # em porcentagem
  remove: -90.0
  # Máximo que o preço poderá flutuar a cada operação de compra e venda
  # em porcentagem
  adjust: 5.0
]]>
</code-block>
</chapter>

</chapter>


## Erros comuns
<primary-label ref="errors"/>

Antes de configurar o plugin, revise os pontos listados aqui para evitar problemas frequentes durante a configuração.

<seealso style="cards">
    <category ref="wrs">
        <a href="yplugins.md"></a>        <a href="https://ystoreplugins.com.br/plugins/detalhes/147-yChestShopDinamicoAddon">Site do plugin yChestShopDinamicoAddon</a>
    </category>
</seealso>