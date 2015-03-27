#Action Planner

Los archivos donde programarán sus máquinas de estados están en la ruta *ActionPlanner/Tests/StateMachines*

AhEencontrarán un archivo de clase por cada una de las máquinas de estados correspondientes a las pruebas de Robocup:

* AudioTest.cs - para Speech Recognition & Audio Detection Test
* GPSR.cs - para GPSR
* ManipulationTest.cs - para Manipulation And Object Recognition
* NavigationTest.cs - para Navigation Test
* OpenChallenge.cs - para Open Challenge
* PersonRecognition.cs - para Person Recognition Test
* Restaurant.cs - para Restaurant
* RoboNurse.cs - para Robo-Nurse
* RoboZoo.cs - para Robo-Zoo
* WakeMeUp.cs - para Wake me up test

Cada archivo cuenta con lo mú‹imo necesario que debe tener una máquina de estados. Modifiquen los archivos que correspondan a las pruebas que tienen asignadas.

En la ruta *ActionPlanner/Tests/ConfigurationFiles* encontrarán archivos de clase para la configuración de cada una de las máquinas de estados:

* AudioTest_WORLD.cs corresponde a AudioTest.cs
* GPSR_WORLD.cs corresponde a GPSR.cs
* ManipulationTest_WORLD.cs corresponde a ManipulationTest.cs
* NavigationTest_WORLD.cs corresponde a NavigationTest.cs
* OpenChallenge_WORLD.cs corresponde a OpenChallenge.cs
* PersonRecognition_WORLD.cs corresponde a PersonRecognition.cs
* Restaurant_WORLD.cs corresponde a Restaurant.cs
* RoboNurse_WORLD.cs corresponde a RoboNurse.cs
* RoboZoo_WORLD.cs corresponde a RoboZoo.cs
* WakeMeUp_WORLD.cs corresponde a WakeMeUp.cs

En estas clases pueden configurar todo lo correspondiente al estado del robot (posiciones de brazos, locations del motion planner, mensajes para el spgen, etc.). Pueden usarlos si gustan o pueden configurar todo en la máquina de estados, como se sientan más cómodos.

En la ruta *ActionPlanner/ComplexActions*
encontrarán máquinas de estado de "uso común" (entrar a la arena, tomar objetos, etc). A estas las pueden mandar a llamar desde otra máquina de estados.

En el archivo DefaultStateMachineSM.cs encontrarán un ejemplo de una máquina de estados simple (entrar a la arena->tomar un objeto de una mesa->dejar el objeto en otra mesa->salir de la arena) y en el archivo DefaultStateMachine_WORLD.cs la clase de configuración correspondiente a la máquina de estados. Pueden usar esto como ejemplo base (el código estEcomentado).

AsEmismo, se separEla clase Command Manager en varios archivos (uno por cada módulo del robot):

* HAL9000CmdMan.ARMS.cs - contiene todos los comandos para ARMS
* HAL9000CmdMan.BLK.cs - contiene todos los comandos para blackboard
* HAL9000CmdMan.OBJ_FNDT.cs - contiene todos los comandos de visión
* etc...

Por último, cada una de las máquinas de estado ya tiene un botón de la interfaz gráfica asociado, por lo que sólo deberán preocuparse de modificar la clase correspondiente a la prueba que estén programando.