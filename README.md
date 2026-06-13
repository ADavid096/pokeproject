# pokeproject
Proyecto simple sobre pokemon para practicar web development
## Contexto del Proyecto
Se desea desarrollar una aplicación web enfocada en la consulta de información y la simulación de combates de Pokémon. El sistema debe permitir almacenar y gestionar datos de las diferentes generaciones de los videojuegos oficiales, considerando que la información de cada Pokémon puede variar entre generaciones.
En una primera etapa, la aplicación estará orientada a la consulta de información. Los usuarios podrán acceder a datos relacionados con los Pokémon, tales como sus características, estadísticas, tipos, movimientos, habilidades y demás elementos presentes en los videojuegos. La información deberá estar organizada por generación, de modo que sea posible consultar los datos correspondientes a una versión específica de los juegos.
En una segunda etapa, la aplicación incorporará un módulo de simulación de combates. Este módulo permitirá enfrentar Pokémon bajo distintas configuraciones definidas por el usuario. Para ello, será necesario considerar las reglas, mecánicas y datos vigentes en la generación seleccionada, ya que aspectos como estadísticas base, movimientos disponibles, habilidades, tipos, efectividades y otras mecánicas pueden cambiar entre generaciones.
El sistema deberá permitir seleccionar una generación como contexto de trabajo, garantizando que toda la información utilizada en consultas y simulaciones corresponda a dicha generación. Esto implica que un mismo Pokémon puede poseer diferentes características dependiendo de la generación elegida.
El objetivo principal es disponer de una plataforma que represente de manera fiel la información histórica de los videojuegos de Pokémon y que permita realizar simulaciones de combate basadas en los datos y reglas correspondientes a cada generación.
## Alcance
- Gestionar información de Pokémon pertenecientes a distintas generaciones.
- Mantener versiones históricas de los datos cuando existan cambios entre generaciones.
- Consultar información detallada de Pokémon, movimientos, tipos, habilidades y otros elementos relacionados.
- Seleccionar una generación específica para realizar consultas.
- Simular combates utilizando los datos y reglas de la generación elegida.
- Permitir configurar parámetros de la simulación según las necesidades del usuario.
- Garantizar la coherencia entre los datos utilizados y la generación seleccionada.
## Detalles de diseño
Quiero poder consultar el pokemon contra el que me estoy enfrentando en determinada generación y/o juego y saber que tipo es, que habilidades puede tener, que naturaleza puede tener y que movimientos se maneja. Tambien quiero tener una lista de los ítems que existan, consumibles y ítems que puede llevar el pokemon por generación. Los movimientos deben mostrar la efectividad por tipo de pokemon y tipo de ataque y de alguna forma también se deberá poder ver que movimientos el pokemon aprende normalmente con el nivel y que movimientos puede aprender con MT.
La plataforma web consistirá de dos partes, el pokedex para consultar datos del pokemon, y la simulación de combate para probar habilidades en combates 1v1 y 2v2 de forma personalizada o estándar(preconfigurada).
El usuario podrá ingresar a la pagina como invitado o podrá registrarse para guardar sus datos de consultas y simulaciones realizadas. Tendra acceso a las dos opciones.
El pokedex tendrá filtros de la generación, la rareza (normal, legendario, semi legendario, etc), el tipo(agua, fuego, planta, etc) y filtro personalizado(puede ser creado por el usuario, tiene opción de guardar varios filtros con un nombre respectivo)
El pokedex mostrara la imagen del pokemon(puede ser el mismo que tiene en la generación o uno estandar) el numero en la pokedex de esa generación con su nombre. El tipo de pokemon, La rareza mostrada en estrellas u otro símbolo(Se tendrá una leyenda para esto). Tendra un deslizable o imagen de I II III IV V en romanos para ir cambiando las generaciones y los datos relativos a este. Tambien se mostrara un desplegable de Nivel(de esta forma iniciara en nivel 1 el dato pero se podrá cambiar en base a los niveles máximos de cada generacion). Se mostraran los stats básicos (atq, atq esp., def, def. esp, vel, etc) también los IVs dependiendo de la generacion. Se mostraran las habilidades que pueda obtener el pokemon (por lo general no son tantas) en una lista básica que muestre las opciones. Se mostraran las naturalezas que pueda obtener(si la naturaleza es random y puede ser obtenida por cualquier pokemon, entonces solo será un desplegable. Se mostraran las debilidades de tipo y por cuanto es cada uno, también las ventajas de tipo. Tambien mostrara los ítems para elegir como desplegable. Tendra un botón que lo haga shiny o no y en base a eso cambiara sus stats. Por ultimo habrá un botón para probarlo o guardarlo con mote si se quiere, esto tendrá un enlace directo a las simulaciones para probarlo en 1v1 o 2v2. Tambien habrá otro botón de comparar para hacer una comparación sencilla entre 2 pokemones en stats y tipos como si compararas características de un smartphone.

El simulador de lucha será 1v1 y 2v2, podrá ampliarse dependiendo de que tal funcione las mecánicas. Los cálculos de daño se realizarán en base a las reglas de la generación. Los versus serán en base a la generación en la que se este probando. Podra habilitarse o no el uso de ítems. Tambien podrá habilitarse el jugar con un equipo de 6 pokemones o los que quieras contra los que quieras que tenga el oponente. Sera un poco pokemon showdown pero se tratara de modificar cosas. Se hará experimental el probar peleas entre generaciones, de tal forma que el daño y defensa de cada pokemon sea en base a su generacion, entonces las habilidades serán en base a la gen

## Entidades
Lluvia de ideas para definir las entidades o similares a considerar para la base de datos
- El usuario
- El pokemon
- El entrenador
- La generacion
- Las habilidades
- Las naturalezas
- Los movimientos
- Los items
- Los gimnasios
- Las ligas
- Los estados
- Los climas
- Las teraevoluciones
- Los megas
- Los movimientos x e y
- Los combates
- Las imagenes de los pokemon
- Los lugares(ciudades, rutas, otras ubicaciones)

## Atributos
Luego de definir las entidades, se definen los atributos respectivos de cada entidad, si se repiten entonces se procede a verificar si una entidad puede asimilar otra porque es innecesaria.
