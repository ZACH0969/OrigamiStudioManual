# Interaction



## Interaction

Capture touch events on specific layers. Note that layers must be enabled and have an opacity larger than 0 to receive touches.

Detect[Double Tap](http://origami.design/documentation/patches/origami.doubleTap.html)or[Long Press](http://origami.design/documentation/patches/origami.longPress.html)with additional patches.

Use the Touch button on a layer to quickly add interactions.



### Layer

The layer to check for touch interactions. When no layer is specified, the touches on the whole screen are registered.

### Enable

A boolean that is true when touch detection is on. To disable interactions on this layer, disable it.



### Down

A boolean that is true when there is a touch on the layer.

### Tap

A pulse that represents the moment a touch has been released from the layer \(touch up\) as long as the touch is inside of the layer and hasn’t moved.

### Position

The position of the touch, relative to the center of the layer’s parent group or device

### Force

A number between 0 and 1 that represents the force of the touch.



# Scroll

Scroll a layer using free or paged \(carousel\) scrolling. The layer will be scrolled inside of its parent layer group.

Use the Touch button on a layer to quickly add interactions.

### 

### Content Layer

The layer to scroll.

### Enable

A boolean that is true when scrolling is enabled.

### Scroll X

The horizontal scrolling style - None, Free or Paging.

### Scroll Y

The vertical scrolling style - None, Free or Paging.

### Settings

Custom scroll settings. To be used with the output of the[Scroll Settings](http://origami.design/documentation/patches/origami.scroll.settings.html)patch.

### X

The current horizontal scroll position. Connect to the X Position of the selected layer.

### Y

The current vertical scroll position. Connect to the Y Position of the selected layer.

