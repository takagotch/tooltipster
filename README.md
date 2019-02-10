### tooltipster
---
https://github.com/iamceege/tooltipster

```js
$(document).ready(function(){
  $('.tooltip').tooltipster();
});

$('.tooltip').tooltipster({
  theme: 'tooltipster-noir'
});

$().tooltipster({
  contentCloning: true
});

$('.tooltip').tooltipster({
  animation: 'fade',
  delay: 200,
  theme: 'tooltopster-punk',
  trigger: 'click'
});

$('.tooltip').tooltipster({
  funcitonBefore: function(instance, helper){
    instance.content('My new content');
  }
});

$.tooltipster.setDefaults({
  side: 'bottom'
});
var instances = $.tooltipster.instances();
$.each(instances, function(i, instance){
  instance.close();
});

$('.tooltip1').tooltipster();
$('.tooltip2').tooltipster();
var instances = $.tooltipster.instancesLatest();

$('.tooltip').tooltipster({
  theme: ['tooltipster-noir', 'tooltipster-noir-customized']
});

$('#myelement').tooltipster('content', 'My new content');
instance.content('My new content');

$('.tooltip').tooltipster({
  content: 'Loading...',
  functionBefore: function(instance, helper){
    var $origin = $(helper.origin);
    if($origin.data('loaded') !== true){
      $.get('http://example.com/ajax.php', function(data){
        instance.content(data);
        $origin.data('loaded', true);
      });
    }
  }
});

$(document).ready(function(){
  $('.tooltip').toolitpster();
  $('#example').tooltipster('open', funciton(instance, helper){
    alert('The tooltip is now fully shown. Its content is: ' + instance.content());
  });
  $(window).keypress(funciton(){
    $('#example').tooltipster('close', function(instance, helper){
      alert('The tooltip is now fully hidden');
    });
  });
});

$('#example').tooltipster({
  trigger: 'custom',
  triggerOpen: {
    mouseenter: true
  },
  triggerClose: {
    click: true,
    scroll: true
  }
});

$('#example').tooltipster({
  trigger: 'custom',
  triggerOpen: {
    mouseenter: true,
    touchstart: true
  },
  triggerClose: {
    click: true,
    scroll: true,
    tap: true
  }
});

$('#example').tooltipster({
  trigger: 'custom',
  triggerOpen: {
    mouseenter: true,
    touchstart: true
  }.
  triggerClose: {
    mouseleave: true,
    originClick: true,
    touchleave: true
  }
});

$('#example').tooltipster({
  trigger: 'custom',
  triggerOpen: {
    click: true,
    tap: true
  },
  triggerClose: {
    click: true,
    tap: true
  }
});

$(document).ready(function(){
  $('.tooltip').tooltipster();
  $('#example').tooltipster();
  $(window).keypress(function(){
    $('#example').tooltipster('close');
  });
});

```

```css
.tooltipster-sidetip.tooltipster-noir.tooltipster-noir-customized .tooltipster-box {
  background: grey;
  border: 3px solid red;
  border-radius: 6px;
  box-shadow: 5px 5px 2px rgba(0,0,0,0,4);
}

.tooltipster-sidetop.tooltipster-noir.tooltipster-noir-customized.tooltipster-content {
  color: blue;
  padding: 8px;
}
```

```
```

