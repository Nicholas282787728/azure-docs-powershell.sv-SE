---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093172"
---
# <span data-ttu-id="76c3a-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="76c3a-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="76c3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="76c3a-103">Anger resurs tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="76c3a-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="76c3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76c3a-104">SYNTAX</span></span>

### <span data-ttu-id="76c3a-105">SetByExtensionName (standard)</span><span class="sxs-lookup"><span data-stu-id="76c3a-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="76c3a-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="76c3a-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="76c3a-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="76c3a-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="76c3a-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="76c3a-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76c3a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76c3a-109">DESCRIPTION</span></span>
<span data-ttu-id="76c3a-110">Cmdleten **set-AzureVMExtension** anger resurs tillägg för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="76c3a-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="76c3a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76c3a-111">EXAMPLES</span></span>

### <span data-ttu-id="76c3a-112">Exempel 1: skapa en virtuell dator med resurs tilläggen</span><span class="sxs-lookup"><span data-stu-id="76c3a-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="76c3a-113">Det här kommandot skapar en virtuell dator med resurs tillägg som tillämpas.</span><span class="sxs-lookup"><span data-stu-id="76c3a-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="76c3a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76c3a-114">PARAMETERS</span></span>

### <span data-ttu-id="76c3a-115">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="76c3a-115">-Disable</span></span>
<span data-ttu-id="76c3a-116">Anger att denna cmdlet inaktiverar tillägget.</span><span class="sxs-lookup"><span data-stu-id="76c3a-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="76c3a-117">-ExtensionName</span></span>
<span data-ttu-id="76c3a-118">Anger namnet på den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="76c3a-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="76c3a-119">-ForceUpdate</span></span>
<span data-ttu-id="76c3a-120">Anger att denna cmdlet Återtillämpar en konfiguration för ett tillägg när konfigurationen inte har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="76c3a-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76c3a-121">-InformationAction</span></span>
<span data-ttu-id="76c3a-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="76c3a-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76c3a-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="76c3a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76c3a-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="76c3a-124">Continue</span></span>
- <span data-ttu-id="76c3a-125">Över</span><span class="sxs-lookup"><span data-stu-id="76c3a-125">Ignore</span></span>
- <span data-ttu-id="76c3a-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="76c3a-126">Inquire</span></span>
- <span data-ttu-id="76c3a-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76c3a-127">SilentlyContinue</span></span>
- <span data-ttu-id="76c3a-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="76c3a-128">Stop</span></span>
- <span data-ttu-id="76c3a-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="76c3a-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76c3a-130">-InformationVariable</span></span>
<span data-ttu-id="76c3a-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="76c3a-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="76c3a-132">-PrivateConfigKey</span></span>
<span data-ttu-id="76c3a-133">Anger en privat konfigurations.</span><span class="sxs-lookup"><span data-stu-id="76c3a-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="76c3a-134">-PrivateConfigPath</span></span>
<span data-ttu-id="76c3a-135">Anger sökväg för privat konfiguration.</span><span class="sxs-lookup"><span data-stu-id="76c3a-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c3a-136">-PrivateConfiguration</span></span>
<span data-ttu-id="76c3a-137">Anger den privata konfigurations texten.</span><span class="sxs-lookup"><span data-stu-id="76c3a-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="76c3a-138">-Profile</span></span>
<span data-ttu-id="76c3a-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="76c3a-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76c3a-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="76c3a-141">-PublicConfigKey</span></span>
<span data-ttu-id="76c3a-142">Anger den offentliga konfigurations knappen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="76c3a-143">-PublicConfigPath</span></span>
<span data-ttu-id="76c3a-144">Anger den offentliga konfigurations Sök vägen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c3a-145">-PublicConfiguration</span></span>
<span data-ttu-id="76c3a-146">Anger den allmänna konfigurations texten.</span><span class="sxs-lookup"><span data-stu-id="76c3a-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="76c3a-147">-Publisher</span></span>
<span data-ttu-id="76c3a-148">Anger utgivaren av tillägget.</span><span class="sxs-lookup"><span data-stu-id="76c3a-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="76c3a-149">-ReferenceName</span></span>
<span data-ttu-id="76c3a-150">Anger anknytningens referens namn.</span><span class="sxs-lookup"><span data-stu-id="76c3a-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="76c3a-151">Det här är en användardefinierad sträng som kan användas för att referera till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="76c3a-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="76c3a-152">Du måste ange den när tillägget läggs till på den virtuella datorn för första gången.</span><span class="sxs-lookup"><span data-stu-id="76c3a-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="76c3a-153">För framtida uppdateringar måste du ange det tidigare använda referens namnet när du uppdaterar tillägget.</span><span class="sxs-lookup"><span data-stu-id="76c3a-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="76c3a-154">ReferenceName som tilldelats till ett tillägg returneras med cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="76c3a-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-155">-Avinstallera</span><span class="sxs-lookup"><span data-stu-id="76c3a-155">-Uninstall</span></span>
<span data-ttu-id="76c3a-156">Anger att den här cmdleten avinstallerar resurs tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="76c3a-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-157">-Version</span><span class="sxs-lookup"><span data-stu-id="76c3a-157">-Version</span></span>
<span data-ttu-id="76c3a-158">Anger tilläggs versionen.</span><span class="sxs-lookup"><span data-stu-id="76c3a-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-159">-VM</span><span class="sxs-lookup"><span data-stu-id="76c3a-159">-VM</span></span>
<span data-ttu-id="76c3a-160">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="76c3a-160">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76c3a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c3a-161">CommonParameters</span></span>
<span data-ttu-id="76c3a-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c3a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c3a-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c3a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c3a-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76c3a-164">INPUTS</span></span>

## <span data-ttu-id="76c3a-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76c3a-165">OUTPUTS</span></span>

## <span data-ttu-id="76c3a-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76c3a-166">NOTES</span></span>

## <span data-ttu-id="76c3a-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76c3a-167">RELATED LINKS</span></span>

[<span data-ttu-id="76c3a-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="76c3a-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="76c3a-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="76c3a-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="76c3a-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="76c3a-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


