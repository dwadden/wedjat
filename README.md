# Wedjat

Wedjat was created in the hopes of allowing completely locked in individuals to
communicate with a computer.

## Installation

### Prerequisites
Wedjat requires that the following software be installed:

- [Git](https://git-scm.com/)
- [Node.js](http://nodejs.org/)
- [npm](http://npmjs.org/)

### Package dependencies
Clone the repository. Change to the installation directory and execute the
following to install the requisite packages from npm:

```
npm install
```

Wedjat runs on Github's [Electron](http://electron.atom.io/). You may install it
globally using:

```
npm install -g electron-prebuilt
```

### Running the program

If Electron is installed globally, navigate to the Wedjat home directory and
enter:

```
electron .
```

The program will launch. If Electron is installed locally, locate the executable
and invoke in the same fashion.

## Usage

### Interaction Concepts
Wedjat consists of a series of menus. Each menu contains buttons. When a button
is selected, it triggers an action. Common actions include writing letters to
the text buffer and opening other menus.

Wedjat recognizes two gestures from the user. For the original user, these two
gestures are two types of gazes: an upward gaze and an extended upward gaze
(lasting 2 seconds or more).

The user issues input by listening as the program scans through available menu
options, and performing a gesture when the desired option is spoken. When
launched, the program does not scan; it awaits an extended upward gaze from the
user to start. Once started, a short gaze indicates a selection, while an
extended gaze indicates a cancellation.

### Simulating interactions with the keyboard
Developers and assistants may wish to simulate interactions with the program
without actually gazing. The keyboard may be used for this purpose. Pressing the
letter "e" fires an extended gaze event, while pressing "g" fires a short gaze
event.

### Controlling Scan Speed
A slider at the bottom of the application window allows an assistant to adjust
the rate at which the program scans through buttons.

## Documentation

Comments in the code follow [JSDoc](http://usejsdoc.org/) syntax. You may
generate documentation by entering the following at the command line, from the
installation directory:

```
jsdoc wedjat.js
```

For information, see the JSDoc documentation.
