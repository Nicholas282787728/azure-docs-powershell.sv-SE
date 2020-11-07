---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: c8de667ae818749e980d3e917838717ec3c85b07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924937"
---
# <span data-ttu-id="44b9c-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-101">Remove-AzVmss</span></span>

## <span data-ttu-id="44b9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="44b9c-103">Tar bort VMSS eller en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="44b9c-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="44b9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44b9c-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b9c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="44b9c-106">Cmdleten **Remove-AzVmss** tar bort den virtuella datorns skal uppsättning (VMSS) från Azure.</span><span class="sxs-lookup"><span data-stu-id="44b9c-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="44b9c-107">Denna cmdlet kan också användas för att ta bort en specifik virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="44b9c-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="44b9c-108">Du kan använda parametern *InstanceID* för att ta bort en specifik virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="44b9c-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="44b9c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44b9c-109">EXAMPLES</span></span>

### <span data-ttu-id="44b9c-110">Exempel 1: ta bort en VMSS</span><span class="sxs-lookup"><span data-stu-id="44b9c-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="44b9c-111">Det här kommandot tar bort VMSS-VMScaleSet001 som tillhör resurs gruppen som heter Group001.</span><span class="sxs-lookup"><span data-stu-id="44b9c-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="44b9c-112">Exempel 2: ta bort en virtuell dator från en VMSS</span><span class="sxs-lookup"><span data-stu-id="44b9c-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="44b9c-113">Det här kommandot tar bort den virtuella datorn med instans-ID 3 från VMSS-VMScaleSet002 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="44b9c-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="44b9c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44b9c-114">PARAMETERS</span></span>

### <span data-ttu-id="44b9c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44b9c-115">-AsJob</span></span>
<span data-ttu-id="44b9c-116">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="44b9c-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="44b9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b9c-117">-DefaultProfile</span></span>
<span data-ttu-id="44b9c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44b9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44b9c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="44b9c-119">-Force</span></span>
<span data-ttu-id="44b9c-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="44b9c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44b9c-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="44b9c-121">-InstanceId</span></span>
<span data-ttu-id="44b9c-122">Anger, som en sträng mat ris, ID: t för de instanser som måste startas.</span><span class="sxs-lookup"><span data-stu-id="44b9c-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="44b9c-123">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="44b9c-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="44b9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="44b9c-125">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="44b9c-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="44b9c-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="44b9c-126">-VMScaleSetName</span></span>
<span data-ttu-id="44b9c-127">Arter namnet på den VMSS som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="44b9c-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="44b9c-128">Om du anger *InstanceID* -parametern tas den angivna virtuella datorn bort från VMSS som heter med den här parametern.</span><span class="sxs-lookup"><span data-stu-id="44b9c-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="44b9c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44b9c-129">-Confirm</span></span>
<span data-ttu-id="44b9c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44b9c-130">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="44b9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b9c-131">-WhatIf</span></span>
<span data-ttu-id="44b9c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="44b9c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44b9c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="44b9c-133">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="44b9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b9c-134">CommonParameters</span></span>
<span data-ttu-id="44b9c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b9c-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b9c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b9c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44b9c-137">INPUTS</span></span>

### <span data-ttu-id="44b9c-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="44b9c-138">None</span></span>
<span data-ttu-id="44b9c-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="44b9c-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44b9c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44b9c-140">OUTPUTS</span></span>

### <span data-ttu-id="44b9c-141">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="44b9c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="44b9c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44b9c-142">NOTES</span></span>

## <span data-ttu-id="44b9c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44b9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="44b9c-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="44b9c-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="44b9c-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="44b9c-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="44b9c-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="44b9c-149">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="44b9c-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44b9c-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


