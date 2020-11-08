---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093249"
---
# <span data-ttu-id="09797-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="09797-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="09797-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09797-102">SYNOPSIS</span></span>
<span data-ttu-id="09797-103">Skapar en volym i en angiven volym behållare.</span><span class="sxs-lookup"><span data-stu-id="09797-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="09797-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09797-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="09797-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09797-105">DESCRIPTION</span></span>
<span data-ttu-id="09797-106">Cmdleten **New-AzureStorSimpleDeviceVolume** skapar en volym i en angiven volym behållare.</span><span class="sxs-lookup"><span data-stu-id="09797-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="09797-107">Denna cmdlet associerar varje volym med en eller flera åtkomst kontroll poster.</span><span class="sxs-lookup"><span data-stu-id="09797-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="09797-108">Använd cmdleten **Get-AzureStorSimpleAccessControlRecord** för att hämta **AccessControlRecord** -objekt.</span><span class="sxs-lookup"><span data-stu-id="09797-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="09797-109">Ange ett namn, en storlek och AppType för volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="09797-110">Ange också om du vill skapa volymen online, om du vill aktivera standard säkerhets kopiering och om du vill aktivera övervakning.</span><span class="sxs-lookup"><span data-stu-id="09797-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="09797-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09797-111">EXAMPLES</span></span>

### <span data-ttu-id="09797-112">Exempel 1: skapa en volym</span><span class="sxs-lookup"><span data-stu-id="09797-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="09797-113">Det första kommandot får åtkomst kontroll posterna i StorSimple Manager-tjänsten genom att använda cmdleten **Get-AzureStorSimpleAccessControlRecord** och sedan lagra dem i $AcrList variabel.</span><span class="sxs-lookup"><span data-stu-id="09797-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="09797-114">Det andra kommandot får volymen med namnet VolumeContainer07 för enheten som heter Contoso63-AppVm genom att använda cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="09797-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="09797-115">Kommandot skickar den behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="09797-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="09797-116">Denna cmdlet skapar volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="09797-117">Kommandot anger namnet på volymen, storleken och åtkomst kontroll posterna som lagras i $AcrList.</span><span class="sxs-lookup"><span data-stu-id="09797-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="09797-118">Det här kommandot startar jobbet och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="09797-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="09797-119">Använd cmdleten **Get-AzureStorSimpleTask** för att se status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="09797-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="09797-120">Exempel 2: skapa en volym utan åtkomst Controlaccess kontroll recordsaccess kontroll</span><span class="sxs-lookup"><span data-stu-id="09797-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="09797-121">Det här kommandot får volymen med namnet VolumeContainer01 för enheten som heter Contoso63-AppVm genom att använda cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="09797-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="09797-122">Kommandot skickar den behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="09797-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="09797-123">Denna cmdlet skapar volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="09797-124">Kommandot anger namnet på volymen, storlek och ett tomt värde för åtkomst kontroll poster.</span><span class="sxs-lookup"><span data-stu-id="09797-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="09797-125">Det här kommandot anger parametern *WaitForComplete* , så att den returnerar en **TaskStatusInfo** när volymen har skapats.</span><span class="sxs-lookup"><span data-stu-id="09797-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="09797-126">Eftersom det inte finns några åtkomst kontroll poster på den här volymen kan den inte nås.</span><span class="sxs-lookup"><span data-stu-id="09797-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="09797-127">Du kan lägga till Access senare genom att använda cmdleten **set-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="09797-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="09797-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09797-128">PARAMETERS</span></span>

### <span data-ttu-id="09797-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="09797-129">-AccessControlRecords</span></span>
<span data-ttu-id="09797-130">Anger en lista över åtkomst kontroll poster som ska kopplas till volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09797-131">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="09797-131">-DeviceName</span></span>
<span data-ttu-id="09797-132">Anger namnet på den StorSimple-enhet där du vill skapa volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="09797-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="09797-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="09797-134">Anger om du vill aktivera standard säkerhets kopiering för volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-134">Specifies whether to enable default backup for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09797-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="09797-135">-EnableMonitoring</span></span>
<span data-ttu-id="09797-136">Anger om övervakning ska aktive ras för volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-136">Specifies whether to enable monitoring for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09797-137">-Online</span><span class="sxs-lookup"><span data-stu-id="09797-137">-Online</span></span>
<span data-ttu-id="09797-138">Anger om volymen är online.</span><span class="sxs-lookup"><span data-stu-id="09797-138">Specifies whether to create the volume online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09797-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="09797-139">-Profile</span></span>
<span data-ttu-id="09797-140">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="09797-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="09797-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="09797-141">-VolumeAppType</span></span>
<span data-ttu-id="09797-142">Anger om du vill skapa en primär eller Arkiv volym.</span><span class="sxs-lookup"><span data-stu-id="09797-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="09797-143">Giltiga värden är: PrimaryVolume och ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="09797-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09797-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="09797-144">-VolumeContainer</span></span>
<span data-ttu-id="09797-145">Anger behållaren som ett **DataContainer** -objekt där volymen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="09797-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="09797-146">Om du vill hämta ett **VirtualDisk** -objekt använder du cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="09797-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09797-147">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="09797-147">-VolumeName</span></span>
<span data-ttu-id="09797-148">Anger ett namn för den nya volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09797-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="09797-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="09797-150">Anger volym storleken i byte.</span><span class="sxs-lookup"><span data-stu-id="09797-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09797-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="09797-151">-WaitForComplete</span></span>
<span data-ttu-id="09797-152">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="09797-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="09797-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09797-153">CommonParameters</span></span>
<span data-ttu-id="09797-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09797-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09797-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09797-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09797-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09797-156">INPUTS</span></span>

### <span data-ttu-id="09797-157">DataContainer, lista\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="09797-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="09797-158">Denna cmdlet accepterar ett **DataContainer** -objekt och en lista med **AccessControlRecord** -objekt för den nya volymen.</span><span class="sxs-lookup"><span data-stu-id="09797-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="09797-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09797-159">OUTPUTS</span></span>

### <span data-ttu-id="09797-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="09797-160">TaskStatusInfo</span></span>
<span data-ttu-id="09797-161">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="09797-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="09797-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09797-162">NOTES</span></span>

## <span data-ttu-id="09797-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09797-163">RELATED LINKS</span></span>

[<span data-ttu-id="09797-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="09797-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="09797-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="09797-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="09797-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="09797-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="09797-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="09797-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="09797-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="09797-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="09797-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="09797-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


