---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582159"
---
# <span data-ttu-id="30c83-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="30c83-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="30c83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30c83-102">SYNOPSIS</span></span>
<span data-ttu-id="30c83-103">Ändrar egenskaperna för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="30c83-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30c83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30c83-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30c83-105">DESCRIPTION</span></span>
<span data-ttu-id="30c83-106">Cmdleten **Update-AzureStorageServiceProperty** ändrar egenskaperna för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="30c83-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="30c83-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30c83-107">EXAMPLES</span></span>

### <span data-ttu-id="30c83-108">Exempel 1: Ange BLOB service-DefaultServiceVersion till 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="30c83-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="30c83-109">Det här kommandot anger DefaultServiceVersion för Blob-tjänsten till 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="30c83-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="30c83-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30c83-110">PARAMETERS</span></span>

### <span data-ttu-id="30c83-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="30c83-111">-Context</span></span>
<span data-ttu-id="30c83-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="30c83-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="30c83-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="30c83-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30c83-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="30c83-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="30c83-115">DefaultServiceVersion anger vilken standard version som ska användas för förfrågningar till Blob-tjänsten om en inkommande begärans version inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="30c83-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="30c83-116">Möjliga värden inkluderar version 2008-10-27 och alla nyare versioner.</span><span class="sxs-lookup"><span data-stu-id="30c83-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="30c83-117">Mer information finns i https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="30c83-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c83-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30c83-118">-PassThru</span></span>
<span data-ttu-id="30c83-119">Visa ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="30c83-119">Display ServiceProperties</span></span>

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

### <span data-ttu-id="30c83-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="30c83-120">-ServiceType</span></span>
<span data-ttu-id="30c83-121">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="30c83-121">Specifies the storage service type.</span></span>
<span data-ttu-id="30c83-122">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="30c83-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="30c83-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="30c83-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30c83-124">Object</span><span class="sxs-lookup"><span data-stu-id="30c83-124">Blob</span></span> 
- <span data-ttu-id="30c83-125">Tabell</span><span class="sxs-lookup"><span data-stu-id="30c83-125">Table</span></span>
- <span data-ttu-id="30c83-126">Svarskö</span><span class="sxs-lookup"><span data-stu-id="30c83-126">Queue</span></span>
- <span data-ttu-id="30c83-127">Fil</span><span class="sxs-lookup"><span data-stu-id="30c83-127">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c83-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30c83-128">-Confirm</span></span>
<span data-ttu-id="30c83-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30c83-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c83-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c83-130">-WhatIf</span></span>
<span data-ttu-id="30c83-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30c83-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30c83-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30c83-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c83-133">CommonParameters</span></span>
<span data-ttu-id="30c83-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c83-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c83-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c83-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30c83-136">INPUTS</span></span>

### <span data-ttu-id="30c83-137">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="30c83-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="30c83-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30c83-138">OUTPUTS</span></span>

### <span data-ttu-id="30c83-139">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="30c83-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="30c83-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30c83-140">NOTES</span></span>

## <span data-ttu-id="30c83-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30c83-141">RELATED LINKS</span></span>

