---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573666"
---
# <span data-ttu-id="42d54-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="42d54-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="42d54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42d54-102">SYNOPSIS</span></span>
<span data-ttu-id="42d54-103">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="42d54-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42d54-104">SYNTAX</span></span>

### <span data-ttu-id="42d54-105">SetCustomScriptExtensionByContainerAndFileNames (standard)</span><span class="sxs-lookup"><span data-stu-id="42d54-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d54-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="42d54-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d54-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42d54-107">DESCRIPTION</span></span>
<span data-ttu-id="42d54-108">Cmdleten **set-AzureRmVMCustomScriptExtension** lägger till ett anpassat tillägg för virtuella skript på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="42d54-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="42d54-109">Med det här tillägget kan du köra egna skript på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="42d54-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="42d54-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42d54-110">EXAMPLES</span></span>

### <span data-ttu-id="42d54-111">Exempel 1: lägga till ett eget skript</span><span class="sxs-lookup"><span data-stu-id="42d54-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="42d54-112">Det här kommandot lägger till ett anpassat skript till den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="42d54-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="42d54-113">Skript filen är contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="42d54-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="42d54-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42d54-114">PARAMETERS</span></span>

### <span data-ttu-id="42d54-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="42d54-115">-Argument</span></span>
<span data-ttu-id="42d54-116">Anger argument som skript tillägget skickar till skriptet.</span><span class="sxs-lookup"><span data-stu-id="42d54-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="42d54-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="42d54-117">-ContainerName</span></span>
<span data-ttu-id="42d54-118">Anger namnet på den Azure Storage-behållare där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="42d54-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d54-119">-DefaultProfile</span></span>
<span data-ttu-id="42d54-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42d54-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="42d54-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="42d54-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="42d54-122">-FileName</span></span>
<span data-ttu-id="42d54-123">Anger namnet på skript filen.</span><span class="sxs-lookup"><span data-stu-id="42d54-123">Specifies the name of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="42d54-124">-FileUri</span></span>
<span data-ttu-id="42d54-125">Anger skript filens URI.</span><span class="sxs-lookup"><span data-stu-id="42d54-125">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="42d54-126">-ForceRerun</span></span>
<span data-ttu-id="42d54-127">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="42d54-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="42d54-128">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="42d54-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="42d54-129">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="42d54-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="42d54-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="42d54-130">-Location</span></span>
<span data-ttu-id="42d54-131">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="42d54-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="42d54-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="42d54-132">-Name</span></span>
<span data-ttu-id="42d54-133">Anger namnet på det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="42d54-133">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="42d54-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d54-134">-ResourceGroupName</span></span>
<span data-ttu-id="42d54-135">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="42d54-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="42d54-136">-Kör</span><span class="sxs-lookup"><span data-stu-id="42d54-136">-Run</span></span>
<span data-ttu-id="42d54-137">Anger det kommando som ska användas för att köra skriptet.</span><span class="sxs-lookup"><span data-stu-id="42d54-137">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="42d54-138">-SecureExecution</span></span>
<span data-ttu-id="42d54-139">Anger att värdet för *Kör* -parametern inte är inloggad på servern eller att den returneras till användaren med Get-filtillägg API.</span><span class="sxs-lookup"><span data-stu-id="42d54-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="42d54-140">Värdet för *Kör* kan innehålla hemligheter eller lösen ord som skickas till skript filen säkert.</span><span class="sxs-lookup"><span data-stu-id="42d54-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="42d54-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="42d54-141">-StorageAccountKey</span></span>
<span data-ttu-id="42d54-142">Anger tangenten för Azure Storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="42d54-142">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42d54-143">-StorageAccountName</span></span>
<span data-ttu-id="42d54-144">Anger namnet på det Azure Storage-konto där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="42d54-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="42d54-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="42d54-146">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="42d54-146">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d54-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="42d54-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="42d54-148">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="42d54-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="42d54-149">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="42d54-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="42d54-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="42d54-150">-VMName</span></span>
<span data-ttu-id="42d54-151">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="42d54-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="42d54-152">Denna cmdlet lägger till det anpassade skript tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="42d54-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="42d54-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42d54-153">-Confirm</span></span>
<span data-ttu-id="42d54-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42d54-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d54-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d54-155">-WhatIf</span></span>
<span data-ttu-id="42d54-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42d54-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="42d54-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42d54-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d54-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d54-158">CommonParameters</span></span>
<span data-ttu-id="42d54-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d54-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d54-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d54-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d54-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42d54-161">INPUTS</span></span>

## <span data-ttu-id="42d54-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42d54-162">OUTPUTS</span></span>

## <span data-ttu-id="42d54-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42d54-163">NOTES</span></span>

## <span data-ttu-id="42d54-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42d54-164">RELATED LINKS</span></span>

[<span data-ttu-id="42d54-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="42d54-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="42d54-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="42d54-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


