# LVGL for MicroBlocks
## Introduction

Introduction
LVGL (Light and Versatile Graphics Library) is a GUI library for embedded systems with a graphical display and some form of input (such as a touchscreen, rotary encoder, etc.). It helps create attractive user interfaces, with the logic and rendering handled entirely by the LVGL library. The user only needs to focus on the layout and responds to events triggered by user interactions.

## Integration in MicroBlocks

LVGL is a complex library that offers a wide variety of widgets. Each widget supports numerous style settings and configuration options. One of the strengths of MicroBlocks is its self-explanatory nature, where the blocks clearly convey their function. We have aimed to stay as close to that principle as possible in this integration.

# LVGL library
## Objects
In MicroBlcoks all widgets objects have a name. The name is used to reference its objects. If you create a button with name `btn`, than you can use the name `btn` to set its position, change it's size and change it's text. The objects are internally stored in a map in which the objects are indexed with their names. 

## General modifiers

A number of general modifiers are available for most of the widgets

![set_pos](https://github.com/user-attachments/assets/b7b28433-2294-4a2c-943a-eab7746bbcbf)

position: determines the possition relative to its parent

![set_size](https://github.com/user-attachments/assets/74c7d23d-6fa6-489b-b6ed-1b0109267687)
  
size: changes the size of a widget.

![set_color](https://github.com/user-attachments/assets/42165ebc-e490-4853-8675-ec7e06d5cc47)

color: changes the colors of attributes of a widget. The first color is usually the background color, the second color is the color for the indicator (e.g. for an Arc, a bar or a slider) and the third color is the color for the knob (for Arc and Slider).
  

## Button
![image](https://github.com/user-attachments/assets/cf3ad661-0cdf-4369-82bb-1181d9521c66)

A button is created by the `btn` block.

![simple_button](https://github.com/user-attachments/assets/df9415f9-dd93-417a-8d19-aa708c69fa11)

Here, for simplicity, the name of the button is automatically used as the text written in the button. So if you create a button with name `OK`, a button with `OK` written in it is created.

![expanded_button](https://github.com/user-attachments/assets/835d8e87-87c5-4a9f-bbc7-c2b186893191)

The button blocks has a number of extra fields. You can change the text size ranging from 1 to 4 mapping on a 14, 24, 40 and 48 points font. A sperate `text` field allows for a text that is different than the button name. The `parent` field refers to the name of a parent object. The default value is the main screen (`lv_scr_act`). A parent can be a tab in a tabview or a tile in a tileview.

## Label
![image](https://github.com/user-attachments/assets/b98ddd9a-365a-4311-9191-1a698a0d3c87)

A label is created using the `label` block.

![simple_label](https://github.com/user-attachments/assets/3e91b30f-00a6-4c0c-b7f4-49c8d4fa3a01)

Like the button block, here the text in the label defaults to the name of the label.

![expanded_label](https://github.com/user-attachments/assets/efa0c3f1-d7f4-4ab7-a02b-0f302039e06e)

The expanded label block has similar fileds as the button block.

## Arc
![image](https://github.com/user-attachments/assets/8ba122d0-5431-4e28-bedb-abff209f7a3b)

An arc is drawn using the generic add object block, where from the drop down `arc` is selected.

![add_arc](https://github.com/user-attachments/assets/73293166-0a86-4b06-921a-2e29d242f33c)

Some of the properties of the arc can be changed.

![set_range](https://github.com/user-attachments/assets/2c3e8244-5e5c-47ee-81c4-7e4649798671)

Changes the start end end scale of the arc (default 0 to 100)

![set_angles](https://github.com/user-attachments/assets/244bce33-abd0-4adf-9394-fdaacf4cbc63)

Changes the start en end angle of the scale of an arc. Zero degrees is at the middle right (3 o'clock) of the object and the degrees are increasing in clockwise direction. The angles should be in the [0;360] range.

![set_rotation](https://github.com/user-attachments/assets/71021e68-68cb-42f4-a173-6dd0515c5d11)

Determines he angle of the 0 degree point on the scale with respect to the background.

![get_val](https://github.com/user-attachments/assets/a15f9069-f6d2-4356-8c52-892fc4ea70cb)

Returns the value of the indicator.

![set_val](https://github.com/user-attachments/assets/6b2cceef-33d4-4378-8ea6-73658031a21c)

Detemines the position of the indicator.

## Slider
![image](https://github.com/user-attachments/assets/f22fa70d-76bb-4393-a963-9ef8e5e4326b)

An slider is drawn using the generic add object block, where from the drop down `slider` is selected.

![add_slider](https://github.com/user-attachments/assets/9020a5e0-fbf9-43de-8a7e-7d74cc308aa0)

Some of the properties of a slider can be changed.

![set_range](https://github.com/user-attachments/assets/2c3e8244-5e5c-47ee-81c4-7e4649798671)

Changes the start end end scale of the arc (default 0 to 100)

![get_val](https://github.com/user-attachments/assets/a15f9069-f6d2-4356-8c52-892fc4ea70cb)

Returns the value of the indicator.

![set_val](https://github.com/user-attachments/assets/6b2cceef-33d4-4378-8ea6-73658031a21c)

Detemines the position of the indicator.

## Bar
![image](https://github.com/user-attachments/assets/12bfc7c6-257c-4b7d-8e1a-c64a6a24c759)

## Led
![image](https://github.com/user-attachments/assets/71031ef4-ddac-4011-b372-3426495f442a)

## Switch
![image](https://github.com/user-attachments/assets/c7d51e6b-61fc-4c00-9d15-f3297859baf6)

## List
![image](https://github.com/user-attachments/assets/81164ee9-2119-41b7-9d29-416cbba2b957)

## Roller
![image](https://github.com/user-attachments/assets/aa05cb08-553a-4405-8b59-302ebd7c505d)







