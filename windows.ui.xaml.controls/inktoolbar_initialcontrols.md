---
-api-id: P:Windows.UI.Xaml.Controls.InkToolbar.InitialControls
-api-type: winrt property
---

<!-- Property syntax
public Windows.UI.Xaml.Controls.InkToolbarInitialControls InitialControls { get;  set; }
-->

# Windows.UI.Xaml.Controls.InkToolbar.InitialControls

## -description
Gets or sets the collection of built-in buttons added to the [InkToolbar](inktoolbar.md) at initialization.

This property overrides the default collection of built-in buttons.


By default, the [InkToolbar](inktoolbar.md) consists of two distinct groups of button types:

+ A [RadioButton](radiobutton.md) group containing the built-in drawing ([InkToolbarBallpointPenButton](inktoolbarballpointpenbutton.md), [InkToolbarPencilButton](inktoolbarpencilbutton.md)), erasing ([InkToolbarEraserButton](inktoolbareraserbutton.md)), and highlighting ([InkToolbarHighlighterButton](inktoolbarhighlighterbutton.md)) buttons. This group is where [InkToolbarCustomPenButton](inktoolbarcustompenbutton.md) and [InkToolbarCustomToolButton](inktoolbarcustomtoolbutton.md) objects are added.

> Feature selection is mutually exclusive.
+ A toggle button group containing the built-in ruler ([InkToolbarRulerButton](inktoolbarrulerbutton.md)) button. This group is where [InkToolbarCustomToggleButton](inktoolbarcustomtogglebutton.md) objects are added.

> Features are not mutually exclusive and can be used concurrently with other active tools.


## -property-value
The collection of built-in buttons to add to the [InkToolbar](inktoolbar.md).

## -remarks
Default built-in buttons, or those specified through [InitialControls](inktoolbar_initialcontrols.md), are not added to the [Children](inktoolbar_children.md) property.

Built-in or custom buttons added programmatically or declared in XAML, are added to the [Children](inktoolbar_children.md) property.

Built-in buttons are displayed in a pre-determined order within their respective control groups. Custom buttons are added to the appropriate control group in the order specified, after all built-in buttons.

## -examples

To specify which built-in buttons are displayed at initialization:

1. Set [InitialControls](inktoolbar_initialcontrols.md) to [None](inktoolbarinitialcontrols.md).
1. Add the individual buttons.
1. Specify the [InkToolbar](inktoolbar.md) UI experience, such as the default button.
The following examples (both XAML and code-behind) show how to clear the default buttons from the InkToolber, add ballpoint pen, pencil, and eraser buttons, and set the default button to pencil.

XAML



[!code-xml[UI](../windows.ui.input.inking/code/Ink_Basic_InkToolbar/csharp/MainPage.xaml#SnippetUI)]



[!code-xml[UI_CB](../windows.ui.input.inking/code/Ink_Basic_InkToolbar/csharp/MainPage_CodeBehind.xaml#SnippetUI_CB)]

[!code-csharp[InkToolbarMainPageCB](../windows.ui.input.inking/code/Ink_Basic_InkToolbar/csharp/MainPage_CodeBehind.xaml.cs#SnippetInkToolbarMainPageCB)]

[!code-csharp[InkToolbarLoadingCB](../windows.ui.input.inking/code/Ink_Basic_InkToolbar/csharp/MainPage_CodeBehind.xaml.cs#SnippetInkToolbarLoadingCB)]

[!code-csharp[InkToolbarLoadedCB](../windows.ui.input.inking/code/Ink_Basic_InkToolbar/csharp/MainPage_CodeBehind.xaml.cs#SnippetInkToolbarLoadedCB)]

## -see-also
[InitialControlsProperty](inktoolbar_initialcontrolsproperty.md)