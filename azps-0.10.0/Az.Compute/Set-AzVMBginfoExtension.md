---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 21b8b73d1063881104b799c016c2cfab618a9705
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924825"
---
# <span data-ttu-id="52380-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="52380-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="52380-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52380-102">SYNOPSIS</span></span>
<span data-ttu-id="52380-103">Lägger till BGInfo-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="52380-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="52380-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52380-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52380-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52380-105">DESCRIPTION</span></span>
<span data-ttu-id="52380-106">Cmdleten **set-AzVMBGInfoExtension** lägger till BgInfo-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="52380-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="52380-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52380-107">EXAMPLES</span></span>

### <span data-ttu-id="52380-108">Exempel 1: lägga till BGInfo-tillägget för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="52380-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="52380-109">Det här kommandot lägger till BGInfo-tillägget på den virtuella datorn med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="52380-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="52380-110">Kommandot anger den virtuella datorns resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="52380-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="52380-111">Kommandot anger namn och version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="52380-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="52380-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52380-112">PARAMETERS</span></span>

### <span data-ttu-id="52380-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52380-113">-DefaultProfile</span></span>
<span data-ttu-id="52380-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52380-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52380-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="52380-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="52380-116">Anger att denna cmdlet hindrar Azure gäst agenten från att automatiskt uppdatera tillägget till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="52380-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="52380-117">Som standard aktiverar denna cmdlet gäst agenten att uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="52380-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="52380-118">-ForceRerun</span></span>
<span data-ttu-id="52380-119">Anger att tillägget ska köras igen med samma offentliga eller skyddade inställningar.</span><span class="sxs-lookup"><span data-stu-id="52380-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="52380-120">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="52380-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="52380-121">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="52380-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="52380-122">-Location</span></span>
<span data-ttu-id="52380-123">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="52380-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="52380-124">-Name</span></span>
<span data-ttu-id="52380-125">Anger namnet på BGInfo-tillägget som denna cmdlet lägger till till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="52380-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52380-126">-ResourceGroupName</span></span>
<span data-ttu-id="52380-127">Anger namnet på resurs gruppen för den virtuella dator där denna cmdlet lägger till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="52380-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="52380-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="52380-129">Anger den version av tillägget som denna cmdlet lägger till på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="52380-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="52380-130">-VMName</span></span>
<span data-ttu-id="52380-131">Anger namnet på den virtuella dator där denna cmdlet lägger till BGInfo-tillägget.</span><span class="sxs-lookup"><span data-stu-id="52380-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52380-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52380-132">-Confirm</span></span>
<span data-ttu-id="52380-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52380-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52380-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52380-134">-WhatIf</span></span>
<span data-ttu-id="52380-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52380-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="52380-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52380-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52380-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52380-137">CommonParameters</span></span>
<span data-ttu-id="52380-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52380-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52380-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52380-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52380-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52380-140">INPUTS</span></span>

### <span data-ttu-id="52380-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="52380-141">None</span></span>
<span data-ttu-id="52380-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="52380-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52380-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52380-143">OUTPUTS</span></span>

### <span data-ttu-id="52380-144">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="52380-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="52380-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52380-145">NOTES</span></span>

## <span data-ttu-id="52380-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52380-146">RELATED LINKS</span></span>
