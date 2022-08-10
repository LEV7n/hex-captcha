Use `npm run test` for getting immediately result

If you have problem with canvas.node compilation - use instruction from [stackoverflow](https://stackoverflow.com/a/52796884/7835958)

1. Require all dependencies you need in the `main.js` file that is run by electron. (this seemed to be the first important part for me)
2. Run `npm i -D electron-rebuild` to add the [electron-rebuild](https://github.com/electron/electron-rebuild) package
3. Remove the `node-modules` folder, as well as the `packages-lock.json` file.
4. Run `npm i` to install all modules.
5. Run `./node_modules/.bin/electron-rebuild` (`.\node_modules\.bin\electron-rebuild.cmd` for Windows) to rebuild everything

It is very important to run `./node_modules/.bin/electron-rebuild` directly after npm i otherwise it did not work on my mac.