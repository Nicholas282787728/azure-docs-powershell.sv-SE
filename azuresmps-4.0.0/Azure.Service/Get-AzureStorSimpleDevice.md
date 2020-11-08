---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C5A2A8D2-A840-4712-A8BD-F49C6063D193
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1156b4887e7b97d4e783ec738a939d320fe397a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099522"
---
# <span data-ttu-id="fced0-101">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="fced0-101">Get-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="fced0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fced0-102">SYNOPSIS</span></span>
<span data-ttu-id="fced0-103">Hämtar enheter som är anslutna till resursen.</span><span class="sxs-lookup"><span data-stu-id="fced0-103">Gets devices attached to the resource.</span></span>

## <span data-ttu-id="fced0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fced0-104">SYNTAX</span></span>

### <span data-ttu-id="fced0-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="fced0-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDevice [-Type <String>] [-ModelID <String>] [-Detailed] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="fced0-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="fced0-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDevice [-DeviceId <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fced0-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="fced0-107">IdentifyByName</span></span>
```
Get-AzureStorSimpleDevice [-DeviceName <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fced0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fced0-108">DESCRIPTION</span></span>
<span data-ttu-id="fced0-109">Cmdleten **Get-AzureStorSimpleDevice** hämtar en lista över StorSimple-enheter som är anslutna till resursen.</span><span class="sxs-lookup"><span data-stu-id="fced0-109">The **Get-AzureStorSimpleDevice** cmdlet gets a list of StorSimple devices attached to the resource.</span></span>
<span data-ttu-id="fced0-110">Du kan ange enhets-ID, namn, modell-ID och typ.</span><span class="sxs-lookup"><span data-stu-id="fced0-110">You can specify device ID, name, model ID, and type.</span></span>
<span data-ttu-id="fced0-111">Använd egenskapen **DeviceID** som hämtas genom att använda denna cmdlet för att ange enheter för andra StorSimple-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="fced0-111">Use the **DeviceID** property obtained by using this cmdlet to specify devices for other StorSimple cmdlets.</span></span>

## <span data-ttu-id="fced0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fced0-112">EXAMPLES</span></span>

### <span data-ttu-id="fced0-113">Exempel 1: Hämta tillgängliga enheter på en resurs</span><span class="sxs-lookup"><span data-stu-id="fced0-113">Example 1: Get available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice
DeviceId                  : 6f9ab151-39c7-4ded-b7d0-f5b0968f2766
DeviceName                : 8600-: SHX0881018G88
SerialNumber              : SHX0881018G88
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Offline
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0991018g00e4-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T16:32:30.2960842Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 12693995520

DeviceId                  : eb30ea31-c856-4cf2-9a02-aee611d6a3b9
DeviceName                : 8100-Delta 001
SerialNumber              : SHX90391XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8100
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8100-shx90193xxxxxxx-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T14:53:14.4219391Z
AvailableStorageInBytes   : 205509890146304
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 219902325555200
UsingStorageInBytes       : 23904321536

DeviceId                  : edcb0b9b-1ed5-4102-9c5d-c589f7632994
DeviceName                : 8600-Bravo 001
SerialNumber              : SHX0900915G44SY
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0900915g44sy-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T15:36:26.0870525Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 978893799424
```

<span data-ttu-id="fced0-114">Det här kommandot får alla tillgängliga enheter på en resurs.</span><span class="sxs-lookup"><span data-stu-id="fced0-114">This command gets all available devices on a resource.</span></span>
<span data-ttu-id="fced0-115">I det här exemplet är bara en enhet tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="fced0-115">In this example, only one device is available.</span></span>

### <span data-ttu-id="fced0-116">Exempel 2: Hämta specifika enheter på en resurs</span><span class="sxs-lookup"><span data-stu-id="fced0-116">Example 2: Get specific available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -DeviceName "8600-SHX90193XXXXXXX" -Type Appliance -ModelId "8600"
DeviceId                  : f9db31da-8a6c-4718-8f5b-5ce89e600f28
DeviceName                : 8600-SHX90193XXXXXXX
SerialNumber              : SHX90193XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx90193xxxxxxx-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T18:10:46.4524766Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 14445182976
```

<span data-ttu-id="fced0-117">Det här kommandot får alla tillgängliga enheter på en resurs med angivet namn, typ och modell-ID.</span><span class="sxs-lookup"><span data-stu-id="fced0-117">This command gets all available devices on a resource that have the specified name, type, and model ID.</span></span>

### <span data-ttu-id="fced0-118">Exempel 3: Hämta information för en enhet</span><span class="sxs-lookup"><span data-stu-id="fced0-118">Example 3: Get details for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -Name "8600-SHX90193XXXXXXX" -Type Appliance -Detailed
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : f9db31da-8a6c-4718-8f5b-5ce89e600f28
Name                           : 
NetInterfaceList               : {Data0, Data1, Data2, Data3...} 
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings

RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : Appliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings
```

