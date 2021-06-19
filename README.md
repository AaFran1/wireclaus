# wireclaus

Existen tres tipos de redes en las cuáles funciona el módulo wireclaus:

## Redes cableadas

Las redes cableadas pueden adoptar varias formas. Todos involucran algún tipo de hardware diseñado para permitir que las señales eléctricas se envíen de un dispositivo a otro a través de un alambre o cable. Por lo tanto, las redes de sensores que emplean comunicación por cable también deben agregar hardware de red a los nodos de la red.
Existe una forma especial de red cableada que utiliza señales ópticas. Los cables están hechos de fibras de vidrio que utilizan ondas de luz en lugar de señales eléctricas.

Como se mencionó anteriormente, puede usar un Arduino con un escudo Ethernet para conectar los nodos del sensor a los nodos agregados o de recopilación de datos. Si sus sensores estuvieran alojados en computadoras Raspberry Pi, ya tendría el hardware necesario para conectar dos computadoras Raspberry Pi; todas tienen puertos LAN RJ-45.

Por supuesto, usar Ethernet por cable no es tan simple como conectar un cable a dos dispositivos. A menos que utilice un cable cruzado, necesita algún tipo de conmutador Ethernet para conectar los dispositivos. Una discusión detallada de las redes Ethernet y el hardware está más allá del alcance de este libro, pero es un medio de comunicación viable para las redes de sensores.

## Redes inalámbricas

Un medio más popular y versátil es la comunicación inalámbrica. En este caso, usa un dispositivo inalámbrico como un escudo WiFi para cada Arduino o adaptadores WiFi para computadoras Raspberry Pi. Al igual que Ethernet con cable, Ethernet inalámbrico (WiFi) requiere la adición de un enrutador inalámbrico. Sin embargo, WiFi tiene una distancia máxima mucho más corta, por lo que puede no ser adecuado para algunas redes.

Pero tienes otra forma de [conexión inalámbrica](https://transpero.net/ip/192-168-1-254/) a tu disposición. Puede utilizar módulos inalámbricos XBee en lugar de Ethernet (WiFi). XBee proporciona un protocolo ligero y especializado que es ideal para su uso en nodos sensores y pequeños microcontroladores y sistemas integrados. El resto de este libro utiliza módulos XBee para el mecanismo de comunicación de los proyectos de redes de sensores de ejemplo.

Una de las características de los módulos XBee es que son de bajo consumo y se pueden colocar en un modo de suspensión periódico para ahorrar energía. Sin embargo, la mejor característica es que los módulos XBee se pueden conectar directamente a los sensores, lo que le permite construir nodos de sensores aún más livianos (y más baratos).

## Redes híbridas

Algunas redes de sensores sofisticadas requieren la combinación de ambos medios de comunicación. Por ejemplo, una red de sensores industriales puede recopilar datos utilizando nodos de sensores instalados en muchos edificios o habitaciones diferentes. Es posible que se desee aislar las redes de sensores en subsistemas porque cada área puede requerir una forma diferente de red de sensores.

En este caso, puede ser mejor utilizar la tecnología inalámbrica para ciertos segmentos en los que el uso de redes cableadas es difícil (por ejemplo, un sensor en un robot industrial en movimiento) y Ethernet cableada para vincular los subsistemas a un registro de datos central o sistema de monitoreo.
