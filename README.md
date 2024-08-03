# Contexto
El restaurante "Sabores del Mundo", es conocido por su auténtica cocina y su ambiente acogedor.
Este restaurante lanzó un nuevo menú a principios de año y ha estado recopilando información detallada sobre las transacciones de los clientes para identificar áreas de oportunidad y aprovechar al máximo sus datos para optimizar las ventas.
## Objetivo

Identificar cuáles son los productos del menú que han tenido más éxito y cuales son los que menos han gustado a los clientes.
Pasos a seguir:

  a)	Crear la base de datos con el archivo create_restaurant_db.sql

  b)	Explorar la tabla “menu_items” para conocer los productos del menú.
  
      1.- Realizar consultas para contestar las siguientes preguntas:
      
	● Encontrar el número de artículos en el menú.
          SELECT COUNT(*)
          FROM MENU_ITEMS
        
	● ¿Cuál es el artículo menos caro y el más caro en el menú?
          Menos caro Edamame	a $5.00
          SELECT item_name, price
	        FROM menu_items 
	        ORDER BY PRICE ASC LIMIT 1;
          
          Más caro Shrimp Scampi 19.95
          SELECT item_name, price
	        FROM menu_items 
	        ORDER BY PRICE DESC LIMIT 1;
        ●	¿Cuántos platos americanos hay en el menú?

        
        ●	¿Cuál es el precio promedio de los platos?
  
  c) Explorar la tabla “order_details” para conocer los datos que han sido recolectados.
      1.- Realizar consultas para contestar las siguientes preguntas:
        ●	¿Cuántos pedidos únicos se realizaron en total?
        ●	¿Cuáles son los 5 pedidos que tuvieron el mayor número de artículos?
        ●	¿Cuándo se realizó el primer pedido y el último pedido?
        ●	¿Cuántos pedidos se hicieron entre el '2023-01-01' y el '2023-01-05'?
  
  d) Usar ambas tablas para conocer la reacción de los clientes respecto al menú.
      1.- Realizar un left join entre entre order_details y menu_items con el identificador item_id(tabla order_details) y menu_item_id(tabla menu_items).
  
  e) Una vez que hayas explorado los datos en las tablas correspondientes y respondido las preguntas planteadas, realiza un análisis adicional utilizando este join entre las tablas. El objetivo es identificar 5 puntos clave que puedan ser de utilidad para los dueños del restaurante en el lanzamiento de su nuevo menú. Para ello, crea tus propias consultas y utiliza los resultados obtenidos para llegar a estas             conclusiones.
      1.- Lo más vendido son las Hamburguesas pero han tenido mayores ingresos con la venta de Korean Beef Bowl
      2.- Lo menos vendido son los Chicken Tacos
      3.- La comida Asiatica es la más vendida pero la comida Italiana es la que trae un mayor ingreso
      4.- La comida americana es la menos vendida y con la que hemos tenido un menor ingreso
      5.- Entre las 12 y las 13:59 es la hora con más ventas
      
## Diccionario de datos de las tablas.

 ![Capturatabla](https://github.com/user-attachments/assets/7a40a7f0-a810-4d33-b02d-1d45830f45d7)


