---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924758"
---
# <span data-ttu-id="f8730-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-101">Set-AzVmss</span></span>

## <span data-ttu-id="f8730-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8730-102">SYNOPSIS</span></span>
<span data-ttu-id="f8730-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8730-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="f8730-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8730-104">SYNTAX</span></span>

### <span data-ttu-id="f8730-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="f8730-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8730-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f8730-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8730-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8730-107">DESCRIPTION</span></span>
<span data-ttu-id="f8730-108">Cmdleten **set-AzVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f8730-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f8730-109">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="f8730-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="f8730-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8730-110">EXAMPLES</span></span>

### <span data-ttu-id="f8730-111">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="f8730-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f8730-112">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="f8730-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f8730-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8730-113">PARAMETERS</span></span>

### <span data-ttu-id="f8730-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8730-114">-AsJob</span></span>
<span data-ttu-id="f8730-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="f8730-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f8730-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8730-116">-DefaultProfile</span></span>
<span data-ttu-id="f8730-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8730-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f8730-118">-InstanceId</span></span>
<span data-ttu-id="f8730-119">Instans-ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f8730-119">The instance ID of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-120">-Ombild</span><span class="sxs-lookup"><span data-stu-id="f8730-120">-Reimage</span></span>
<span data-ttu-id="f8730-121">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8730-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="f8730-122">-ReimageAll</span></span>
<span data-ttu-id="f8730-123">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8730-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8730-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8730-125">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8730-125">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f8730-126">-VMScaleSetName</span></span>
<span data-ttu-id="f8730-127">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="f8730-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8730-128">-Confirm</span></span>
<span data-ttu-id="f8730-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8730-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8730-130">-WhatIf</span></span>
<span data-ttu-id="f8730-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8730-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8730-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8730-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8730-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8730-133">CommonParameters</span></span>
<span data-ttu-id="f8730-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8730-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8730-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8730-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8730-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8730-136">INPUTS</span></span>

### <span data-ttu-id="f8730-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="f8730-137">None</span></span>
<span data-ttu-id="f8730-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f8730-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8730-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8730-139">OUTPUTS</span></span>

### <span data-ttu-id="f8730-140">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f8730-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f8730-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8730-141">NOTES</span></span>

## <span data-ttu-id="f8730-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8730-142">RELATED LINKS</span></span>

[<span data-ttu-id="f8730-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f8730-144">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="f8730-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f8730-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="f8730-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f8730-148">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="f8730-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f8730-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


