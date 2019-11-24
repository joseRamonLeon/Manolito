# Manolito
Controla a Manolito (<i>Kit 31313 de Lego Ev3 Mindstorms</i>) con <b>Alexa</b> desde cualquier dispositivo compatible de <b>Amazon</b>.

Este ejemplo nace gracias al gran trabajo de Documentación de <b>Lazauk</b> https://github.com/LazaUK/AlexaGadgetKit-LegoEV3 que me ha permitido avanzar de 0 a 100 para poder disfrutar con Manolito desde cualquier dispositivo compatible con <b>Alexa.</b> 

<p>También se ha usado el material que Amazon ha suministrado para el concurso de <a href="https://www.hackster.io/contests/alexa-lego-voice-challenge" target="_blank"><b>LEGO MINDSTORMS Voice Challenge</b></a>

Para poder usar este código necesitas varias cosas:

<ul>

<li><b>Tarjeta microSD</b>: En esta tarjeta implementaremos un sistema operativo compatible con el Ladrillo de Ev3 así como en BrickPi (RaspberryPi)

- <b>ev3Dev</b>. Es un sistema operativo basado en <b>Linux</b> que funciona tanto en los ladrillos de <b>LEGO® MINDSTORMS</b> EV3 como en una <b>Raspberry Pi</b> con asteroides gracias a <b>BrickPi</b>. 

    ¿Como lo consigo? ¡Muy fácil! en la web de <i>ev3Dev</i>: https://www.ev3dev.org/downloads/. También se puede conseguir directamente desde páginas de la web oficial de <b>Lego</b>, pero <b><i>¡ojo!</i></b> es una versión anterior. Funciona, pero la sincronización por Bluetooth no va muy fina y cuesta entender como hacerlo.
    
    Para sincronizar tu <b>Ev3</b> con <b>ev3Dev</b> con un <b>Mac</b>, lo tienes a continuación en video (incluiré la documentación en texto mas adelante...) 
    <div style="width: 100%; padding: 0; margin: 0 auto;">
    <span style="margin: 10px auto; text-align: center;"><a href="https://youtu.be/SSxdLdfKS5E" target="_blank" >
        <img border="0" alt="Como implementar EV3DEV en tu ladrillo de Lego EV3 Mindstorms (1ª parte: Descarga EV3DEV + MicroSD)" src="http://www.ytopic.es/ev3/videoev3devimagen1.jpg" width="260" height="182">
    </a>
    </span>
     <span style="margin: 10px auto; text-align: center;">
    <a href="https://youtu.be/h6alAdD6sWc" target="_blank">
        <img border="0" alt="Como implementar EV3DEV en tu ladrillo de Lego EV3 Mindstorms (2ª parte: Sincronización Bluetooth)" src="http://www.ytopic.es/ev3/videoev3devimagen2.jpg" width="260" height="182">
    </a>
    </span>
    <span style="margin: 10px auto; text-align: center;">
    <a href="https://youtu.be/2zy9iwp4Kgs" target="_blank">
        <img border="0" alt="Como implementar EV3DEV en tu brick de Lego EV3 (3ª parte: Controla ev3DEV con Visual Studio Code)" src="http://www.ytopic.es/ev3/videoev3devimagen3.jpg" width="260" height="182">
    </a> 
    </span>
    </div>
    
    Una vez que tenemos el ev3dev funcionando y conectado por wifi y por bluetooth a nuestro equipo, nos conectamos por SSH y lanzamos las dos siguientes órdenes:
    
<code>sudo apt-get update</code><br/>
<code>sudo apt install python3-pip</code>

<p>Si nos dá este error:</p>

<code>_bluetooth.error: (98, 'Address already in use')</code><br/>

Podemos lanzar las siguientes instrucciones:

<code>sudo netstat -nlp | grep 8069</code><br/>
<code>sudo kill -9 10869</code><br/>
</li>
<li><b>Kit 31313 de Lego Ev3 Mindstorms</b>: Puedes adquirirlo en <a href="https://www.amazon.es/s?k=lego+31313&__mk_es_ES=%C3%85M%C3%85%C5%BD%C3%95%C3%91&ref=nb_sb_noss_2" target="_blank"><b>Amazon</b></a>, en la tienda online de Lego, asi como en las tiendas de juguetería de tu pueblo o ciudad.</li>

<li><b>Dispositivo Amazon compatible con Alexa</b>: Puedes adquirir cualquiera de estos dispositvos en <a href="https://www.amazon.es/s?k=alexa" target="_blank"><b>Amazon</b></a>.</li>
<li><b>App Amazon Alexa</b>: Esta aplicación es gratuita, y podrás adquirila de forma gratuita desde tu App Store:
<ul>
<li>Android: Descargar App desde <a href="https://play.google.com/store/apps/details?id=com.amazon.dee.app&hl=es" target="_blank"><b>Google Play Store</b></a>.</li>
<li>IOS: Desdcargar App desde la <a href="https://apps.apple.com/us/app/amazon-alexa/id944011620" target="_blank"><b>App Store</b></a>.</li>
</li>
</ul>