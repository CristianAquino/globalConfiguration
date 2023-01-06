# Pasos configuracion husky

## [Usando husky](https://typicode.github.io/husky/#/)

husky para ejecutar automaticamente git hooks(scripts) antes o despues de realizar un commit

lint-staged se usa para que se revicen solo los ficheros que se modificaron y anadieron al repositorio

- Realizamos la instalacion:

  - `npm i husky -D`
  - `npx i lint-staged -D`
  - creamos un fichero para el lint `.lintstagedrc` con la siguiente configuracion
    ![](img/lintstage.png)
  - agreamos un script al package.json mediante `npm set-script prepare 'husky install'` o escribirlo directamente como
    ![](img/prepare.png)
  - ejecutamos mediante `npm run prepare` e instalara los hooks en la carpeta husky

#

- Para crear un pre hook:
  - ejecutamos `npx husky add .husky/pre-commit "npx lint-staged"`
