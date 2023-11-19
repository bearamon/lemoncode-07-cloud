## Ejercicio 1:

Ejecutando el siguiente comando se realiza el despliegue manual (link: https://github.com/bearamon/lemoncode-07-cloud/actions/runs/6920116511)

```
npm run deploy -- -r git@github.com:bearamon/lemoncode-07-cloud.git
```

## Ejercicio 2:

En el repositorio de Github > Settings > Environments, he cambiado la regla para el deploy para que se ejecute cuando se haga una rama release.
Además, he añadido una Secret Key.
En la configuración personal > Settings > Developer settings > Personal access tokens, he añadido un nuevo token.
Luego en el paso de Deploy he usado esa key:
```
- name: Deploy
        run: |
          git remote set-url origin https://git:${GITHUB_TOKEN}@github.com/bearm23/lemoncode-07-cloud.git
          npm run deploy -u "github-actions-bot <support+actions@github.com>"
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
Otro paso necesario para que funcione y no de 403 el enlace a Github, es ir a las Settings del repositorio > Actions > General > Workflow permissions > Check Read and write permissions.