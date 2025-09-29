# Architecture

This application is a mod of the [Neural Numbers Mini app](https://github.com/IMAGINARY/neural-numbers-mini).

It installs the base application source code, copies a series of extra files on top of it, and uses the
original application's build script to build the final application.

## Build process

The build process is started by the `build` action in the `package.json` file. It takes the
following steps (please check the file for potential updates):

- Remove the `dist` directory if it exists.
- Clone the base application source code into the `neural-numbers-mini` directory using git.
- Copy the contents of the `extras` directory into the `neural-numbers-mini` directory.
- Run `npm install` and `npm build` into the `neural-numbers-mini` directory to build the application.
- Copy `neural-numbers-mini/dist` into the `dist` directory.

