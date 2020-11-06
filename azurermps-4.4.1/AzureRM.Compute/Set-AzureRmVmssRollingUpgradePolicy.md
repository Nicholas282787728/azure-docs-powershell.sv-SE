---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: dc147fa18d4db87b9a72aaf497f9fac59ea2a864
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573652"
---
# <span data-ttu-id="ce92a-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ce92a-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="ce92a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce92a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce92a-103">Anger princip egenskaperna för VMSS rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="ce92a-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce92a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce92a-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce92a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce92a-105">DESCRIPTION</span></span>
<span data-ttu-id="ce92a-106">Anger princip egenskaperna för VMSS rullande uppgradering.</span><span class="sxs-lookup"><span data-stu-id="ce92a-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="ce92a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce92a-107">EXAMPLES</span></span>

### <span data-ttu-id="ce92a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ce92a-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="ce92a-109">Det här kommandot anger 40 procent för MaxBatchInstance, 35 procent för MaxUnhealthyInstance, 30 procent för MaxUnhealthyUpgradedInstance och 30 sekunders paus tid mellan batchar för VMSS lokala objekt $vmss.</span><span class="sxs-lookup"><span data-stu-id="ce92a-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="ce92a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce92a-110">PARAMETERS</span></span>

### <span data-ttu-id="ce92a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce92a-111">-DefaultProfile</span></span>
<span data-ttu-id="ce92a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce92a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ce92a-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="ce92a-114">Maximalt procent av totalt antal virtuella dator instanser som kommer att uppgraderas samtidigt av den rullande uppgraderingen i en grupp.</span><span class="sxs-lookup"><span data-stu-id="ce92a-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="ce92a-115">Eftersom det är ett maximalt, kan felaktiga instanser i tidigare eller framtida batchar leda till att procent andelen instanser i en grupp minskar för att säkerställa högre pålitlighet.</span><span class="sxs-lookup"><span data-stu-id="ce92a-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="ce92a-116">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="ce92a-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ce92a-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="ce92a-118">Den maximala procent andelen av de totala virtuella dator instanserna i den skala som kan vara ohälsosamt, antingen som ett resultat av att den har uppgraderats, eller genom att hitta en felaktig status av hälso kontroller för den virtuella datorn innan den rullande uppgraderingen avbryts.</span><span class="sxs-lookup"><span data-stu-id="ce92a-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="ce92a-119">Det här villkoret kontrol leras innan en batch startas.</span><span class="sxs-lookup"><span data-stu-id="ce92a-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="ce92a-120">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="ce92a-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ce92a-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="ce92a-122">Den maximala procent andelen uppgraderade virtuella dator instanser som kan upptäckas vara felfria.</span><span class="sxs-lookup"><span data-stu-id="ce92a-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="ce92a-123">Denna kontroll sker efter att varje kommando har uppgraderats.</span><span class="sxs-lookup"><span data-stu-id="ce92a-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="ce92a-124">Om denna procents ATS överskrids avbryts den rullande uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="ce92a-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="ce92a-125">Om värdet inte anges är det inställt på 20.</span><span class="sxs-lookup"><span data-stu-id="ce92a-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="ce92a-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="ce92a-127">Vänte tiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa sats.</span><span class="sxs-lookup"><span data-stu-id="ce92a-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="ce92a-128">Tids längden ska anges i ISO 8601-format.</span><span class="sxs-lookup"><span data-stu-id="ce92a-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="ce92a-129">Standardvärdet är 0 sekunder (PT0S).</span><span class="sxs-lookup"><span data-stu-id="ce92a-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ce92a-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ce92a-131">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="ce92a-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="ce92a-132">Du kan använda New-AzureRmVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="ce92a-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce92a-133">-Confirm</span></span>
<span data-ttu-id="ce92a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce92a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce92a-135">-WhatIf</span></span>
<span data-ttu-id="ce92a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce92a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce92a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce92a-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce92a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce92a-138">CommonParameters</span></span>
<span data-ttu-id="ce92a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce92a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce92a-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce92a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce92a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce92a-141">INPUTS</span></span>

### <span data-ttu-id="ce92a-142">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ce92a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="ce92a-143">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="ce92a-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="ce92a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce92a-144">OUTPUTS</span></span>

### <span data-ttu-id="ce92a-145">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ce92a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ce92a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce92a-146">NOTES</span></span>

## <span data-ttu-id="ce92a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce92a-147">RELATED LINKS</span></span>

