---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 331850ff03feeaf1f49bd8e6a6c8486bd9b0e95a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754464"
---
# <span data-ttu-id="0bc48-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0bc48-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="0bc48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bc48-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc48-103">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0bc48-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="0bc48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bc48-104">SYNTAX</span></span>

### <span data-ttu-id="0bc48-105">ByNameWithContainerAndFileNamesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0bc48-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc48-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bc48-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc48-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bc48-113">DESCRIPTION</span></span>
<span data-ttu-id="0bc48-114">Cmdleten **set-AzVMCustomScriptExtension** lägger till ett anpassat tillägg för virtuella skript på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0bc48-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="0bc48-115">Med det här tillägget kan du köra egna skript på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0bc48-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="0bc48-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bc48-116">EXAMPLES</span></span>

### <span data-ttu-id="0bc48-117">Exempel 1: lägga till ett eget skript</span><span class="sxs-lookup"><span data-stu-id="0bc48-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="0bc48-118">Det här kommandot lägger till ett anpassat skript till den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0bc48-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="0bc48-119">Skript filen är contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="0bc48-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="0bc48-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bc48-120">PARAMETERS</span></span>

### <span data-ttu-id="0bc48-121">-Argument</span><span class="sxs-lookup"><span data-stu-id="0bc48-121">-Argument</span></span>
<span data-ttu-id="0bc48-122">Anger argument som skript tillägget skickar till skriptet.</span><span class="sxs-lookup"><span data-stu-id="0bc48-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="0bc48-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0bc48-123">-ContainerName</span></span>
<span data-ttu-id="0bc48-124">Anger namnet på den Azure Storage-behållare där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="0bc48-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc48-125">-DefaultProfile</span></span>
<span data-ttu-id="0bc48-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0bc48-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bc48-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0bc48-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="0bc48-128">-FileName</span><span class="sxs-lookup"><span data-stu-id="0bc48-128">-FileName</span></span>
<span data-ttu-id="0bc48-129">Anger namnet på skript filen.</span><span class="sxs-lookup"><span data-stu-id="0bc48-129">Specifies the name of the script file.</span></span> <span data-ttu-id="0bc48-130">Om filen är lagrad i Azure Blob Storage är värdet för fil namn Skift-senstive.</span><span class="sxs-lookup"><span data-stu-id="0bc48-130">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="0bc48-131">Fil namn för filer som lagras i Azure-fillagring är inte senstive.</span><span class="sxs-lookup"><span data-stu-id="0bc48-131">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="0bc48-132">-FileUri</span></span>
<span data-ttu-id="0bc48-133">Anger skript filens URI.</span><span class="sxs-lookup"><span data-stu-id="0bc48-133">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="0bc48-134">-ForceRerun</span></span>
<span data-ttu-id="0bc48-135">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="0bc48-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="0bc48-136">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="0bc48-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="0bc48-137">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="0bc48-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="0bc48-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bc48-138">-InputObject</span></span>
<span data-ttu-id="0bc48-139">Objekt för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0bc48-139">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="0bc48-140">-Location</span></span>
<span data-ttu-id="0bc48-141">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0bc48-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="0bc48-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="0bc48-142">-Name</span></span>
<span data-ttu-id="0bc48-143">Anger namnet på det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="0bc48-143">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc48-144">-ResourceGroupName</span></span>
<span data-ttu-id="0bc48-145">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0bc48-145">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc48-146">-ResourceId</span></span>
<span data-ttu-id="0bc48-147">VM-tillägg ResourceID.</span><span class="sxs-lookup"><span data-stu-id="0bc48-147">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-148">-Kör</span><span class="sxs-lookup"><span data-stu-id="0bc48-148">-Run</span></span>
<span data-ttu-id="0bc48-149">Anger det kommando som ska användas för att köra skriptet.</span><span class="sxs-lookup"><span data-stu-id="0bc48-149">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="0bc48-150">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="0bc48-150">-SecureExecution</span></span>
<span data-ttu-id="0bc48-151">Anger att värdet för *Kör* -parametern inte är inloggad på servern eller att den returneras till användaren med Get-filtillägg API.</span><span class="sxs-lookup"><span data-stu-id="0bc48-151">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="0bc48-152">Värdet för *Kör* kan innehålla hemligheter eller lösen ord som skickas till skript filen säkert.</span><span class="sxs-lookup"><span data-stu-id="0bc48-152">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="0bc48-153">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0bc48-153">-StorageAccountKey</span></span>
<span data-ttu-id="0bc48-154">Anger tangenten för Azure Storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="0bc48-154">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-155">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0bc48-155">-StorageAccountName</span></span>
<span data-ttu-id="0bc48-156">Anger namnet på det Azure Storage-konto där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="0bc48-156">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-157">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0bc48-157">-StorageEndpointSuffix</span></span>
<span data-ttu-id="0bc48-158">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="0bc48-158">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0bc48-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="0bc48-160">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0bc48-160">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="0bc48-161">För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och CustomScriptExtension för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="0bc48-161">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="0bc48-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="0bc48-162">-VMName</span></span>
<span data-ttu-id="0bc48-163">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0bc48-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0bc48-164">Denna cmdlet lägger till det anpassade skript tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0bc48-164">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-165">-VMObject</span><span class="sxs-lookup"><span data-stu-id="0bc48-165">-VMObject</span></span>
<span data-ttu-id="0bc48-166">VM-objekt.</span><span class="sxs-lookup"><span data-stu-id="0bc48-166">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bc48-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bc48-167">-Confirm</span></span>
<span data-ttu-id="0bc48-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bc48-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc48-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc48-169">-WhatIf</span></span>
<span data-ttu-id="0bc48-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bc48-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc48-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bc48-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc48-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc48-172">CommonParameters</span></span>
<span data-ttu-id="0bc48-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc48-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc48-174">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc48-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc48-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bc48-175">INPUTS</span></span>

### <span data-ttu-id="0bc48-176">System. String</span><span class="sxs-lookup"><span data-stu-id="0bc48-176">System.String</span></span>

### <span data-ttu-id="0bc48-177">System. string []</span><span class="sxs-lookup"><span data-stu-id="0bc48-177">System.String[]</span></span>

### <span data-ttu-id="0bc48-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0bc48-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0bc48-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bc48-179">OUTPUTS</span></span>

### <span data-ttu-id="0bc48-180">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0bc48-180">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0bc48-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bc48-181">NOTES</span></span>

## <span data-ttu-id="0bc48-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bc48-182">RELATED LINKS</span></span>

[<span data-ttu-id="0bc48-183">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0bc48-183">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="0bc48-184">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0bc48-184">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


