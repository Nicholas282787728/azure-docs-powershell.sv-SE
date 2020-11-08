---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090008"
---
# <span data-ttu-id="f0af7-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f0af7-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="f0af7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0af7-102">SYNOPSIS</span></span>
<span data-ttu-id="f0af7-103">Hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f0af7-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f0af7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0af7-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0af7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0af7-105">DESCRIPTION</span></span>
<span data-ttu-id="f0af7-106">Cmdleten **Get-AzStorageServiceMetricsProperty** hämtar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f0af7-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f0af7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0af7-107">EXAMPLES</span></span>

### <span data-ttu-id="f0af7-108">Exempel 1: Hämta mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f0af7-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="f0af7-109">Det här kommandot får Metric-egenskaper för blob-lagring för typen timme.</span><span class="sxs-lookup"><span data-stu-id="f0af7-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="f0af7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0af7-110">PARAMETERS</span></span>

### <span data-ttu-id="f0af7-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f0af7-111">-Context</span></span>
<span data-ttu-id="f0af7-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="f0af7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f0af7-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="f0af7-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f0af7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0af7-114">-DefaultProfile</span></span>
<span data-ttu-id="f0af7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0af7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0af7-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="f0af7-116">-MetricsType</span></span>
<span data-ttu-id="f0af7-117">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="f0af7-117">Specifies a metrics type.</span></span>
<span data-ttu-id="f0af7-118">Med den här cmdleten hämtas mått för Azure Storage-tjänsten för de mått typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f0af7-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="f0af7-119">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="f0af7-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="f0af7-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f0af7-120">-ServiceType</span></span>
<span data-ttu-id="f0af7-121">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="f0af7-121">Specifies the storage service type.</span></span>
<span data-ttu-id="f0af7-122">Denna cmdlet hämtar måtten för den typ som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f0af7-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="f0af7-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f0af7-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0af7-124">Object</span><span class="sxs-lookup"><span data-stu-id="f0af7-124">Blob</span></span> 
- <span data-ttu-id="f0af7-125">Tabell</span><span class="sxs-lookup"><span data-stu-id="f0af7-125">Table</span></span>
- <span data-ttu-id="f0af7-126">Svarskö</span><span class="sxs-lookup"><span data-stu-id="f0af7-126">Queue</span></span>
- <span data-ttu-id="f0af7-127">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="f0af7-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="f0af7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0af7-128">CommonParameters</span></span>
<span data-ttu-id="f0af7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0af7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0af7-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0af7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0af7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0af7-131">INPUTS</span></span>

### <span data-ttu-id="f0af7-132">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0af7-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f0af7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0af7-133">OUTPUTS</span></span>

### <span data-ttu-id="f0af7-134">Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="f0af7-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="f0af7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0af7-135">NOTES</span></span>

## <span data-ttu-id="f0af7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0af7-136">RELATED LINKS</span></span>

[<span data-ttu-id="f0af7-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0af7-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f0af7-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f0af7-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


