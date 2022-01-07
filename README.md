# Resolution Solution
Scale library, that help you add resolution support to your games in love2d!

# What it does/how to use:

1 drop library into your main.lua:

local scaling = require("resolution_solution")

2 You set game virtual size (that library will use to scale game to)

scaling.setGame(1920, 1080)

3 additionaly configure it, if you need:

set scaling mode:
scaling.scaleMode = 1 or 2

set color for black bars/lines:
scaling.setColor(1, 1, 1, 0.5)

4 update library
 love.update = function()
    scaling.update()
 end
 
5 draw it

love.draw = function()
    scaling.start()
    
    scaling.stop()
end

For more info go to source file or demo folder
demo and source was commented (probably) pretty well, so you shouldn't be losted in this library

# Some features
It have 2 scale mode:
1 aspect scaling mode (that creates black lines/bars)
2 and stretching

Also it provides some usefull functions to deal with scaling math, such as:
toGame, toScreen

Provides offset data, mouse data, scaling data and so on generated by library

Provide cursor function, that determine if cursor is touching black bars, so if you don't need to collide with something, that hided with black lines/bars, use that function

# Demostration video:
https://www.youtube.com/watch?v=lvDzdOhtt_0
