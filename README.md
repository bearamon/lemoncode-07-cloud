## Ejercicio 1:

Ejecutando el siguiente comando se realiza el despliegue manual (link: https://github.com/bearamon/lemoncode-07-cloud/actions/runs/6920116511)

```
npm run deploy -- -r git@github.com:bearamon/lemoncode-07-cloud.git
```

## Ejercicio 2:

En el repositorio de Github > Settings > Environments, he cambiado la regla para el deploy para que se ejecute cuando se haga una rama release.
Además, he añadido una Secret Key.
En la configuración personal > Settings > Developer settings > Personal access tokens, he añadido un nuevo token y el nombre es el que usaré para mi step de Deploy.
