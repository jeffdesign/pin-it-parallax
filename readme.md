## Synopsis

I was researching through the world wide web for a javascript function ”pin parallax scroll event” or whatever you’d like to call it.

Scrollmagic has a solution of this, but it has a set value. Many times you wont know the actual height of the content.

Couldn't find a solution that was fitting my needs so I built my own in jQuery.


## Code Example

```
//The elevator algorithm
if ( (currentPos >= targetElemTopPos) && (currentPos <= targetElemenBotPos) ) {
    //If the current position is greater than targets top position
    //AND if the current position is less than targets bottom position
    //Start the elevator
    console.log('Elevator in movement');
    $('#elevator .left').addClass('fixed');
    $( '#elevator .left' ).css( 'top', 0 );
} else if (currentPos >= targetElemTopPos) {
    //Howeaver if the current position is greater than targets bottom position
    // Stop the elevator and push it down so we can take the elevator up later if we want to
    console.log('Elevator has reached the destination');
    $('#elevator .left').removeClass('fixed');
    $( '#elevator .left' ).css( 'top', amountOfTop );
} else {
    //Else just let the elevator wait on a passanger
    console.log('Elevator on standby');
    $('#elevator .left').removeClass('fixed');
    $( '#elevator .left' ).css( 'top', 0 );
}
```

* [Demo](https://codepen.io/jeffdesign/pen/jBOdgE) Demo

## Contributors

Jefrey Örnerstedt - jeffdesign.se

## License

MIT
