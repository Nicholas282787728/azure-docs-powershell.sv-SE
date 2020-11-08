---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099683"
---
# <span data-ttu-id="ad614-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ad614-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="ad614-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad614-102">SYNOPSIS</span></span>
<span data-ttu-id="ad614-103">Tar bort en volym behållare från en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="ad614-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="ad614-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad614-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ad614-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad614-105">DESCRIPTION</span></span>
<span data-ttu-id="ad614-106">Cmdleten **Remove-AzureStorSimpleDeviceVolumeContainer** tar bort ett volym behållar objekt från en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="ad614-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="ad614-107">Denna cmdlet uppmanar dig att bekräfta om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ad614-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="ad614-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad614-108">EXAMPLES</span></span>

### <span data-ttu-id="ad614-109">Exempel 1: ta bort en behållare genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="ad614-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="ad614-110">Det här kommandot får volymen med namnet Container08 på enheten som heter Contoso63-AppVm genom att använda cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="ad614-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="ad614-111">Kommandot skickar volym behållaren till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ad614-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ad614-112">Det här kommandot startar uppgiften för att ta bort behållaren och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad614-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="ad614-113">Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.</span><span class="sxs-lookup"><span data-stu-id="ad614-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="ad614-114">Det här kommandot anger parametern *Force* , så du behöver inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ad614-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ad614-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad614-115">PARAMETERS</span></span>

### <span data-ttu-id="ad614-116">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="ad614-116">-DeviceName</span></span>
<span data-ttu-id="ad614-117">Anger namnet på den StorSimple-enhet som du vill ta bort volymen för.</span><span class="sxs-lookup"><span data-stu-id="ad614-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

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

### <span data-ttu-id="ad614-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad614-118">-Force</span></span>
<span data-ttu-id="ad614-119">Anger att du inte behöver bekräfta med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad614-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="ad614-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad614-120">-Profile</span></span>
<span data-ttu-id="ad614-121">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="ad614-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ad614-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ad614-122">-VolumeContainer</span></span>
<span data-ttu-id="ad614-123">Anger volymen som ska tas bort som ett **DataContainer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad614-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="ad614-124">Om du vill hämta ett **DataContainer** -objekt använder du cmdleten **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="ad614-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad614-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ad614-125">-WaitForComplete</span></span>
<span data-ttu-id="ad614-126">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="ad614-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ad614-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad614-127">CommonParameters</span></span>
<span data-ttu-id="ad614-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad614-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad614-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad614-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad614-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad614-130">INPUTS</span></span>

### <span data-ttu-id="ad614-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="ad614-131">DataContainer</span></span>
<span data-ttu-id="ad614-132">Denna cmdlet accepterar ett **DataContainer** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ad614-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="ad614-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad614-133">OUTPUTS</span></span>

### <span data-ttu-id="ad614-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="ad614-134">TaskStatusInfo</span></span>
<span data-ttu-id="ad614-135">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="ad614-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="ad614-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad614-136">NOTES</span></span>

## <span data-ttu-id="ad614-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad614-137">RELATED LINKS</span></span>

[<span data-ttu-id="ad614-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ad614-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="ad614-139">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ad614-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


