---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: f041a0b4d07a5123554b3d9b544ea496c87e19ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574992"
---
# <span data-ttu-id="048ce-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="048ce-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="048ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="048ce-102">SYNOPSIS</span></span>
<span data-ttu-id="048ce-103">Konfigurerar DSC-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="048ce-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="048ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="048ce-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="048ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="048ce-105">DESCRIPTION</span></span>
<span data-ttu-id="048ce-106">Cmdleten **set-AzureRmVMDscExtension** konfigurerar tillägget DSC (önskad State Configuration) för Windows PowerShell på en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="048ce-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="048ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="048ce-107">EXAMPLES</span></span>

### <span data-ttu-id="048ce-108">Exempel 1: Ange ett DSC-tillägg</span><span class="sxs-lookup"><span data-stu-id="048ce-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="048ce-109">Det här kommandot anger DSC-tillägget på den virtuella datorn med namnet VM07 för att ladda ned Sample.ps1.zip från lagrings kontot med namnet STG och standard behållaren.</span><span class="sxs-lookup"><span data-stu-id="048ce-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="048ce-110">Kommandot anropar konfigurationen med namnet ConfigName.</span><span class="sxs-lookup"><span data-stu-id="048ce-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="048ce-111">Sample.ps1.zip filen har redan laddats upp med **publicering-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="048ce-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="048ce-112">Exempel 2: Ange en DSC-anknytning med konfigurations data</span><span class="sxs-lookup"><span data-stu-id="048ce-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="048ce-113">Det här kommandot anger tillägget på den virtuella datorn med namnet VM13 för att ladda ned Sample.ps1.zip från lagrings kontot med namnet STG och behållaren med namnet WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="048ce-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="048ce-114">Kommandot ConfigName och anger konfigurations data och argument.</span><span class="sxs-lookup"><span data-stu-id="048ce-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="048ce-115">Sample.ps1.zip filen har redan laddats upp med **publicering-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="048ce-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="048ce-116">Exempel 3: Ange en DSC-anknytning med konfigurations data som har automatisk uppdatering</span><span class="sxs-lookup"><span data-stu-id="048ce-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="048ce-117">Det här kommandot anger tillägget på den virtuella datorn med namnet VM22 för att ladda ned Sample.ps1.zip från lagrings kontot med namnet STG och behållaren med namnet WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="048ce-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="048ce-118">Kommandot anropar konfigurationen med namnet ConfigName och anger konfigurations data och argument.</span><span class="sxs-lookup"><span data-stu-id="048ce-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="048ce-119">Det här kommandot aktiverar också automatisk uppdatering av tilläggs hanteraren till den senaste versionen.</span><span class="sxs-lookup"><span data-stu-id="048ce-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="048ce-120">Sample.ps1.zip har tidigare laddats upp med **publicering-AzureRmVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="048ce-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="048ce-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="048ce-121">PARAMETERS</span></span>

