

```html
<file-system exec="readDir" args="/foo" results="{{files}}"></file-system>
<paper-menu>
  <template is="dom-repeat" items="{{files}}">
    <file-system exec="lstat" args="/foo/{{item}}" results="{{stats}}"></file-system>
    <paper-icon-item>
      <template is="dom-if" if="{{stats.isDirectory()}}" restamp="true">
        <iron-icon icon="folder" item-icon></iron-icon>
      </template>
      <template is="dom-if" if="{{stats.isFile()}}" restamp="true">
        <iron-icon icon="" item-icon></iron-icon>
      </template>
      <template is="dom-if" if="{{stats.isSymbolicLink()}}" restamp="true">
        <iron-icon icon="link" item-icon></iron-icon>
      </template>
      {{item}}
    </paper-icon-item>
  </template>
</paper-menu>

```
