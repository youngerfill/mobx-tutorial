mobx-tutorial
=============

The code from the mobx 10-minute tutorial.

https://mobx.js.org/getting-started.html

Using mobx with react
---------------------

Make sure npm and create-react-app are installed
::

    sudo pacman -Syu npm
    npm install -g create-react-app

Create a sample react app
::

    npx create-react-app hello-mobx
    cd hello-mobx

'Eject' the project
::

    npm run eject

Install mobx & mobx-react
::

   npm install mobx mobx-react

Install support for decorators
::

    npm i --save-dev @babel/plugin-proposal-class-properties @babel/plugin-proposal-decorators

Enable support for decorators. In 'package.json', look for this:
::

    "babel": {
        "presets": [
            "react-app"
        ]
    },

and change it into this:
::
    "babel": {
        "presets": [
            "react-app"
        ],
        "plugins": [
            [
                "@babel/plugin-proposal-decorators",
                {
                    "legacy": true
                }
            ],
            [
                "@babel/plugin-proposal-class-properties",
                {
                    "loose": true
                }
            ]
        ]
    },



