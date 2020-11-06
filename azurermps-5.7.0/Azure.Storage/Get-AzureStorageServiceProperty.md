---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577332"
---
# <span data-ttu-id="2c9cc-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2c9cc-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="2c9cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9cc-103">Hämtar egenskaper för Azure Storage-tjänster.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c9cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c9cc-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c9cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c9cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9cc-106">Cmdleten **Get-AzureStorageServiceProperty** hämtar egenskaperna för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="2c9cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c9cc-107">EXAMPLES</span></span>

### <span data-ttu-id="2c9cc-108">Exempel 1: skaffa Azure Storage Services-egenskap för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="2c9cc-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29

```

<span data-ttu-id="2c9cc-109">Det här kommandot får egenskapen DefaultServiceVersion för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="2c9cc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c9cc-110">PARAMETERS</span></span>

### <span data-ttu-id="2c9cc-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2c9cc-111">-Context</span></span>
<span data-ttu-id="2c9cc-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2c9cc-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2c9cc-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2c9cc-114">-ServiceType</span></span>
<span data-ttu-id="2c9cc-115">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-115">Specifies the storage service type.</span></span>
<span data-ttu-id="2c9cc-116">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="2c9cc-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2c9cc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2c9cc-118">Object</span><span class="sxs-lookup"><span data-stu-id="2c9cc-118">Blob</span></span> 
- <span data-ttu-id="2c9cc-119">Tabell</span><span class="sxs-lookup"><span data-stu-id="2c9cc-119">Table</span></span>
- <span data-ttu-id="2c9cc-120">Svarskö</span><span class="sxs-lookup"><span data-stu-id="2c9cc-120">Queue</span></span>
- <span data-ttu-id="2c9cc-121">Fil</span><span class="sxs-lookup"><span data-stu-id="2c9cc-121">File</span></span>

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

### <span data-ttu-id="2c9cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9cc-122">CommonParameters</span></span>
<span data-ttu-id="2c9cc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9cc-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9cc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9cc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c9cc-125">INPUTS</span></span>

### <span data-ttu-id="2c9cc-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c9cc-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2c9cc-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c9cc-127">OUTPUTS</span></span>

### <span data-ttu-id="2c9cc-128">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="2c9cc-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="2c9cc-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c9cc-129">NOTES</span></span>

## <span data-ttu-id="2c9cc-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c9cc-130">RELATED LINKS</span></span>

