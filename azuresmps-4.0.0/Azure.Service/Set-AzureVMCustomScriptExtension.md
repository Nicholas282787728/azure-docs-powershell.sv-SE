---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099267"
---
# <span data-ttu-id="2c2da-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2c2da-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="2c2da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c2da-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2da-103">Anger information för ett anpassat skript tillägg för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="2c2da-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="2c2da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c2da-104">SYNTAX</span></span>

### <span data-ttu-id="2c2da-105">SetCustomScriptExtensionByContainerAndFileNames (standard)</span><span class="sxs-lookup"><span data-stu-id="2c2da-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c2da-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2c2da-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2c2da-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2c2da-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2c2da-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="2c2da-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2c2da-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c2da-109">DESCRIPTION</span></span>
<span data-ttu-id="2c2da-110">Cmdleten **set-AzureVMCustomScriptExtension** anger information för ett anpassat skript tillägg för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="2c2da-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="2c2da-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c2da-111">EXAMPLES</span></span>

### <span data-ttu-id="2c2da-112">Exempel 1: Ange information för ett anpassat skript tillägg för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="2c2da-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="2c2da-113">Det här kommandot anger information för ett anpassat skript tillägg för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2c2da-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="2c2da-114">Exempel 2: Ange information för ett anpassat skript tillägg för en virtuell dator med en fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="2c2da-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="2c2da-115">Det här kommandot anger information för ett anpassat skript tillägg för en virtuell dator med flera fil-URL: er.</span><span class="sxs-lookup"><span data-stu-id="2c2da-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="2c2da-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c2da-116">PARAMETERS</span></span>

### <span data-ttu-id="2c2da-117">-Argument</span><span class="sxs-lookup"><span data-stu-id="2c2da-117">-Argument</span></span>
<span data-ttu-id="2c2da-118">Anger en sträng som tillhandahåller ett argument som denna cmdlet körs på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2c2da-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2c2da-119">-ContainerName</span></span>
<span data-ttu-id="2c2da-120">Anger namnet på behållaren i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="2c2da-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-121">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="2c2da-121">-Disable</span></span>
<span data-ttu-id="2c2da-122">Anger att denna cmdlet inaktiverar tillägget.</span><span class="sxs-lookup"><span data-stu-id="2c2da-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-123">-FileName</span><span class="sxs-lookup"><span data-stu-id="2c2da-123">-FileName</span></span>
<span data-ttu-id="2c2da-124">Anger en sträng mat ris som innehåller namnen på BLOB-filerna i den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="2c2da-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="2c2da-125">-FileUri</span></span>
<span data-ttu-id="2c2da-126">Anger en sträng mat ris som innehåller URL-adresserna för BLOB-filerna.</span><span class="sxs-lookup"><span data-stu-id="2c2da-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="2c2da-127">-ForceUpdate</span></span>
<span data-ttu-id="2c2da-128">Anger att denna cmdlet Återtillämpar en konfiguration för ett tillägg när konfigurationen inte har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="2c2da-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2c2da-129">-InformationAction</span></span>
<span data-ttu-id="2c2da-130">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="2c2da-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2c2da-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2c2da-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c2da-132">Vidare</span><span class="sxs-lookup"><span data-stu-id="2c2da-132">Continue</span></span>
- <span data-ttu-id="2c2da-133">Över</span><span class="sxs-lookup"><span data-stu-id="2c2da-133">Ignore</span></span>
- <span data-ttu-id="2c2da-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="2c2da-134">Inquire</span></span>
- <span data-ttu-id="2c2da-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2c2da-135">SilentlyContinue</span></span>
- <span data-ttu-id="2c2da-136">Stanna</span><span class="sxs-lookup"><span data-stu-id="2c2da-136">Stop</span></span>
- <span data-ttu-id="2c2da-137">Avbryt</span><span class="sxs-lookup"><span data-stu-id="2c2da-137">Suspend</span></span>

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

### <span data-ttu-id="2c2da-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2c2da-138">-InformationVariable</span></span>
<span data-ttu-id="2c2da-139">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="2c2da-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2c2da-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="2c2da-140">-Profile</span></span>
<span data-ttu-id="2c2da-141">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2c2da-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c2da-142">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2c2da-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c2da-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="2c2da-143">-ReferenceName</span></span>
<span data-ttu-id="2c2da-144">Anger namnet på referensen för tillägget.</span><span class="sxs-lookup"><span data-stu-id="2c2da-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="2c2da-145">Den här parametern är en användardefinierad sträng som kan användas för att referera till ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="2c2da-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="2c2da-146">Det anges när tillägget läggs till på den virtuella datorn för första gången.</span><span class="sxs-lookup"><span data-stu-id="2c2da-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="2c2da-147">För framtida uppdateringar måste du ange det tidigare använda referens namnet när du uppdaterar tillägget.</span><span class="sxs-lookup"><span data-stu-id="2c2da-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="2c2da-148">*ReferenceName* som tilldelats till ett tillägg returneras med cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="2c2da-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-149">-Kör</span><span class="sxs-lookup"><span data-stu-id="2c2da-149">-Run</span></span>
<span data-ttu-id="2c2da-150">Anger det kommando som denna cmdlet körs av tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2c2da-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="2c2da-151">Endast "powershell.exe" stöds.</span><span class="sxs-lookup"><span data-stu-id="2c2da-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2c2da-152">-StorageAccountKey</span></span>
<span data-ttu-id="2c2da-153">Anger lagrings kontots nycklar</span><span class="sxs-lookup"><span data-stu-id="2c2da-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c2da-154">-StorageAccountName</span></span>
<span data-ttu-id="2c2da-155">Anger namnet på lagrings kontot i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2c2da-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2c2da-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="2c2da-157">Anger lagrings tjänstens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="2c2da-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-158">-Avinstallera</span><span class="sxs-lookup"><span data-stu-id="2c2da-158">-Uninstall</span></span>
<span data-ttu-id="2c2da-159">Anger att den här cmdleten avinstallerar det anpassade skript tillägget från den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2c2da-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-160">-Version</span><span class="sxs-lookup"><span data-stu-id="2c2da-160">-Version</span></span>
<span data-ttu-id="2c2da-161">Anger versionen för det anpassade skript tillägget.</span><span class="sxs-lookup"><span data-stu-id="2c2da-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2da-162">-VM</span><span class="sxs-lookup"><span data-stu-id="2c2da-162">-VM</span></span>
<span data-ttu-id="2c2da-163">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="2c2da-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2c2da-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2da-164">CommonParameters</span></span>
<span data-ttu-id="2c2da-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c2da-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2da-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c2da-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2da-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c2da-167">INPUTS</span></span>

## <span data-ttu-id="2c2da-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c2da-168">OUTPUTS</span></span>

## <span data-ttu-id="2c2da-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c2da-169">NOTES</span></span>

## <span data-ttu-id="2c2da-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c2da-170">RELATED LINKS</span></span>

[<span data-ttu-id="2c2da-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2c2da-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="2c2da-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2c2da-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="2c2da-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2c2da-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


