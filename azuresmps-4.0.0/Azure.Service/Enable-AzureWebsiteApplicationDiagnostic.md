---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093408"
---
# <span data-ttu-id="2ec02-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2ec02-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="2ec02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ec02-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec02-103">Aktiverar Programdiagnostik på en Azure-webbplats.</span><span class="sxs-lookup"><span data-stu-id="2ec02-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="2ec02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ec02-104">SYNTAX</span></span>

### <span data-ttu-id="2ec02-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec02-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ec02-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec02-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ec02-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec02-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ec02-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ec02-108">DESCRIPTION</span></span>
<span data-ttu-id="2ec02-109">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="2ec02-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2ec02-110">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2ec02-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2ec02-111">Aktiverar Programdiagnostik på en Azure-webbplats och låter dig konfigurera lagring av loggar på ett fil system eller på Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2ec02-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="2ec02-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ec02-112">EXAMPLES</span></span>

### <span data-ttu-id="2ec02-113">Exempel 1: Aktivera diagnostik med fil system</span><span class="sxs-lookup"><span data-stu-id="2ec02-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="2ec02-114">I det här exemplet aktive ras program loggning i fil systemet med utförlig nivå.</span><span class="sxs-lookup"><span data-stu-id="2ec02-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="2ec02-115">Exempel 2: Aktivera loggning med Azure Storage</span><span class="sxs-lookup"><span data-stu-id="2ec02-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="2ec02-116">I det här exemplet aktive ras program loggning med lagrings konto som heter mitt konto med loggnings nivå inställd på information.</span><span class="sxs-lookup"><span data-stu-id="2ec02-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="2ec02-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ec02-117">PARAMETERS</span></span>

### <span data-ttu-id="2ec02-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="2ec02-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-119">-Fil</span><span class="sxs-lookup"><span data-stu-id="2ec02-119">-File</span></span>
<span data-ttu-id="2ec02-120">Anger att du vill använda ett fil system för att lagra loggfilerna.</span><span class="sxs-lookup"><span data-stu-id="2ec02-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="2ec02-121">-LogLevel</span></span>
<span data-ttu-id="2ec02-122">Den loggnings nivå som ska lagras.</span><span class="sxs-lookup"><span data-stu-id="2ec02-122">The log level to store.</span></span>
<span data-ttu-id="2ec02-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2ec02-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ec02-124">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="2ec02-124">Error</span></span>
- <span data-ttu-id="2ec02-125">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="2ec02-125">Warning</span></span>
- <span data-ttu-id="2ec02-126">Routningsinformation</span><span class="sxs-lookup"><span data-stu-id="2ec02-126">Information</span></span>
- <span data-ttu-id="2ec02-127">Utförlig</span><span class="sxs-lookup"><span data-stu-id="2ec02-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ec02-128">-Name</span></span>
<span data-ttu-id="2ec02-129">Anger namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="2ec02-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="2ec02-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ec02-130">-PassThru</span></span>
<span data-ttu-id="2ec02-131">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2ec02-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ec02-132">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2ec02-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ec02-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ec02-133">-Profile</span></span>
<span data-ttu-id="2ec02-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2ec02-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ec02-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2ec02-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ec02-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="2ec02-136">-Slot</span></span>
<span data-ttu-id="2ec02-137">Anger namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="2ec02-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="2ec02-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2ec02-138">-StorageAccountName</span></span>
<span data-ttu-id="2ec02-139">Det lagrings konto som ska användas för lagring av loggar.</span><span class="sxs-lookup"><span data-stu-id="2ec02-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="2ec02-140">Om inget anges används CurrentStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="2ec02-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="2ec02-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="2ec02-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="2ec02-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec02-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec02-144">CommonParameters</span></span>
<span data-ttu-id="2ec02-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec02-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec02-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec02-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec02-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ec02-147">INPUTS</span></span>

## <span data-ttu-id="2ec02-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ec02-148">OUTPUTS</span></span>

## <span data-ttu-id="2ec02-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ec02-149">NOTES</span></span>

## <span data-ttu-id="2ec02-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ec02-150">RELATED LINKS</span></span>

[<span data-ttu-id="2ec02-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2ec02-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="2ec02-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2ec02-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2ec02-153">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2ec02-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="2ec02-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2ec02-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="2ec02-155">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2ec02-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


