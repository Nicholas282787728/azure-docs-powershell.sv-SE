---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 0d7e14657d22ac8f8431e82b51cee81d62d5328f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930309"
---
# <span data-ttu-id="c62ee-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="c62ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c62ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c62ee-103">Tar bort VMSS eller en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="c62ee-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c62ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c62ee-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c62ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c62ee-105">DESCRIPTION</span></span>
<span data-ttu-id="c62ee-106">Cmdleten **Remove-AzureRmVmss** tar bort den virtuella datorns skal uppsättning (VMSS) från Azure.</span><span class="sxs-lookup"><span data-stu-id="c62ee-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="c62ee-107">Denna cmdlet kan också användas för att ta bort en specifik virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="c62ee-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="c62ee-108">Du kan använda parametern *InstanceID* för att ta bort en specifik virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="c62ee-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="c62ee-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c62ee-109">EXAMPLES</span></span>

### <span data-ttu-id="c62ee-110">Exempel 1: ta bort en VMSS</span><span class="sxs-lookup"><span data-stu-id="c62ee-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="c62ee-111">Det här kommandot tar bort VMSS-VMScaleSet001 som tillhör resurs gruppen som heter Group001.</span><span class="sxs-lookup"><span data-stu-id="c62ee-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="c62ee-112">Exempel 2: ta bort en virtuell dator från en VMSS</span><span class="sxs-lookup"><span data-stu-id="c62ee-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="c62ee-113">Det här kommandot tar bort den virtuella datorn med instans-ID 3 från VMSS-VMScaleSet002 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="c62ee-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="c62ee-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c62ee-114">PARAMETERS</span></span>

### <span data-ttu-id="c62ee-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c62ee-115">-AsJob</span></span>
<span data-ttu-id="c62ee-116">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="c62ee-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c62ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62ee-117">-DefaultProfile</span></span>
<span data-ttu-id="c62ee-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c62ee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c62ee-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c62ee-119">-Force</span></span>
<span data-ttu-id="c62ee-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c62ee-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c62ee-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c62ee-121">-InstanceId</span></span>
<span data-ttu-id="c62ee-122">Anger, som en sträng mat ris, ID: t för de instanser som måste startas.</span><span class="sxs-lookup"><span data-stu-id="c62ee-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="c62ee-123">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c62ee-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="c62ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="c62ee-125">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="c62ee-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="c62ee-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c62ee-126">-VMScaleSetName</span></span>
<span data-ttu-id="c62ee-127">Arter namnet på den VMSS som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c62ee-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="c62ee-128">Om du anger *InstanceID* -parametern tas den angivna virtuella datorn bort från VMSS som heter med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="c62ee-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="c62ee-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c62ee-129">-Confirm</span></span>
<span data-ttu-id="c62ee-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c62ee-130">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="c62ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c62ee-131">-WhatIf</span></span>
<span data-ttu-id="c62ee-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c62ee-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c62ee-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c62ee-133">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="c62ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62ee-134">CommonParameters</span></span>
<span data-ttu-id="c62ee-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62ee-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c62ee-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62ee-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c62ee-137">INPUTS</span></span>

### <span data-ttu-id="c62ee-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="c62ee-138">None</span></span>
<span data-ttu-id="c62ee-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c62ee-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c62ee-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c62ee-140">OUTPUTS</span></span>

### <span data-ttu-id="c62ee-141">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c62ee-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c62ee-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c62ee-142">NOTES</span></span>

## <span data-ttu-id="c62ee-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c62ee-143">RELATED LINKS</span></span>

[<span data-ttu-id="c62ee-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c62ee-145">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c62ee-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c62ee-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c62ee-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c62ee-149">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c62ee-150">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c62ee-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


