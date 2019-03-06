# Lesson--
-----------------------------------------------------------------------------------------
--
-- how to calculate the area of a trapezoid
--
-----------------------------------------------------------------------------------------
local AOfTrapezoidTextField = native.newTextField( display.contentCenterX, display.contentCenterY - 25 , 420 , 75 )
AOfTrapezoidTextField.id = "a textField"
local BOfTrapezoidTextField = native.newTextField( display.contentCenterX, display.contentCenterY + 75 , 420 , 75 )
BOfTrapezoidTextField.id = "b textField"
local HeightOfTrapezoidTextField = native.newTextField( display.contentCenterX, display.contentCenterY + 175 , 420 , 75 )
HeightOfTrapezoidTextField.id = "h textField"
local areaOfTrapezoidTextField = display.newText( "Trapezoid area", display.contentCenterX, display.contentCenterY - 250 , native.systemFont, 75 )
areaOfTrapezoidTextField.id = "area textField"
areaOfTrapezoidTextField:setFillColor( 1, 1, 1 )
local calculateButton = display.newImageRect( "./assets/sprites/calculateButton.png", 406, 157 )
calculateButton.x = 550
calculateButton.y = 1500
calculateButton.id = "calculate button"
 
local function calculateButtonTouch( event )
    -- this function calculates the area of a trapezoid given the length of one of its sides
 
    local AOfTrapezoid
    local BOfTrapezoid
    local HeightOfTrapezoid
    local areaOffTrapezoid
 
   AOfTrapezoid=AOfTrapezoidTextField.text
   BOfTrapezoid=BOfTrapezoidTextField.text
   HeightOfTrapezoid=HeightOfTrapezoidTextField.text
   areaOfTrapezoid= ( AOfTrapezoid + BOfTrapezoid) * (HeightOfTrapezoid / 2)
    -- print( areaOfTrapezoid )
    areaOfTrapezoidTextField.text = "The area is " .. areaOfTrapezoid
    return true
end
calculateButton:addEventListener( "touch", calculateButtonTouch )
