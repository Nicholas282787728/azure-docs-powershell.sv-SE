---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 4ed63b1afa2f72e8f557cc95381883973ae7feb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092364"
---
# <span data-ttu-id="ea1fc-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ea1fc-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="ea1fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1fc-103">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="ea1fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea1fc-104">SYNTAX</span></span>

### <span data-ttu-id="ea1fc-105">ByNameWithContainerAndFileNamesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ea1fc-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea1fc-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1fc-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea1fc-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea1fc-113">DESCRIPTION</span></span>
<span data-ttu-id="ea1fc-114">Cmdleten **set-AzVMCustomScriptExtension** lägger till ett anpassat tillägg för virtuella skript på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="ea1fc-115">Med det här tillägget kan du köra egna skript på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="ea1fc-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea1fc-116">EXAMPLES</span></span>

### <span data-ttu-id="ea1fc-117">Exempel 1: lägga till ett eget skript</span><span class="sxs-lookup"><span data-stu-id="ea1fc-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="ea1fc-118">Det här kommandot lägger till ett anpassat skript till den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ea1fc-119">Skript filen är contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="ea1fc-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea1fc-120">PARAMETERS</span></span>

### <span data-ttu-id="ea1fc-121">-Argument</span><span class="sxs-lookup"><span data-stu-id="ea1fc-121">-Argument</span></span>
<span data-ttu-id="ea1fc-122">Anger argument som skript tillägget skickar till skriptet.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="ea1fc-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ea1fc-123">-ContainerName</span></span>
<span data-ttu-id="ea1fc-124">Anger namnet på den Azure Storage-behållare där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="ea1fc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1fc-125">-DefaultProfile</span></span>
<span data-ttu-id="ea1fc-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea1fc-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ea1fc-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="ea1fc-128">-FileName</span><span class="sxs-lookup"><span data-stu-id="ea1fc-128">-FileName</span></span>
<span data-ttu-id="ea1fc-129">Anger namnet på skript filen.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-129">Specifies the name of the script file.</span></span> <span data-ttu-id="ea1fc-130">Om filen är lagrad i Azure Blob Storage är värdet för fil namn Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-130">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="ea1fc-131">Fil namn för filer som lagras i Azure File Storage är inte Skift läges känsliga.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-131">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="ea1fc-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="ea1fc-132">-FileUri</span></span>
<span data-ttu-id="ea1fc-133">Anger skript filens URI.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-133">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="ea1fc-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ea1fc-134">-ForceRerun</span></span>
<span data-ttu-id="ea1fc-135">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ea1fc-136">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ea1fc-137">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ea1fc-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea1fc-138">-InputObject</span></span>
<span data-ttu-id="ea1fc-139">Objekt för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-139">VM extension object.</span></span>

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

### <span data-ttu-id="ea1fc-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="ea1fc-140">-Location</span></span>
<span data-ttu-id="ea1fc-141">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ea1fc-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea1fc-142">-Name</span></span>
<span data-ttu-id="ea1fc-143">Anger namnet på det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-143">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="ea1fc-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ea1fc-144">-NoWait</span></span>
<span data-ttu-id="ea1fc-145">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-145">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ea1fc-146">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-146">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ea1fc-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1fc-147">-ResourceGroupName</span></span>
<span data-ttu-id="ea1fc-148">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ea1fc-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea1fc-149">-ResourceId</span></span>
<span data-ttu-id="ea1fc-150">VM-tillägg ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-150">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="ea1fc-151">-Kör</span><span class="sxs-lookup"><span data-stu-id="ea1fc-151">-Run</span></span>
<span data-ttu-id="ea1fc-152">Anger det kommando som ska användas för att köra skriptet.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-152">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="ea1fc-153">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="ea1fc-153">-SecureExecution</span></span>
<span data-ttu-id="ea1fc-154">Anger att värdet för *Kör* -parametern inte är inloggad på servern eller att den returneras till användaren med Get-filtillägg API.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-154">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="ea1fc-155">Värdet för *Kör* kan innehålla hemligheter eller lösen ord som skickas till skript filen säkert.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-155">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="ea1fc-156">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea1fc-156">-StorageAccountKey</span></span>
<span data-ttu-id="ea1fc-157">Anger tangenten för Azure Storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-157">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="ea1fc-158">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea1fc-158">-StorageAccountName</span></span>
<span data-ttu-id="ea1fc-159">Anger namnet på det Azure Storage-konto där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-159">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="ea1fc-160">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ea1fc-160">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ea1fc-161">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-161">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="ea1fc-162">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ea1fc-162">-TypeHandlerVersion</span></span>
<span data-ttu-id="ea1fc-163">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-163">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ea1fc-164">För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och CustomScriptExtension för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="ea1fc-164">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="ea1fc-165">-VMName</span><span class="sxs-lookup"><span data-stu-id="ea1fc-165">-VMName</span></span>
<span data-ttu-id="ea1fc-166">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-166">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ea1fc-167">Denna cmdlet lägger till det anpassade skript tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-167">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea1fc-168">-VMObject</span><span class="sxs-lookup"><span data-stu-id="ea1fc-168">-VMObject</span></span>
<span data-ttu-id="ea1fc-169">VM-objekt.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-169">VM object.</span></span>

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

### <span data-ttu-id="ea1fc-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea1fc-170">-Confirm</span></span>
<span data-ttu-id="ea1fc-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1fc-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1fc-172">-WhatIf</span></span>
<span data-ttu-id="ea1fc-173">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea1fc-174">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1fc-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1fc-175">CommonParameters</span></span>
<span data-ttu-id="ea1fc-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1fc-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1fc-177">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea1fc-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1fc-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea1fc-178">INPUTS</span></span>

### <span data-ttu-id="ea1fc-179">System. String</span><span class="sxs-lookup"><span data-stu-id="ea1fc-179">System.String</span></span>

### <span data-ttu-id="ea1fc-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="ea1fc-180">System.String[]</span></span>

### <span data-ttu-id="ea1fc-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ea1fc-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea1fc-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea1fc-182">OUTPUTS</span></span>

### <span data-ttu-id="ea1fc-183">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ea1fc-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ea1fc-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea1fc-184">NOTES</span></span>

## <span data-ttu-id="ea1fc-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea1fc-185">RELATED LINKS</span></span>

[<span data-ttu-id="ea1fc-186">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ea1fc-186">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="ea1fc-187">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ea1fc-187">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)

