# WP-Starter-Plugin
A starter plugin for WordPress.

This plugin provides the basic foundation upon which to build a plugin. It is built following modern coding standards.

Features:
* The plugin is 'namespaced'.
* A class autoloader loads classes without including files manually.
* Constants are created automatically from the plugin headers where possible.
* A function detects if the plugin is in debug mode. In that case, all of the assets are versioned from their file timestamp to bypass browser cache. Every time a file is saved the version changes and the file is refreshed.
* A basic composer file install PHP unit and a few dev tools.
* A Gulp file written for Gulp 4 provides the tools for the following.
     * Compile Sass to CSS.
     * Minification.
     * Image compression.
     * Transpile Javascript ES6 to ES5.
     * plugin packaging.

## Instructions to use Gulp

From the terminal, give the following commands
* **npm run start**: launches Gulp in development mode and watches files for changes. The following tasks are performed 
    * Sass is compiled to CSS but not minified.
    * JavaScript is transpiled from ES6 to ES5 but not minified.
    * Images are compressed. Original non compressed images must be under *src/images/*
    * A .pot file is generated and saved under the folder *languages*.
    * Opens the browser on a new URL and refreshes it automatically every time that a script changes.
* **npm run build**: launches Gulp in production mode. The following tasks are performed 
    * Sass is compiled to CSS and minified.
    * JavaScript is transpiled from ES6 to ES5 and minified.
    * Images are compressed. Original non compressed images must be under *src/images/*
    * A .pot file is generated and saved under the folder *languages*.
    * Creates the zip file of the plugin and saves it under the folder *bundled*