### <span data-ttu-id="048ce-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="048ce-122">-ArchiveBlobName</span></span>
<span data-ttu-id="048ce-123">Anger namnet på den konfigurations fil som tidigare laddades upp av Publish-AzureRmVMDscConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="048ce-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="048ce-124">-ArchiveContainerName</span></span>
<span data-ttu-id="048ce-125">Artens namn för Azure Storage-behållaren där konfigurations arkivet finns.</span><span class="sxs-lookup"><span data-stu-id="048ce-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048ce-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="048ce-127">Anger namnet på den resurs grupp som innehåller det lagrings konto som innehåller konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="048ce-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="048ce-128">Den här parametern är valfri om lagrings konto och virtuell dator finns i samma resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="048ce-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="048ce-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="048ce-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="048ce-130">Anger namnet på det Azure Storage-konto som används för att ladda ned ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="048ce-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="048ce-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="048ce-132">Anger suffix för lagrings slut punkter.</span><span class="sxs-lookup"><span data-stu-id="048ce-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="048ce-133">-AutoUpdate</span></span>
<span data-ttu-id="048ce-134">Anger den versions hanterare som anges av parametern *version* .</span><span class="sxs-lookup"><span data-stu-id="048ce-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="048ce-135">Standard tilläggs hanteraren uppdateras inte automatiskt.</span><span class="sxs-lookup"><span data-stu-id="048ce-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="048ce-136">Använd parametern *AutoUpdate* för att aktivera automatisk uppdatering av tilläggs hanteraren till den senaste versionen som och när den är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="048ce-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="048ce-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="048ce-137">-ConfigurationArgument</span></span>
<span data-ttu-id="048ce-138">Anger en hash-tabell som innehåller argumenten till funktionen konfiguration.</span><span class="sxs-lookup"><span data-stu-id="048ce-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="048ce-139">-ConfigurationData</span></span>
<span data-ttu-id="048ce-140">Anger sökvägen till en. psd1-fil som anger data för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="048ce-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="048ce-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="048ce-141">-ConfigurationName</span></span>
<span data-ttu-id="048ce-142">Anger namnet på den konfiguration som DSC-tillägget anropar.</span><span class="sxs-lookup"><span data-stu-id="048ce-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="048ce-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="048ce-143">-DataCollection</span></span>
<span data-ttu-id="048ce-144">Anger data insamlings typen.</span><span class="sxs-lookup"><span data-stu-id="048ce-144">Specifies the data collection type.</span></span>
<span data-ttu-id="048ce-145">De acceptabla värdena för den här parametern är: enable och Disable.</span><span class="sxs-lookup"><span data-stu-id="048ce-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048ce-146">-DefaultProfile</span></span>
<span data-ttu-id="048ce-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="048ce-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="048ce-148">-Force</span><span class="sxs-lookup"><span data-stu-id="048ce-148">-Force</span></span>
<span data-ttu-id="048ce-149">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="048ce-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="048ce-150">-Plats</span><span class="sxs-lookup"><span data-stu-id="048ce-150">-Location</span></span>
<span data-ttu-id="048ce-151">Anger sökvägen till resurs tillägget.</span><span class="sxs-lookup"><span data-stu-id="048ce-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="048ce-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="048ce-152">-Name</span></span>
<span data-ttu-id="048ce-153">Anger namnet på Azure Resource Manager-resursen som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="048ce-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="048ce-154">Standardvärdet är Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="048ce-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="048ce-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048ce-155">-ResourceGroupName</span></span>
<span data-ttu-id="048ce-156">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="048ce-156">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-157">-Version</span><span class="sxs-lookup"><span data-stu-id="048ce-157">-Version</span></span>
<span data-ttu-id="048ce-158">Anger vilken version av DSC-tillägget som Set-AzureRmVMDscExtension använder inställningarna för.</span><span class="sxs-lookup"><span data-stu-id="048ce-158">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="048ce-159">-VMName</span></span>
<span data-ttu-id="048ce-160">Anger namnet på den virtuella dator där DSC-tilläggsprovider är installerat.</span><span class="sxs-lookup"><span data-stu-id="048ce-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="048ce-161">-WmfVersion</span></span>
<span data-ttu-id="048ce-162">Anger WMF-versionen.</span><span class="sxs-lookup"><span data-stu-id="048ce-162">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048ce-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="048ce-163">-Confirm</span></span>
<span data-ttu-id="048ce-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="048ce-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="048ce-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048ce-165">-WhatIf</span></span>
<span data-ttu-id="048ce-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="048ce-166">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="048ce-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="048ce-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="048ce-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048ce-168">CommonParameters</span></span>
<span data-ttu-id="048ce-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048ce-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048ce-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048ce-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048ce-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="048ce-171">INPUTS</span></span>

## <span data-ttu-id="048ce-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="048ce-172">OUTPUTS</span></span>

## <span data-ttu-id="048ce-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="048ce-173">NOTES</span></span>

## <span data-ttu-id="048ce-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="048ce-174">RELATED LINKS</span></span>

[<span data-ttu-id="048ce-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="048ce-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="048ce-176">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="048ce-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="048ce-177">Publicera – AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ce-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


