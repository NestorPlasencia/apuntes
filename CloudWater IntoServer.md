
# Visualizar mqtt #

##inresa al servidor
ingresa colocando el siguiente comando
```
ssh root@45.55.130.79
```

vamos a la raiz de mqtt
```
cd /var/www/mqtt
```

aqui tenemos todos los proyectos iot
```
ls
```

##Datos pm2
tenemos tres servidores endemoniados donde(0,1,2) es un id
pm2 0 -> web
pm2 1 -> mqtt
pm2 2 -> api

para mas informacion
```
pm2 info 0
pm2 info 1
pm2 info 2
```

Cuando realizamos cambios o volver a correr algun servidor con su id
```
pm2 restart id
```

o para los tres a al vez
```
pm2 restart server
```

para detener un servidor endemoniado
```
pm2 stop id
```

##visualizamos

ingresamos a iotmqtt
```
cd iotmqtt
```

detenemos pm2 de mqtt
```
pm2 stop 1
```

y corremos el servidor en su version de desarrollo
```
npm run dev
```

al finalizar volvemos a endemoniar el servidor
```
pm2 restart 1
```



