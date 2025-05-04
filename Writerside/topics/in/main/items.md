# Como usar o ItemStack Builder

### Exemplo Completo de Configuração
<procedure title="Exemplo Completo de Configuração">
   <p>Aqui está um exemplo completo de como poderia ser uma configuração com todas as opções mencionadas:</p>
   <code-block lang="yaml">
      id: 'DIAMOND_SWORD'
      data: 5
      amount: 3
      name: '&6Espada de Diamante'
      lore:
        - '&7A espada mais forte do mundo'
        - '&6Aproveite sua jornada!'
      glow: true
      custom-skull: true
      url: 'http://textures.minecraft.net/texture/abc123'
      hide-attributes: true
      hide-potion-effects: true
      hide-unbreakable: true
      hide-destroys: true
      hide-placed-on: true
      hide-enchants: true
      disable-metadata: true
      flags:
        - 'HIDE_ENCHANTS'
        - 'HIDE_UNBREAKABLE'
      custom-model-data: 123
      color: '255:0:0'
      nbt-tag:
        - 'CustomName=>Espada do Herói'
      effects:
        - 'SPEED-true-false'
   </code-block>
</procedure>

### Opções Disponíveis na Configuração
<procedure title="Opções Disponíveis na Configuração">
   <p>Aqui estão os parâmetros que podem ser passados para o `section` e seus respectivos efeitos:</p>
   
   <step><b>id / ID / material / Material</b>: 
      <p>Define o tipo de material do item. Pode ser um nome de material do Minecraft (com ou sem data) (ex: <b>STONE</b>, <b>IRON_SWORD</b>, <b>STONE:1</b>), o id de um material (com ou sem data) (ex: <b>1</b> para <b>STONE</b>, <b>1:1</b> para <b>STONE:1</b>), o id de um item criado pelo yPlugins ou um id de uma cabeça do <b>minecraft-heads.com</b>.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">material: 'DIAMOND_SWORD'</code-block>
      <code-block lang="yaml">material: 'STONE:1'</code-block>
      <code-block lang="yaml">material: '1'</code-block>
      <code-block lang="yaml">material: '1:1'</code-block>
      <code-block lang="yaml">material: '[YSTORE_ITEM]i2h3do2h42p2po42iog42opj42in'</code-block>
      <code-block lang="yaml">material: 'c25af966a326f9d98466a7bf8582ca4da6453de271b3bc9e59f57a99b63511c6'</code-block>
   </step>

   <step><b>data / Data</b>: 
      <p>Especifica o valor de dados para o item, caso o material possua variações (ex: cor de couro ou tipo de bloco).</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">data: 5</code-block>
   </step>

   <step><b>amount / Amount</b>: 
      <p>Define a quantidade do item. O valor padrão é 1 se não especificado.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">amount: 5</code-block>
   </step>

   <step><b>name / Name</b>: 
      <p>Define o nome do item. O nome pode ser estilizado com códigos de cor (<b>&</b>).</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">name: '&6Espada de Diamante'</code-block>
   </step>

   <step><b>lore / Lore</b>: 
      <p>Define a descrição do item. A descrição pode ser estilizada com códigos de cor (<b>&</b>).</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">lore: ['&7A espada mais forte do mundo']</code-block>
   </step>

   <step><b>glow / Glow</b>: 
      <p>Define se o item terá o efeito de brilho. Se <b>true</b>, o item brilhará.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">glow: true</code-block>
   </step>

   <step><b>custom-skull / CustomSkull</b>: 
      <p>Define se o item será uma cabeça personalizada (ex: uma cabeça de jogador ou uma cabeça com textura customizada).</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">custom-skull: true</code-block>
   </step>

   <step><b>url / URL</b>: 
      <p>URL de uma imagem personalizada usada para itens do tipo "skull" (cabeça). Isso é utilizado quando o item é uma cabeça customizada.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">url: 'http://textures.minecraft.net/texture/abc123'</code-block>
   </step>

   <step><b>hide-attributes</b>: 
      <p>Se <b>true</b>, oculta os atributos do item.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">hide-attributes: true</code-block>
   </step>

   <step><b>hide-potion-effects</b>: 
      <p>Se <b>true</b>, oculta os efeitos da poção.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">hide-potion-effects: true</code-block>
   </step>

   <step><b>hide-unbreakable</b>: 
      <p>Se <b>true</b>, oculta a informação de que o item é inquebrável.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">hide-unbreakable: true</code-block>
   </step>

   <step><b>hide-destroys</b>: 
      <p>Se <b>true</b>, oculta os blocos que o item pode destruir.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">hide-destroys: true</code-block>
   </step>

   <step><b>hide-placed-on</b>: 
      <p>Se <b>true</b>, oculta os blocos onde o item pode ser colocado.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">hide-placed-on: true</code-block>
   </step>

   <step><b>hide-enchants</b>: 
      <p>Se <b>true</b>, oculta os encantamentos do item.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">hide-enchants: true</code-block>
   </step>

   <step><b>disable-metadata</b>: 
      <p>Se <b>true</b>, desativa a adição de metadados NBT no item.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">disable-metadata: true</code-block>
   </step>

   <step><b>flags</b>: 
      <p>Define as flags do item. As flags alteram o comportamento e a aparência do item.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">flags: ['HIDE_ENCHANTS', 'HIDE_UNBREAKABLE']</code-block>
   </step>

   <step><b>custom-model-data</b>: 
      <p>Define o ID do modelo customizado para o item, permitindo usar modelos personalizados.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">custom-model-data: 123</code-block>
   </step>

   <step><b>color</b>: 
      <p>Define a cor do item. Usado principalmente em armaduras de couro.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">color: '255:0:0'</code-block>
   </step>

   <step><b>nbt-tag / nbt-tag-int / nbt-tag-short / nbt-tag-byte</b>: 
      <p>Define os NBT tags adicionais para o item. São usados para armazenar dados extras no item (ex: etiquetas personalizadas, atributos adicionais).</p>
      <p>Há uma NBT-Tag geral para a execução de comandos em itens de "enfeite" nos menus dos plugins: <b>"yStore-Menu-Command"</b></p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">nbt-tag: ['CustomName=>Meu Item']</code-block>
      <code-block lang="yaml">nbt-tag: ['yStore-Menu-Command=>sudo {player} /g oi']</code-block>
   </step>

   <step><b>effects</b>: 
      <p>Define os efeitos de poção para itens do tipo <b>POTION</b>. O formato é <b>"POTION_TYPE-EXTEND-UPGRADE"</b>.</p>
      <p><b>Exemplo:</b></p>
      <code-block lang="yaml">effects: ['SPEED-true-false']</code-block>
   </step>
</procedure>
