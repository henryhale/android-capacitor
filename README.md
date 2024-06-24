# android-capacitor

## Overview
This template is created to be a starting point for developing mobile
applications using web technologies.

>It uses [capacitorjs](https://capacitorjs.com) to generate an Android app in **debug mode**.

## Motivation
Today, there many web-based development environments like GitHub Codespaces, StackBlitz and more with GitHub intergration.
Anyone can build & test websites on the go, whenever they are.
You don't have to install anything. But you need a good internet connection.

To build Android apps, you need to set up quite a number of tools and most importantly of all, a good pc (8GB RAM, 8GB disk space and more).
Take a look at the recommended computer specifications on this page [here](https://developer.android.com/studio/install).

So if you are building something awesome but on a resource-constrained device or limited environment (internet cafe or school computer lab), here's a solution. 
Leverage GitHub Actions to build Android apps using [capacitorjs](https://capacitorjs.com). 
Download the app from GitHub Releases on mobile and enjoy :rocket:

## Usage
1. First of all, add a build script in your `package.json` file, for example `vite build` while using [vite](https://vitejs.dev). 

2. Secondly, edit the [capacitor.config.ts](./capacitor.config.ts) file.
Edit the config object to suit your project. The `webDir` key takes the folder in which your bundled files are located for example `dist`.

>In case you have no build step, add `"build": "echo no build"` under `scripts` in your `package.json` file. Make `webDir` in [capacitor.config.ts](./capacitor.config.ts) correspond to the folder in which your project files are located for example `src`.

3. Place the app icon in `resources/` folder and name it `icon.png`. It should be at least 1024x1024 in dimensions. For new projects, replace the existing file.

4. Ensure that your have the [.github/workflows/build.yml](.github/workflows/build.yml) file. You can rename it incase of naming collisions.

5. To generate the app;

   - Create a git new tag for example initial release with tag name `v0.0.1`, run

    ```sh
    git tag v0.0.1
    ```

   - Push the tag to GitHub
 
    ```sh
    git push origin v0.0.1
    ```

    This will trigger the workflow and generate your app in the GitHub Releases.

6. Repeat step 5 using a new tag every time you want to re-build the app.

7. Enjoy :rocket:

## Contributing
In case of any issue or bug, please open a new issue [here](https://github.com/henryhale/android-capacitor/issues/new).

## License

Released under [MIT License](./LICENSE.md)

Copyright &copy; 2024 [Henry Hale](https://github.com/henryhale)
