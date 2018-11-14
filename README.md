# Electron Webview Focus Issue.

Calling `.focus()` on a webview does not properly transfer focus in Electron 3.

## Reproduction

Start this demo with electron version 2.0.5 to see how things are supposed to work.

```
npm install
npm start
```

Put you cursor in the text input in child1.html. Type something and press enter. The text is transfered to child2.html with the cursor focused on child2.html's text input. **This is the correct and exprected behavior**.

Change the electron version in package.json to 3.0.9 (or check out the branch "bug").

```
git checkout bug
npm install
npm start
```

Do the same thing and notice that the focus is not transfered to the text input in child2.html.
