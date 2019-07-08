# treeselect

Reproduction case for PR # - scroll & resize listeners not being removed in Internet Explorer 11.

Install with `yarn`, run with `yarn serve`.

Once the dev server is running, open `http://localhost:8080` (or whatever port the server's running on) in Internet Explorer and make sure you open Developer Tools. 

You should see a button labelled `Toggle`, clicking it should show an (empty) `Treeselect`

Now click on `Tree` then check the `Events` tab in the Developer Tools again, you should see some new event listeners, some added by `vue-router`, some added by `vue-treeselect`. We're interested in the `resize` and `scroll` handlers, which call `adjustMenuOpenDirection`.

Click on `Home` again and, again, check the `Events` tab. The `resize` and `scroll` listeners should still be there. Moreover, scrolling the page or resizing it should log an unhandled exception:

```
Unable to get property '$refs' of undefined or null referenceFile: vue-treeselect.js, 
Line: 1479, Column: 7
```
