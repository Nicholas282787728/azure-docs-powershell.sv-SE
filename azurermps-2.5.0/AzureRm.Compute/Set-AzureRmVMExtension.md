---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: a714fb524de9c7c40c6b74dba321412e7aa457e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931002"
---
# <span data-ttu-id="ed645-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ed645-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="ed645-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed645-102">SYNOPSIS</span></span>
<span data-ttu-id="ed645-103">Uppdaterar tilläggs egenskaper eller lägger till ett tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ed645-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed645-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed645-104">SYNTAX</span></span>

### <span data-ttu-id="ed645-105">Inställningar (standard)</span><span class="sxs-lookup"><span data-stu-id="ed645-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed645-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="ed645-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed645-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed645-107">DESCRIPTION</span></span>
<span data-ttu-id="ed645-108">Cmdleten **set-AzureRmVMExtension** för befintliga virtuella dator tillägg eller tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ed645-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="ed645-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed645-109">EXAMPLES</span></span>

### <span data-ttu-id="ed645-110">Exempel 1: ändra inställningar med hjälp av hash-tabeller</span><span class="sxs-lookup"><span data-stu-id="ed645-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="ed645-111">De första två kommandona använder standard syntaxen i Windows PowerShell för att skapa hash-tabeller och lagrar sedan dessa hash-tabeller i $Settings och $ProtectedSettings variabler.</span><span class="sxs-lookup"><span data-stu-id="ed645-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="ed645-112">Om du vill ha mer information skriver du `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="ed645-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="ed645-113">Det andra kommandot inkluderar två värden som redan har skapats och lagrats i variabler.</span><span class="sxs-lookup"><span data-stu-id="ed645-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="ed645-114">Det sista kommandot ändrar en förlängning av den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11 enligt innehållet i $Settings och $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="ed645-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="ed645-115">Kommandot anger annan nödvändig information som inkluderar utgivaren och tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="ed645-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="ed645-116">Exempel 2: ändra inställningar med hjälp av strängar</span><span class="sxs-lookup"><span data-stu-id="ed645-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="ed645-117">De två första kommandona skapar strängar som innehåller inställningar och lagrar dem sedan i $SettingsString och $ProtectedSettingsString variabler.</span><span class="sxs-lookup"><span data-stu-id="ed645-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="ed645-118">Det sista kommandot ändrar en förlängning av den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11 enligt innehållet i $SettingsString och $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="ed645-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="ed645-119">Kommandot anger annan nödvändig information som inkluderar utgivaren och tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="ed645-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="ed645-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed645-120">PARAMETERS</span></span>

### <span data-ttu-id="ed645-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed645-121">-AsJob</span></span>
<span data-ttu-id="ed645-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ed645-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed645-123">-DefaultProfile</span></span>
<span data-ttu-id="ed645-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed645-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ed645-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ed645-126">Anger att denna cmdlet hindrar Azure gäst agenten från att automatiskt uppdatera tilläggen till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="ed645-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="ed645-127">Som standard aktiverar denna cmdlet gäst agenten att uppdatera tilläggen.</span><span class="sxs-lookup"><span data-stu-id="ed645-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="ed645-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="ed645-128">-ExtensionType</span></span>
<span data-ttu-id="ed645-129">Anger fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="ed645-129">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ed645-130">-ForceRerun</span></span>
<span data-ttu-id="ed645-131">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="ed645-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ed645-132">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="ed645-132">The value can be any string different from the current value.</span></span>

<span data-ttu-id="ed645-133">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="ed645-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ed645-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="ed645-134">-Location</span></span>
<span data-ttu-id="ed645-135">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ed645-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ed645-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed645-136">-Name</span></span>
<span data-ttu-id="ed645-137">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="ed645-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="ed645-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="ed645-138">-ProtectedSettings</span></span>
<span data-ttu-id="ed645-139">Anger privat konfiguration för tillägget som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ed645-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ed645-140">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ed645-140">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="ed645-141">-ProtectedSettingString</span></span>
<span data-ttu-id="ed645-142">Anger privat konfiguration för tillägget som en sträng.</span><span class="sxs-lookup"><span data-stu-id="ed645-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="ed645-143">Denna cmdlet krypterar den privata konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ed645-143">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ed645-144">-Publisher</span></span>
<span data-ttu-id="ed645-145">Anger namnet på tilläggs utgivaren.</span><span class="sxs-lookup"><span data-stu-id="ed645-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="ed645-146">Utgivaren får ett namn när utgivaren registrerar ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="ed645-146">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed645-147">-ResourceGroupName</span></span>
<span data-ttu-id="ed645-148">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ed645-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ed645-149">-Inställningar</span><span class="sxs-lookup"><span data-stu-id="ed645-149">-Settings</span></span>
<span data-ttu-id="ed645-150">Anger offentlig konfiguration för tillägget som en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ed645-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ed645-151">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed645-151">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-152">-SettingString</span><span class="sxs-lookup"><span data-stu-id="ed645-152">-SettingString</span></span>
<span data-ttu-id="ed645-153">Anger offentlig konfiguration för tillägget, som en sträng.</span><span class="sxs-lookup"><span data-stu-id="ed645-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="ed645-154">Denna cmdlet krypterar inte offentlig konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed645-154">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed645-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ed645-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="ed645-156">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ed645-156">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="ed645-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="ed645-157">-VMName</span></span>
<span data-ttu-id="ed645-158">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ed645-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ed645-159">Denna cmdlet ändrar tillägg för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ed645-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed645-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed645-160">-Confirm</span></span>
<span data-ttu-id="ed645-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed645-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed645-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed645-162">-WhatIf</span></span>
<span data-ttu-id="ed645-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed645-163">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ed645-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed645-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed645-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed645-165">CommonParameters</span></span>
<span data-ttu-id="ed645-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed645-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed645-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed645-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed645-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed645-168">INPUTS</span></span>

### <span data-ttu-id="ed645-169">Ingen</span><span class="sxs-lookup"><span data-stu-id="ed645-169">None</span></span>
<span data-ttu-id="ed645-170">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ed645-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed645-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed645-171">OUTPUTS</span></span>

### <span data-ttu-id="ed645-172">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ed645-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ed645-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed645-173">NOTES</span></span>

## <span data-ttu-id="ed645-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed645-174">RELATED LINKS</span></span>

[<span data-ttu-id="ed645-175">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ed645-175">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="ed645-176">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ed645-176">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

