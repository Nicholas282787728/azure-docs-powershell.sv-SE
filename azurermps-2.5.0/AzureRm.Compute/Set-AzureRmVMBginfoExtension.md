---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbginfoextension
schema: 2.0.0
ms.openlocfilehash: 2d0b09e60872050ff1bad98b468763f69edfa723
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930270"
---
# <span data-ttu-id="1e901-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="1e901-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="1e901-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e901-102">SYNOPSIS</span></span>
<span data-ttu-id="1e901-103">Lägger till BGInfo-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1e901-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e901-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e901-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e901-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e901-105">DESCRIPTION</span></span>
<span data-ttu-id="1e901-106">Cmdleten **set-AzureRmVMBGInfoExtension** lägger till BgInfo-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1e901-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="1e901-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e901-107">EXAMPLES</span></span>

### <span data-ttu-id="1e901-108">Exempel 1: lägga till BGInfo-tillägget för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1e901-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="1e901-109">Det här kommandot lägger till BGInfo-tillägget på den virtuella datorn med namnet ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="1e901-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="1e901-110">Kommandot anger den virtuella datorns resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="1e901-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="1e901-111">Kommandot anger namn och version för tillägget.</span><span class="sxs-lookup"><span data-stu-id="1e901-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="1e901-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e901-112">PARAMETERS</span></span>

### <span data-ttu-id="1e901-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e901-113">-DefaultProfile</span></span>
<span data-ttu-id="1e901-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e901-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e901-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1e901-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1e901-116">Anger att denna cmdlet hindrar Azure gäst agenten från att automatiskt uppdatera tillägget till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="1e901-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="1e901-117">Som standard aktiverar denna cmdlet gäst agenten att uppdatera tillägget.</span><span class="sxs-lookup"><span data-stu-id="1e901-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="1e901-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1e901-118">-ForceRerun</span></span>
<span data-ttu-id="1e901-119">Anger att tillägget ska köras igen med samma offentliga eller skyddade inställningar.</span><span class="sxs-lookup"><span data-stu-id="1e901-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="1e901-120">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="1e901-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="1e901-121">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="1e901-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1e901-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="1e901-122">-Location</span></span>
<span data-ttu-id="1e901-123">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1e901-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1e901-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e901-124">-Name</span></span>
<span data-ttu-id="1e901-125">Anger namnet på BGInfo-tillägget som denna cmdlet lägger till till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1e901-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="1e901-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e901-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e901-127">Anger namnet på resurs gruppen för den virtuella dator där denna cmdlet lägger till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="1e901-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="1e901-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1e901-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="1e901-129">Anger den version av tillägget som denna cmdlet lägger till på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1e901-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="1e901-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="1e901-130">-VMName</span></span>
<span data-ttu-id="1e901-131">Anger namnet på den virtuella dator där denna cmdlet lägger till BGInfo-tillägget.</span><span class="sxs-lookup"><span data-stu-id="1e901-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="1e901-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e901-132">-Confirm</span></span>
<span data-ttu-id="1e901-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e901-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e901-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e901-134">-WhatIf</span></span>
<span data-ttu-id="1e901-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e901-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1e901-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e901-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e901-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e901-137">CommonParameters</span></span>
<span data-ttu-id="1e901-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e901-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e901-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e901-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e901-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e901-140">INPUTS</span></span>

### <span data-ttu-id="1e901-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="1e901-141">None</span></span>
<span data-ttu-id="1e901-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1e901-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e901-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e901-143">OUTPUTS</span></span>

### <span data-ttu-id="1e901-144">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1e901-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1e901-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e901-145">NOTES</span></span>

## <span data-ttu-id="1e901-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e901-146">RELATED LINKS</span></span>
