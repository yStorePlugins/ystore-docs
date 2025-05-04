# Como usar o ItemStack Builder

### Primeiros passos para utilizar o método `setup`
<procedure title="Passos para utilizar o método `setup`">
   <p>Confira os primeiros passos para utilizar o método `setup` para configurar um item no seu servidor.</p>
   <step>Obtenha uma instância de `ConfigurationSection` com as configurações do item.</step>
   <step>Chame o método `setup`, passando a instância `ConfigurationSection` e o valor para `loreb`.</step>
    <code-block lang="java">
    ConfigurationSection section = ...;  // Obtém as configurações do item
    boolean loreb = true;  // Se deseja adicionar o lore ao item
    ItemStack item = setup(section, loreb);
    </code-block>
   <step>Após isso, o método irá retornar um `ItemStack` configurado com base nas opções passadas.</step>
   <p>Parabéns, agora você pode usar o item configurado em seu servidor!</p>
</procedure>

### Primeiros passos para configurar o item com a `ConfigurationSection`
<procedure title="Passos para configurar o item com `ConfigurationSection`">
   <p>Confira como configurar os atributos do item utilizando a `ConfigurationSection`.</p>
   <step>Crie a `ConfigurationSection` com as configurações desejadas para o item.</step>
   <step>Defina as opções como `id`, `name`, `lore`, entre outras. Veja os parâmetros abaixo:</step>
   <code-block lang="yaml">
   id: DIAMOND_SWORD
   amount: 1
   name: '&6Espada de Diamante'
   lore:
     - '&7A espada mais forte do mundo'
   glow: true
   amount: 1
   </code-block>
   <step>Chame o método `setup` passando a `ConfigurationSection` criada.</step>
   <step>O método irá processar os dados e retornar o item configurado.</step>
   <p>Agora você tem um item personalizado com as configurações fornecidas!</p>
</procedure>

### Opções Disponíveis no `ConfigurationSection`
<procedure title="Opções disponíveis no `ConfigurationSection`">
   <p>Abaixo estão as opções que você pode configurar para personalizar o seu item.</p>
   
   <step><b>id / ID / material / Material</b>: Define o tipo de material do item (ex: `STONE`, `IRON_SWORD`).</step>
   <step><b>data / Data</b>: Define o valor de dados para variações do item (ex: cor de couro ou tipo de bloco).</step>
   <step><b>amount / Amount</b>: Define a quantidade do item (padrão é 1 se não especificado).</step>
   <step><b>name / Name</b>: Define o nome do item. Pode usar códigos de cor (`&`).</step>
   <step><b>lore / Lore</b>: Define a descrição do item. Pode ser estilizado com códigos de cor (`&`).</step>
   <step><b>glow / Glow</b>: Define se o item terá o efeito de brilho. Se `true`, o item brilha.</step>
   <step><b>custom-skull / CustomSkull</b>: Se `true`, o item será uma cabeça personalizada com uma URL fornecida.</step>
   <step><b>url / URL</b>: URL de uma imagem personalizada para o item do tipo "skull".</step>
   <step><b>hide-attributes</b>: Se `true`, oculta os atributos do item.</step>
   <step><b>hide-potion-effects</b>: Se `true`, oculta os efeitos da poção.</step>
   <step><b>hide-unbreakable</b>: Se `true`, oculta a informação de que o item é inquebrável.</step>
   <step><b>hide-destroys</b>: Se `true`, oculta os blocos que o item pode destruir.</step>
   <step><b>hide-placed-on</b>: Se `true`, oculta os blocos onde o item pode ser colocado.</step>
   <step><b>hide-enchants</b>: Se `true`, oculta os encantamentos do item.</step>
   <step><b>disable-metadata</b>: Se `true`, desativa a adição de metadados NBT no item.</step>
   <step><b>flags</b>: Define as flags do item. As flags alteram o comportamento do item.</step>
   <step><b>custom-model-data</b>: Define o ID do modelo customizado para o item, permitindo usar modelos personalizados.</step>
   <step><b>color</b>: Define a cor do item. Usado principalmente em armaduras de couro.</step>
   <step><b>nbt-tag / nbt-tag-int / nbt-tag-short / nbt-tag-byte</b>: Define os NBT tags do item.</step>
   <step><b>effects</b>: Define os efeitos de poção para itens do tipo `POTION`.</step>
</procedure>

<seealso style="cards">
    <category ref="itemstack-creation">
        <a href="itemstack-customizations.md"/>
        <a href="nbt-tags.md"/>
        <a href="item-enchants.md"/>
        <a href="effects.md"/>
    </category>
</seealso>
