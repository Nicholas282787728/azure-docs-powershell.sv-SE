---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578284"
---
# <span data-ttu-id="de1ee-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="de1ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="de1ee-103">Tar bort VMSS eller en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="de1ee-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de1ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de1ee-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de1ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de1ee-105">DESCRIPTION</span></span>
<span data-ttu-id="de1ee-106">Cmdleten **Remove-AzureRmVmss** tar bort den virtuella datorns skal uppsättning (VMSS) från Azure.</span><span class="sxs-lookup"><span data-stu-id="de1ee-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="de1ee-107">Denna cmdlet kan också användas för att ta bort en specifik virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="de1ee-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="de1ee-108">Du kan använda parametern *InstanceID* för att ta bort en specifik virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="de1ee-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="de1ee-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de1ee-109">EXAMPLES</span></span>

### <span data-ttu-id="de1ee-110">Exempel 1: ta bort en VMSS</span><span class="sxs-lookup"><span data-stu-id="de1ee-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="de1ee-111">Det här kommandot tar bort VMSS-VMScaleSet001 som tillhör resurs gruppen som heter Group001.</span><span class="sxs-lookup"><span data-stu-id="de1ee-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="de1ee-112">Exempel 2: ta bort en virtuell dator från en VMSS</span><span class="sxs-lookup"><span data-stu-id="de1ee-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="de1ee-113">Det här kommandot tar bort den virtuella datorn med instans-ID 3 från VMSS-VMScaleSet002 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="de1ee-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="de1ee-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de1ee-114">PARAMETERS</span></span>

### <span data-ttu-id="de1ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="de1ee-115">-Force</span></span>
<span data-ttu-id="de1ee-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="de1ee-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de1ee-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="de1ee-117">-InstanceId</span></span>
<span data-ttu-id="de1ee-118">Anger, som en sträng mat ris, ID: t för de instanser som måste startas.</span><span class="sxs-lookup"><span data-stu-id="de1ee-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="de1ee-119">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="de1ee-119">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="de1ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de1ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="de1ee-121">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="de1ee-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="de1ee-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="de1ee-122">-VMScaleSetName</span></span>
<span data-ttu-id="de1ee-123">Arter namnet på den VMSS som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="de1ee-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="de1ee-124">Om du anger *InstanceID* -parametern tas den angivna virtuella datorn bort från VMSS som heter med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="de1ee-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="de1ee-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de1ee-125">-Confirm</span></span>
<span data-ttu-id="de1ee-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de1ee-126">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de1ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de1ee-127">-WhatIf</span></span>
<span data-ttu-id="de1ee-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de1ee-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de1ee-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de1ee-129">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de1ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1ee-130">CommonParameters</span></span>
<span data-ttu-id="de1ee-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1ee-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de1ee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1ee-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de1ee-133">INPUTS</span></span>

### <span data-ttu-id="de1ee-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="de1ee-134">None</span></span>
<span data-ttu-id="de1ee-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="de1ee-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de1ee-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de1ee-136">OUTPUTS</span></span>

## <span data-ttu-id="de1ee-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de1ee-137">NOTES</span></span>

## <span data-ttu-id="de1ee-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de1ee-138">RELATED LINKS</span></span>

[<span data-ttu-id="de1ee-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="de1ee-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="de1ee-141">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="de1ee-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="de1ee-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="de1ee-144">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="de1ee-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="de1ee-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


