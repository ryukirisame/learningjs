
# Event Propagation
Event propagation in JavaScript describes the order in which events are handled as they travel through the DOM.

It consists of three phases:
1. Capturing Phase
2. Target Phase
3. Bubbling Phase

### Consider this example

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Event Propagation Example</title>
</head>
<body>
  <div id="outer">
    <div id="inner">
      <button id="myButton">Click me</button>
    </div>
  </div>
  <script>
    document.getElementById('outer').addEventListener('click', function(event) {
      console.log('Outer DIV clicked - Capturing phase');
    }, true);

    document.getElementById('inner').addEventListener('click', function(event) {
      console.log('Inner DIV clicked - Capturing phase');
    }, true);

    document.getElementById('myButton').addEventListener('click', function(event) {
      console.log('Button clicked - Target phase');
    });

    document.getElementById('inner').addEventListener('click', function(event) {
      console.log('Inner DIV clicked - Bubbling phase');
    });

    document.getElementById('outer').addEventListener('click', function(event) {
      console.log('Outer DIV clicked - Bubbling phase');
    });
  </script>
</body>
</html>

```


## Capturing Phase/ Trickling Phase

Event Capturing is a method of Event Propagation in which the event is propagated from the top of the hierarchy and goes all the way down to the target element.

In our example, 
The outer div's capturing listener is triggered first. Then, the inner div's capturing listener is triggered.

NOTE: If we want to fire an event listener in capturing phase then, pass true as the third argument in addEventListener.


## Target Phase

The event reaches the target element and fires its listener.

NOTE: Modern browsers do not treat the target phase independently. The target phase which happens when the event reaches the target element that triggered the event.


## Bubbling Phase (Default)

In this phase, the events bubble up from target element back to the document root.
So basically, the event travels/propagates from the target element to the document root.

In our example, The inner div's bubbling listener is triggered. Finally, the outer div's bubbling listener is triggered.

![image](https://github.com/ryukirisame/learningweb/assets/40791172/950b04ef-ce17-4f7a-8585-ad18f42f85ef)

# Stopping Event Propagation

Sometimes, you might want to stop the event from propagating further. You can do this using:

1. event.stopPropagation(): Stops the event from propagating further in the capturing and bubbling phases.
2. event.stopImmediatePropagation(): Stops the event from propagating and prevents any other listeners of the same event from being called.


```
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log('Button clicked - Target phase');
  event.stopPropagation(); // Stops the event from propagating
});
```

### Application of Event Propagation

### Event Delegation
Event Delegation: Using event propagation to attach a single event listener to a parent element instead of multiple listeners to each child. It is possible because of event bubbling.

Advantage of event delegation:

1. Performance Optimization - It Improves the performance by reducing the number of event listeners from the DOM. Instead of attaching an event listener to each individual child element, you attach a single event listener to the parent element.
2. Memory - Since less event listeners are added it decrease the memory usage, compared to attaching an event listener to each and every element.
3. Code Readability, Easy Maintenance

Limitations of event delegation:
1. All the events are not bubbled up, some events like load, resize, blur, focus are not bubbled up.
2. If e.stopPropogation is used in child, then events are not bubbled up, and hence event delegation is not possible in that case.

# closest() method

The closest() method in JavaScript is used to find the nearest ancestor of the current element (or the element itself) that matches a given CSS selector. It traverses the DOM tree from the current element up to the root of the document, stopping as soon as it finds a match.

`element.closest(selector)
`
- element: The DOM element from which the search begins.
- selector: A string representing the CSS selector to match against the ancestors of the element.

# event.composedPath()

The event.composedPath() method in JavaScript provides a way to obtain the event's path through the DOM. This method returns an array of all the elements that the event passed through, from the topmost element to the target element, including shadow DOM elements if applicable.

