---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323556"
---
# <span data-ttu-id="edc93-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="edc93-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="edc93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edc93-102">SYNOPSIS</span></span>
<span data-ttu-id="edc93-103">Ändrar tjänste egenskaperna för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="edc93-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="edc93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edc93-104">SYNTAX</span></span>

### <span data-ttu-id="edc93-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="edc93-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc93-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="edc93-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc93-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="edc93-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edc93-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edc93-108">DESCRIPTION</span></span>
<span data-ttu-id="edc93-109">Cmdleten **Update-AzStorageBlobServiceProperty** ändrar tjänst egenskaperna för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="edc93-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="edc93-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edc93-110">EXAMPLES</span></span>

### <span data-ttu-id="edc93-111">Exempel 1: Ange BLOB service-DefaultServiceVersion till 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="edc93-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="edc93-112">Det här kommandot anger DefaultServiceVersion för Blob-tjänsten till 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="edc93-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="edc93-113">Exempel 2: Aktivera Changefeed i Blob-tjänsten för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="edc93-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="edc93-114">Det här kommandot aktiverar Changefeed för Blob-tjänsten för ett lagrings konto för byte av feed-stöd i Azure Blob Storage för att avlyssna ett GPv2-eller BLOB lagrings konto för att skapa, ändra eller ta bort BLOB-händelser.</span><span class="sxs-lookup"><span data-stu-id="edc93-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="edc93-115">Sedan sparas en ordnad logg över händelser för de blob som lagras i $blobchangefeed-behållaren i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="edc93-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="edc93-116">De Serialiserade ändringarna bevaras som en Apache avro-fil och kan behandlas asynkront och stegvis.</span><span class="sxs-lookup"><span data-stu-id="edc93-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="edc93-117">Exempel 3: Aktivera versions hantering för Blob-tjänsten för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="edc93-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="edc93-118">Det här kommandot aktiverar versions hantering för Blob-tjänsten för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="edc93-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="edc93-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edc93-119">PARAMETERS</span></span>

### <span data-ttu-id="edc93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc93-120">-DefaultProfile</span></span>
<span data-ttu-id="edc93-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edc93-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc93-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="edc93-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="edc93-123">Standard tjänst version att ange</span><span class="sxs-lookup"><span data-stu-id="edc93-123">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="edc93-124">-EnableChangeFeed</span></span>
<span data-ttu-id="edc93-125">Aktivera ändra feed-loggning för lagrings kontot genom att ange $true och inaktivera ändra feed-loggning genom att ange $false.</span><span class="sxs-lookup"><span data-stu-id="edc93-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="edc93-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="edc93-127">Hämtar eller anger versions hantering är aktiverat om värdet är true.</span><span class="sxs-lookup"><span data-stu-id="edc93-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc93-128">-ResourceGroupName</span></span>
<span data-ttu-id="edc93-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="edc93-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edc93-130">-ResourceId</span></span>
<span data-ttu-id="edc93-131">Ange ett resurs-ID för lagrings-ID eller egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="edc93-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="edc93-132">-StorageAccount</span></span>
<span data-ttu-id="edc93-133">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="edc93-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="edc93-134">-StorageAccountName</span></span>
<span data-ttu-id="edc93-135">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="edc93-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="edc93-136">-Confirm</span></span>
<span data-ttu-id="edc93-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="edc93-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc93-138">-WhatIf</span></span>
<span data-ttu-id="edc93-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="edc93-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edc93-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="edc93-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc93-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc93-141">CommonParameters</span></span>
<span data-ttu-id="edc93-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edc93-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc93-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc93-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc93-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edc93-144">INPUTS</span></span>

### <span data-ttu-id="edc93-145">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edc93-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="edc93-146">System. String</span><span class="sxs-lookup"><span data-stu-id="edc93-146">System.String</span></span>

## <span data-ttu-id="edc93-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edc93-147">OUTPUTS</span></span>

### <span data-ttu-id="edc93-148">Microsoft. Azure. commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="edc93-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="edc93-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edc93-149">NOTES</span></span>

## <span data-ttu-id="edc93-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edc93-150">RELATED LINKS</span></span>
