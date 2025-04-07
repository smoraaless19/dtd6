<!-- 
Nombre: Sergio Morales 
Curso: ASIR1 
Fecha: 06/04/2025 
Ejercicio: DTD6 
-->

<!-- 
Documento XML con DTD interna.
 Los errores estaban en el contenido del XML, ahora corregido.
-->

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE pedido [
  <!-- 
  Un pedido contiene una o más líneas.
  Cada línea tiene: producto, cantidad, y precio.
  -->
  <!ELEMENT pedido (linea+)>
  <!ELEMENT linea (producto, cantidad, precio)>
  <!ELEMENT producto (#PCDATA)>
  <!ELEMENT cantidad (#PCDATA)>
  <!ELEMENT precio (#PCDATA)>
]>

<!-- Pedido con varias líneas de productos -->
<pedido>
  <!--  Línea 1 del pedido -->
  <linea>
    <producto>Teclado mecánico</producto>
    <cantidad>2</cantidad>
    <precio>45.99</precio>
  </linea>

  <!--  Línea 2 del pedido -->
  <linea>
    <producto>Monitor 24 pulgadas</producto>
    <cantidad>1</cantidad>
    <precio>129.50</precio>
  </linea>
</pedido>
