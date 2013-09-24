JQuery UI resizable layout
==========================


How to use:
===========

Creating a vertical resizable layout:

```javascript
<script>
  $(function() {
      $('#layout').layout({
        type: 'vertical',
        resizable: true,
        helper: false,
        panes: [
          ['#pane1', {minWidth: 200, maxWidth: 400}],
          ['#pane2']
        ]
      });
  });
</script>
  
<div id="layout">
  <div id="grid1" style="width: 200px">Some Content Here</div>
  <div id="grid2">Some Content Here</div>
</div>
```

Creating a horizontal layout:

```javascript
<script>
  $(function() {
     $('#hLayout').layout({
       type: 'horizontal',
       resizable: true,
       helper: 'ui-layout-resize-h',
       panes: [
         ['#pane3', {minHeight: 200, maxHeight: 400}],
         ['#pane4']
       ]
     });
  });
</script>
  
<div id="hLayout">
  <div id="pane3" style="height: 200px">Some content</div>
  <div id="pane4">Some content</div>
</div>
```
Creating a mixture of horizontal and vertical layouts:

```javascript
<script>
  $(function() {
    $('#layout').layout({
      type: 'vertical',
      resizable: true,
      helper: false,
      panes: [
        ['#pane1', {minWidth: 200, maxWidth: 400}],
        ['#pane2']
      ]
    });
                     
    $('#hLayout').layout({
      type: 'horizontal',
      resizable: true,
      helper: 'ui-layout-resize-h',
      panes: [
        ['#pane3', {minHeight: 200, maxHeight: 400}],
        ['#pane4']
      ]
    });
  });
</script>
  
<div id="layout">
  <div id="pane1" style="width: 200px;">Your content</div>
  <div id="pane2">
    <div id="hLayout">
      <div id="pane3" style="height: 200px">Your Content</div>
      <div id="pane4">Your content</div>
    </div>
  </div>
</div>
```
Options:
========

- type - determines the type of the layout (horizontal or vertical);
- resizable - if true than the layout would be resizable be the users
- helper - enables or disables the use of helpers when resizing
- panes - an array of panes; the pane should be set as an array: the first element of the array should be the id of the element and the second is optional and it should be an object that holds the minimum and maximum width or height used when resizing.
