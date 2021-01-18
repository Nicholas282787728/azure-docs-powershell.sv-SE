---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521631"
---
# <span data-ttu-id="c667e-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c667e-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="c667e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c667e-102">SYNOPSIS</span></span>
<span data-ttu-id="c667e-103">Skapar en resurs grupp som en mall och sparar den i en fil.</span><span class="sxs-lookup"><span data-stu-id="c667e-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="c667e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c667e-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c667e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c667e-105">DESCRIPTION</span></span>
<span data-ttu-id="c667e-106">Cmdleten **export-AzResourceGroup** fångar den angivna resurs gruppen som en mall och sparar den i en JSON-fil. Det här kan vara användbart i de fall då du redan har skapat resurser i resurs gruppen och sedan vill använda en mall för distribution av mallar.</span><span class="sxs-lookup"><span data-stu-id="c667e-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="c667e-107">Denna cmdlet är ett enkelt sätt att börja skapa en mall för de befintliga resurserna i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c667e-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="c667e-108">Det kan finnas vissa fall där denna cmdlet inte kan generera vissa delar av mallen.</span><span class="sxs-lookup"><span data-stu-id="c667e-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="c667e-109">Varnings meddelanden meddelar dig om de resurser som misslyckats.</span><span class="sxs-lookup"><span data-stu-id="c667e-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="c667e-110">Mallen skapas fortfarande för de delar som lyckades.</span><span class="sxs-lookup"><span data-stu-id="c667e-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="c667e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c667e-111">EXAMPLES</span></span>

### <span data-ttu-id="c667e-112">Exempel 1: exportera en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c667e-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="c667e-113">Det här kommandot fångar resurs gruppen som heter TestGroup som en mall och sparar den i en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="c667e-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="c667e-114">Exempel 2: exportera en enstaka resurs från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c667e-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="c667e-115">Det här kommandot fångar upp den virtuella dator resursen med namnet "TestVirtualMachine" från resurs gruppen "TestGroup" som en mall och sparar den i en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="c667e-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="c667e-116">Exempel 3: exportera ett urval av resurser från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c667e-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="c667e-117">Det här kommandot fångar in två resurser från resurs gruppen "TestGroup" som en mall och sparar den i en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="c667e-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="c667e-118">Den genererade mallen kommer inte att innehålla några genererade parametrar.</span><span class="sxs-lookup"><span data-stu-id="c667e-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="c667e-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c667e-119">PARAMETERS</span></span>

### <span data-ttu-id="c667e-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c667e-120">-ApiVersion</span></span>
<span data-ttu-id="c667e-121">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c667e-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c667e-122">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="c667e-122">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c667e-123">-DefaultProfile</span></span>
<span data-ttu-id="c667e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c667e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c667e-125">-Force</span></span>
<span data-ttu-id="c667e-126">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c667e-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="c667e-127">-IncludeComments</span></span>
<span data-ttu-id="c667e-128">Anger att den här åtgärden exporterar mallen med kommentarer.</span><span class="sxs-lookup"><span data-stu-id="c667e-128">Indicates that this operation exports the template with comments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="c667e-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="c667e-130">Anger att den här åtgärden exporterar mallparameter med standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="c667e-130">Indicates that this operation exports the template parameter with the default value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c667e-131">-Path</span></span>
<span data-ttu-id="c667e-132">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="c667e-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="c667e-133">-För</span><span class="sxs-lookup"><span data-stu-id="c667e-133">-Pre</span></span>
<span data-ttu-id="c667e-134">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="c667e-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-135">-Resurs</span><span class="sxs-lookup"><span data-stu-id="c667e-135">-Resource</span></span>
<span data-ttu-id="c667e-136">En lista med resourceIds som du kan filtrera resultat efter.</span><span class="sxs-lookup"><span data-stu-id="c667e-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c667e-137">-ResourceGroupName</span></span>
<span data-ttu-id="c667e-138">Anger namnet på den resurs grupp som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="c667e-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="c667e-139">-SkipAllParameterization</span></span>
<span data-ttu-id="c667e-140">Hoppa över alla parameterization.</span><span class="sxs-lookup"><span data-stu-id="c667e-140">Skip all parameterization.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="c667e-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="c667e-142">Hoppa över resurs namn parameterization.</span><span class="sxs-lookup"><span data-stu-id="c667e-142">Skip resource name parameterization.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c667e-143">-Confirm</span></span>
<span data-ttu-id="c667e-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c667e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c667e-145">-WhatIf</span></span>
<span data-ttu-id="c667e-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c667e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c667e-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c667e-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c667e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c667e-148">CommonParameters</span></span>
<span data-ttu-id="c667e-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c667e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c667e-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c667e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c667e-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c667e-151">INPUTS</span></span>

### <span data-ttu-id="c667e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c667e-152">System.String</span></span>

## <span data-ttu-id="c667e-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c667e-153">OUTPUTS</span></span>

### <span data-ttu-id="c667e-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c667e-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c667e-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c667e-155">NOTES</span></span>

## <span data-ttu-id="c667e-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c667e-156">RELATED LINKS</span></span>

[<span data-ttu-id="c667e-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c667e-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


