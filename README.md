# Nest CheatSheet
![border](./assets/line/border_deco_rt.png)

<!-- Main image  -->

![border](./assets/img/Nest_cheatsheet.png)


```
$ npm install -g @nestjs/cli
nest new name-app
```


# Sommaire

- [Le main](#le-main)
- [App.module](#appmodule)

# Navigation

- [Benchmark SGBDR](./doc/benchmark-sgbdr.md)

![border](./assets/line/line-pink-point_l.png)

# Premiers pas 

## le Main

- L'application commence dans le main , on peut créer à partir de ce main en quelques lignes de code un serveur qui écoute sur le port 3000

- et nous voyons les lignes suivantes dans le main car nest encoruage à créer des modules  

```
import { AppModule } from './app.module';
```
## App.module

- ainsi avec la logique **app module** nous allosn créer tout un tas de models pour répondre aux besoin de notre applciation; ainsi si nous avons un module 

- pour gérer l'auth on crée un module user 
- créer des clients on crée un module customer 
- un module pour les produits on crée un module product etc .. 
- Nous remarquons que nous appelons aussi un controller


```
import { AppController } from './app.controller';
```


### Controller 

- le controlleur est le composant de notre application
- il écoute les requetes entrantes pour **renvoyer une reponse**
- SRP single responsability pattern 
- grace au **decorateur controlleur** la classe AppController devient un controlleur  

```ts
@Controller()
export class AppController {
  constructor(private readonly appService: AppService) {}
```


### Service 

- Il fournit les focntionnalités au controlleur 





<a href="#sommaire">
<img src="assets/button/back_to_top.png" alt="Home page" style="width: 150px; height: auto;">
</a>

![border](./assets/line/line-teal-point_l.png)

![border](./assets/line/border_deco_rt.png)
