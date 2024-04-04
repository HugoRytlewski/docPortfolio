# Doc-Front-End NextEvents

# Language

- [English](#english)
- [Francais](#français)

## English

NextEvents is an online platform for managing and planning internal events (meetups, workshops, training, etc...), as well as managing participation.

## Build Projet

To build the project, navigate to the `/front` directory and run the following commands:

```bash
npm install
npm run dev
```

# Technologies Used

## Nuxt.js (3)

Nuxt is a server-side rendering framework built on Vue.js. The framework is presented as a "meta-framework for creating universal applications".

## Tailwind css

Tailwind CSS is an open-source CSS framework. The main feature of this library is, unlike other CSS frameworks like Bootstrap, it does not provide a series of predefined classes for elements such as buttons or tables.

## Figma

- Design: [View design on Figma](https://www.figma.com/file/tIajBP8lOIEacBDZ16Qf3G/NEXTEVENTS?type=design&node-id=0-1&mode=design&t=23craAaCjUF8d8LA-0)
- Workflow: [View workflow on Figma](https://www.figma.com/file/VxD04PtuoNOtTc0JwKEvQs/NEXTEVENTS---WORKFLOW?type=whiteboard&node-id=0-1&t=mRwIlfjwEPleb8Mi-0)

# Project Structure

<img src="Arborescence.png" alt="image" width="300" height="auto">

## Components

<img src="Components.png" alt="image" width="300" height="auto">

Nuxt automatically imports all components from this directory.

### Box

<img src="box.png" alt="image" width="300" height="auto">

This folder contains all the components that are box, tags.

### Forms

<img src="form.png" alt="image" width="300" height="auto">

This folder contains all the components that are inputs.

### Layouts

<img src="layouts.png" alt="image" width="300" height="auto">

Layouts are components that define the basic structure of a page. They are used to organize common elements such as headers, footers, and sidebars, which are present on multiple pages.

## Composables

<img src="composables.png" alt="image" width="300" height="auto">

In the context of Vue applications, a "composable" is a function that leverages Vue's composition API to encapsulate and reuse stateful logic. It involves writing the function only once to call it in our views.

### `useAuth.ts`

This function provides authentication features. It allows you to connect with Google, log out, and get information about the logged-in user.

### `useAuthUser.ts`

This function is used to add and read user data in the Nuxt.js state (`useState`).

### `useDaysJs.ts`

This function is a date manipulation utility. It allows you to convert a date to the format`DD/MM/YYYY à HH:mm`.

### `useForm.ts`

This function is a form management utility. It allows you to retrieve all the fields of a form and return them as JSON.

### `useNotyf.ts`

This function is a notification utility. It allows you to display a green (1), red (2), or orange (3) notification.

### `useScrollFixed.ts`

This function is a scroll management utility. It allows you to block the page scroll when a modal window is open, and close this modal window by pressing the Esc key on the keyboard. ```

## Français

NextEvents est une plateforme en ligne de gestion et de planification d’évènements internes (meetup, workshop, formation, etc…), ainsi que de gestion de participation

## Construction du Projet

Pour construire le projet, naviguez vers le répertoire `/front` et exécutez les commandes suivantes:

```bash
npm install
npm run dev
```

# Technologies utilisées

## Nuxt.js (3)

Nuxt est un framework de rendu côté serveur construit sur Vue.js. Le framework est présenté comme un « meta-framework pour créer des applications universelles »

## Tailwind css

Tailwind CSS est un framework CSS open source. La fonctionnalité principale de cette bibliothèque est, contrairement à d'autres frameworks CSS comme Bootstrap, qu'elle ne procure pas une série de classes prédéfinies pour des éléments tels que des boutons ou des tables

## Figma

- Design: [Voir le design sur Figma](https://www.figma.com/file/tIajBP8lOIEacBDZ16Qf3G/NEXTEVENTS?type=design&node-id=0-1&mode=design&t=23craAaCjUF8d8LA-0)
- Workflow: [Voir le workflow sur Figma](https://www.figma.com/file/VxD04PtuoNOtTc0JwKEvQs/NEXTEVENTS---WORKFLOW?type=whiteboard&node-id=0-1&t=mRwIlfjwEPleb8Mi-0)

# Arborescence du projet

<img src="Arborescence.png" alt="image" width="250" height="auto">

## Components

<img src="Components.png" alt="image" width="250" height="auto">

Nuxt importe automatiquement tous les composants de ce répertoire.

### Box

<img src="box.png" alt="image" width="250" height="auto">

Ce dossier contient tous les components qui sont des boxs , tags

### Forms

<img src="form.png" alt="image" width="250" height="auto">

Ce dossier contient tous les components qui sont des inputs

### Layouts

<img src="layouts.png" alt="image" width="250" height="auto">

Les layouts sont des composants qui définissent la structure de base d'une page. Ils sont utilisés pour organiser des éléments communs tels que les en-têtes, les pieds de page et les barres latérales, qui sont présents sur plusieurs pages.

## Composables

<img src="composables.png" alt="image" width="250" height="auto">

Dans le contexte des applications Vue, un « composable » est une fonction qui
exploite l'API de composition de Vue pour encapsuler et réutiliser la logique avec état. Elle consiste a écrire qu'une seule fois la fonction afin de l'appeler dans nos vues .

### `useAuth.ts`

Cette fonction offre des fonctionnalités d'authentification. Elle permet de se connecter avec Google, de se déconnecter, et d'obtenir des informations sur l'utilisateur connecté.

### `useAuthUser.ts`

Cette fonction est utilisée pour ajouter et lire les données de l'utilisateur dans l'état de Nuxt.js (`useState`).

### `useDaysJs.ts`

Cette fonction est un utilitaire de manipulation de dates. Elle permet de convertir une date en format `DD/MM/YYYY à HH:mm`.

### `useForm.ts`

Cette fonction est un utilitaire de gestion de formulaires. Elle permet de récupérer tous les champs d'un formulaire et de les renvoyer sous forme de JSON.

### `useNotyf.ts`

Cette fonction est un utilitaire de notifications. Elle permet d'afficher une notification de couleur verte (1), rouge (2) ou orange (3).

### `useScrollFixed.ts`

Cette fonction est un utilitaire de gestion du défilement. Elle permet de bloquer le défilement de la page lorsqu'une fenêtre modale est ouverte, et de fermer cette fenêtre modale en appuyant sur la touche Echap du clavier.
