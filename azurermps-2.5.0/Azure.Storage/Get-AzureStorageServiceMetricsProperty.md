---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 1d7d536d7815206f942a89da4458f4669c0c9fd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929150"
---
# <span data-ttu-id="67421-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="67421-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="67421-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67421-102">SYNOPSIS</span></span>
<span data-ttu-id="67421-103">Hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="67421-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67421-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67421-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67421-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67421-105">DESCRIPTION</span></span>
<span data-ttu-id="67421-106">Cmdleten **Get-AzureStorageServiceMetricsProperty** hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="67421-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="67421-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67421-107">EXAMPLES</span></span>

### <span data-ttu-id="67421-108">Exempel 1: Hämta mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="67421-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="67421-109">Det här kommandot får Metric-egenskaper för blob-lagring för typen timme.</span><span class="sxs-lookup"><span data-stu-id="67421-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="67421-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67421-110">PARAMETERS</span></span>

### <span data-ttu-id="67421-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="67421-111">-Context</span></span>
<span data-ttu-id="67421-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="67421-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="67421-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="67421-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="67421-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67421-114">-DefaultProfile</span></span>
<span data-ttu-id="67421-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67421-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67421-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="67421-116">-MetricsType</span></span>
<span data-ttu-id="67421-117">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="67421-117">Specifies a metrics type.</span></span>
<span data-ttu-id="67421-118">Med den här cmdleten hämtas mått för Azure Storage-tjänsten för de mått typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67421-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="67421-119">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="67421-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67421-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="67421-120">-ServiceType</span></span>
<span data-ttu-id="67421-121">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="67421-121">Specifies the storage service type.</span></span>
<span data-ttu-id="67421-122">Denna cmdlet hämtar måtten för den typ som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67421-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="67421-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="67421-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="67421-124">Object</span><span class="sxs-lookup"><span data-stu-id="67421-124">Blob</span></span> 
- <span data-ttu-id="67421-125">Tabell</span><span class="sxs-lookup"><span data-stu-id="67421-125">Table</span></span>
- <span data-ttu-id="67421-126">Svarskö</span><span class="sxs-lookup"><span data-stu-id="67421-126">Queue</span></span>
- <span data-ttu-id="67421-127">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="67421-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="67421-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67421-128">CommonParameters</span></span>
<span data-ttu-id="67421-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67421-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67421-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67421-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67421-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67421-131">INPUTS</span></span>

### <span data-ttu-id="67421-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="67421-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="67421-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67421-133">OUTPUTS</span></span>

### <span data-ttu-id="67421-134">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="67421-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="67421-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67421-135">NOTES</span></span>

## <span data-ttu-id="67421-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67421-136">RELATED LINKS</span></span>

[<span data-ttu-id="67421-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="67421-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="67421-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="67421-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


