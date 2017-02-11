---
-api-id: T:Windows.UI.Xaml.Automation.Peers.RadioButtonAutomationPeer
-api-type: winrt class
---

<!-- Class syntax.
public class RadioButtonAutomationPeer : Windows.UI.Xaml.Automation.Peers.ToggleButtonAutomationPeer, Windows.UI.Xaml.Automation.Peers.IRadioButtonAutomationPeer, Windows.UI.Xaml.Automation.Provider.ISelectionItemProvider
-->

# Windows.UI.Xaml.Automation.Peers.RadioButtonAutomationPeer

## -description
Exposes [RadioButton](../windows.ui.xaml.controls/radiobutton.md) types to Microsoft UI Automation.

## -remarks
The Windows Runtime  [RadioButton](../windows.ui.xaml.controls/radiobutton.md) class creates a new [RadioButtonAutomationPeer](radiobuttonautomationpeer.md) as its [OnCreateAutomationPeer](../windows.ui.xaml/uielement_oncreateautomationpeer.md) definition. Derive your automation peer from [RadioButtonAutomationPeer](radiobuttonautomationpeer.md) if you are deriving a custom class from [RadioButton](../windows.ui.xaml.controls/radiobutton.md) and want to add automation support for additional features that you enabled in your custom class. Then override [OnCreateAutomationPeer](../windows.ui.xaml/uielement_oncreateautomationpeer.md) so that it returns your custom peer.

### Default peer implementation and overrides in **RadioButtonAutomationPeer**

[RadioButtonAutomationPeer](radiobuttonautomationpeer.md) has overrides of **Core** methods such that the associated [AutomationPeer](automationpeer.md) methods provide peer-specific information to a Microsoft UI Automation client.

+ [GetPattern](automationpeer_getpattern.md) reports that the peer provides pattern support for [PatternInterface.SelectionItem](patterninterface.md) ([ISelectionItemProvider](../windows.ui.xaml.automation.provider/iselectionitemprovider.md)). Also, the [ToggleButtonAutomationPeer](togglebuttonautomationpeer.md) peer base reports support for [PatternInterface.Toggle](patterninterface.md) ([IToggleProvider](../windows.ui.xaml.automation.provider/itoggleprovider.md)).
+ [GetClassName](automationpeer_getclassname.md) returns "RadioButton".
+ [GetAutomationControlType](automationpeer_getautomationcontroltype.md) returns [AutomationControlType.RadioButton](automationcontroltype.md).
+ [IsControlElement](automationpeer_iscontrolelement.md) returns **true**.
<!--not sure how this gets set cannot see in the partial cpp-->
This peer has the base classes [ButtonBaseAutomationPeer](buttonbaseautomationpeer.md) and [ToggleButtonAutomationPeer](togglebuttonautomationpeer.md) and inherits behavior other than the overrides indicated above. Notably, [GetName](automationpeer_getname.md) returns a string value based on examining the current **Content**. For more info, see [ButtonBaseAutomationPeer](buttonbaseautomationpeer.md).

The peer also has other behaviors that are provided by the base [FrameworkElementAutomationPeer](frameworkelementautomationpeer.md) class. For more info, see "Base implementation in FrameworkElementAutomationPeer" section of [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4).

## -examples

## -see-also
[RadioButton](../windows.ui.xaml.controls/radiobutton.md), [ToggleButtonAutomationPeer](togglebuttonautomationpeer.md), [IToggleProvider](../windows.ui.xaml.automation.provider/itoggleprovider.md), [ISelectionItemProvider](../windows.ui.xaml.automation.provider/iselectionitemprovider.md), [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4)