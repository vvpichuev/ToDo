# Todo list
This is a project that is a simple task list implemented using Vue.js.
## Table of Contents
* Stack
* Installation
* Requirements
* Features
## Stack
* CSR
* [Vue JS](https://ru.vuejs.org/)
* [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
* [Vite](https://vitejs.dev/)
* [HTML](https://html.spec.whatwg.org/multipage/)
* [SCSS](https://sass-lang.com/)
* [GIT](https://www.git-scm.com/)
* [BEM](https://getbem.com/)
## Installation
#### To get up and running, follow these steps:
#### Clone repository
    git clone https://github.com/vvpichuev/ToDo.git
#### Install dependencies
    npm install
#### Run the project
    npm run dev
## Requirements
    node v20.12.0
## Features
The project is a simple task list with the ability to add, delete, and edit tasks.

## Projest practices
**Code style:** we use Prettier for code formatting.

Also we use the BEM SCSS system in the project, it's a component-based approach.

**Folders:**

The “accets” folder is used to store fonts, icons, images and styles.

The "page" folder is used to store pages components.

The “components” folder contain folders buttons, common, icons.

"buttons" - for all buttons components in projest.

"icons"  for all icons components.

"common" - for others components in this project.

**Components:**

**In this project we used the following components:**

MainPage- component of a whole todo page.
It stores information about created tasks and contains components such as TaskCard, TheTask and TheButton for interacting with the created task.
Also, using this component, we can search for tasks.

TaskCard - component for displaying tasks created by the user.

TheTask - an input field component that allows users to create items.

TheButton - a button component allows users to interact with an input field to add, update, and delete tasks.

TaskCard - component for displaying tasks created by the user.

BasketIcon, PenIcon, PlusIcon and SaveIcon - components for displaying svg pictures inside TheButton.
