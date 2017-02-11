---
-api-id: T:Windows.System.Profile.HardwareIdentification
-api-type: winrt class
---

<!-- Class syntax.
public class HardwareIdentification 
-->

# Windows.System.Profile.HardwareIdentification

## -description
Provides the ability to obtain a hardware identifier that represents the current hardware.

## -remarks
See [Guidance on using the App Specific Hardware ID (ASHWID) to implement per-device app logic](http://msdn.microsoft.com/library/ee93f175-b0ce-42fd-9889-c43cd23eec6c) for more information.

> [!NOTE]
> : This class is not agile, which means that you need to consider its threading model and marshaling behavior. For more info, see [Threading and Marshaling (C++/CX)](http://go.microsoft.com/fwlink/p/?linkid=258275) and [Using Windows Runtime objects in a multithreaded environment (.NET)](http://go.microsoft.com/fwlink/p/?linkid=258277).

## -examples
The following code shows how to get the hardware id of a device using [GetPackageSpecificToken](hardwareidentification_getpackagespecifictoken.md).

```javascript
// nonce is an IBuffer object that would be sent from the cloud service.
var packageSpecificToken;

packageSpecificToken =  Windows.System.Profile.HardwareIdentification.getPackageSpecificToken(nonce);

// hardware id, signature, certificate IBuffer objects 
// that can be accessed through properties.
var hardwareId = packageSpecificToken.id;
var signature = packageSpecificToken.signature;
var certificate = packageSpecificToken.certificate;


```

```csharp
// nonce is an IBuffer object that would be sent from the cloud service.
HardwareToken packageSpecificToken;

packageSpecificToken =  Windows.System.Profile.HardwareIdentification.GetPackageSpecificToken(nonce);

// hardware id, signature, certificate IBuffer objects 
// that can be accessed through properties.
IBuffer hardwareId  = packageSpecificToken.Id;
IBuffer signature = packageSpecificToken.Signature;
IBuffer certificate = packageSpecificToken.Certificate;

```

```cpp
// nonce is an IBuffer object that would be sent from the cloud service.
HardwareToken^ packageSpecificToken;

packageSpecificToken =  Windows::System::Profile::HardwareIdentification::GetPackageSpecificToken(nonce);

// hardware id, signature, certificate IBuffer objects 
// that can be accessed through properties.
IBuffer^ hardwareId = packageSpecificToken->Id;
IBuffer^ signature = packageSpecificToken->Signature;
IBuffer^ certificate = packageSpecificToken->Certificate;



```

```vb
// nonce is an IBuffer object that would be sent from the cloud service.
Dim packageSpecificToken As Windows.System.Profile.HardwareToken

packageSpecificToken = Windows.System.Profile.HardwareIdentification.GetPackageSpecificToken(nonce)

// hardware id, signature, certificate IBuffer objects 
// that can be accessed through properties.
Dim hardwareId As Windows.Storage.Streams.IBuffer = packageSpecificToken.Id
Dim signature As Windows.Storage.Streams.IBuffer = packageSpecificToken.Signature
Dim certificate As Windows.Storage.Streams.IBuffer = packageSpecificToken.Certificate

```



## -see-also
[Guidance on using the App Specific Hardware ID (ASHWID) to implement per-device app logic](http://msdn.microsoft.com/library/ee93f175-b0ce-42fd-9889-c43cd23eec6c)