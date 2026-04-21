<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

# NEST TEMPLATE CON TYPEORM + POSTGRES Y DOCKER

1. Instalar dependencias
```
yarn
```

2. Copiar __.env.template__, renombrar a __.env__ y cambiar variables de entorno 

3. Cambiar el __container_name__ en __docker-compose.yaml__

4. Levantar database
```
docker compose up -d
```

5. Levantar aplicación 
```
yarn start:dev
```

## IMPORTANTE

Antes de cargar tu API a algún servidor como __Render__, cambiar la variable de entorno __STAGE__ a __prod__. También en __app.module.ts__ descomentar la línea ```// ssl: configService.get('STAGE') === 'prod',``` y borrar o comentar la línea ```ssl: false,```