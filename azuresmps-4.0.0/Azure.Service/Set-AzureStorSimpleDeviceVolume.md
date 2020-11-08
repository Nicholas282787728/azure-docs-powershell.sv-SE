---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099648"
---
# <span data-ttu-id="38680-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="38680-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="38680-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38680-102">SYNOPSIS</span></span>
<span data-ttu-id="38680-103">Uppdaterar egenskaperna för en befintlig volym.</span><span class="sxs-lookup"><span data-stu-id="38680-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="38680-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38680-104">SYNTAX</span></span>

### <span data-ttu-id="38680-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="38680-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="38680-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="38680-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38680-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38680-107">DESCRIPTION</span></span>
<span data-ttu-id="38680-108">Cmdleten **set-AzureStorSimpleDeviceVolume** uppdaterar egenskaperna för en befintlig volym.</span><span class="sxs-lookup"><span data-stu-id="38680-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="38680-109">Denna cmdlet associerar en volym med en eller flera åtkomst kontroll poster.</span><span class="sxs-lookup"><span data-stu-id="38680-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="38680-110">Använd cmdleten **Get-AzureStorSimpleAccessControlRecord** för att hämta **AccessControlRecord** -objekt.</span><span class="sxs-lookup"><span data-stu-id="38680-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="38680-111">Uppdatera volymens storlek eller typ.</span><span class="sxs-lookup"><span data-stu-id="38680-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="38680-112">Uppdatera också om du vill skapa volymen online.</span><span class="sxs-lookup"><span data-stu-id="38680-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="38680-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38680-113">EXAMPLES</span></span>

### <span data-ttu-id="38680-114">Exempel 1: uppdatera värdet online för en volym</span><span class="sxs-lookup"><span data-stu-id="38680-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="38680-115">Det här kommandot uppdaterar volymen som heter Volume18 för att ha ett online-värde för $False.</span><span class="sxs-lookup"><span data-stu-id="38680-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="38680-116">Det här kommandot startar uppgiften och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="38680-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="38680-117">Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.</span><span class="sxs-lookup"><span data-stu-id="38680-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="38680-118">Exempel 2: ändra värdet för online och skriv</span><span class="sxs-lookup"><span data-stu-id="38680-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="38680-119">Det här kommandot uppdaterar volymen som heter Volume18.</span><span class="sxs-lookup"><span data-stu-id="38680-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="38680-120">Den ändrar typen och ändrar värdet för parametern *online* till $true.</span><span class="sxs-lookup"><span data-stu-id="38680-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="38680-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38680-121">PARAMETERS</span></span>

### <span data-ttu-id="38680-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="38680-122">-AccessControlRecords</span></span>
<span data-ttu-id="38680-123">Anger en lista över åtkomst kontroll poster som ska kopplas till volymen.</span><span class="sxs-lookup"><span data-stu-id="38680-123">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38680-124">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="38680-124">-DeviceName</span></span>
<span data-ttu-id="38680-125">Anger namnet på den StorSimple-enhet som volymen ska uppdateras på.</span><span class="sxs-lookup"><span data-stu-id="38680-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="38680-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="38680-126">-InformationAction</span></span>
<span data-ttu-id="38680-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="38680-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38680-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="38680-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38680-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="38680-129">Continue</span></span>
- <span data-ttu-id="38680-130">Över</span><span class="sxs-lookup"><span data-stu-id="38680-130">Ignore</span></span>
- <span data-ttu-id="38680-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="38680-131">Inquire</span></span>
- <span data-ttu-id="38680-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38680-132">SilentlyContinue</span></span>
- <span data-ttu-id="38680-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="38680-133">Stop</span></span>
- <span data-ttu-id="38680-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="38680-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38680-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38680-135">-InformationVariable</span></span>
<span data-ttu-id="38680-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="38680-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38680-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="38680-137">-NewName</span></span>
<span data-ttu-id="38680-138">Anger ett nytt namn på StorSimple-enheten.</span><span class="sxs-lookup"><span data-stu-id="38680-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="38680-139">-Online</span><span class="sxs-lookup"><span data-stu-id="38680-139">-Online</span></span>
<span data-ttu-id="38680-140">Anger om volymen är online.</span><span class="sxs-lookup"><span data-stu-id="38680-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38680-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="38680-141">-Profile</span></span>
<span data-ttu-id="38680-142">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="38680-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="38680-143">-Volym</span><span class="sxs-lookup"><span data-stu-id="38680-143">-Volume</span></span>
<span data-ttu-id="38680-144">Anger namnet på volymen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="38680-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38680-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="38680-145">-VolumeAppType</span></span>
<span data-ttu-id="38680-146">Anger om volymen ska uppdateras till primär eller Arkiv volym.</span><span class="sxs-lookup"><span data-stu-id="38680-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="38680-147">Giltiga värden är: PrimaryVolume och ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="38680-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38680-148">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="38680-148">-VolumeName</span></span>
<span data-ttu-id="38680-149">Anger namnet på volymen som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="38680-149">Specifies the name of the volume to update.</span></span>

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

### <span data-ttu-id="38680-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="38680-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="38680-151">Anger den uppdaterade storleken i byte för volymen.</span><span class="sxs-lookup"><span data-stu-id="38680-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38680-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="38680-152">-WaitForComplete</span></span>
<span data-ttu-id="38680-153">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="38680-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="38680-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38680-154">CommonParameters</span></span>
<span data-ttu-id="38680-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38680-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38680-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38680-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38680-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38680-157">INPUTS</span></span>

### <span data-ttu-id="38680-158">Förteckning\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="38680-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="38680-159">Denna cmdlet accepterar en lista med **AccessControlRecord** -objekt som ska kopplas till en volym.</span><span class="sxs-lookup"><span data-stu-id="38680-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="38680-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38680-160">OUTPUTS</span></span>

### <span data-ttu-id="38680-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="38680-161">TaskStatusInfo</span></span>
<span data-ttu-id="38680-162">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="38680-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="38680-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38680-163">NOTES</span></span>

## <span data-ttu-id="38680-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38680-164">RELATED LINKS</span></span>

[<span data-ttu-id="38680-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="38680-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="38680-166">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="38680-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="38680-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="38680-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="38680-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="38680-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="38680-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="38680-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


