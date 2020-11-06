---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573810"
---
# <span data-ttu-id="39b5d-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="39b5d-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="39b5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="39b5d-103">Hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="39b5d-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39b5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39b5d-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="39b5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="39b5d-106">Cmdleten **Get-AzureStorageServiceMetricsProperty** hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="39b5d-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="39b5d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="39b5d-108">Exempel 1: Hämta mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="39b5d-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="39b5d-109">Det här kommandot får Metric-egenskaper för blob-lagring för typen timme.</span><span class="sxs-lookup"><span data-stu-id="39b5d-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="39b5d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39b5d-110">PARAMETERS</span></span>

### <span data-ttu-id="39b5d-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="39b5d-111">-Context</span></span>
<span data-ttu-id="39b5d-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="39b5d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="39b5d-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="39b5d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="39b5d-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="39b5d-114">-MetricsType</span></span>
<span data-ttu-id="39b5d-115">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="39b5d-115">Specifies a metrics type.</span></span>
<span data-ttu-id="39b5d-116">Med den här cmdleten hämtas mått för Azure Storage-tjänsten för de mått typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="39b5d-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="39b5d-117">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="39b5d-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39b5d-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="39b5d-118">-ServiceType</span></span>
<span data-ttu-id="39b5d-119">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="39b5d-119">Specifies the storage service type.</span></span>
<span data-ttu-id="39b5d-120">Denna cmdlet hämtar måtten för den typ som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="39b5d-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="39b5d-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="39b5d-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39b5d-122">Object</span><span class="sxs-lookup"><span data-stu-id="39b5d-122">Blob</span></span> 
- <span data-ttu-id="39b5d-123">Tabell</span><span class="sxs-lookup"><span data-stu-id="39b5d-123">Table</span></span>
- <span data-ttu-id="39b5d-124">Svarskö</span><span class="sxs-lookup"><span data-stu-id="39b5d-124">Queue</span></span>
- <span data-ttu-id="39b5d-125">Fil</span><span class="sxs-lookup"><span data-stu-id="39b5d-125">File</span></span> 

<span data-ttu-id="39b5d-126">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="39b5d-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="39b5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b5d-127">CommonParameters</span></span>
<span data-ttu-id="39b5d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b5d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b5d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b5d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39b5d-130">INPUTS</span></span>

### <span data-ttu-id="39b5d-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39b5d-131">IStorageContext</span></span>

<span data-ttu-id="39b5d-132">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="39b5d-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="39b5d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39b5d-133">OUTPUTS</span></span>

### <span data-ttu-id="39b5d-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="39b5d-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="39b5d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39b5d-135">NOTES</span></span>

## <span data-ttu-id="39b5d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39b5d-136">RELATED LINKS</span></span>

[<span data-ttu-id="39b5d-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="39b5d-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="39b5d-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="39b5d-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


