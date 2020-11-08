---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269565"
---
# <span data-ttu-id="db70d-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="db70d-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="db70d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db70d-102">SYNOPSIS</span></span>
<span data-ttu-id="db70d-103">Hämtar egenskaper för Azure Storage-tjänster.</span><span class="sxs-lookup"><span data-stu-id="db70d-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="db70d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db70d-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db70d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db70d-105">DESCRIPTION</span></span>
<span data-ttu-id="db70d-106">Cmdleten **Get-AzStorageServiceProperty** hämtar egenskaperna för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="db70d-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="db70d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db70d-107">EXAMPLES</span></span>

### <span data-ttu-id="db70d-108">Exempel 1: skaffa Azure Storage Services-egenskap för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="db70d-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="db70d-109">Det här kommandot får egenskapen DefaultServiceVersion för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="db70d-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="db70d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db70d-110">PARAMETERS</span></span>

### <span data-ttu-id="db70d-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="db70d-111">-Context</span></span>
<span data-ttu-id="db70d-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="db70d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="db70d-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="db70d-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db70d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db70d-114">-DefaultProfile</span></span>
<span data-ttu-id="db70d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db70d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db70d-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="db70d-116">-ServiceType</span></span>
<span data-ttu-id="db70d-117">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="db70d-117">Specifies the storage service type.</span></span>
<span data-ttu-id="db70d-118">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="db70d-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="db70d-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="db70d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db70d-120">Object</span><span class="sxs-lookup"><span data-stu-id="db70d-120">Blob</span></span> 
- <span data-ttu-id="db70d-121">Tabell</span><span class="sxs-lookup"><span data-stu-id="db70d-121">Table</span></span>
- <span data-ttu-id="db70d-122">Svarskö</span><span class="sxs-lookup"><span data-stu-id="db70d-122">Queue</span></span>
- <span data-ttu-id="db70d-123">Fil</span><span class="sxs-lookup"><span data-stu-id="db70d-123">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db70d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db70d-124">CommonParameters</span></span>
<span data-ttu-id="db70d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db70d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db70d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db70d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db70d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db70d-127">INPUTS</span></span>

### <span data-ttu-id="db70d-128">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="db70d-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="db70d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db70d-129">OUTPUTS</span></span>

### <span data-ttu-id="db70d-130">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="db70d-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="db70d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db70d-131">NOTES</span></span>

## <span data-ttu-id="db70d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db70d-132">RELATED LINKS</span></span>
