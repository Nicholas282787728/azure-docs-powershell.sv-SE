---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099112"
---
# <span data-ttu-id="13a0a-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="13a0a-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="13a0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="13a0a-103">Publicerar ett skript för önskat tillstånds konfiguration i Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="13a0a-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="13a0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13a0a-104">SYNTAX</span></span>

### <span data-ttu-id="13a0a-105">UploadArchive (standard)</span><span class="sxs-lookup"><span data-stu-id="13a0a-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13a0a-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="13a0a-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a0a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="13a0a-108">Cmdleten **Publishing-AzureVMDscConfiguration** publicerar ett skript för önskat tillstånds konfiguration i Azure Blob Storage som senare kan tillämpas på virtuella Azure-datorer via cmdleten **set-AzureVMDscExtension** .</span><span class="sxs-lookup"><span data-stu-id="13a0a-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="13a0a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13a0a-109">EXAMPLES</span></span>

### <span data-ttu-id="13a0a-110">Exempel 1: publicera ett skript för tillstånds konfiguration i Blob Storage</span><span class="sxs-lookup"><span data-stu-id="13a0a-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="13a0a-111">Det här kommandot skapar ett. zip-paket för det angivna skriptet och eventuella underordnade moduler och uppladdar det till Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="13a0a-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="13a0a-112">Exempel 2: publicera ett skript för tillstånds konfiguration i en lokal fil</span><span class="sxs-lookup"><span data-stu-id="13a0a-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="13a0a-113">Det här kommandot skapar ett. zip-paket för det angivna skriptet och eventuella underordnade moduler och lagrar dem i den lokala filen .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="13a0a-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="13a0a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13a0a-114">PARAMETERS</span></span>

### <span data-ttu-id="13a0a-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="13a0a-115">-AdditionalPath</span></span>
<span data-ttu-id="13a0a-116">Anger en matris med ytterligare sökvägar.</span><span class="sxs-lookup"><span data-stu-id="13a0a-116">Specifies an array of additional paths.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0a-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="13a0a-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="13a0a-118">Anger sökvägen till en lokal zip-fil som denna cmdlet skriver konfigurations arkivet.</span><span class="sxs-lookup"><span data-stu-id="13a0a-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="13a0a-119">Konfigurations skriptet laddas inte upp till Azure Blob Storage om du använder den här parametern.</span><span class="sxs-lookup"><span data-stu-id="13a0a-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0a-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="13a0a-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="13a0a-121">Anger en sökväg till en konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="13a0a-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="13a0a-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="13a0a-122">-ConfigurationPath</span></span>
<span data-ttu-id="13a0a-123">Anger sökvägen till en fil som innehåller en eller flera konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="13a0a-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="13a0a-124">Filen kan vara en Windows PowerShell-skriptfil (. ps1-fil), modul (. psm1-fil) eller en arkivfil (. zip-fil) som innehåller en uppsättning med Windows PowerShell-moduler, med varje modul i en separat katalog.</span><span class="sxs-lookup"><span data-stu-id="13a0a-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0a-125">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="13a0a-125">-ContainerName</span></span>
<span data-ttu-id="13a0a-126">Anger namnet på den Azure Storage-behållare som konfigurationen laddas upp till.</span><span class="sxs-lookup"><span data-stu-id="13a0a-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="13a0a-127">-Force</span></span>
<span data-ttu-id="13a0a-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="13a0a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13a0a-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="13a0a-129">-InformationAction</span></span>
<span data-ttu-id="13a0a-130">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="13a0a-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13a0a-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="13a0a-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13a0a-132">Vidare</span><span class="sxs-lookup"><span data-stu-id="13a0a-132">Continue</span></span>
- <span data-ttu-id="13a0a-133">Över</span><span class="sxs-lookup"><span data-stu-id="13a0a-133">Ignore</span></span>
- <span data-ttu-id="13a0a-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="13a0a-134">Inquire</span></span>
- <span data-ttu-id="13a0a-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13a0a-135">SilentlyContinue</span></span>
- <span data-ttu-id="13a0a-136">Stanna</span><span class="sxs-lookup"><span data-stu-id="13a0a-136">Stop</span></span>
- <span data-ttu-id="13a0a-137">Avbryt</span><span class="sxs-lookup"><span data-stu-id="13a0a-137">Suspend</span></span>

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

### <span data-ttu-id="13a0a-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13a0a-138">-InformationVariable</span></span>
<span data-ttu-id="13a0a-139">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="13a0a-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13a0a-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13a0a-140">-PassThru</span></span>
<span data-ttu-id="13a0a-141">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="13a0a-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13a0a-142">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="13a0a-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13a0a-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="13a0a-143">-Profile</span></span>
<span data-ttu-id="13a0a-144">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="13a0a-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13a0a-145">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="13a0a-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13a0a-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="13a0a-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="13a0a-147">Anger att den här cmdleten hoppar över identifiering av beroenden.</span><span class="sxs-lookup"><span data-stu-id="13a0a-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="13a0a-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="13a0a-148">-StorageContext</span></span>
<span data-ttu-id="13a0a-149">Anger den Azure Storage-kontext som tillhandahåller de säkerhets inställningar som används för att överföra konfigurations skriptet till den behållare som anges av *ContainerName* -parametern.</span><span class="sxs-lookup"><span data-stu-id="13a0a-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="13a0a-150">Den här kontexten ger skriv åtkomst till behållaren.</span><span class="sxs-lookup"><span data-stu-id="13a0a-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0a-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="13a0a-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="13a0a-152">Anger suffix för slut punkten för lagring, till exempel core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="13a0a-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a0a-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13a0a-153">-Confirm</span></span>
<span data-ttu-id="13a0a-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13a0a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a0a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a0a-155">-WhatIf</span></span>
<span data-ttu-id="13a0a-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13a0a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a0a-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13a0a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a0a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a0a-158">CommonParameters</span></span>
<span data-ttu-id="13a0a-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a0a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a0a-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a0a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a0a-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13a0a-161">INPUTS</span></span>

## <span data-ttu-id="13a0a-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13a0a-162">OUTPUTS</span></span>

## <span data-ttu-id="13a0a-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13a0a-163">NOTES</span></span>

## <span data-ttu-id="13a0a-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13a0a-164">RELATED LINKS</span></span>

[<span data-ttu-id="13a0a-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="13a0a-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


