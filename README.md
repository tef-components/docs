# TEF Components

## What is it?

TEF Components is a UI Kit, aimed to use in Telefonica projects.
Although is an open source project, so we encorage you to use it anywhere!
And we would appreciate your contribution back to the project by filing issues and fixing bugs :)

We are using [less](http://lesscss.org/) to compile our CSS files.

Four flavours are provided for each branding in the company.
Please visit the following examples to preview all themes.

* [Telefonica](http://tef-components.github.io/theme_telefonica/index.html)
* [Movistar](http://tef-components.github.io/theme_movistar/index.html)
* [O2](http://tef-components.github.io/theme_o2/index.html)
* [vivo](http://tef-components.github.io/theme_vivo/index.html)

We also have a demo where you could switch brands and inspect breackpoints:

* [Breackpoint inspector](http://tef-components.github.io/tools/index.html)

See all components:

* [Components](http://tef-components.github.io/tools/components.html)

And all templates (components combined together):

* [Components](http://tef-components.github.io/tools/templates.html)


## Installation

Use [bower](http://bower.io) to install one of the themes:

```bash
bower install tef-components/theme_telefonica
```
In case you want to use other themes use:

* `theme_movistar`
* `theme_o2`
* `theme_vivo`

You will get the following file structure:

|-- bower_components
|   |-- [buttons](http://tef-components.github.io/buttons/index.html)
|   |-- [checkboxes](http://tef-components.github.io/checkboxes/index.html)
|   |-- [dropdowns](http://tef-components.github.io/dropdowns/index.html)
|   |-- [grid](http://tef-components.github.io/grid/index.html)
|   |-- [headers](http://tef-components.github.io/headers/index.html)
|   |-- [icons](http://tef-components.github.io/icons/fonts/icons.html)
|   |-- [inputs](http://tef-components.github.io/inputs/index.html)
|   |-- [lists](http://tef-components.github.io/lists/index.html)
|   |-- [modals](http://tef-components.github.io/modals/index.html)
|   |-- [radios](http://tef-components.github.io/radios/index.html)
|   |-- [sidebars](http://tef-components.github.io/sidebars/index.html)
|   |-- [tables](http://tef-components.github.io/tables/index.html)
|   |-- [tabs](http://tef-components.github.io/tabs/index.html)
|   |-- [theme_telefonica](http://tef-components.github.io/theme_telefonica/index.html)
|   |-- [toolbars](http://tef-components.github.io/toolbars/index.html)
|   |-- [tooltips](http://tef-components.github.io/tooltips/index.html)
|   |-- utils

* Most folders will contain a component (click on each name to get a preview).
* theme_telefonica folder, in that case, is were we will generate our styles.
* utils folder contain a set of mixins and resets (nothing to demo here).

## Usage

Browse your installed theme.
Those are the important files:

|-- buttons
|   |-- less
|   |   |-- buttons.less
.
.
.
|-- theme_yourthemename
|   |-- Gruntfile.js
|   |-- less
|   |   |-- theme.less
|   |   |-- variables.less


### Gruntfile.js

If you don't need the full set of components, you will be able to remove the unneeded ones by commenting the lines:

```json
less: {
  default: {
    files: {
      'css/components.telefonica.css': 'less/theme.less',
      'templates/variables.css': 'templates/variables.less',

      // components
      'css/components/buttons.css': 'less/buttons.less',
      ...

      // web components
      'css/web_components/tef_button.css': 'less/tef_button.less',
      ...
    }
  }
```

and the minified version:

```json
target: {
  files: {
    'css/components.telefonica.min.css': 'css/components.telefonica.css',

    // components
    'css/components/buttons.min.css': 'css/components/buttons.css',
    ...

    // web components
    'css/web_components/tef_button.min.css': 'css/web_components/tef_button.css',
    ...
  }
```

### theme.less

Same thing here. To exclude unneeded components, comment the lines:

// Components
@import '../../grid/less/grid.less';
@import '../../buttons/less/buttons.less';
@import '../../inputs/less/inputs.less';
@import '../../dropdowns/less/dropdowns.less';
...

### Compiling less

You will need [grunt](http://gruntjs.com/) installed.
Then run in your console:

```bash
  grunt
```
You'll be watching for changes in your LESS files and they'll be compiled into CSS.

### Let's edit!

Go an edit any property in a component (i.e: buttons/less/buttons.less)

Or modify a variable value (i.e: theme_telefonica/less/variables.less)

Then you will get a development and a minified file with all your selected components i.e: 

* theme_telefonica/css/components.telefonica.less
* theme_telefonica/css/components.telefonica.min.less


Enjoy!