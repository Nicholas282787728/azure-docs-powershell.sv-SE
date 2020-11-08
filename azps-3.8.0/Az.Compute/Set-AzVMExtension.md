---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092354"
---
# <span data-ttu-id="73d20-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="73d20-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="73d20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73d20-102">SYNOPSIS</span></span>
<span data-ttu-id="73d20-103">Uppdaterar tilläggs egenskaper eller lägger till ett tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="73d20-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="73d20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73d20-104">SYNTAX</span></span>

### <span data-ttu-id="73d20-105">Inställningar (standard)</span><span class="sxs-lookup"><span data-stu-id="73d20-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73d20-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="73d20-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73d20-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73d20-107">DESCRIPTION</span></span>
<span data-ttu-id="73d20-108">Cmdleten **set-AzVMExtension** för befintliga virtuella dator tillägg eller tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="73d20-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="73d20-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73d20-109">EXAMPLES</span></span>

### <span data-ttu-id="73d20-110">Exempel 1: ändra inställningar med hjälp av hash-tabeller</span><span class="sxs-lookup"><span data-stu-id="73d20-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="73d20-111">De första två kommandona använder standard syntaxen i Windows PowerShell för att skapa hash-tabeller och lagrar sedan dessa hash-tabeller i $Settings och $ProtectedSettings variabler.</span><span class="sxs-lookup"><span data-stu-id="73d20-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="73d20-112">Om du vill ha mer information skriver du `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="73d20-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="73d20-113">Det andra kommandot inkluderar två värden som redan har skapats och lagrats i variabler.</span><span class="sxs-lookup"><span data-stu-id="73d20-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="73d20-114">Det sista kommandot ändrar en förlängning av den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11 enligt innehållet i $Settings och $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="73d20-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="73d20-115">Kommandot anger annan nödvändig information som inkluderar utgivaren och tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="73d20-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="73d20-116">Exempel 2: ändra inställningar med hjälp av strängar</span><span class="sxs-lookup"><span data-stu-id="73d20-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="73d20-117">De två första kommandona skapar strängar som innehåller inställningar och lagrar dem sedan i $SettingsString och $ProtectedSettingsString variabler.</span><span class="sxs-lookup"><span data-stu-id="73d20-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="73d20-118">Det sista kommandot ändrar en förlängning av den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11 enligt innehållet i $SettingsString och $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="73d20-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="73d20-119">Kommandot anger annan nödvändig information som inkluderar utgivaren och tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="73d20-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="73d20-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73d20-120">PARAMETERS</span></span>

### <span data-ttu-id="73d20-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73d20-121">-AsJob</span></span>
<span data-ttu-id="73d20-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="73d20-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73d20-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d20-123">-DefaultProfile</span></span>
<span data-ttu-id="73d20-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73d20-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73d20-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="73d20-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="73d20-126">Anger att denna cmdlet hindrar Azure gäst agenten från att automatiskt uppdatera tilläggen till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="73d20-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="73d20-127">Som standard aktiverar denna cmdlet gäst agenten att uppdatera tilläggen.</span><span class="sxs-lookup"><span data-stu-id="73d20-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="73d20-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="73d20-128">-ExtensionType</span></span>
<span data-ttu-id="73d20-129">Anger fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="73d20-129">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d20-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="73d20-130">-ForceRerun</span></span>
<span data-ttu-id="73d20-131">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="73d20-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="73d20-132">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="73d20-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="73d20-133">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="73d20-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="73d20-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="73d20-134">-Location</span></span>
<span data-ttu-id="73d20-135">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="73d20-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="73d20-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="73d20-136">-Name</span></span>
<span data-ttu-id="73d20-137">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="73d20-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="73d20-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="73d20-138">-NoWait</span></span>
<span data-ttu-id="73d20-139">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="73d20-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="73d20-140">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="73d20-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="73d20-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="73d20-141">-ProtectedSettings</span></span>
<span data-ttu-id="73d20-142">Anger privat konfiguration för tillägget som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="73d20-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="73d20-143">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="73d20-143">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d20-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="73d20-144">-ProtectedSettingString</span></span>
<span data-ttu-id="73d20-145">Anger privat konfiguration för tillägget som en sträng.</span><span class="sxs-lookup"><span data-stu-id="73d20-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="73d20-146">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="73d20-146">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d20-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="73d20-147">-Publisher</span></span>
<span data-ttu-id="73d20-148">Anger namnet på tilläggs utgivaren.</span><span class="sxs-lookup"><span data-stu-id="73d20-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="73d20-149">Utgivaren får ett namn när utgivaren registrerar ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="73d20-149">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d20-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d20-150">-ResourceGroupName</span></span>
<span data-ttu-id="73d20-151">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="73d20-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="73d20-152">-Inställningar</span><span class="sxs-lookup"><span data-stu-id="73d20-152">-Settings</span></span>
<span data-ttu-id="73d20-153">Anger offentlig konfiguration för tillägget som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="73d20-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="73d20-154">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="73d20-154">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d20-155">-SettingString</span><span class="sxs-lookup"><span data-stu-id="73d20-155">-SettingString</span></span>
<span data-ttu-id="73d20-156">Anger offentlig konfiguration för tillägget, som en sträng.</span><span class="sxs-lookup"><span data-stu-id="73d20-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="73d20-157">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="73d20-157">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d20-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="73d20-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="73d20-159">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="73d20-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="73d20-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="73d20-160">-VMName</span></span>
<span data-ttu-id="73d20-161">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="73d20-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="73d20-162">Denna cmdlet ändrar tillägg för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="73d20-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="73d20-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73d20-163">-Confirm</span></span>
<span data-ttu-id="73d20-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73d20-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73d20-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73d20-165">-WhatIf</span></span>
<span data-ttu-id="73d20-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73d20-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73d20-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73d20-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73d20-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d20-168">CommonParameters</span></span>
<span data-ttu-id="73d20-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d20-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d20-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73d20-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d20-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73d20-171">INPUTS</span></span>

### <span data-ttu-id="73d20-172">System. String</span><span class="sxs-lookup"><span data-stu-id="73d20-172">System.String</span></span>

### <span data-ttu-id="73d20-173">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="73d20-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="73d20-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="73d20-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="73d20-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73d20-175">OUTPUTS</span></span>

### <span data-ttu-id="73d20-176">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="73d20-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="73d20-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73d20-177">NOTES</span></span>

## <span data-ttu-id="73d20-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73d20-178">RELATED LINKS</span></span>

[<span data-ttu-id="73d20-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="73d20-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="73d20-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="73d20-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


