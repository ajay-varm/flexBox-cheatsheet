# **Container**
<br>

* ## **`display: flex`** or **`display: inline-flex`**: creates a flex context (or an inline flex context) for direct children of this element
* ## **`flex-direction`** determines the main and cross axis for the container, valid values are:

  * ## `row` (default): horizontal, in the direction of writing (left to right for English) <br>
  * ## `row-reverse`: horizontal, in the opposite direction of writing (right to left for English)<br>
  * ## `column`: vertical, top to bottom<br>
  * ## `column-reverse`: vertical, bottom to top<br>
* ## **`flex-wrap`** determines if flex items will try to fit in one line, valid values are:<br>

   * ## `nowrap` (default): all flex items will be on one line <br>
   * ## `wrap`: flex items will wrap onto multiple lines, top to bottom <br>
    * ## `wrap-reverse`: flex items will wrap onto multiple lines, bottom to top
* ## `flex-flow`: shorthand combining `flex-direction` and `flex-wrap` <br>
    * ## Formal syntax: `flex-flow: <'flex-direction'> || <'flex-wrap'>` <br>
* ## `justify-content` defines the alignment along the main axis, valid values are: <br>
    * ## `flex-start` (default): pack flex items from the start <br>
    * ## `flex-end`: pack flex items from the end
    * ## `start`: pack items from the start
    * ## `end`: pack items from the end
    * ## `left`: pack items from the left
    * ## `right`: pack items from the right
    * ## `center`: pack items around the center
    * ## `space-around`: distribute items evenly with equal space around them
    * ## `space-between`: distribute items evenly with equal space between them
    * ## `space-evenly`: distribute items evenly, ensuring equal space between any two items
    * ## `stretch`: distribute items evenly, stretching auto-sized items to fit the container
* ## `align-items` defines the alignment along the cross axis, valid values are:
    * ## `flex-start` (default): pack flex items from the start
    * ## `flex-end`: pack flex items from the end
    * ## `start`: pack items from the start
    * ## `end`: pack items from the end
    * ## `center`: pack items around the center
    * ## `baseline`: align items based on their baselines
    * ## `stretch`: stretch items to fill the container
* ## `align-content` defines the alignment of extra space along the cross axis, valid values are:
    * ## `flex-start` (default): pack flex items from the start
    * ## `flex-end`: pack flex items from the end
    * ## `start`: pack items from the start
    * ## `end`: pack items from the end
    * ## `center`: pack items around the center
    * ## `space-around`: distribute items evenly with equal space around them
    * ## `space-between`: distribute items evenly with equal space between them
    * ## `space-evenly`: distribute items evenly, ensuring equal space between any two items
    * ## `stretch`: distribute items evenly, stretching auto-sized items to fit the container
<br>
<img src="https://www.30secondsofcode.org/assets/blog_images/flexbox-diagram.webp">
<br>

# **Items**

* ## `flex-grow` determines how much the item can grow if necessary
    * ## Accepts a single positive number (unitless), default value is `0`
    * ## Specifies how much of the remaining space in the flex container should be assigned to the item
    * ## The remaining space is the size of the flex container minus the size of all flex items' sizes together
    * ## If all items have the same `flex-grow`, all items will receive an equal share of the remaining space
    * ## If not all items have the same `flex-grow`, the remaining space is distributed according to the ratio defined by these values
* ## `flex-shrink` determines how much the items can shrink if necessary
    * ## Accepts a single positive number (unitless), default value is `1`
    * ## If the size of all flex items is larger than the flex container, items shrink to fit according to `flex-shrink`
* ## `flex-basis` determines the initial size of a flex item before the remaining space is distributed
    * ## Can use any valid `width` value, intrinsic size values, `auto` (default) or `content`
    * ## `auto` means "look at my `width` or `height` property", whereas content is used for automatic sizing
* ## `flex`: shorthand combining `flex-grow`, `flex-shrink` and `flex-basis`
    * ## Formal syntax: `flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]`
* ## `align-self` allows the item to override the default `align-items` specified by the container
    * ## Valid values are the same as those of the `align-items` property in the container
* ## `order` determines the ordering of the item
    * ## Accepts an integer value
    * ## Items in a container are sorted by ascending `order` value and then by their source code order
    * ## Might cause accessibility issues if used incorrectly
