---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 5eaf09aec561ed1fff37d2687253634bd1efc921
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088641"
---
# <span data-ttu-id="39bdd-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="39bdd-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="39bdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="39bdd-103">Lägger till VMAccess-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="39bdd-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="39bdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39bdd-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39bdd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="39bdd-106">Cmdleten **set-AzVMAccessExtension** lägger till den virtuella datorns VMAccess-tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="39bdd-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="39bdd-107">VMAccess-tillägget kan användas för att ange ett tillfälligt lösen ord och det bör ändras direkt efter att du har loggat in på datorn.</span><span class="sxs-lookup"><span data-stu-id="39bdd-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="39bdd-108">Det här stöds inte på Windows-domänkontrollanter.</span><span class="sxs-lookup"><span data-stu-id="39bdd-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="39bdd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39bdd-109">EXAMPLES</span></span>

### <span data-ttu-id="39bdd-110">Exempel 1: lägga till ett VMAccess-tillägg</span><span class="sxs-lookup"><span data-stu-id="39bdd-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="39bdd-111">Det här kommandot lägger till ett VMAccess-tillägg för den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="39bdd-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>
<span data-ttu-id="39bdd-112">Kommandot anger namn och typ av hanterarmappning för VMAccess.</span><span class="sxs-lookup"><span data-stu-id="39bdd-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="39bdd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39bdd-113">PARAMETERS</span></span>

### <span data-ttu-id="39bdd-114">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="39bdd-114">-Credential</span></span>
<span data-ttu-id="39bdd-115">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="39bdd-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="39bdd-116">Om du skriver ett annat namn än det nuvarande lokala administratörs kontot på din virtuella dator, lägger VMAccess-tillägget till ett lokalt administratörs konto med det namnet och tilldelar ditt lösen ord till kontot.</span><span class="sxs-lookup"><span data-stu-id="39bdd-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="39bdd-117">Om det lokala administratörs kontot på din VM finns återställs lösen ordet och om kontot är inaktiverat aktiverar VMAccess-tillägget det.</span><span class="sxs-lookup"><span data-stu-id="39bdd-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="39bdd-118">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="39bdd-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="39bdd-119">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="39bdd-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="39bdd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bdd-120">-DefaultProfile</span></span>
<span data-ttu-id="39bdd-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39bdd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39bdd-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="39bdd-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="39bdd-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="39bdd-123">-ForceRerun</span></span>
<span data-ttu-id="39bdd-124">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="39bdd-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="39bdd-125">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="39bdd-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="39bdd-126">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="39bdd-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="39bdd-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="39bdd-127">-Location</span></span>
<span data-ttu-id="39bdd-128">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="39bdd-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="39bdd-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="39bdd-129">-Name</span></span>
<span data-ttu-id="39bdd-130">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39bdd-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="39bdd-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="39bdd-131">-NoWait</span></span>
<span data-ttu-id="39bdd-132">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="39bdd-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="39bdd-133">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="39bdd-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="39bdd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39bdd-134">-ResourceGroupName</span></span>
<span data-ttu-id="39bdd-135">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="39bdd-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="39bdd-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="39bdd-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="39bdd-137">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="39bdd-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="39bdd-138">För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="39bdd-138">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="39bdd-139">TypeHandlerVersion måste vara 2,0 eller senare, eftersom version 1 är föråldrad.</span><span class="sxs-lookup"><span data-stu-id="39bdd-139">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="39bdd-140">-VMName</span><span class="sxs-lookup"><span data-stu-id="39bdd-140">-VMName</span></span>
<span data-ttu-id="39bdd-141">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="39bdd-141">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="39bdd-142">Denna cmdlet lägger till VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="39bdd-142">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="39bdd-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39bdd-143">-Confirm</span></span>
<span data-ttu-id="39bdd-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39bdd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bdd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bdd-145">-WhatIf</span></span>
<span data-ttu-id="39bdd-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39bdd-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bdd-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39bdd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bdd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bdd-148">CommonParameters</span></span>
<span data-ttu-id="39bdd-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bdd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bdd-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39bdd-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bdd-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39bdd-151">INPUTS</span></span>

### <span data-ttu-id="39bdd-152">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="39bdd-152">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="39bdd-153">System. String</span><span class="sxs-lookup"><span data-stu-id="39bdd-153">System.String</span></span>

### <span data-ttu-id="39bdd-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39bdd-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39bdd-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39bdd-155">OUTPUTS</span></span>

### <span data-ttu-id="39bdd-156">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="39bdd-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="39bdd-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39bdd-157">NOTES</span></span>

## <span data-ttu-id="39bdd-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39bdd-158">RELATED LINKS</span></span>

[<span data-ttu-id="39bdd-159">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="39bdd-159">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="39bdd-160">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="39bdd-160">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="39bdd-161">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="39bdd-161">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="39bdd-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="39bdd-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


