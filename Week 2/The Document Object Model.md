# The Document Object Model

## Event Bubbling 

Bubbling is what the event itself does. 

If you’ve ever watched the bubbles in a glass of soda, you’ll understand how event bubbling works. 

The event starts at the element that triggered it (Clicking 1. Element button, An Event Listener would be attached to each element). Then, it bubbles up to each of it’s parent elements until it reaches the document. Any listeners on any of those parent elements would get triggered as it bubbles up. Causing all the events to occur on the page possibly slowing down your application. 

Using a form field as an example, the event would bubble up to the parent form, then any containers or divs the form was in, then the body, then the html element, then the document, then the window. 

### Event Propagation


```JS

handleCheck = e => { 

  e.stopPropagation() 

  // talk to my API, set the record as "done" or not 

} 

<span onClick={this.handleCheck}>[]</span> 

```

That e.stopPropagation() halts this “bubbling” of events “up” through the DOM. We stop all the events from the parents occurring. 

## Event Delegation

Capturing and bubbling allow us to implement one of the most powerful event handling patterns called event delegation.

The idea is that if we have a lot of elements handled in a similar way, then instead of assigning a handler to each of them – we put a single handler on their common ancestor.

In the handler we get event.target to see where the event actually happened and handle it.

Let’s see an example – the Ba-Gua diagram reflecting the ancient Chinese philosophy.  

The table has 9 cells, but there could be 99 or 9999, doesn’t matter.

Our task is to highlight a cell <td> on click.

Instead of assign an onclick handler to each <td> (can be many) – we’ll setup the “catch-all” handler on <table> element.

It will use event.target to get the clicked element and highlight it.

```HTML

<table>
  <tr>
    <th colspan="3"><em>Bagua</em> Chart: Direction, Element, Color, Meaning</th>
  </tr>
  <tr>
    <td class="nw"><strong>Northwest</strong><br>Metal<br>Silver<br>Elders</td>
    <td class="n">...</td>
    <td class="ne">...</td>
  </tr>
  <tr>...2 more lines of this kind...</tr>
  <tr>...2 more lines of this kind...</tr>
</table>

```

Such a code doesn’t care how many cells there are in the table. We can add/remove td dynamically at any time and the highlighting will still work.

Still, there’s a drawback.

The click may occur not on the td, but inside it.

In our case if we take a look inside the HTML, we can see nested tags inside td, like strong:

```JS

let selectedTd;

table.onclick = function(event) {
  let target = event.target; // where was the click?

  if (target.tagName != 'TD') return; // not on TD? Then we're not interested

  highlight(target); // highlight it
};

function highlight(td) {
  if (selectedTd) { // remove the existing highlight if any
    selectedTd.classList.remove('highlight');
  }
  selectedTd = td;
  selectedTd.classList.add('highlight'); // highlight the new td
}

```
