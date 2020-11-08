---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093292"
---
# <span data-ttu-id="981f6-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="981f6-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="981f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="981f6-102">SYNOPSIS</span></span>
<span data-ttu-id="981f6-103">Hämtar volymer på en enhet.</span><span class="sxs-lookup"><span data-stu-id="981f6-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="981f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="981f6-104">SYNTAX</span></span>

### <span data-ttu-id="981f6-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="981f6-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="981f6-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="981f6-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="981f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="981f6-107">DESCRIPTION</span></span>
<span data-ttu-id="981f6-108">Cmdleten **Get-AzureStorSimpleDeviceVolume** hämtar en lista med volymer för en viss volym behållare eller volym som har det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="981f6-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="981f6-109">Det returnerade objektet innehåller följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="981f6-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="981f6-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="981f6-110">**AccessType**</span></span>
- <span data-ttu-id="981f6-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="981f6-111">**AcrList**</span></span>
- <span data-ttu-id="981f6-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="981f6-112">**AppType**</span></span>
- <span data-ttu-id="981f6-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="981f6-113">**DataContainer**</span></span>
- <span data-ttu-id="981f6-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="981f6-114">**DataContainerId**</span></span>
- <span data-ttu-id="981f6-115">**Instans**</span><span class="sxs-lookup"><span data-stu-id="981f6-115">**InstanceId**</span></span>
- <span data-ttu-id="981f6-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="981f6-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="981f6-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="981f6-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="981f6-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="981f6-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="981f6-119">**Namn**</span><span class="sxs-lookup"><span data-stu-id="981f6-119">**Name**</span></span>
- <span data-ttu-id="981f6-120">**Support**</span><span class="sxs-lookup"><span data-stu-id="981f6-120">**Online**</span></span>
- <span data-ttu-id="981f6-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="981f6-121">**OperationInProgress**</span></span>
- <span data-ttu-id="981f6-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="981f6-122">**SizeInBytes**</span></span>
- <span data-ttu-id="981f6-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="981f6-123">**VSN**</span></span>

## <span data-ttu-id="981f6-124">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="981f6-124">EXAMPLES</span></span>

### <span data-ttu-id="981f6-125">Exempel 1: Hämta volymer i en angiven behållare</span><span class="sxs-lookup"><span data-stu-id="981f6-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="981f6-126">Det här kommandot får volymen med namnet Container03 på enheten som heter Contoso63-AppVm genom att använda cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="981f6-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="981f6-127">Kommandot använder pipeline-operatorn för att skicka behållaren till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="981f6-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="981f6-128">Denna cmdlet får alla volymer i behållaren för enheten med namnet Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="981f6-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="981f6-129">Exempel 2: skaffa en volym med dess namn</span><span class="sxs-lookup"><span data-stu-id="981f6-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="981f6-130">Det här kommandot får volymen som heter Volume18 på enheten Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="981f6-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="981f6-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="981f6-131">PARAMETERS</span></span>

### <span data-ttu-id="981f6-132">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="981f6-132">-DeviceName</span></span>
<span data-ttu-id="981f6-133">Anger namnet på den StorSimple-enhet som du vill hämta volymer från.</span><span class="sxs-lookup"><span data-stu-id="981f6-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="981f6-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="981f6-134">-Profile</span></span>
<span data-ttu-id="981f6-135">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="981f6-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="981f6-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="981f6-136">-VolumeContainer</span></span>
<span data-ttu-id="981f6-137">Anger volym containern, som ett **DataContainer** -objekt, som innehåller de volymer som ska visas.</span><span class="sxs-lookup"><span data-stu-id="981f6-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="981f6-138">För att få en **DataContainer** använder du cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="981f6-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="981f6-139">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="981f6-139">-VolumeName</span></span>
<span data-ttu-id="981f6-140">Anger namnet på den volym som ska visas.</span><span class="sxs-lookup"><span data-stu-id="981f6-140">Specifies the name of the volume to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="981f6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981f6-141">CommonParameters</span></span>
<span data-ttu-id="981f6-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="981f6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981f6-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981f6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981f6-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="981f6-144">INPUTS</span></span>

### <span data-ttu-id="981f6-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="981f6-145">DataContainer</span></span>
<span data-ttu-id="981f6-146">Denna cmdlet accepterar ett **DataContainer** -objekt som innehåller volymen som ska användas.</span><span class="sxs-lookup"><span data-stu-id="981f6-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="981f6-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="981f6-147">OUTPUTS</span></span>

### <span data-ttu-id="981f6-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="981f6-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="981f6-149">Denna cmdlet returnerar ett **VirtualDisk** -objekt om du anger parametern *volym* namn.</span><span class="sxs-lookup"><span data-stu-id="981f6-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="981f6-150">Om du anger *VolumeContainer* returnerar denna cmdlet ett **ilist \<VirtualDisk\>** -objekt.</span><span class="sxs-lookup"><span data-stu-id="981f6-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="981f6-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="981f6-151">NOTES</span></span>

## <span data-ttu-id="981f6-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="981f6-152">RELATED LINKS</span></span>

[<span data-ttu-id="981f6-153">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="981f6-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="981f6-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="981f6-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="981f6-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="981f6-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="981f6-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="981f6-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


