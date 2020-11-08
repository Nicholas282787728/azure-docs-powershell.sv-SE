---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A62D1A9D-C0EF-4305-B1F9-3AE68A79222D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a5023abffae6bbc2b70b7400e604ffabb1d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099690"
---
# <span data-ttu-id="f3c7f-101">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f3c7f-101">Remove-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="f3c7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c7f-103">Tar bort en volym från en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-103">Removes a volume from a StorSimple device.</span></span>

## <span data-ttu-id="f3c7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3c7f-104">SYNTAX</span></span>

### <span data-ttu-id="f3c7f-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="f3c7f-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3c7f-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="f3c7f-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3c7f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3c7f-107">DESCRIPTION</span></span>
<span data-ttu-id="f3c7f-108">Cmdleten **Remove-AzureStorSimpleDeviceVolume** tar bort en volym från en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-108">The **Remove-AzureStorSimpleDeviceVolume** cmdlet removes a volume from a StorSimple device.</span></span>
<span data-ttu-id="f3c7f-109">Denna cmdlet uppmanar dig att bekräfta om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="f3c7f-109">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="f3c7f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c7f-111">Exempel 1: ta bort en volym med pipelinen</span><span class="sxs-lookup"><span data-stu-id="f3c7f-111">Example 1: Remove a volume by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" | Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: 2933e24d-9564-42b5-9053-5f0bc4f59ea8_PS
VERBOSE: ClientRequestId: 7c2d854b-537a-4253-bb0c-c15bc8aa2b49_PS
VERBOSE: ClientRequestId: 4bf749ac-517c-49e7-8027-a8f62e272014_PS
VERBOSE: ClientRequestId: 7d9ec87a-616d-4ca9-bfb8-158859174d59_PS

Confirm
Are you sure you want to remove the volume? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 67a38e28-a015-44b1-8159-c1a6604f4d81_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: 56101c10-07ca-40f4-8f19-c6fdd895e3a5_PS
32925451-4451-4478-89f7-d8930505d3fb
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
32925451-4451-4478-89f7-d8930505d3fb for tracking the task's status
VERBOSE: Volume with name: Volume18 is found.
```

<span data-ttu-id="f3c7f-112">Det här kommandot får volymen som heter Volume18 på den enhet som heter Contoso63-AppVm och överför den volymen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-112">This command gets the volume named Volume18 on the device named Contoso63-AppVm, and then passes that volume to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3c7f-113">Den aktuella cmdleten startar aktiviteten som tar bort volymen och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-113">The current cmdlet starts the task that removes the volume, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="f3c7f-114">Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="f3c7f-115">Kommandot anger inte parametern *Force* , så cmdlet uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-115">The command does not specify the *Force* parameter, so the cmdlet prompts you for confirmation.</span></span>

### <span data-ttu-id="f3c7f-116">Exempel 2: ta bort en volym utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="f3c7f-116">Example 2: Remove a volume without confirmation</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Force
VERBOSE: ClientRequestId: 72f13290-41eb-4ac4-9535-da1a42d0fa0b_PS
VERBOSE: ClientRequestId: ae0c1d99-1a66-4a69-9260-f2c8c12546bd_PS
VERBOSE: ClientRequestId: 9610744f-d031-488f-87e6-3ecddb305e13_PS
VERBOSE: About to run a job to remove your volume! 
VERBOSE: ClientRequestId: d33525d8-7276-4d2a-942d-d10f8078f1f7_PS
483f8cb4-ebc3-46a9-a9e6-0989e25738a0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
483f8cb4-ebc3-46a9-a9e6-0989e25738a0 for tracking the task's status
```

<span data-ttu-id="f3c7f-117">Det här kommandot tar bort volymen som heter Volume18 från enheten Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-117">This command removes the volume named Volume18 from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="f3c7f-118">Kommandot anger parametern *Force* , så cmdleten ber dig inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-118">The command specifies the *Force* parameter, so the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f3c7f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3c7f-119">PARAMETERS</span></span>

### <span data-ttu-id="f3c7f-120">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="f3c7f-120">-DeviceName</span></span>
<span data-ttu-id="f3c7f-121">Anger namnet på den StorSimple-enhet där volymen ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-121">Specifies the name of the StorSimple device on which to the volume to remove exists.</span></span>

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

### <span data-ttu-id="f3c7f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f3c7f-122">-Force</span></span>
<span data-ttu-id="f3c7f-123">Anger att du inte behöver bekräfta med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-123">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="f3c7f-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3c7f-124">-Profile</span></span>
<span data-ttu-id="f3c7f-125">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-125">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f3c7f-126">-Volym</span><span class="sxs-lookup"><span data-stu-id="f3c7f-126">-Volume</span></span>
<span data-ttu-id="f3c7f-127">Anger vilken volym som ska tas bort som ett **VirtualDisk** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-127">Specifies the volume to remove, as a **VirtualDisk** object.</span></span>
<span data-ttu-id="f3c7f-128">Om du vill hämta ett **VirtualDisk** -objekt använder du cmdleten **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="f3c7f-128">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

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

### <span data-ttu-id="f3c7f-129">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="f3c7f-129">-VolumeName</span></span>
<span data-ttu-id="f3c7f-130">Anger namnet på den volym som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-130">Specifies the name of the volume to remove.</span></span>

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

### <span data-ttu-id="f3c7f-131">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f3c7f-131">-WaitForComplete</span></span>
<span data-ttu-id="f3c7f-132">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-132">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f3c7f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c7f-133">CommonParameters</span></span>
<span data-ttu-id="f3c7f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c7f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c7f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c7f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3c7f-136">INPUTS</span></span>

### <span data-ttu-id="f3c7f-137">VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="f3c7f-137">VirtualDisk</span></span>
<span data-ttu-id="f3c7f-138">Denna cmdlet godkänner antingen det **VirtualDisk** -objekt som ska tas bort eller volym namnet på **VirtualDisk** som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f3c7f-138">This cmdlet accepts either the **VirtualDisk** object to delete or the volume name of the **VirtualDisk** to delete.</span></span>

## <span data-ttu-id="f3c7f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3c7f-139">OUTPUTS</span></span>

### <span data-ttu-id="f3c7f-140">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="f3c7f-140">TaskStatusInfo</span></span>
<span data-ttu-id="f3c7f-141">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="f3c7f-141">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="f3c7f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3c7f-142">NOTES</span></span>

## <span data-ttu-id="f3c7f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3c7f-143">RELATED LINKS</span></span>

[<span data-ttu-id="f3c7f-144">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f3c7f-144">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="f3c7f-145">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f3c7f-145">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="f3c7f-146">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="f3c7f-146">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="f3c7f-147">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="f3c7f-147">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


