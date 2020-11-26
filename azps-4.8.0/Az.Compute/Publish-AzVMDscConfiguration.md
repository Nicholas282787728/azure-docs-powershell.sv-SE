---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103039"
---
# <span data-ttu-id="81720-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="81720-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="81720-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81720-102">SYNOPSIS</span></span>
<span data-ttu-id="81720-103">Laddar upp ett DSC-skript till Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="81720-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="81720-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81720-104">SYNTAX</span></span>

### <span data-ttu-id="81720-105">UploadArchive (standard)</span><span class="sxs-lookup"><span data-stu-id="81720-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81720-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="81720-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81720-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81720-107">DESCRIPTION</span></span>
<span data-ttu-id="81720-108">Cmdleten **Publishing-AzVMDscConfiguration** laddar upp ett DSC-skript (Desired State Configuration) till Azure Blob Storage, som senare kan tillämpas på virtuella Azure-datorer med cmdleten Set-AzVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="81720-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="81720-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81720-109">EXAMPLES</span></span>

### <span data-ttu-id="81720-110">Exempel 1: skapa ett zip-paket ett Ladda upp i Azure Storage</span><span class="sxs-lookup"><span data-stu-id="81720-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="81720-111">Det här kommandot skapar ett. zip-paket för det angivna skriptet och eventuella underordnade moduler och uppladdar det till Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="81720-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="81720-112">Exempel 2: skapa ett zip-paket och lagra det i en lokal fil</span><span class="sxs-lookup"><span data-stu-id="81720-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="81720-113">Det här kommandot skapar ett. zip-paket för det angivna skriptet och eventuella underordnade moduler och lagrar dem i den lokala filen som heter .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="81720-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="81720-114">Exempel 3: lägga till konfigurationen i arkivet och sedan överföra den till lagrings plats</span><span class="sxs-lookup"><span data-stu-id="81720-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="81720-115">Det här kommandot lägger till konfigurationen som heter Sample.ps1 i konfigurations arkivet för överföring till Azure-lagring och hoppar över moduler som är underordnade.</span><span class="sxs-lookup"><span data-stu-id="81720-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="81720-116">Exempel 4: lägga till konfigurations-och konfigurations data i arkivet och sedan överföra det till lagrings utrymme</span><span class="sxs-lookup"><span data-stu-id="81720-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="81720-117">Det här kommandot lägger till konfigurationen som heter Sample.ps1 och konfigurations data med namnet SampleData.psd1 i konfigurations arkivet för överföring till Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="81720-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="81720-118">Exempel 5: lägga till konfiguration, konfigurations data och ytterligare innehåll i arkivet och sedan överföra det till lagrings utrymme</span><span class="sxs-lookup"><span data-stu-id="81720-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="81720-119">Det här kommandot lägger till konfigurationen med namnet Sample.ps1, konfigurations data SampleData.psd1 och ytterligare innehåll i konfigurations arkivet för överföring till Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="81720-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="81720-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81720-120">PARAMETERS</span></span>

### <span data-ttu-id="81720-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="81720-121">-AdditionalPath</span></span>
<span data-ttu-id="81720-122">Anger sökvägen till en fil eller en katalog som ska ingå i konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="81720-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="81720-123">Den laddas ner till den virtuella datorn tillsammans med konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="81720-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="81720-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="81720-125">Anger sökvägen till en. psd1-fil som anger data för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="81720-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="81720-126">Detta läggs till i konfigurations arkivet och överförs sedan till funktionen konfiguration.</span><span class="sxs-lookup"><span data-stu-id="81720-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="81720-127">Den skrivs över av konfigurations data Sök vägen via Set-AzVMDscExtension cmdlet</span><span class="sxs-lookup"><span data-stu-id="81720-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="81720-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="81720-128">-ConfigurationPath</span></span>
<span data-ttu-id="81720-129">Anger sökvägen till en fil som innehåller en eller flera konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="81720-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="81720-130">Filen kan vara en Windows PowerShell-skriptfil (. ps1) eller en Windows PowerShell-modul (. psm1).</span><span class="sxs-lookup"><span data-stu-id="81720-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="81720-131">-ContainerName</span></span>
<span data-ttu-id="81720-132">Anger namnet på den Azure Storage-behållare som konfigurationen laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="81720-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81720-133">-DefaultProfile</span></span>
<span data-ttu-id="81720-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81720-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81720-135">-Force</span><span class="sxs-lookup"><span data-stu-id="81720-135">-Force</span></span>
<span data-ttu-id="81720-136">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="81720-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81720-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="81720-137">-OutputArchivePath</span></span>
<span data-ttu-id="81720-138">Anger sökvägen till en lokal zip-fil för att skriva konfigurations arkivet till.</span><span class="sxs-lookup"><span data-stu-id="81720-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="81720-139">När den här parametern används laddas inte konfigurations skriptet till Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="81720-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81720-140">-ResourceGroupName</span></span>
<span data-ttu-id="81720-141">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="81720-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="81720-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="81720-143">Anger att denna cmdlet exkluderar DSC-resurstilldelningar från konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="81720-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="81720-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="81720-144">-StorageAccountName</span></span>
<span data-ttu-id="81720-145">Anger namnet på det Azure Storage-konto som används för att ladda upp konfigurations skriptet till den behållare som anges av *ContainerName* -parametern.</span><span class="sxs-lookup"><span data-stu-id="81720-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="81720-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="81720-147">Anger suffixet för lagrings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="81720-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81720-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81720-148">-Confirm</span></span>
<span data-ttu-id="81720-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81720-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81720-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81720-150">-WhatIf</span></span>
<span data-ttu-id="81720-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81720-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81720-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81720-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81720-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81720-153">CommonParameters</span></span>
<span data-ttu-id="81720-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81720-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81720-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81720-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81720-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81720-156">INPUTS</span></span>

### <span data-ttu-id="81720-157">System. String</span><span class="sxs-lookup"><span data-stu-id="81720-157">System.String</span></span>

### <span data-ttu-id="81720-158">System. string []</span><span class="sxs-lookup"><span data-stu-id="81720-158">System.String[]</span></span>

## <span data-ttu-id="81720-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81720-159">OUTPUTS</span></span>

### <span data-ttu-id="81720-160">System. String</span><span class="sxs-lookup"><span data-stu-id="81720-160">System.String</span></span>

## <span data-ttu-id="81720-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81720-161">NOTES</span></span>

## <span data-ttu-id="81720-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81720-162">RELATED LINKS</span></span>

[<span data-ttu-id="81720-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="81720-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="81720-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="81720-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="81720-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="81720-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)

