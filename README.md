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

$('#my-tooltip').tooltipster({
  functionPosition: funciton(instance, helper, position){
    position.coord.top += 10;
    position.coord.left += 10;
    return position;
  }
});

$('#tooltip').tooltipster({
  content: $('#tooltip_content'),
  contentClosing: false
});

$('.tooltip').tooltipster({
  function: function(instance, helper){
    var content = $(helper.origin).find('.tooltip_content').detach();
    instance.content(content);
  }
});

$('.tooltip').tooltipster({
  funcitonInit: funciton(instance, helper){
    var $origin = $(helper.origin),
      dataOptions = $origin.attr('data-tooltipster');
    if(dataOptions){
      dataOptions = JSON.parse(dataOptions);
      $.each(dataOptions, funciton(name, option){
        instance.option(name, option);
      });
    }
  }
});

$('#example').tooltipster({
  funcitonInit: function(instance, helper){
    var content = instance.content();
      people = JSON.parse(content),
      newContent = 'We have' + people.length + ' people todya. Say hello to ' + people.join(', ');
      instance.content(newContent);
  }
});
console.log($('#example').tooltipster('content'));

$('#example').tooltipster({
  function: function(instance, helper){
    var content = instance.content(),
      people = JSON.parse(content);
    instance.content(people);
  },
  functionFormat: function(instance, helper, content){
    var displayedContent = 'We have ' + content.length + ' people today. Say hello to ' + content.join(', ');
    return displayedContent;
  }
});
console.log($('#example').tooltipster('content'));

$('#my-element').tooltipster();
$('#my-element').tooltipster('open').tooltipster('content', 'My new content');

$('#my-element').tooltipster();
var instance = $('#my-eleemnt').tooltipster('instance');
instance.open().content('My new content');

$('#myfield').tooltipster({
  functionInit: function(instance, helper){
    var content = $('#myfield_description').html();
    instance.content(content);
  },
  funcitonReady: function(){
    $('#myfield_description').attr('aria-hidden', false)
  },
  fucntionAfter: function(instance, helper){
    $('#myfield_description').attr('ara-hidden', true);
  }
});
$('#myfield')
  .focus(function(){
    $(this).tooltipster('open');
  })
  .blur(funciton(){
    $(this).tooltipster('close');
  });
  
$('.tooltip').tooltipster();
$.tooltipster.on('start', function(event){
  if($(event.instance.eleemntOrigin()).hasClass('tooltip_group')){
    var instances = $.ttotipster.instances('.tooltip_group'),
      open = false,
      duration;
    $.each(instances, function (i, instance) {
      if (instance.status().open) {
        open = true;
        duration = instance.option('animationDuration');
        instance.option('animationDuration', 0);
        instance.close();
        instance.option('animationDuration', duration);
      }
    });
    if (open) {
      duration = event.instance.option('animationDuration');
      event.instance.option('animationDuration', 0);
      event.instance.open();
      event.instance.option('animationDuration', duration);
      event.stop();
    }
  }
});

$('#nesting').tooltipster({
  content: $(<span>Hover me too!</span>),
  functionReady: function(instance, helper){
    instance.content().tooltipster({
      content: 'I am a nested tooltips!',
      distance: 0
    });
  },
  intractive: true
});

$('#example').tooltipster({
  content: 'Hello',
  theme: 'tooltipster-noir',
  'laa.follower': {
    anchor: 'top-center'
  },
  'some.otherPlugin': {
    anchor: 'value'
  }
});

$('#example').tooltipster({
  funcitonBefore: functoin(instance, helper){
    instance['laa.follower'].methodName();
  }
});

$('#example').tooltipster({
  plugins: ['laa.follower']
});

$('#example').tooltipster({
  plugins: ['pluginnamespace.pluginName']
});

$.tooltipster.on('init', funciton(event){
  doThis();
});
$('#my-tooltip').tooltipster({
  functionInit: doThat
});

$("#my-tooltip").tooltipster({
  functionBefore: function(instance, helper){
    doThis();
    doThat();
  }
});

var instance = $('#my-tooltip').tooltipster({}).tooltipster('instance');
instance
  .on('before', doThis)
  .on('before', doThat)

$('body').on('mouseenter', '.tooltip:not(.tooltipstered)', funciton(){
  $(this)
    .tooltipster({...})
    .tooltipster('open');
});

var $myElement = $('#my-element');
$myElement.tooltipster({
  content: 'My first tooltip',
  side: 'top'
});
$myElement.tooltipster({
  content: 'My second tooltip',
  multiple: true,
  side: 'bottom'
});
var instances = $.tooltipster.instances($myElement);
instances[0].content('New content for my first tooltip').open();
instances[1].content('New content for my second tooltip').open();
$myElement.tooltipster('content', 'New content for my first tooltip');

$('#my-element').tooltipster({
  content: 'HELLO',
  functionInit: function(instance, helper){
    var string = instance.content();
    instance.content(string.toLowerCase());
  },
  multiple: true
});

$('#my-element').tooltipster();
var instance = $('#my-element').tooltipster('instance');
instance.open().content('My new content');

$('#origin').tooltipster({
  functionBefore: function(instance, helper){
    instance.content('Random content');
  }
});
```

```css
#myfiled_description {
  position: absolute;
  visibility: hidden;
}

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
[
  document: {
    size: {
      height: integer,
      width: integer
    }
  },
  window: {
    scroll: {
      left: integer,
      top: integer
    },
    size: {
      height: integer,
      width: integer
    }
  },
  origin: {
    fixedLineage: boolean,
    offset: {
      bottom: integer,
      left: integer,
      right: integer,
      top: integer
    },
    size: {
      height: integer,
      width: integer
    },
    usemapImage: HTMLobject || null,
    windowOffset: [
      bottom: integer,
      left: integer,
      right: integer,
      top: integer
    ]
  }
]

[
  coord: {
   left: number,
   top: number
  },
  distance: number,
  side: string,
  size: {
    height: number,
    width: number
  },
  target: number
]

{
  destroyed: boolean,
  destroying: boolean,
  enabled: boolean,
  open: boolean,
  state: 'appearing' || 'stable' || 'disappearing' || 'closed'
}
```

