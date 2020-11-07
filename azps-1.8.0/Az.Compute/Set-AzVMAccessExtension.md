---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754468"
---
# <span data-ttu-id="dc056-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="dc056-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="dc056-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc056-102">SYNOPSIS</span></span>
<span data-ttu-id="dc056-103">Lägger till VMAccess-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dc056-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="dc056-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc056-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc056-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc056-105">DESCRIPTION</span></span>
<span data-ttu-id="dc056-106">Cmdleten **set-AzVMAccessExtension** lägger till den virtuella datorns VMAccess-tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dc056-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="dc056-107">VMAccess-tillägget kan användas för att ange ett tillfälligt lösen ord och det bör ändras direkt efter att du har loggat in på datorn.</span><span class="sxs-lookup"><span data-stu-id="dc056-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="dc056-108">Det här stöds inte på Windows-domänkontrollanter.</span><span class="sxs-lookup"><span data-stu-id="dc056-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="dc056-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc056-109">EXAMPLES</span></span>

### <span data-ttu-id="dc056-110">Exempel 1: lägga till ett VMAccess-tillägg</span><span class="sxs-lookup"><span data-stu-id="dc056-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="dc056-111">Det här kommandot lägger till ett VMAccess-tillägg för den virtuella datorn med namnet VirtualMachine07 i ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dc056-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="dc056-112">Kommandot anger namn och typ av hanterarmappning för VMAccess.</span><span class="sxs-lookup"><span data-stu-id="dc056-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="dc056-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc056-113">PARAMETERS</span></span>

### <span data-ttu-id="dc056-114">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="dc056-114">-Credential</span></span>
<span data-ttu-id="dc056-115">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="dc056-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="dc056-116">Om du skriver ett annat namn än det nuvarande lokala administratörs kontot på din virtuella dator, lägger VMAccess-tillägget till ett lokalt administratörs konto med det namnet och tilldelar ditt lösen ord till kontot.</span><span class="sxs-lookup"><span data-stu-id="dc056-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="dc056-117">Om det lokala administratörs kontot på din VM finns återställs lösen ordet och om kontot är inaktiverat aktiverar VMAccess-tillägget det.</span><span class="sxs-lookup"><span data-stu-id="dc056-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="dc056-118">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="dc056-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="dc056-119">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="dc056-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc056-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc056-120">-DefaultProfile</span></span>
<span data-ttu-id="dc056-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc056-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc056-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dc056-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="dc056-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="dc056-123">-ForceRerun</span></span>
<span data-ttu-id="dc056-124">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="dc056-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="dc056-125">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="dc056-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="dc056-126">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="dc056-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="dc056-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="dc056-127">-Location</span></span>
<span data-ttu-id="dc056-128">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dc056-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="dc056-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc056-129">-Name</span></span>
<span data-ttu-id="dc056-130">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc056-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="dc056-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc056-131">-ResourceGroupName</span></span>
<span data-ttu-id="dc056-132">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dc056-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dc056-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dc056-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="dc056-134">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dc056-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="dc056-135">För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="dc056-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="dc056-136">TypeHandlerVersion måste vara 2,0 eller senare, eftersom version 1 är föråldrad.</span><span class="sxs-lookup"><span data-stu-id="dc056-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="dc056-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="dc056-137">-VMName</span></span>
<span data-ttu-id="dc056-138">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="dc056-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dc056-139">Denna cmdlet lägger till VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="dc056-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc056-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc056-140">-Confirm</span></span>
<span data-ttu-id="dc056-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc056-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc056-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc056-142">-WhatIf</span></span>
<span data-ttu-id="dc056-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc056-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc056-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc056-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc056-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc056-145">CommonParameters</span></span>
<span data-ttu-id="dc056-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc056-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc056-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc056-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc056-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc056-148">INPUTS</span></span>

### <span data-ttu-id="dc056-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="dc056-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="dc056-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dc056-150">System.String</span></span>

### <span data-ttu-id="dc056-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc056-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc056-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc056-152">OUTPUTS</span></span>

### <span data-ttu-id="dc056-153">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dc056-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dc056-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc056-154">NOTES</span></span>

## <span data-ttu-id="dc056-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc056-155">RELATED LINKS</span></span>

[<span data-ttu-id="dc056-156">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="dc056-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="dc056-157">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="dc056-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="dc056-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="dc056-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="dc056-159">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="dc056-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


