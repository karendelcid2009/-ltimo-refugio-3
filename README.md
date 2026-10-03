# -ultimo-refugio-3
#karen Estephania del cid Sical soy programador JR. con conocimiento y buenas prácticas poo.
#fase 1 Análisis escrito en la parte de código encontrará el análisis escrito de cómo se espera que sea el juego con datos importantes en el para el desarrollo de su respectivo diagrama de flujo.
#fase 2 diagrama de flujo del juego en la parte del código se encuentra el respectivo diagrama de flujo que se hizo después del análisis que indica las direcciones los mundos los aparatos el vestuario, herramientas, personajes junto con lo que todavía se necesita terminar el juego.
#fase 3 código en VISUAL STUDIO en lenguaje de Python jugable para la consola de visual es el código en donde el videojuego toma vida y en donde se cumple todo lo del análisis y diagrama de flujo
#fase 4 repositorio en Github creamos un repositorio interactivo que permita que todo lo que hagamos se pueda editar exportar y compartir con otros usuarios y jugadores 
# partes del juego 
#​El proyecto es un juego de estrategia, supervivencia y rol por turnos en consola, donde un grupo de jugadores (de 1 a 4 participantes) debe cooperar para sobrevivir a oleadas de zombies tácticos dentro de escenarios como "Nivel 1: El Búnker Olvidado". 
#(import)
​Para dar vida a este juego, en Python se recurre habitualmente a módulos estándar:
​import random: Fundamental para calcular la probabilidad de fallar/acertar ataques, la generación aleatoria del daño de los zombies, el dinero recolectado o la selección al azar de a qué jugador ataca la IA zombie.  
​import time: Utilizado para añadir pausas de lectura (usando time.sleep()), simular tiempos de carga ("CARGANDO NIVEL 1...") y dar mayor dinamismo a la interfaz por consola.
#​El código está estructurado mediante clases y métodos para gestionar las entidades principales del juego:
​Clase Jugador:
​Atributos: Mantiene el control sobre el nombre del jugador, puntos de vida (Vida: 100/100), lista de inventario/armas (['Pistola Básica']), dinero disponible ($0), comida guardada, estado de salud ([Vivo]) y Puntos de Acción (PA: 3/3).  
​Métodos: Funciones para moverse, interactuar por chat, realizar compras, atacar y finalizar turno gastando Puntos de Acción (PA).  
​Clase Zombie / IA de Zombies:
​Atributos: Tipo de zombie (ej. Zombie Lento), vida inicial (Vida: 60/60) y estado (zambie_esta_vivo()).  
​Comportamiento (IA Zombie): Al terminar el turno de los jugadores, la IA de los zombies busca automáticamente un objetivo y lanza ataques de daño aleatorio a los jugadores con vida.  
​Gestor de la Partida / Campo de Batalla:
​Métodos de auditoría y monitoreo como mostrar_estado_general(self) 
#​Establece el objetivo inicial ("Sobrevivir a la oleada inicial").  
​Pausa el flujo hasta que los usuarios confirmen presionado ENTER.  
​Generación de Enemigos y Despliegue:
​Instancia enemigos con estadísticas predefinidas y muestra el número de zombies generados.
#Bucle Principal del Juego (Sistema de Turnos y Puntos de Acción - PA):
​Cada jugador cuenta con 3 Puntos de Acción (PA) por turno para elegir entre las opciones del menú interactivo:  
​[M]overse (Gasta 1 PA): Cambia la posición táctica del jugador.  
​[I]nteractuar (Chat) (Gasta 0 PA).  
​[C]omprar (Armas/Comida) (Gasta 2 PA): Valida si el jugador posee fondos suficientes antes de realizar la transacción (ej. valida si posee mínimo $10).  
​[A]tacar Zombie (Gasta 1 PA): Aplica daño directo a la vida del enemigo seleccionado.  
​[D]esbloquear Debilidades (Gasta 0 PA): Muestra el estado y estadísticas de los zombies activos.  
​[F]inalizar Turno: Pasa la mano al siguiente jugador o activa el turno de la IA Enemiga.
#
