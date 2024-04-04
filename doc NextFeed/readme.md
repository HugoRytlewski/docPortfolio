


#  NEXTFEED  

> Nextfeed est développé en utilisant Vue.js, un framework JavaScript progressif pour la construction d'interfaces utilisateur. Il utilise également Symfony pour le back c'est un framework PHP 

<br>


# Fonctionnalités principales

<br>

## Flux RSS et articles

<br>

```javascript
setRssFeed(dataFeed: string, category: string, limit: boolean)
```
Cette fonction permet de récupérer les données d'un flux RSS, de les traiter et de les stocker dans la liste des articles. Les articles sont triés par date de publication.


```javascript
getHomeArticles(fluxRssList: any)
```
Cette fonction récupère les articles à partir d'une liste de flux RSS et les ajoute à la liste des articles. Elle est utilisée pour afficher les articles par défaut à l'accueil.

```javascript
incrementLimitArticles()
```
Cette fonction permet d'augmenter le nombre d'articles affichés lorsqu'un bouton "Charger plus" est cliqué.

```javascript
comparerArticles(a, b)
```
Cette fonction de comparaison est utilisée pour trier les articles par ordre décroissant en fonction de leur date de publication. 

<br>

## Flux préférés de l'utilisateur

<br>


```javascript
removeFluxPref(fluxpreffremove_id: string)
```
Cette fonction supprime un flux RSS des favoris de l'utilisateur.
```javascript
addAll(fluxRssId: any)
```
Cette fonction ajoute tous les flux RSS disponibles aux favoris de l'utilisateur.

```javascript
removeAll(fluxRssId: any)
```
Cette fonction supprime tous les flux RSS des favoris de l'utilisateur.

<br>

## Catégories
```javascript
loadCategory()
```
Cette fonction charge les articles en fonction de la catégorie sélectionnée par l'utilisateur.

<br>

`allCategory`: Cette variable  contient la liste de toutes les catégories disponibles.

`selectCategoryId`: Cette variable  stocke l'ID de la catégorie sélectionnée par l'utilisateur.

<br>

## Api

```javascript
const {data: allCategory} = await useAsyncData < any > (() => $fetch(`${apiUrl}/category`, {
        headers: {
            Authorization: `Bearer ${bearer.value}`,
        },
    }));
```
Cette Variable nous permet d'obtenir toutes les catégories présentes dans la base de données .

```javascript
const {data: fluxpreff,refresh} = await useAsyncData < any > (() => $fetch(`${apiUrl}/user/favorite`, {
        headers: {
            Authorization: `Bearer ${bearer.value}`,
        },
    }));    
```
Cette Variable nous permet d'obtenir tous les flux préféres de l'utilisateur.

```javascript
const {data: allRss} = await useAsyncData < any > (() => $fetch(`${apiUrl}/fluxrss`, {
        headers: {
            Authorization: `Bearer ${bearer.value}`,

        },
    }));  
```
Cette Variable nous permet d'obtenir tous les flux RSS présentes dans la base de données.

