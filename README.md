# Trustvox Sales

Este módulo foi desenvolvido com o objetivo de integrar de uma maneira mais simplificada o widget da Trustvox.

Necessário Magento 1.9+

### Version
1.0.0

### Como usar

Automaticamente o módulo adiciona o widget da Trustvox na página do produto (se a configuração "posição do widget" estiver como "Padrão"). Caso você queira colocar o widget em um local diferente na página do produto, basta colocar a configuração "posição do widget" como "Personalizado" e colar o código abaixo aonde desejar.

```php
<?php
echo $this
    ->getLayout()
    ->createBlock('core/template')
    ->setTemplate('trustvox/widget_trustvox.phtml')
    ->toHtml();
?>
```

#### Estrelas
Para colocar as estrelas de avaliação do produto, basta colocar o código abaixo na listagem de produtos ou na página do produto.

```php
<?php
// $product_id deve ser o id do produto.
echo Mage::helper('trustvox')->mostrarEstrelas($product_id);
?>
```
