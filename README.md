# PROYECTO DE REDES CON MININET Y CÓMO SE INTERACTÚA CON COMANDOS MEDIANTE LA TERMINAL DE UBUNTU

- Adrian Gome
- Esteysi Guzman
- Jairo Fernande
- Victor Seleme

## Option 2: Native Installation from Source se uso para la descarga de miminet 
## Installation


```sh
git clone https://github.com/mininet/mininet
```

Tenga en cuenta que el comando git anterior verificará la última y mejor Mininet (¡lo cual recomendamos!). Si desea ejecutar la última versión etiquetada/publicada de Mininet, o cualquier otra versión, puede verificar esa versión explícitamente:

```sh
mininet/util/install.sh [options]
```
Una vez que tengas el árbol de fuentes, el comando para instalar Mininet es:
```sh
mininet/util/install.sh [options]



Las opciones típicas de install.sh incluyen:

-a: instale todo lo que está incluido en Mininet VM, incluidas dependencias como Open vSwitch y adiciones como OpenFlow wirehark dissector y POX. De forma predeterminada, estas herramientas se integrarán en directorios creados en su directorio de inicio.
-nfv: instala Mininet, el conmutador de referencia OpenFlow y Open vSwitch
-s mydir: utilice esta opción antes que otras opciones para colocar árboles de origen/compilación en un directorio específico en lugar de en su directorio de inicio.
Por lo tanto, probablemente desee utilizar uno (y sólo uno) de los siguientes comandos:


```sh
To install everything (using your home directory): install.sh -a
To install everything (using another directory for build): install.sh -s mydir -a
To install Mininet + user switch + OvS (using your home dir): install.sh -nfv
To install Mininet + user switch + OvS (using another dir:) install.sh -s mydir -nfv
```


Puede obtener información sobre otras opciones útiles (por ejemplo, instalar el disector OpenFlow Wireshark, si aún no está incluido en su versión de Wireshark) usando 

```sh
install.sh -h
```

Una vez completada la instalación, pruebe la funcionalidad básica de Mininet

```sh
sudo mn --switch ovsbr --test pingall
```
Luego continúe con los pasos 3-5 anteriores. Si se encuentra con errores, primero consulte las preguntas frecuentes, la documentación y los archivos de la lista de correo para ver si se ha visto antes algo parecido a su problema y si podría haber una posible solución. Si esas cosas no ayudan y todavía tienes problemas que no puedes resolver por tu cuenta (o con ayuda de Google :)), puedes solicitar ayuda en la amigable lista de correo mininet-discuss.

##### PROCEDIMIENTOS

1. **Ejecutar un comando de prueba con Mininet:**
    ```bash
     sudo mn --topo single, 4
     ```

2. **Obtener ayuda sobre los comandos disponibles en Mininet:**
    ```bash
     help
     ```

3. **Ver los nodos conectados en la red:**
    ```bash
     nodes
     ```

4. **Ver los puertos y enlaces de la red:**
    ```bash
     net
     ```

5. **Obtener detalles de todos los nodos:**
    ```bash
     dump
     ```

6. **Ver los procesos activos en un host específico (ejemplo: h1):**
    ```bash
     h1 ps -a
     ```

7. **Iniciar Mininet desde la terminal:**
    ```bash
     sudo mn
     ```

8. **Hacer ping entre dos nodos específicos (ejemplo: h1 a h2):**
    ```bash
     h1 ping -c 1 h2
     ```

9. **Hacer ping a todos los nodos de la red:**
     ```bash
      pingall
      ```

10. **Habilitar un enlace de un switch (ejemplo: s1):**
     ```bash
      link s1 up
      ```

11. **Deshabilitar un enlace de un switch (ejemplo: s1):**
     ```bash
      link s1 down
      ```

12. **Salir de Mininet:**
     ```bash
      exit
      ```

     **Link de los archivos desarrollados para el proyecto**
    ``https://drive.google.com/drive/folders/19767jDCuqMFYzvfF_G-OMuTHuslfdl1N?usp=sharing
