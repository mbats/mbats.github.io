---
layout:     post
title:      "Keyboard shortcuts"
subtitle:   
date:       2015-04-07 12:00:00
author:     "Mélanie Bats"
header-img: "img/post-bg-01.jpg"
---

Usually when you are using a graphical modeler, you do most of the actions with the mouse. [Sirius](http://www.eclipse.org/sirius) based modelers have several built-in shortcut keys that you can use to save time in your day to day workflow. Shortcut keys are commonly accessed by using the ![](https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Alt_T.png?raw=true) key, ![](https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true) key, or ![](https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true) key in conjunction with other keys.

1.  [Keyboards shortcuts](#Keyboardsshortcuts)
    1.  [Common shortcuts](#Commonshortcuts)
    2.  [Diagram shortcuts](#Diagramshortcuts)
        1.  [Navigate](#Navigate)
        2.  [Select](#Select)
        3.  [Edit](#Edit)
        4.  [Diagram editor](#Diagrameditor)
        5.  [Palette](#Palette)
    3.  [Table & Tree shortcuts](#TableTreeshortcuts)

## Common shortcuts

Some shortcuts are available for all the representations (diagram, table, tree…).

<table width="100%" border="0">
<colgroup>
<col style="width: 20%;" />
<col style="width: 30%; text-align: center;" />
<col style="width: 50%;" /></colgroup>
<tbody>
<tr>
<th>Action</th>
<th>Shortcut</th>
<th>Description</th>
</tr>
<tr>
<td>Refresh</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_F5_T.png?raw=true" alt="" border="0" /></td>
<td>Force an update of the diagram according to the latest version of the semantic model.</td>
</tr>
<tr>
<td>Copy semantic element</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_C_T.png?raw=true" alt="" border="0" /></td>
<td>On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mac_cmd_key.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_C_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Paste semantic element</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_V_T.png?raw=true" alt="" border="0" /></td>
<td>On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mac_cmd_key.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_V_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Copy layout</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Alt_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_C_T.png?raw=true" alt="" border="0" /></td>
<td>See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Copypasteoflayout">copy/paste layout</a> documentation.</td>
</tr>
<tr>
<td>Paste layout</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Alt_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_V_T.png?raw=true" alt="" border="0" /></td>
<td>See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Copypasteoflayout">copy/paste layout</a> documentation.</td>
</tr>
<tr>
<td>Hide element</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_H_T.png?raw=true" alt="" border="0" /></td>
<td>See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Hidingelements">hide elements</a> documentation.</td>
</tr>
<tr>
<td>Hide label</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_L_T.png?raw=true" alt="" border="0" /></td>
<td>See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Hidinglabels">hide labels</a> documentation. On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mac_cmd_key.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_L_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Show label</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_L_T.png?raw=true" alt="" border="0" /></td>
<td>On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mac_cmd_key.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_L_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Move shape</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Arrows_T.png?raw=true" alt="" border="0" /></td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/Move.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Cycle on element handles</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Period_T.png?raw=true" alt="" border="0" /></td>
<td>Cycle on Position Handle / 8 Side and Corner Size Handles / Position Handle. Clockwise rotation.</td>
</tr>
<tr>
<td>Cycle through edge points</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Period_T.png?raw=true" alt="" border="0" /></td>
<td>Cycle through the endpoints, bendpoints, and midpoints of a connection. Clockwise rotation.</td>
</tr>
<tr>
<td>Manage edge</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Minus_T.png?raw=true" alt="" border="0" /></td>
<td>Remove all the bend-points to retrieve an original straight edge. See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Manageedges">manage edge</a> documentation. On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mac_cmd_key.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Minus_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Move a component</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Period_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_hand_small_T.png?raw=true" alt="" border="0" /></td>
<td>Cycle once to the Move handle using the <code>period key (.)</code>, use navigation keys to move, press <code>Enter</code> to accept new location or press <code>Escape</code> to cancel the move.</td>
</tr>
<tr>
<td>Constrained move</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_hand_small_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /></td>
<td>This action constrained the move by snaping the shape to the grid.</td>
</tr>
<tr>
<td>Move without snap</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_hand_small_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Alt_T.png?raw=true" alt="" border="0" /></td>
<td>This action allows to ignore the snap while dragging a shape. On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_hand_small_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Resize a component</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Period_T.png?raw=true" alt="" border="0" /> + Resize</td>
<td>Cycle to desired resize handle using the period key, use navigation keys to resize, press <code>Enter</code> to accept new size or press <code>Escape</code> to cancel the resize.</td>
</tr>
<tr>
<td>Centered resize</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_large_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /></td>
<td>Expands the shape on both opposite sides. See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Resizingelements">resize elements</a> documentation. On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_large_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Alt_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Resize that keeps the ratio</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_large_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /></td>
<td>See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Resizingelements">resize elements</a> documentation.</td>
</tr>
<tr>
<td>Resize without snap</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_large_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Alt_T.png?raw=true" alt="" border="0" /></td>
<td>Temporarily disables the snap during the resize if it is activated. See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Resizingelements">resize elements</a> documentation. On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_large_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Resize container keeping children relative</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_large_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_F3_T.png?raw=true" alt="" border="0" /></td>
<td>When the shape is resized using the left and/or top border, the children (contained nodes for container and border nodes for all shapes) are moved with the border. See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#Resizingelements">resize elements</a> documentation.</td>
</tr>
<tr>
<td>Reset diagram</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_and_T.png?raw=true" alt="" border="0" /></td>
<td>The diagram can have a negative origin or can be shifted toward the bottom-right with a blank zone at the top-left. This action aims to move all diagram elements to retrieve its origin while keeping the element layout. See Sirius <a href="http://www.eclipse.org/sirius/doc/user/diagrams/Diagrams.html#ResetDiagramorContainerOrigin">reset diagram</a> documentation. On Mac : <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mac_cmd_key.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_and_T.png?raw=true" alt="" border="0" /></td>
</tr>
</tbody>
</table>

### Palette

Keyboard shortcuts save you time by letting you explore the palette quickly.

<table width="100%" border="0">
<colgroup>
<col style="width: 20%;" />
<col style="width: 30%; text-align: center;" />
<col style="width: 50%;" /></colgroup>
<tbody>
<tr>
<th>Action</th>
<th>Shortcut</th>
<th>Description</th>
</tr>
<tr>
<td>Zoom in</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_num_row_Equals_T.png?raw=true" alt="" border="0" /></td>
<td><a href="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/full/Zoom_in.png?raw=true"><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/Zoom_in.png?raw=true" alt="" border="0" /></a></td>
</tr>
<tr>
<td>Zoom out</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Minus_T.png?raw=true" alt="" border="0" /></td>
<td><a href="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/full/Zoom_out.png?raw=true"><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/Zoom_out.png?raw=true" alt="" border="0" /></a></td>
</tr>
<tr>
<td>Pan when zoomed in</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Space_bar_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/mouse_pointer_hand_small_T.png?raw=true" alt="" border="0" /></td>
<td>Hold down <code>spacebar</code> and drag the mouse</td>
</tr>
<tr>
<td>Scroll in diagram</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Ctrl_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Arrows_T.png?raw=true" alt="" border="0" /></td>
<td></td>
</tr>
<tr>
<td>Invokes the context menu for the shape</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Shift_T.png?raw=true" alt="" border="0" /> + <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_F10_T.png?raw=true" alt="" border="0" /></td>
<td><a href="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/full/Context_menu.png?raw=true"><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/Context_menu.png?raw=true" alt="" border="0" /></a></td>
</tr>
</tbody>
</table>

## Table & Tree shortcuts

Some specific key shortcuts are also available on tables and trees.

<table width="100%" border="0">
<colgroup>
<col style="width: 20%;" />
<col style="width: 30%; text-align: center;" />
<col style="width: 50%;" /></colgroup>
<tbody>
<tr>
<th>Action</th>
<th>Shortcut</th>
</tr>
<tr>
<td>Expand direct children</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Plus_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Collapse</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_Minus_T.png?raw=true" alt="" border="0" /> or <img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_slash_T.png?raw=true" alt="" border="0" /></td>
</tr>
<tr>
<td>Expand all children</td>
<td><img src="https://github.com/mbats/sirius-blog/blob/master/keyboard/blog/images/computer_key_mul_T.png?raw=true" alt="" border="0" /></td>
</tr>
</tbody>
</table>

Use keyboard shortcuts and increase your productivity!

This post is available on github : [https://github.com/mbats/sirius-blog/tree/master/keyboard](https://github.com/mbats/sirius-blog/tree/master/keyboard)