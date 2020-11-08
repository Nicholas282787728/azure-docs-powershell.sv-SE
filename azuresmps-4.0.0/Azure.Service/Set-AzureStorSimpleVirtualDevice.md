---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093161"
---
# <span data-ttu-id="aebd4-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="aebd4-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="aebd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aebd4-102">SYNOPSIS</span></span>
<span data-ttu-id="aebd4-103">Skapar eller uppdaterar enhets konfigurationen för en virtuell StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="aebd4-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="aebd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aebd4-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aebd4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aebd4-105">DESCRIPTION</span></span>
<span data-ttu-id="aebd4-106">Cmdleten **set-AzureStorSimpleVirtualDevice** skapar eller uppdaterar enhets konfigurationen för en Azure StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="aebd4-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="aebd4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aebd4-107">EXAMPLES</span></span>

### <span data-ttu-id="aebd4-108">Exempel 1: uppdatera en virtuell enhet</span><span class="sxs-lookup"><span data-stu-id="aebd4-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="aebd4-109">I det första kommandot används **system. TimeZoneInfo** .NET-klass och standardsyntax för att hämta Pacific Standard Time Zone och lagra objektet i $TimeZoneInfo variabel.</span><span class="sxs-lookup"><span data-stu-id="aebd4-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="aebd4-110">Det andra kommandot uppdaterar enheten med namnet Contoso23 för att använda tids zonen som anges i $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="aebd4-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="aebd4-111">Kommandot kräver att den hemliga knappen har åtkomst till den virtuella enhetens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aebd4-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="aebd4-112">Exempel 2: uppdatera en virtuell enhet med pipeline-operatorn</span><span class="sxs-lookup"><span data-stu-id="aebd4-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="aebd4-113">Det här kommandot uppdaterar enheten med namnet Contoso23 för att använda den tidszon som kommandot skapar.</span><span class="sxs-lookup"><span data-stu-id="aebd4-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="aebd4-114">Kommandot kräver att den hemliga knappen har åtkomst till den virtuella enhetens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aebd4-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="aebd4-115">Det här kommandot fungerar på samma sätt som föregående exempel, förutom att tids zonen skickas till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="aebd4-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="aebd4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aebd4-116">PARAMETERS</span></span>

### <span data-ttu-id="aebd4-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="aebd4-117">-AdministratorPassword</span></span>
<span data-ttu-id="aebd4-118">Anger administratörs lösen ordet för den virtuella enhet som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="aebd4-118">Specifies the administrator password of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebd4-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="aebd4-119">-DeviceName</span></span>
<span data-ttu-id="aebd4-120">Anger namnet på den virtuella enhet som ska konfigureras.</span><span class="sxs-lookup"><span data-stu-id="aebd4-120">Specifies the name of the virtual device to configure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebd4-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="aebd4-121">-Profile</span></span>
<span data-ttu-id="aebd4-122">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="aebd4-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="aebd4-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="aebd4-123">-SecretKey</span></span>
<span data-ttu-id="aebd4-124">Anger en tjänst krypterings nycklar för den virtuella enheten.</span><span class="sxs-lookup"><span data-stu-id="aebd4-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="aebd4-125">Den här tangenten skapas när den första fysiska enheten registreras hos en resurs.</span><span class="sxs-lookup"><span data-stu-id="aebd4-125">This key is generated when the first physical device is registered with a resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebd4-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="aebd4-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="aebd4-127">Anger lösen ordet för Snapshot Manager.</span><span class="sxs-lookup"><span data-stu-id="aebd4-127">Specifies the snapshot manager password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebd4-128">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="aebd4-128">-TimeZone</span></span>
<span data-ttu-id="aebd4-129">Anger en tidszon för enheten.</span><span class="sxs-lookup"><span data-stu-id="aebd4-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="aebd4-130">Du kan skapa ett **TimeZoneInfo** -objekt med metoden **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="aebd4-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="aebd4-131">Det här kommandot skapar till exempel ett objekt för tids zons information för Pacific, normal tid: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="aebd4-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aebd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebd4-132">CommonParameters</span></span>
<span data-ttu-id="aebd4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aebd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebd4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aebd4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebd4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aebd4-135">INPUTS</span></span>

### <span data-ttu-id="aebd4-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="aebd4-136">TimeZoneInfo</span></span>
<span data-ttu-id="aebd4-137">Du kan ha ett **TimeZoneInfo** -objekt i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aebd4-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="aebd4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aebd4-138">OUTPUTS</span></span>

### <span data-ttu-id="aebd4-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="aebd4-139">DeviceJobDetails</span></span>
<span data-ttu-id="aebd4-140">Denna cmdlet returnerar uppdaterad enhets information för den virtuella enheten.</span><span class="sxs-lookup"><span data-stu-id="aebd4-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="aebd4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aebd4-141">NOTES</span></span>

## <span data-ttu-id="aebd4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aebd4-142">RELATED LINKS</span></span>

[<span data-ttu-id="aebd4-143">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="aebd4-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="aebd4-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="aebd4-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


