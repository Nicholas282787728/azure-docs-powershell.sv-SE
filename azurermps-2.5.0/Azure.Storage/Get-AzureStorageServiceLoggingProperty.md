---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929153"
---
# <span data-ttu-id="ce615-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ce615-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ce615-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce615-102">SYNOPSIS</span></span>
<span data-ttu-id="ce615-103">Hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="ce615-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce615-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce615-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce615-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce615-105">DESCRIPTION</span></span>
<span data-ttu-id="ce615-106">Cmdleten **Get-AzureStorageServiceLoggingProperty** hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="ce615-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ce615-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce615-107">EXAMPLES</span></span>

### <span data-ttu-id="ce615-108">Exempel 1: Hämta loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ce615-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="ce615-109">Det här kommandot får loggnings egenskaper för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="ce615-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="ce615-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce615-110">PARAMETERS</span></span>

### <span data-ttu-id="ce615-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ce615-111">-Context</span></span>
<span data-ttu-id="ce615-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ce615-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ce615-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ce615-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ce615-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce615-114">-DefaultProfile</span></span>
<span data-ttu-id="ce615-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce615-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce615-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ce615-116">-ServiceType</span></span>
<span data-ttu-id="ce615-117">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="ce615-117">Specifies the storage service type.</span></span>
<span data-ttu-id="ce615-118">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ce615-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ce615-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ce615-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce615-120">Object</span><span class="sxs-lookup"><span data-stu-id="ce615-120">Blob</span></span> 
- <span data-ttu-id="ce615-121">Tabell</span><span class="sxs-lookup"><span data-stu-id="ce615-121">Table</span></span>
- <span data-ttu-id="ce615-122">Svarskö</span><span class="sxs-lookup"><span data-stu-id="ce615-122">Queue</span></span>
- <span data-ttu-id="ce615-123">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="ce615-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ce615-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce615-124">CommonParameters</span></span>
<span data-ttu-id="ce615-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce615-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce615-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce615-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce615-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce615-127">INPUTS</span></span>

### <span data-ttu-id="ce615-128">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce615-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ce615-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce615-129">OUTPUTS</span></span>

### <span data-ttu-id="ce615-130">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="ce615-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="ce615-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce615-131">NOTES</span></span>

## <span data-ttu-id="ce615-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce615-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce615-133">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce615-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ce615-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ce615-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


