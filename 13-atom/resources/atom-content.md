# Atom Module :atom:

Today, we will be creating our first atom plugin! First let’s see what is Atom. Atom is a free and open-source source code editor developed by GitHub designed with hackability and usability in mind. The editor is meant to be customized in every possible way. It is built on a Chromium browser with HTML, Javascript, CSS, and Node.js and has complete access to the standard developer console window in Chrome.

In this example, we will create a plugin that implements the basic functionality of a dictionary lookup. It will allow a user to search a word directly in the editor, by either highlighting the word or placing the cursor somewhere in the word.

## Install Atom

To get started building your first Atom Plugin, you must have Atom installed. If you do not already have it, go grab it for free from their website: ()[https://atom.io/]

If you are having any trouble navigate to this link for more information on installing : [Getting started - installing Atom ](http://flight-manual.atom.io/getting-started/sections/installing-atom/)

## Navigating and customizing Atom

Now that we have Atom installed let’s get familiar with the editor and configure it.

### Useful terms

The following terms may be used often throughout this module, so let’s make sure we understand them before continuing.

**Command Palette** - The command palette is a super useful search command that will let you do just about any major task in Atom. It’s a search driven-menu, saving you time on clicking around the application to find something.  Let’s remember we can initiative the command palette by `Cmd+Shift+P`

**Keybinding** - A keybinding is the mapping of a key combination. A key combination is one such like the command palette one `Cmd+Shift+P` or it could be something like some like `Ctrl+Enter`.

**Panel** - A piece of the Atom UI that is outside the editor space.

**Pane** - A visual component of the editor. Each panel can hold multiple pane items. An Atom window has at least one pane.

**Package** = Plugin

More useful terms found here: [Atom Flight Manual - Glossary](http://flight-manual.atom.io/resources/sections/glossary/)

### Customizing

Atom has a number of settings and preferences you can modify in the Settings View. To get to the Setting View you can either get there by:


  - A) By the menu bar, `Atom > Preferences`
  - B) By using the Command Palette and type `settings-view:open`
  - C) By the keybinding `CMD+``

**Changing the Theme**
  - Navigate to Atom > Preferences
  - Open the Themes tab
  - Search the themes and cluck the blue install button

You can create your own custom theme by following the steps [here](http://flight-manual.atom.io/hacking-atom/sections/creating-a-theme/).

**Specify your whitespace and wrapping preferences**

  - Navigate to Atom > Preferences
  - Open the Editor tab
  - Select the settings you prefer for whitespace and wrapping

**Install Plugins**

  - Navigate to Atom > Preferences
  - Open the Install tab
  - Install pre-built plugins.

## Creating a plugin

### Package Structure

Atom stores all its plugins within the atom folder, .atom. It is usually located at ``\Users\user-name\.atom` unless you placed it somewhere else upon install. Within the atom folder, there is a subfolder called packages. Which, as you may have guessed, is where all the packages can be found. Note every package has its own folder.

The first step is to create a package for the plugin. I will create a folder called `kims-dictionary-plugin`.

Depending on the type of package you want to build, you may not require all these folders (or you may require additional ones). Nonetheless, this gives you a good breakdown of what a basic package structure looks in Atom:

```my-first-plugin/
├─ keymaps/
├─ lib/
├─ menus/
├─ spec/
├─ styles/
└─ package.json
```

Now let’s take a look at some of these folders and files.

#### package.json

