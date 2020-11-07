---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755314"
---
# <span data-ttu-id="e0c06-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e0c06-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="e0c06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0c06-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c06-103">Hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="e0c06-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0c06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0c06-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0c06-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0c06-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c06-106">Cmdleten **Get-AzureStorageServiceLoggingProperty** hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="e0c06-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="e0c06-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0c06-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c06-108">Exempel 1: Hämta loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e0c06-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="e0c06-109">Det här kommandot får loggnings egenskaper för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="e0c06-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="e0c06-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0c06-110">PARAMETERS</span></span>

### <span data-ttu-id="e0c06-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e0c06-111">-Context</span></span>
<span data-ttu-id="e0c06-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e0c06-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e0c06-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="e0c06-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e0c06-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e0c06-114">-ServiceType</span></span>
<span data-ttu-id="e0c06-115">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="e0c06-115">Specifies the storage service type.</span></span>
<span data-ttu-id="e0c06-116">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e0c06-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="e0c06-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e0c06-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0c06-118">Object</span><span class="sxs-lookup"><span data-stu-id="e0c06-118">Blob</span></span> 
- <span data-ttu-id="e0c06-119">Tabell</span><span class="sxs-lookup"><span data-stu-id="e0c06-119">Table</span></span>
- <span data-ttu-id="e0c06-120">Svarskö</span><span class="sxs-lookup"><span data-stu-id="e0c06-120">Queue</span></span>
- <span data-ttu-id="e0c06-121">Fil</span><span class="sxs-lookup"><span data-stu-id="e0c06-121">File</span></span>

<span data-ttu-id="e0c06-122">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="e0c06-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e0c06-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c06-123">CommonParameters</span></span>
<span data-ttu-id="e0c06-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c06-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c06-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0c06-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c06-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0c06-126">INPUTS</span></span>

### <span data-ttu-id="e0c06-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0c06-127">IStorageContext</span></span>

<span data-ttu-id="e0c06-128">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e0c06-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e0c06-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0c06-129">OUTPUTS</span></span>

### <span data-ttu-id="e0c06-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="e0c06-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="e0c06-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0c06-131">NOTES</span></span>

## <span data-ttu-id="e0c06-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0c06-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0c06-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0c06-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e0c06-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e0c06-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


