#orbit


###experimental, consumable orbital effects for your DOM elements

![alt tag](https://raw.github.com/jh3y/pics/master/orbit/orbit.gif)

#### Usage
1. Include the [stylesheet](https://raw2.github.com/jh3y/orbit/master/dist/orbit.css) (_advisable to use minified version).
2. Create the DOM structure for your orbital element.
```html
    <ul class="orbit">
      <li class="planet center">
        <div>
          <a>o</a>
        </div>
      </li>
      <li pause-on-hover data-orbit-width="1" data-orbit-depth="3" class="planet">
        <div>
          <a>r</a>
        </div>
      </li>
      <li pause-on-hover data-orbit-width="2" data-orbit-depth="3" class="planet">
        <div>
          <a>b</a>
        </div>
      </li>
    </ul>
```
3. Define necessary data attributes and classes to different elements to achieve the desired behavior[* see helpers](#helpers).

That's it!

##### Browser Support

From what I can gather having a look at _caniuse_, orbit will only be supported by those browsers that fully support animation keyframes.

##### Helpers

There are helper classes and attributes to define how your orbit will work.

######Classes
* `orbit`(container)
	The orbit class must be applied to the container for your orbit (This will be updated to also include data attribute if requested).
* `planet`
  The planet class is given to every orbiting element within the orbit container.
* `center`
  An additional center class can be given to a planet to define that it is the center.

######Attributes
* `data-orbit-delay` - number
  Define the delay in seconds for the orbit to start (up to 10s by default).
* `data-orbit-duration`- number
  Defines the duration for an element to orbit (up to 10s by default).
* `data-orbit-depth` - number level
  Defines the level at which an orbiting element will traverse on the z-index.
* `data-orbit-width`
  Defines the level at which an orbiting element will traverse on the x-index.
* `data-orbit-height`
  Defines the level at which an orbiting element will traverse on the y-index.
* `pause-on-hover`
  Defines whether an element will pause its orbit on hover.


#### How does this work?
orbit takes advantage of preprocessing tools to heavily leverage the use of mixins and loops to generate various different combinations of animation keyframes bespoke for different combinations.

For example, an element with a depth level of 2, a width level of 3 and a height level of 4 will have its own specific animation keyframe assigned to it.

#### Development/Customisation
##### Editing the source
__orbit__ is developed with __less__ making the actual amount of code written minimal in order to generate the stylesheet by making use of looping and mixins.

The source is commented to help aid in understanding how to edit orbit to behave how you'd like.

If you do want to use orbit in a project I highly recommend editing the source to make the output minimal as in its current state, orbit is quite sizely, even in its minimised state.

#### Contributing

Any suggestions, improvements or issues are welcome. :)


#### License

MIT

Copyright (c) 2014 [@jh3y](https://github.com/jh3y)
