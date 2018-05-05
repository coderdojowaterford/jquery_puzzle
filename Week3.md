## Challenges

This week we're going to make the following alterations to our Puzzle Game.

Game after Week 3:
![before-pic][before]

Game after today
![after-pic][after]

You need to make the following changes:

- Add your name to the title of the game. i.e. Bob's Dojo Puzzle
- Add a bootstrap row and create two columns, place the game in the left column and controls (play button) in the right other. (https://getbootstrap.com/docs/4.0/layout/grid/)
- Add a CSS border to the right column. (https://www.w3schools.com/css/css_border.asp)
- Left align the Play button and add help text. e.g. This button starts a new game.
- Change the JavaScript code so that the Play button is no longer hidden when it is clicked. (http://api.jquery.com/prop/);
- Add a 'difficulty' dropdown element with the options noob, semi-noob, pro, master. (https://getbootstrap.com/docs/4.0/components/dropdowns/)
- Alter the for loop in the Play button's function so that it iterates a different amount based on the dropdown value (https://www.w3schools.com/js/js_loop_for.asp):
    - noob - 15 times
    - semi-noob - 30 
    - pro - 40
    - master - 1000
- Add a counter that keeps track of the number of moves.     
- Add a reset button (with help text) that makes a call to a function that sets the game back to the default state. It should:
    - Set the Play button disabled property to false.
    - Set the move count to 0
    - Move all the tiles back to their original positions. 
- Set all buttons to 100 pixels wide.(https://www.w3schools.com/cssref/pr_dim_width.asp)


### Dropdown code:

```html

<div class="dropdown">
    <button type="button" class="btn btn-primary dropdown-toggle " data-toggle="dropdown">
        Difficulty:
        <span id="difficultyVal" class="game-text">Noob</span>
    </button>
    <div class="dropdown-menu">
        <a class="dropdown-item" data-val="15"     href="#">Noob</a>
        <a class="dropdown-item" data-val="30"    href="#">Semi Noob</a>
        <a class="dropdown-item" data-val="40"    href="#">Pro</a>
        <a class="dropdown-item" data-val="1000"  href="#">Master</a>
    </div>
</div>
```

```javascript
$('.dropdown-item').click(function (e) {
    iters = $(this).attr( 'data-val' );
    $('#difficultyVal').html($(this).html());
    e.preventDefault();
})
```

[before]: screenshots/before.png "Before"
[after]: screenshots/after.png "After"
