---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089921"
---
# <span data-ttu-id="4db23-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="4db23-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="4db23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4db23-102">SYNOPSIS</span></span>
<span data-ttu-id="4db23-103">Lägger till BGInfo-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4db23-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="4db23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4db23-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4db23-105">DESCRIPTION</span></span>
<span data-ttu-id="4db23-106">Cmdleten **set-AzVMBGInfoExtension** lägger till BgInfo-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4db23-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="4db23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4db23-107">EXAMPLES</span></span>

### <span data-ttu-id="4db23-108">Exempel 1: lägga till BGInfo-tillägget för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4db23-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="4db23-109">Det här kommandot lägger till BGInfo-tillägget på den virtuella datorn med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="4db23-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="4db23-110">Kommandot anger den virtuella datorns resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="4db23-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="4db23-111">Kommandot anger namn och version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="4db23-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="4db23-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4db23-112">PARAMETERS</span></span>

### <span data-ttu-id="4db23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db23-113">-DefaultProfile</span></span>
<span data-ttu-id="4db23-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4db23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4db23-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4db23-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4db23-116">Anger att denna cmdlet hindrar Azure gäst agenten från att automatiskt uppdatera tillägget till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="4db23-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="4db23-117">Som standard aktiverar denna cmdlet gäst agenten att uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="4db23-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db23-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="4db23-118">-ForceRerun</span></span>
<span data-ttu-id="4db23-119">Anger att tillägget ska köras igen med samma offentliga eller skyddade inställningar.</span><span class="sxs-lookup"><span data-stu-id="4db23-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="4db23-120">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="4db23-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="4db23-121">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="4db23-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="4db23-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="4db23-122">-Location</span></span>
<span data-ttu-id="4db23-123">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4db23-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="4db23-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4db23-124">-Name</span></span>
<span data-ttu-id="4db23-125">Anger namnet på BGInfo-tillägget som denna cmdlet lägger till till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4db23-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db23-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4db23-126">-NoWait</span></span>
<span data-ttu-id="4db23-127">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="4db23-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4db23-128">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="4db23-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4db23-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db23-129">-ResourceGroupName</span></span>
<span data-ttu-id="4db23-130">Anger namnet på resurs gruppen för den virtuella dator där denna cmdlet lägger till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="4db23-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db23-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4db23-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="4db23-132">Anger den version av tillägget som denna cmdlet lägger till på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4db23-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db23-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="4db23-133">-VMName</span></span>
<span data-ttu-id="4db23-134">Anger namnet på den virtuella dator där denna cmdlet lägger till BGInfo-tillägget.</span><span class="sxs-lookup"><span data-stu-id="4db23-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db23-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4db23-135">-Confirm</span></span>
<span data-ttu-id="4db23-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4db23-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db23-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db23-137">-WhatIf</span></span>
<span data-ttu-id="4db23-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4db23-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db23-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4db23-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db23-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db23-140">CommonParameters</span></span>
<span data-ttu-id="4db23-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db23-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db23-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4db23-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db23-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4db23-143">INPUTS</span></span>

### <span data-ttu-id="4db23-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4db23-144">System.String</span></span>

### <span data-ttu-id="4db23-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4db23-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4db23-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4db23-146">OUTPUTS</span></span>

### <span data-ttu-id="4db23-147">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4db23-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4db23-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4db23-148">NOTES</span></span>

## <span data-ttu-id="4db23-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4db23-149">RELATED LINKS</span></span>
