When a customizable widget element is rendered, the widget fires the corresponding event, which enables you to modify the rendered element for your requirements. You can assign the function which handles the required event to the **on*Element*Rendered** option, where *Element* is a name of the rendered widget element. For instance, pass the event handling function to the **onTitleRendered** option to handle the event that occurs when the widget title is rendered. If a widget contains customizable content, the option holding a function called when widget content is rendered is called **onContentReady**.

    <!--JavaScript-->
    var popoverOptions = {
        onTitleRendered: titleRenderedHandler
    }

The object passed to the handler function enables you to access the rendered markup element and the data model associated with the current view.

    <!--JavaScript-->
    var myTitle = "Popover Title";
    var titleRenderedHandler = function(e) {
        // Use the 'e' object to access the widget markup element, rendered element and data model
        e.titleElement.append("<h1>" + myTitle + "</h1>");
    }

Refer to the required event description for detailed information on the supported fields of the parameter object.

Note that **rendered** (for example **onItemRendered**, **onGroupRendered**) event handlers for collection items have other parameters. For more information, refer to the [Customize Collection Item Appearance](/Documentation/Guide/UI_Widgets/Common/Customize_Widget_Element_Appearance/#Customize_Collection_Item_Appearance) article.

#####See Also#####
- [Customize Widget Element Appearance](/concepts/10%20UI%20Widgets/80%20Common/30%20Customize%20Widget%20Element%20Appearance '/Documentation/Guide/UI_Widgets/Common/Customize_Widget_Element_Appearance/') 
- [Customize Widget Element Appearance - MVVM Approach](/concepts/10%20UI%20Widgets/80%20Common/35%20Customize%20Widget%20Element%20Appearance%20-%20MVVM%20Approach '/Documentation/Guide/UI_Widgets/Common/Customize_Widget_Element_Appearance_-_MVVM_Approach/')