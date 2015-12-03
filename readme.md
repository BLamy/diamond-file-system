

```html
<diamond-file-system exec="readDir" args="/foo" results="{{files}}"></diamond-file-system>
<paper-menu>
  <template is="dom-repeat" items="{{files}}">
    <paper-item>
      {{item}}
    </paper-item>
  </template>
</paper-menu>

```
