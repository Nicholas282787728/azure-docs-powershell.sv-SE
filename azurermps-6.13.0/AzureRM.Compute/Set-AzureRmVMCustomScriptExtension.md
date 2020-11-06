---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 926a33040421acbcb6424c89ec10da89ad87e5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577092"
---
# <span data-ttu-id="3468c-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3468c-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="3468c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3468c-102">SYNOPSIS</span></span>
<span data-ttu-id="3468c-103">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3468c-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3468c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3468c-104">SYNTAX</span></span>

### <span data-ttu-id="3468c-105">SetCustomScriptExtensionByContainerAndFileNames (standard)</span><span class="sxs-lookup"><span data-stu-id="3468c-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3468c-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="3468c-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3468c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3468c-107">DESCRIPTION</span></span>
<span data-ttu-id="3468c-108">Cmdleten **set-AzureRmVMCustomScriptExtension** lägger till ett anpassat tillägg för virtuella skript på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3468c-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="3468c-109">Med det här tillägget kan du köra egna skript på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3468c-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="3468c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3468c-110">EXAMPLES</span></span>

### <span data-ttu-id="3468c-111">Exempel 1: lägga till ett eget skript</span><span class="sxs-lookup"><span data-stu-id="3468c-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="3468c-112">Det här kommandot lägger till ett anpassat skript till den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="3468c-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="3468c-113">Skript filen är contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="3468c-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="3468c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3468c-114">PARAMETERS</span></span>

### <span data-ttu-id="3468c-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="3468c-115">-Argument</span></span>
<span data-ttu-id="3468c-116">Anger argument som skript tillägget skickar till skriptet.</span><span class="sxs-lookup"><span data-stu-id="3468c-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="3468c-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3468c-117">-ContainerName</span></span>
<span data-ttu-id="3468c-118">Anger namnet på den Azure Storage-behållare där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="3468c-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="3468c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3468c-119">-DefaultProfile</span></span>
<span data-ttu-id="3468c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3468c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3468c-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3468c-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="3468c-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="3468c-122">-FileName</span></span>
<span data-ttu-id="3468c-123">Anger namnet på skript filen.</span><span class="sxs-lookup"><span data-stu-id="3468c-123">Specifies the name of the script file.</span></span> <span data-ttu-id="3468c-124">Om filen är lagrad i Azure Blob Storage är värdet för fil namn Skift-senstive.</span><span class="sxs-lookup"><span data-stu-id="3468c-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="3468c-125">Fil namn för filer som lagras i Azure-fillagring är inte senstive.</span><span class="sxs-lookup"><span data-stu-id="3468c-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="3468c-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="3468c-126">-FileUri</span></span>
<span data-ttu-id="3468c-127">Anger skript filens URI.</span><span class="sxs-lookup"><span data-stu-id="3468c-127">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="3468c-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3468c-128">-ForceRerun</span></span>
<span data-ttu-id="3468c-129">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="3468c-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="3468c-130">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="3468c-130">The value can be any string different from the current value.</span></span>
<span data-ttu-id="3468c-131">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="3468c-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="3468c-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="3468c-132">-Location</span></span>
<span data-ttu-id="3468c-133">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3468c-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="3468c-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="3468c-134">-Name</span></span>
<span data-ttu-id="3468c-135">Anger namnet på det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="3468c-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="3468c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3468c-136">-ResourceGroupName</span></span>
<span data-ttu-id="3468c-137">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3468c-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3468c-138">-Kör</span><span class="sxs-lookup"><span data-stu-id="3468c-138">-Run</span></span>
<span data-ttu-id="3468c-139">Anger det kommando som ska användas för att köra skriptet.</span><span class="sxs-lookup"><span data-stu-id="3468c-139">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="3468c-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="3468c-140">-SecureExecution</span></span>
<span data-ttu-id="3468c-141">Anger att värdet för *Kör* -parametern inte är inloggad på servern eller att den returneras till användaren med Get-filtillägg API.</span><span class="sxs-lookup"><span data-stu-id="3468c-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="3468c-142">Värdet för *Kör* kan innehålla hemligheter eller lösen ord som skickas till skript filen säkert.</span><span class="sxs-lookup"><span data-stu-id="3468c-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="3468c-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3468c-143">-StorageAccountKey</span></span>
<span data-ttu-id="3468c-144">Anger tangenten för Azure Storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="3468c-144">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="3468c-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3468c-145">-StorageAccountName</span></span>
<span data-ttu-id="3468c-146">Anger namnet på det Azure Storage-konto där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="3468c-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="3468c-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3468c-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="3468c-148">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="3468c-148">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="3468c-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3468c-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="3468c-150">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3468c-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="3468c-151">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="3468c-151">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="3468c-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="3468c-152">-VMName</span></span>
<span data-ttu-id="3468c-153">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3468c-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3468c-154">Denna cmdlet lägger till det anpassade skript tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3468c-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3468c-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3468c-155">-Confirm</span></span>
<span data-ttu-id="3468c-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3468c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3468c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3468c-157">-WhatIf</span></span>
<span data-ttu-id="3468c-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3468c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3468c-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3468c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3468c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3468c-160">CommonParameters</span></span>
<span data-ttu-id="3468c-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3468c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3468c-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3468c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3468c-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3468c-163">INPUTS</span></span>

### <span data-ttu-id="3468c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="3468c-164">System.String</span></span>

### <span data-ttu-id="3468c-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="3468c-165">System.String[]</span></span>

### <span data-ttu-id="3468c-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3468c-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3468c-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3468c-167">OUTPUTS</span></span>

### <span data-ttu-id="3468c-168">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3468c-168">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3468c-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3468c-169">NOTES</span></span>

## <span data-ttu-id="3468c-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3468c-170">RELATED LINKS</span></span>

[<span data-ttu-id="3468c-171">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3468c-171">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="3468c-172">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3468c-172">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


