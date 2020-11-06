---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572356"
---
# <span data-ttu-id="e9742-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e9742-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="e9742-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9742-102">SYNOPSIS</span></span>
<span data-ttu-id="e9742-103">Hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e9742-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="e9742-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9742-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="e9742-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9742-105">DESCRIPTION</span></span>
<span data-ttu-id="e9742-106">Cmdleten **Get-AzureStorageServiceMetricsProperty** hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e9742-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="e9742-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9742-107">EXAMPLES</span></span>

### <span data-ttu-id="e9742-108">Exempel 1: Hämta mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e9742-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="e9742-109">Det här kommandot får Metric-egenskaper för blob-lagring för typen timme.</span><span class="sxs-lookup"><span data-stu-id="e9742-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="e9742-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9742-110">PARAMETERS</span></span>

### <span data-ttu-id="e9742-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e9742-111">-Context</span></span>
<span data-ttu-id="e9742-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e9742-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e9742-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="e9742-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e9742-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="e9742-114">-MetricsType</span></span>
<span data-ttu-id="e9742-115">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="e9742-115">Specifies a metrics type.</span></span>
<span data-ttu-id="e9742-116">Med den här cmdleten hämtas mått för Azure Storage-tjänsten för de mått typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e9742-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="e9742-117">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="e9742-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="e9742-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e9742-118">-ServiceType</span></span>
<span data-ttu-id="e9742-119">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="e9742-119">Specifies the storage service type.</span></span>
<span data-ttu-id="e9742-120">Denna cmdlet hämtar måtten för den typ som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e9742-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="e9742-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e9742-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9742-122">Object</span><span class="sxs-lookup"><span data-stu-id="e9742-122">Blob</span></span> 
- <span data-ttu-id="e9742-123">Tabell</span><span class="sxs-lookup"><span data-stu-id="e9742-123">Table</span></span>
- <span data-ttu-id="e9742-124">Svarskö</span><span class="sxs-lookup"><span data-stu-id="e9742-124">Queue</span></span>
- <span data-ttu-id="e9742-125">Fil</span><span class="sxs-lookup"><span data-stu-id="e9742-125">File</span></span> 

<span data-ttu-id="e9742-126">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="e9742-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e9742-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9742-127">CommonParameters</span></span>
<span data-ttu-id="e9742-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9742-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9742-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9742-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9742-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9742-130">INPUTS</span></span>

## <span data-ttu-id="e9742-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9742-131">OUTPUTS</span></span>

## <span data-ttu-id="e9742-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9742-132">NOTES</span></span>

## <span data-ttu-id="e9742-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9742-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9742-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9742-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e9742-135">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e9742-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


