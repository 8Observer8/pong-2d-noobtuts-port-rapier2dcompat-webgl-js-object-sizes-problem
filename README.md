[Solution, but the local coordinate axes become very small and almost invisible.](https://github.com/dimforge/rapier.js/issues/240#issuecomment-1641733378)

[GitHub repository.](https://github.com/8Observer8/pong-2d-noobtuts-port-rapier2dcompat-webgl-js-object-sizes-problem) This repository contains my step-by-step instruction in README that shows how to build it with Rollup for debug and release modes. The release mode uses `uglify-js`. I use `importmap` to make bundles with Rollup. This allows me to simply copy files to Playgrounds and save space on my laptop because I don’t have to install NPM packages for every example.

Playgrounds:

- PlayCode: https://playcode.io/1537433
- Plunker: https://plnkr.co/edit/0nL5CioB7vbrxBbw?preview
- Glitch: https://glitch.com/edit/#!/faint-polyester-fascinator

Instructions for building and running the project in debug and release:

- Install these packages globally with the command:

> npm i -g http-server rollup uglify-js

- Run http-server in the project directory:

> http-server -c-1

Note. The `-c-1` key allows you to disable caching.

- Start development mode with the following command:

> npm run dev

Note. Rollup will automatically keep track of saving changes to files and build a new index.js file ready for debugging. You can debug your project step by step in the browser by setting breakpoints.

- Go to the browser and type the address: localhost:8080/index.html

- Create a compressed file ready for publishing. Stop development mode, for example, with this command Ctrl + C in CMD, if it was launched before and enter the command:

> npm run release

Note. After this command, Rollup will create a compressed index.js file. Compression is done using the uglify-js package.
