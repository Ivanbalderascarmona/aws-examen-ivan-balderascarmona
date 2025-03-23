# Paso 1: Crear una VPC.
1. Configurar la VPC y crearla.
   <img src="./images/img1.png" alt="img1"/>

2. Crear dos subredes.
   1. Subred linux:
      <img src="./images/img2.png" alt="img2"/>
      
    2. Subred Windows:
      <img src="./images/img3.png" alt="img3"/>
3. Crear una Internet Gateway asociada a la VPC.
   1. Crear la Gateway:
      <img src="./images/img4.png" alt="img4"/>
   
   2. Asignar la VPC a la Gateway:
      <img src="./images/img5.png" alt="img5"/>

4. Añade una regla en la tabla de rutas (0.0.0.0/0) hacia la Gateway.
      1. Crear tabla de enrutamiento
         <img src="./images/img6.png" alt="img6"/>
         
      2. Añadir una regla en la tabla de rutas (0.0.0.0/0) hacia la Gateway:
         <img src="./images/img7.png" alt="img7"/>

# Paso 2: Crear una instancia EC2.
1. Instancia EC2 Windows:
   1. Nombre y sistema (Windows Server 2022).
      <img src="./images/img8.png" alt="img8"/>

   2. Tipo de instancia (t3.medium) y par de claves.
      <img src="./images/img9.png" alt="img9"/>

   3. Grupo de seguridad Entrante.
      <img src="./images/img10.png" alt="img10"/>

3. Instancia EC2 Linux:
   1. Nombre y sistema (Ubuntu 22.04).
      <img src="./images/img11.png" alt="img11"/>

   2. Tipo de instancia y par de claves.
      <img src="./images/img12.png" alt="img12"/>

   3. Grupo de seguridad Entrante.
      <img src="./images/img13.png" alt="img13"/>

# Instalación y despliegue web
1. Linux:
   1. Comando 
   ~~~
   sudo apt update
   ~~~
   <img src="./images/img14.jpg" alt="img14"/>

   2. Comando
   ~~~
   sudo apt install nodejs npm -y
   ~~~
   <img src="./images/img15.jpg" alt="img15"/>

   3. Comando
   ~~~
   sudo npm install -g vite serve
   ~~~
   <img src="./images/img16.jpg" alt="img16"/>

   4. Comando
   ~~~
   mkdir web-ivan-balderas && cd web-ivan-balderas
   ~~~
   <img src="./images/img17.jpg" alt="img17"/>

   5. Comando
   ~~~
   npm init vite@latest .
   ~~~
   <img src="./images/img18.jpg" alt="img18"/>

   6. Comando
   ~~~
   npm install
   ~~~
   <img src="./images/img19.jpg" alt="img19"/>

   7. Comando
   ~~~
   npm run build
   ~~~
   <img src="./images/img20.jpg" alt="img20"/>

   8. Comando
   ~~~
   serve -s dist -l 5173
   ~~~
   <img src="./images/img21.jpg" alt="img21"/>

   9. Foto de la página web
   <img src="./images/img22.jpg" alt="img22"/>

# Security Groups
1. Linux
   1. Entrada:
      <img src="./images/img23.png" alt="img23"/>

   2. Salida:

      <img src="./images/img24.png" alt="img24"/>

2. Windows
   1. Entrada:
      <img src="./images/img25.png" alt="img25"/>

   2. Salida:
      <img src="./images/img26.png" alt="img26"/>

# Pull Request

   1. He realizado el Pull Request con Álvaro, le he modificado el index.html.
   <img src="./images/img27.png" alt="img27"/>

   2. He enviado el Pull Request con los detalles y cambios en la descripción de este Pull Request.
   <img src="./images/img28.png" alt="img28"/>