<span data-ttu-id="fced0-119">Det här kommandot får alla tillgängliga enheter på en resurs som har det angivna namnet och typen.</span><span class="sxs-lookup"><span data-stu-id="fced0-119">This command gets all available devices on a resource that have the specified name and type.</span></span>
<span data-ttu-id="fced0-120">Det här kommandot anger den *detaljerade* parametern.</span><span class="sxs-lookup"><span data-stu-id="fced0-120">This command specifies the *Detailed* parameter.</span></span>
<span data-ttu-id="fced0-121">Kommandot ger ytterligare information om vilka enheter det returnerar.</span><span class="sxs-lookup"><span data-stu-id="fced0-121">The command provides additional details about the devices it returns.</span></span>

## <span data-ttu-id="fced0-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fced0-122">PARAMETERS</span></span>

### <span data-ttu-id="fced0-123">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="fced0-123">-Detailed</span></span>
<span data-ttu-id="fced0-124">Anger att denna cmdlet returnerar enhets uppgifter för de enheter som den får.</span><span class="sxs-lookup"><span data-stu-id="fced0-124">Indicates that this cmdlet returns device details for the devices that it gets.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fced0-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fced0-125">-DeviceId</span></span>
<span data-ttu-id="fced0-126">Anger instans-ID för enheten som ska visas.</span><span class="sxs-lookup"><span data-stu-id="fced0-126">Specifies the instance ID of the device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fced0-127">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="fced0-127">-DeviceName</span></span>
<span data-ttu-id="fced0-128">Anger namnet på den StorSimple-enhet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="fced0-128">Specifies the name of the StorSimple device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fced0-129">-ModelID</span><span class="sxs-lookup"><span data-stu-id="fced0-129">-ModelID</span></span>
<span data-ttu-id="fced0-130">Anger ID för den modell på StorSimple-enheter som ska visas.</span><span class="sxs-lookup"><span data-stu-id="fced0-130">Specifies the ID of the model of StorSimple devices to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fced0-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="fced0-131">-Profile</span></span>
<span data-ttu-id="fced0-132">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="fced0-132">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fced0-133">– Skriv</span><span class="sxs-lookup"><span data-stu-id="fced0-133">-Type</span></span>
<span data-ttu-id="fced0-134">Anger typen för en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="fced0-134">Specifies the type of a StorSimple device.</span></span>
<span data-ttu-id="fced0-135">Giltiga värden är: utrustning och VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="fced0-135">Valid values are: Appliance and VirtualAppliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fced0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fced0-136">CommonParameters</span></span>
<span data-ttu-id="fced0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fced0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fced0-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fced0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fced0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fced0-139">INPUTS</span></span>

### <span data-ttu-id="fced0-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="fced0-140">None</span></span>

## <span data-ttu-id="fced0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fced0-141">OUTPUTS</span></span>

### <span data-ttu-id="fced0-142">Lista \<DeviceDetails\> , IEnumerable\<DeviceInfo\></span><span class="sxs-lookup"><span data-stu-id="fced0-142">List\<DeviceDetails\>, IEnumerable\<DeviceInfo\></span></span>
<span data-ttu-id="fced0-143">Denna cmdlet returnerar ett **list \<DeviceDetails\>** objekt om du anger en *detaljerad* parameter.</span><span class="sxs-lookup"><span data-stu-id="fced0-143">This cmdlet returns a **List\<DeviceDetails\>** object, if you specify the *Detailed* parameter.</span></span>
<span data-ttu-id="fced0-144">Om du inte anger den parametern returnerar den ett **IEnumerable \<DeviceInfo\>** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fced0-144">If you do not specify that parameter, it returns an **IEnumerable\<DeviceInfo\>** object.</span></span>

## <span data-ttu-id="fced0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fced0-145">NOTES</span></span>

## <span data-ttu-id="fced0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fced0-146">RELATED LINKS</span></span>

[<span data-ttu-id="fced0-147">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="fced0-147">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="fced0-148">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="fced0-148">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


