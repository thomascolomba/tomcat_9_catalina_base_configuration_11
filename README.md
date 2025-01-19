# tomcat_9_catalina_base_configuration_11

JMX -> remotely manages and monitors: 
- resources
- applications
- devices
- services
- jvm

el archivo jmx_examples.zip ha sido descargado desde : https://docs.oracle.com/javase/6/docs/technotes/guides/jmx/examples.html (ejemplos de SUN)

1) En jmx_examples\Essential\, abro un terminal ejecuto "javac com/example/mbeans/*.java", y "java com.example.mbeans.Main". Eso me enseña el mensaje "Waiting forever...".
2) En el Administrador de tareas (Ctrl+Alt+Supr), buscar el proceso de java que ejecuta el mando "java com.example.mbeans.Main" que hemos lanzado, se llama java.exe, copiar su número de proceso (columna PID), en mi caso es : 17120
3) Abro otro terminal, ejecuto "jconsole 17120", se me abre la jconsole en una interfaz, abro la pestaña "Mbeans", en el menú de la izquierda abro "com.example.mbeans", y abro "Hello".
4.1) En esa interfaz, en "Operations", en "sayHello", clico en el botón [sayHello]
4.2) En el termianl dónde se ejecuta "java com.example.mbeans.Main", y bajo el mensaje previo "Waiting forever...", se ve el nuevo mensaje "hello, world".
5.1) En la interfaz, en "Operations", en "add", en la sección "Operation invocación", cambiar los valores de p1 y p2 (por 10 y 3 por ejemplo), y clicar en el botón [add].
5.2) En la interfaz, sale un popup con el resultado "13".
6.1) En la interfaz, en "Attributes", en "Name", se ve el valor en lectura sólo "Reginald".
7.1) En la interfaz, en "Attributes", en "CacheSize", en la sección "Attribute value", cambiar el valor de CacheSize de 200 a 300 y clicar en el botón [Refresh].
7.2) En la interfaz, se ve que cambió el valor de CacheSize a 300. Y en el terminal dónde se enseñó el mensaje "Waiting forever...", ahora se ve el mensaje "Cache size now 300".


doc JMX : https://docs.oracle.com/javase/6/docs/technotes/guides/jmx/index.html
