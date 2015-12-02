

```html
<diamond-file-system exec="readDir" args="/foo" results="{{files}}"></diamond-file-system>
<paper-menu>
  <template is="dom-repeat" items="{{files}}">
    <diamond-file-system exec="lstat" args="/foo/{{item}}" results="{{stats}}"></diamond-file-system>
    <paper-icon-item>
      <template is="dom-if" if="{{stats.isDirectory()}}">
        <iron-icon icon="folder" item-icon></iron-icon>
      </template>
      <template is="dom-if" if="{{stats.isFile()}}">
        <iron-icon icon="" item-icon></iron-icon>
      </template>
      <template is="dom-if" if="{{stats.isSymbolicLink()}}">
        <iron-icon icon="link" item-icon></iron-icon>
      </template>
      {{item}}
    </paper-icon-item>
  </template>
</paper-menu>

```
