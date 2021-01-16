---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413867"
---
# <span data-ttu-id="cfa2e-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfa2e-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="cfa2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfa2e-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa2e-103">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="cfa2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfa2e-104">SYNTAX</span></span>

### <span data-ttu-id="cfa2e-105">ByNameWithContainerAndFileNamesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cfa2e-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa2e-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa2e-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfa2e-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfa2e-113">DESCRIPTION</span></span>
<span data-ttu-id="cfa2e-114">Cmdleten **set-AzVMCustomScriptExtension** lägger till ett anpassat tillägg för virtuella skript på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="cfa2e-115">Med det här tillägget kan du köra egna skript på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="cfa2e-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfa2e-116">EXAMPLES</span></span>

### <span data-ttu-id="cfa2e-117">Exempel 1: lägga till ett eget skript</span><span class="sxs-lookup"><span data-stu-id="cfa2e-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="cfa2e-118">Det här kommandot lägger till ett anpassat skript till den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="cfa2e-119">Skript filen är contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="cfa2e-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cfa2e-120">Example 2</span></span>

<span data-ttu-id="cfa2e-121">Lägger till ett anpassat skript tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="cfa2e-122">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="cfa2e-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="cfa2e-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfa2e-123">PARAMETERS</span></span>

### <span data-ttu-id="cfa2e-124">-Argument</span><span class="sxs-lookup"><span data-stu-id="cfa2e-124">-Argument</span></span>
<span data-ttu-id="cfa2e-125">Anger argument som skript tillägget skickar till skriptet.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="cfa2e-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="cfa2e-126">-ContainerName</span></span>
<span data-ttu-id="cfa2e-127">Anger namnet på den Azure Storage-behållare där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="cfa2e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa2e-128">-DefaultProfile</span></span>
<span data-ttu-id="cfa2e-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa2e-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cfa2e-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="cfa2e-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="cfa2e-131">-FileName</span></span>
<span data-ttu-id="cfa2e-132">Anger namnet på skript filen.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-132">Specifies the name of the script file.</span></span> <span data-ttu-id="cfa2e-133">Om filen är lagrad i Azure Blob Storage är värdet för fil namn Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="cfa2e-134">Fil namn för filer som lagras i Azure File Storage är inte Skift läges känsliga.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="cfa2e-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="cfa2e-135">-FileUri</span></span>
<span data-ttu-id="cfa2e-136">Anger skript filens URI.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="cfa2e-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="cfa2e-137">-ForceRerun</span></span>
<span data-ttu-id="cfa2e-138">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="cfa2e-139">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="cfa2e-140">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="cfa2e-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfa2e-141">-InputObject</span></span>
<span data-ttu-id="cfa2e-142">Objekt för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-142">VM extension object.</span></span>

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

### <span data-ttu-id="cfa2e-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="cfa2e-143">-Location</span></span>
<span data-ttu-id="cfa2e-144">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="cfa2e-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfa2e-145">-Name</span></span>
<span data-ttu-id="cfa2e-146">Anger namnet på det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="cfa2e-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cfa2e-147">-NoWait</span></span>
<span data-ttu-id="cfa2e-148">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cfa2e-149">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cfa2e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa2e-150">-ResourceGroupName</span></span>
<span data-ttu-id="cfa2e-151">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cfa2e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa2e-152">-ResourceId</span></span>
<span data-ttu-id="cfa2e-153">VM-tillägg ResourceID.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="cfa2e-154">-Kör</span><span class="sxs-lookup"><span data-stu-id="cfa2e-154">-Run</span></span>
<span data-ttu-id="cfa2e-155">Anger det kommando som ska användas för att köra skriptet.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="cfa2e-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="cfa2e-156">-SecureExecution</span></span>
<span data-ttu-id="cfa2e-157">Anger att värdet för *Kör* -parametern inte är inloggad på servern eller att den returneras till användaren med Get-filtillägg API.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="cfa2e-158">Värdet för *Kör* kan innehålla hemligheter eller lösen ord som skickas till skript filen säkert.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="cfa2e-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cfa2e-159">-StorageAccountKey</span></span>
<span data-ttu-id="cfa2e-160">Anger tangenten för Azure Storage-behållaren.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="cfa2e-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cfa2e-161">-StorageAccountName</span></span>
<span data-ttu-id="cfa2e-162">Anger namnet på det Azure Storage-konto där den här cmdleten sparar skriptet.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="cfa2e-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="cfa2e-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="cfa2e-164">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="cfa2e-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cfa2e-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="cfa2e-166">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="cfa2e-167">För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och CustomScriptExtension för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="cfa2e-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="cfa2e-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="cfa2e-168">-VMName</span></span>
<span data-ttu-id="cfa2e-169">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cfa2e-170">Denna cmdlet lägger till det anpassade skript tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfa2e-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="cfa2e-171">-VMObject</span></span>
<span data-ttu-id="cfa2e-172">VM-objekt.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-172">VM object.</span></span>

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

### <span data-ttu-id="cfa2e-173">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfa2e-173">-Confirm</span></span>
<span data-ttu-id="cfa2e-174">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfa2e-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfa2e-175">-WhatIf</span></span>
<span data-ttu-id="cfa2e-176">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfa2e-177">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfa2e-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa2e-178">CommonParameters</span></span>
<span data-ttu-id="cfa2e-179">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa2e-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa2e-180">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfa2e-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa2e-181">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfa2e-181">INPUTS</span></span>

### <span data-ttu-id="cfa2e-182">System. String</span><span class="sxs-lookup"><span data-stu-id="cfa2e-182">System.String</span></span>

### <span data-ttu-id="cfa2e-183">System. string []</span><span class="sxs-lookup"><span data-stu-id="cfa2e-183">System.String[]</span></span>

### <span data-ttu-id="cfa2e-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cfa2e-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cfa2e-185">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfa2e-185">OUTPUTS</span></span>

### <span data-ttu-id="cfa2e-186">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cfa2e-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cfa2e-187">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfa2e-187">NOTES</span></span>

## <span data-ttu-id="cfa2e-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfa2e-188">RELATED LINKS</span></span>

[<span data-ttu-id="cfa2e-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfa2e-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="cfa2e-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfa2e-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