For our package to be recognized by Atom, we need to add a .json file: `package.json`. This json file will contain metadata about the package and is based off of the regular Node `package.json` keys (https://docs.npmjs.com/files/package.json).

A general structure and important keys to implement are as follows:

```json
{
  "name": "my-first-plugin",
  "main": "./lib/my-first-plugin",
  "version": "0.0.0",
  "description": "This is my first Atom plugin that will do magic.",
  "engines": {
    "atom": ">=1.0.0 <2.0.0"
  },
  "dependencies": {},
  "repository": {
    "type": "git",
    "url": "https://github.com/kim-codes/my-first-plugin.git"
  },
  "bugs": {
    "url": "https://github.com/kim-codes/my-first--plugin/issues"
  },
  "activationCommands": {
    "atom-workspace": "first-atom-plugin:toggle"
  },
  "license": "MIT",
}
```

[Link to gist ](https://gist.github.com/kim-codes/ce8f510250876530d9e6b3070514884f)

##### Keys explained

- `name` is the name of the package
- `main` is the location of entry point to the plugin, kind of like main *(usually located in the lib folder named as plugin-name.coffee.. and if the `main` key is not in your `package.json` file, Atom will default to looking for an `index.coffee` or `index.js` file)*
- `version` is the version number of the package, and must follow the convention: `major.minor.bug` *(note you could indicate `0.0.0` for now)*
- `description` informs others about what the package does
- `engines` indicates the minimal required version of Atom
- `dependencies` indicates other packages needed
- `repository` is a URL indicating where the public repository is located
- `bugs` is a URL where others can report issues
- `license` indicates the license

##### Some other keys

- `styles`: an Array of Strings describing the order in which your style sheets need to be loaded *(if not specified they will be loaded alphabetically)*
- `keymaps`: an Array of Strings i describing the order in which your key mappings need to be loaded *(if not specified they will be loaded alphabetically)*
- `menus`: an Array of Strings describing the order in which your menu mappings need to be loaded *(if not specified they will be loaded alphabetically)*

There are many other keys, however for now this is as much as we need to create our plugin.

Now that your package has a valid `package.json` file, Atom can recognize it and load it. However, it’s totally useless right now. So, it’s time to make it useful by giving it some features!

***Note***: *Code snippets will be written mainly in EcmaScript standard for JavaScript.*

### Package logic

Our package logic can be found at *plugin-name.coffee/.js*.

- ***your-plugin.coffee/your-plugin.js*** handles the logic of the plugin and can be viewed as the main package file
- ***your-plugin-view.coffee/.js*** handles the UI elements of the package

In your main, you usually have the following 3 methods: `activate`, `deactivate`, `serialize`

- The `deactivate` method destroys the various class instances created
- The `serialize` method passes on the serialization to the View class
- The `activate` method is what is executed when your plugin is loaded and instantiates the view class.

Here is an example skeleton for *my-first-plugin.js*:

```javascript
'use babel';

import NewPackageView from './new-package-view';
import { CompositeDisposable } from 'atom';

export default {

  newPackageView: null,
  modalPanel: null,
  subscriptions: null,

  activate(state) {
    this.newPackageView = new NewPackageView(state.newPackageViewState);
    this.modalPanel = atom.workspace.addModalPanel({
      item: this.newPackageView.getElement(),
      visible: false
    });

    // Events subscribed to in atom's system can be easily cleaned up with a CompositeDisposable
    this.subscriptions = new CompositeDisposable();

    // Register command that toggles this view
    this.subscriptions.add(atom.commands.add('atom-workspace', {
      'new-package:toggle': () => this.toggle()
    }));
  },

  deactivate() {
    this.modalPanel.destroy();
    this.subscriptions.dispose();
    this.newPackageView.destroy();
  },

  serialize() {
    return {
      newPackageViewState: this.newPackageView.serialize()
    };
  },

  toggle() {
    console.log('NewPackage was toggled!');
    return (
      this.modalPanel.isVisible() ?
      this.modalPanel.hide() :
      this.modalPanel.show()
    );
  }

};
```

[gist here](https://gist.github.com/kim-codes/9b1d797a28ff69e5e40406d5ae41a3da)

##### Explanation:
 *Commands* are events triggered by a user and packages can subscribe to commands. By subscribing, they can execute code in response to the event (a.k.a the command) that was triggered by the user. When we want to subscribe to multiple events that’s where the *[CompositeDisposable](https://msdn.microsoft.com/en-us/library/system.reactive.disposables.compositedisposable%28v=vs.103%29.aspx)* class comes in handy, but we won’t get into any specifics right now.

The `toggle` method is what gets called every time the user wants to run the package *(‘toggles the package’)*. It is invoked either by the menu item or a hotkey.

Here is an example skeleton for *my-first-plugin-view.js*:

```javascript
'use babel';

export default class NewPackageView {

  constructor(serializedState) {
    // Create root element
    this.element = document.createElement('div');
    this.element.classList.add('new-package');

    // Create message element
    const message = document.createElement('div');
    message.textContent = 'The NewPackage package is Alive! It\'s ALIVE!';
    message.classList.add('message');
    this.element.appendChild(message);
  }

  // Returns an object that can be retrieved when package is activated
  serialize() {}

  // Tear down any state and detach
  destroy() {
    this.element.remove();
  }

  getElement() {
    return this.element;
  }

}
```
[gist here](https://gist.github.com/kim-codes/8e3864173c23b200257de401cb04758b)

### Adding Code

So let’s dive in. First, we want to grab the word we want to lookup.

```javascript
editor = atom.workspace.getActiveTextEditor();
wordToSearch = editor.getSelectedText();
if(!wordToSearch){
  wordToSearch = editor.getWordUnderCursor();
}
```
[gist here](https://gist.github.com/kim-codes/7c2e5e9674a2aab41d518a7ecd906173)

We do this by creating an reference to the current state of the editor and finding the word that is either selected or where the user’s cursor is. We will add this snippet to our toggle method. Also, don’t forget to define the variable wordToSearch:

``wordToSearch: null,``

Next, we will add a method in our view to update itself.

```javascript
setElement(){
  this.element.children[0].textContent =  'Word: ' + wordToSearch;
}
```

[gist here](https://gist.github.com/kim-codes/51011b1b396163a901603e246eddcca9)

In our view, the root element only had one child (index starts at 0) and we want to update it’s text to reflect the word we just grabbed from the editor. Afterwards, we will need to go back into our logic and add the following line:

``this.MyFirstPluginView.setElement();``

With this line, we will call the setElement method we created which will update the element with our word.

At this point, you may notice that as you make changes to your package the changes aren’t reflected right away. You need to reload Atom, either by closing and re-opening or hitting *View > Developer > Reload*. This will ensure Atom runs the latest version of our source code.

Therefore, reload Atom and toggle the plugin. The panel now displays the word where the cursor is focused or highlighted.

### Atom flow

Let’s take a moment to look at the flow of our package in Atom:

- First, Atom starts up.
- Second, Atom begins loading packages.
- When Atom reaches our plugin it reads the `package.json`
- Atom is going to load in your keymaps, menus, styles and main
- At some point in time while the user is using Atom, uur package gets toggled `your-plugin:toggle`
- Once our plugin is toggled, Atom executes the `activate` method. The `activate` method sets up the UI by creating a hidden view and then executes `your-pluggin:toggle` which reveals the hidden view!
- Lastly, when toggle is called again Atom executes the toggle command again which hides the view.

### Connecting to an API

Now, we will need to connect our plugin with some sort of Dictionary API. For this tutorial I have chosen the [Oxford Dictionaries](https://developer.oxforddictionaries.com/), but feel free to use any Dictionary API that your comfortable with.

A shortcut to put through the request to the API and process the results for the sake of this tutorial:

```javascript
data = null;
xhr = null;
xhr = new XMLHttpRequest();
xhr.withCredentials = true;
xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    jsonText = JSON.parse(xhr.responseText);
    wordDefinition = jsonText.results[0].lexicalEntries[0].entries[0].senses[0].subsenses[0].definitions[0];
    console.log(jsonText.results[0].lexicalEntries[0].entries[0].senses[0].subsenses[0].definitions[0]);
  }
});
xhr.open("GET", "https://od-api.oxforddictionaries.com:443/api/v1/entries/en/"+wordToSearch+'/definitions', false);
xhr.setRequestHeader("accept", "application/json");
xhr.setRequestHeader("app_id", "xxxx");
xhr.setRequestHeader("app_key", "xxxx");
xhr.send(data);
```

[gist here](https://gist.github.com/kim-codes/3287c5b82e846676836298044c3ee2a1)

We send an XMLHttpRequest to the API by providing my credentials and adding an event listener to the request. This event listener, when it receives a notification that transactions has been completed, it will parse the results (which is in JSON format). The results I get back contain a ton of information, however all we need for the sake of this tutorial is the first definition returned.

For now, we will place this logic in our toggle method. Don’t forget to define our variable that stores the definition:

``wordDefinition: null,``

We will need to update our view to reflect the new changes we made.

```javascript
// Updates with new word and definition
setElements() {
  this.element.children[1].textContent =  'Word: ' + wordToSearch;
  this.element.children[2].textContent =  ' is defined as : ' + wordDefinition;
}
```

[gist here](https://gist.github.com/kim-codes/af38b0e0862a21a511c33868744965d4#file-moedifiedsetelement-js)

Reload atom and toggle again… Volià!

We made our first plugin. Head over to the styles folder and add some CSS to make it look pretty!
