---
layout: page
permalink: /howto/reuse_entered_values
---

<!--- IMPORTANT: This permlink is referenced from InputApp -->

# Reuse last entered values

Input supports faster digitizing of similar features by allowing user to reuse values of repeating attributes. When attribute is marked for reuse, next created feature will have desired attributes prefilled with values from last feature.

To allow this functionality, follow these steps:

 - Open any project from your home screen by clicking on its name
 - Click on three dots (![photos](../images/input_more_icon.png)) to open a menu and navigate to `Settings`
 - Check option to `Reuse last value option`

![photos](../images/reuse_last_value_option.png)

 - Go back to map and click `Record`
 - Now try to create a new feature

 > Note: You can learn how to create a feature in tutorial called [Working with Input](../using_input).

 - In opened form you will see checkboxes next to attributes. In our example we have three editable attributes (besides `fid`). We set Input to remember values for attributes `Name` and `Value` by checking checkboxes next to each of the attributes.

![photos](../images/reuse_last_values_digitize_before.png)

 - Now hit `Save` and create a new feature
 - In a newly opened form checked attributes will have values filled with values from last created feature on this layer.

![photos](../images/reuse_last_values_digitize_after.png)

You can use this feature across multiple layers, Input will remember attributes for each layer separately.


This feature was inspired by QGIS functionality called _Reuse last entered attribute values_.
