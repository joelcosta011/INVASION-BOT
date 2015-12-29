#include <MsgBoxConstants.au3>
#include <AutoItConstants.au3>
Global $g_bPaused = False
HotKeySet("{ESC}", "Terminate")

Func Terminate()
    Exit
EndFunc   ;==>Terminate

;Image Search
$x = 0
$y = 0

Func Start()
   $Search = _ImageSearch('Search.bmp',0, $x, $y, 0)
   If $Search = 1 Then
	  MouseMove($x, $y, 10)
	  
   Else
	  For MouseWheel($MOUSE_WHEEL_UP, 2)
	do Func Start	 
   EndIf
EndFunc

 ; Left click drag from 0, 200 to 600, 700
While 1
MouseClickDrag($MOUSE_CLICK_LEFT,539, 475, 863, 849)
WEnd
