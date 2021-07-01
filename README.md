# Arrow Vomit
Arrow Vomit is a post-modern *masterpiece* created with [Netlogo](https://ccl.northwestern.edu/netlogo/). It depicts the internal struggle of the average Tik-tok user, with each arrow representing their fragmented attention-spans. 


<div style="text-align:center"><img src="https://github.com/G-Justin/ALT-Cellular-Automata/blob/master/arrow_vomit.gif" height="400" /></div>
Animated

<div style="text-align:center"><img src="https://github.com/G-Justin/ALT-Cellular-Automata/blob/master/arrow_vomit%20view.png" height="400" /></div>
Still

## Documentation
You can run the masterpiece yourself using the [nlogo file](https://github.com/G-Justin/ALT-Cellular-Automata/blob/master/arrow_vomit.nlogo). Just click the `setup` to initialize the arrows with random colors, then press `go`. 

<div style="text-align:center"><img src="https://github.com/G-Justin/ALT-Cellular-Automata/blob/master/Screenshot%202021-07-01%20182602.png" height="400" /></div>


Arrow Vomit was created by first creating 14 arrows (turtles) and splitting them into 7 pairs. Each pair is spread out along the x-axis of the world by 5 patches from the center, where each arrow in the pair is set to opposing 45 degree angles.

`setup`:
<pre><code>
 to setup
  clear-all
  reset-ticks
  create-turtles 14

  ;;group 0
  ask turtle 0 [
    set heading 45
    setxy 5 0
  ]
  ask turtle 1 [
    set heading -45
    setxy 5 0
  ]

  ;;group 1
  ask turtle 2 [
    set heading 45
    setxy 10 0
  ]
  ask turtle 3 [
    set heading -45
    setxy 10 0
  ]

  ;;group 2
  ask turtle 4 [
    set heading 45
    setxy 15 0
  ]

  ask turtle 5 [
    set heading -45
    setxy 15 0
  ]

  ;;group 4
  ask turtle 6 [
    set heading 45
    setxy -5 0
  ]
  ask turtle 7 [
    set heading -45
    setxy -5 0
  ]

  ;;group 5
  ask turtle 8 [
    set heading 45
    setxy -10 0
  ]
  ask turtle 9 [
    set heading -45
    setxy -10 0
  ]

  ;;group 6
  ask turtle 10 [
    set heading 45
    setxy -15 0
  ]
  ask turtle 11 [
    set heading -45
    setxy -15 0
  ]

  ;;group 7
  ask turtle 12 [
    set heading 45
  ]
  ask turtle 13 [
    set heading -45
  ]
  
  ask turtles [
    pen-down
  ]
end

</pre></code>

The `go` button executes the `go` function "forever" until pressed again. The `go` function moves all the arrows forward by 3 patches, with each move changing the arrow's color to a random non-gray Netlogo base color.

`go`:
<pre><code>
to go
  ask turtles [
    forward 3
    set color one-of remove gray base-colors
  ]
end
</pre></code>

## Purchase
Arrow Vomit will be available for purchase in the near future as a Non-Fungible Token (NFT) for 3.00 BTC. 
