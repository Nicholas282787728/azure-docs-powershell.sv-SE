---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 6c24c01ebff1d0a74835b968640caea6b5d2b308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573515"
---
# <span data-ttu-id="cb09a-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cb09a-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="cb09a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb09a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb09a-103">Lägger till VMAccess-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cb09a-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb09a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb09a-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb09a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb09a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb09a-106">Cmdleten **set-AzureRmVMAccessExtension** lägger till den virtuella datorns VMAccess-tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cb09a-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="cb09a-107">VMAccess-tillägget kan användas för att ange ett tillfälligt lösen ord och det bör ändras direkt efter att du har loggat in på datorn.</span><span class="sxs-lookup"><span data-stu-id="cb09a-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="cb09a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb09a-108">EXAMPLES</span></span>

### <span data-ttu-id="cb09a-109">Exempel 1: lägga till ett VMAccess-tillägg</span><span class="sxs-lookup"><span data-stu-id="cb09a-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="cb09a-110">Det här kommandot lägger till ett VMAccess-tillägg för den virtuella datorn med namnet VirtualMachine07 i ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cb09a-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="cb09a-111">Kommandot anger namn och typ av hanterarmappning för VMAccess.</span><span class="sxs-lookup"><span data-stu-id="cb09a-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="cb09a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb09a-112">PARAMETERS</span></span>

### <span data-ttu-id="cb09a-113">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cb09a-113">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="cb09a-114">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="cb09a-114">-ForceRerun</span></span>
<span data-ttu-id="cb09a-115">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="cb09a-115">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="cb09a-116">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="cb09a-116">The value can be any string different from the current value.</span></span>

<span data-ttu-id="cb09a-117">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="cb09a-117">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="cb09a-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="cb09a-118">-Location</span></span>
<span data-ttu-id="cb09a-119">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cb09a-119">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="cb09a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb09a-120">-Name</span></span>
<span data-ttu-id="cb09a-121">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb09a-121">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cb09a-122">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="cb09a-122">-Password</span></span>
<span data-ttu-id="cb09a-123">Anger det nya lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cb09a-123">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="cb09a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb09a-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb09a-125">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cb09a-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cb09a-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cb09a-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="cb09a-127">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cb09a-127">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="cb09a-128">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="cb09a-128">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="cb09a-129">-UserName</span><span class="sxs-lookup"><span data-stu-id="cb09a-129">-UserName</span></span>
<span data-ttu-id="cb09a-130">Anger det nya användar namnet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cb09a-130">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="cb09a-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="cb09a-131">-VMName</span></span>
<span data-ttu-id="cb09a-132">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cb09a-132">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cb09a-133">Denna cmdlet lägger till VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="cb09a-133">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb09a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb09a-134">-Confirm</span></span>
<span data-ttu-id="cb09a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb09a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb09a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb09a-136">-WhatIf</span></span>
<span data-ttu-id="cb09a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb09a-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cb09a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb09a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb09a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb09a-139">CommonParameters</span></span>
<span data-ttu-id="cb09a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb09a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb09a-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb09a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb09a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb09a-142">INPUTS</span></span>

### <span data-ttu-id="cb09a-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="cb09a-143">None</span></span>
<span data-ttu-id="cb09a-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cb09a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb09a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb09a-145">OUTPUTS</span></span>

## <span data-ttu-id="cb09a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb09a-146">NOTES</span></span>

## <span data-ttu-id="cb09a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb09a-147">RELATED LINKS</span></span>

[<span data-ttu-id="cb09a-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cb09a-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cb09a-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cb09a-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cb09a-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="cb09a-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="cb09a-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="cb09a-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


