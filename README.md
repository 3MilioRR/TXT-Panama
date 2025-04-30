# TXT-Panama
Jornadas STIC de Panamá: Instrucciones para montar la plataforma de ejercicios TTX

# Antes de empezar.
La plataforma que se ofrece, es una instancia del producto OpenEX, un software open-source desarrollado por la firma Filigran (https://filigran.io).
OpenEX ya no existe y en su lugar, Filgran desarrolla OpenBAS, un producto más evolucionado, más potente y como su nombre indica, con capacidades de 'Breach and Attack Simulation - BAS'
El problema es que OpenBAS requiere de unas capacidades hardware más elevadas que no le permite ejecutarse en un portatil o un ordenador de sobremesa. Además se requieren amplios conociminetos de integración de aplicaciones como MITRE-CALDERA, Red Canary, ...
Sin embargo, OpenEX es completamente funcional y es perfecto para para usuarios con ciertas limitaciones técnicas y/o económicas

<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">Contenido de este repositorio</h2></div>
<ul dir="auto">
<li>Enlace para la descarga de la maquina virtual (ficero .OVA)</li>
<li>Fichero env.txt, donde se indican los parámetros a modificar</li>
<li>Instrucciones</li>
</ul>

# Instrucciones

<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto">Usuarios y password</h2></div>
<ul dir="auto">
<li>De la máqina virtual: root / openex</li>
<li>De la aplicación web: DIREX@acme.es / abc123</li>
<li>Navaja Negra - Son cosas de la E.D.A.D.</li>
</ul>

#Configuración:

Accedemos como root a la maquina
modificamos el archivo .env localizado en /root
ejecutamos <code> ls -la </code> para mostrarlo
editamos con <code> nano .env </code>

ejecutar este comando en la misma ruta que aparece el archivo docker-compose.yml
docker compose stop (parar maquina NO BORRAR)
docekr compose down (parar y borrar)
docker compose up -d (levantar las maquinas desde 0)

si realizas una modificacion del archivo .env
docker compose up -d --force-recreate (solo coge las modificaciones. No se pierde la BD)

para ver los log
docker logs -f
docker logs -f openexhq
