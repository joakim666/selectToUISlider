This is a copy of Filament Group's jQuery UI selectToUISlider plugin, with additional patches added on top of it. 

This repository was created from the original source download from: http://www.filamentgroup.com/lab/update_jquery_ui_slider_from_a_select_element_now_with_aria_support/


The original code has been changed to trigger **slide** events on the select element as the slider is dragged. This because the 
slide callback is used internally by the selectToUISlider plugin and can't be used to get this notification.

This means that you can have code like

    $('select#one,select#two,select#three').bind('slide', function(event, p1, p2) {
        updateGraphics();
    });

to update graphics on the web page as the slider is dragged.
