---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 693809e46823cbcb8331eade7b8cd38c83238be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575706"
---
# <span data-ttu-id="58d26-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="58d26-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="58d26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58d26-102">SYNOPSIS</span></span>
<span data-ttu-id="58d26-103">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58d26-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58d26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58d26-104">SYNTAX</span></span>

### <span data-ttu-id="58d26-105">SetCustomScriptExtensionByContainerAndFileNames (standard)</span><span class="sxs-lookup"><span data-stu-id="58d26-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d26-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="58d26-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d26-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58d26-107">DESCRIPTION</span></span>
<span data-ttu-id="58d26-108">Cmdleten **set-AzureRmVMCustomScriptExtension** lägger till ett anpassat tillägg för virtuella skript på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58d26-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="58d26-109">Med det här tillägget kan du köra egna skript på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="58d26-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="58d26-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58d26-110">EXAMPLES</span></span>

### <span data-ttu-id="58d26-111">Exempel 1: lägga till ett eget skript</span><span class="sxs-lookup"><span data-stu-id="58d26-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="58d26-112">Det här kommandot lägger till ett anpassat skript till den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="58d26-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="58d26-113">Skript filen är contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="58d26-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="58d26-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58d26-114">PARAMETERS</span></span>

### <span data-ttu-id="58d26-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="58d26-115">-Argument</span></span>
<span data-ttu-id="58d26-116">Anger argument som skript tillägget skickar till skriptet.</span><span class="sxs-lookup"><span data-stu-id="58d26-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="58d26-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="58d26-117">-ContainerName</span></span>
<span data-ttu-id="58d26-118">Anger namnet på den Azure Storage-behållare där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="58d26-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="58d26-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="58d26-120">-FileName</span><span class="sxs-lookup"><span data-stu-id="58d26-120">-FileName</span></span>
<span data-ttu-id="58d26-121">Anger namnet på skript filen.</span><span class="sxs-lookup"><span data-stu-id="58d26-121">Specifies the name of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-122">-FileUri</span><span class="sxs-lookup"><span data-stu-id="58d26-122">-FileUri</span></span>
<span data-ttu-id="58d26-123">Anger skript filens URI.</span><span class="sxs-lookup"><span data-stu-id="58d26-123">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-124">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="58d26-124">-ForceRerun</span></span>
<span data-ttu-id="58d26-125">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="58d26-125">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="58d26-126">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="58d26-126">The value can be any string different from the current value.</span></span>

<span data-ttu-id="58d26-127">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="58d26-127">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="58d26-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="58d26-128">-Location</span></span>
<span data-ttu-id="58d26-129">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="58d26-129">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="58d26-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="58d26-130">-Name</span></span>
<span data-ttu-id="58d26-131">Anger namnet på det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="58d26-131">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="58d26-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d26-132">-ResourceGroupName</span></span>
<span data-ttu-id="58d26-133">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58d26-133">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="58d26-134">-Kör</span><span class="sxs-lookup"><span data-stu-id="58d26-134">-Run</span></span>
<span data-ttu-id="58d26-135">Anger det kommando som ska användas för att köra skriptet.</span><span class="sxs-lookup"><span data-stu-id="58d26-135">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-136">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="58d26-136">-SecureExecution</span></span>
<span data-ttu-id="58d26-137">Anger att värdet för *Kör* -parametern inte är inloggad på servern eller att den returneras till användaren med Get-filtillägg API.</span><span class="sxs-lookup"><span data-stu-id="58d26-137">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="58d26-138">Värdet för *Kör* kan innehålla hemligheter eller lösen ord som skickas till skript filen säkert.</span><span class="sxs-lookup"><span data-stu-id="58d26-138">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="58d26-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="58d26-139">-StorageAccountKey</span></span>
<span data-ttu-id="58d26-140">Anger tangenten för Azure Storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="58d26-140">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="58d26-141">-StorageAccountName</span></span>
<span data-ttu-id="58d26-142">Anger namnet på det Azure Storage-konto där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="58d26-142">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-143">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="58d26-143">-StorageEndpointSuffix</span></span>
<span data-ttu-id="58d26-144">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="58d26-144">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d26-145">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="58d26-145">-TypeHandlerVersion</span></span>
<span data-ttu-id="58d26-146">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="58d26-146">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="58d26-147">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="58d26-147">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="58d26-148">-VMName</span><span class="sxs-lookup"><span data-stu-id="58d26-148">-VMName</span></span>
<span data-ttu-id="58d26-149">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58d26-149">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="58d26-150">Denna cmdlet lägger till det anpassade skript tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="58d26-150">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="58d26-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58d26-151">-Confirm</span></span>
<span data-ttu-id="58d26-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58d26-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d26-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d26-153">-WhatIf</span></span>
<span data-ttu-id="58d26-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="58d26-154">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="58d26-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="58d26-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d26-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d26-156">CommonParameters</span></span>
<span data-ttu-id="58d26-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d26-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d26-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d26-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d26-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58d26-159">INPUTS</span></span>

### <span data-ttu-id="58d26-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="58d26-160">None</span></span>
<span data-ttu-id="58d26-161">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="58d26-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58d26-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58d26-162">OUTPUTS</span></span>

## <span data-ttu-id="58d26-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58d26-163">NOTES</span></span>

## <span data-ttu-id="58d26-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58d26-164">RELATED LINKS</span></span>

[<span data-ttu-id="58d26-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="58d26-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="58d26-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="58d26-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


