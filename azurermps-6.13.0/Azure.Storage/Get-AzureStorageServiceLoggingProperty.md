---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: b622f117549a77c54a24964240cd6d17a084993d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756053"
---
# <span data-ttu-id="73159-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="73159-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="73159-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73159-102">SYNOPSIS</span></span>
<span data-ttu-id="73159-103">Hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="73159-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73159-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73159-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73159-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73159-105">DESCRIPTION</span></span>
<span data-ttu-id="73159-106">Cmdleten **Get-AzureStorageServiceLoggingProperty** hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="73159-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="73159-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73159-107">EXAMPLES</span></span>

### <span data-ttu-id="73159-108">Exempel 1: Hämta loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="73159-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="73159-109">Det här kommandot får loggnings egenskaper för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="73159-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="73159-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73159-110">PARAMETERS</span></span>

### <span data-ttu-id="73159-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="73159-111">-Context</span></span>
<span data-ttu-id="73159-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="73159-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="73159-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="73159-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="73159-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73159-114">-DefaultProfile</span></span>
<span data-ttu-id="73159-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73159-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73159-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="73159-116">-ServiceType</span></span>
<span data-ttu-id="73159-117">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="73159-117">Specifies the storage service type.</span></span>
<span data-ttu-id="73159-118">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="73159-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="73159-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="73159-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="73159-120">Object</span><span class="sxs-lookup"><span data-stu-id="73159-120">Blob</span></span> 
- <span data-ttu-id="73159-121">Tabell</span><span class="sxs-lookup"><span data-stu-id="73159-121">Table</span></span>
- <span data-ttu-id="73159-122">Svarskö</span><span class="sxs-lookup"><span data-stu-id="73159-122">Queue</span></span>
- <span data-ttu-id="73159-123">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="73159-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="73159-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73159-124">CommonParameters</span></span>
<span data-ttu-id="73159-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73159-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73159-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73159-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73159-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73159-127">INPUTS</span></span>

### <span data-ttu-id="73159-128">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="73159-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="73159-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73159-129">OUTPUTS</span></span>

### <span data-ttu-id="73159-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="73159-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="73159-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73159-131">NOTES</span></span>

## <span data-ttu-id="73159-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73159-132">RELATED LINKS</span></span>

[<span data-ttu-id="73159-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="73159-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="73159-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="73159-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


