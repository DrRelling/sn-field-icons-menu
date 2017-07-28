# sn-field-icons-menu
A UI macro that automatically moves other icons on a field in ServiceNow into a popover menu.

Just import it from XML, then add the "macro_popover_container" to the field as you would normally using ref_contributions. 

The macro automatically picks up any previous macros in the ref_contributions list (i.e. the ones that would normally appear to the left and/or above it near the field). It takes their HTML, adds it to a little Bootstap popover menu, then removes them from the page. Any icons to the right of it are left as they are, including the preview icon. It then moves itself to the end of the list of icons. Click on the right arrow icon near the field to see the hidden icons.

So, for example, if your attributes field looks like this:

ref_contributions=do_something;do_something_else;macro_popover_container;do_another_thing

then the icons for do_something and do_something_else will be moved to the popover menu, but the icon for do_another_thing will remain where it is.

Useful links:

http://wiki.servicenow.com/index.php?title=Dictionary_Attributes#Adding_an_Attribute

https://v4-alpha.getbootstrap.com/components/popovers/
