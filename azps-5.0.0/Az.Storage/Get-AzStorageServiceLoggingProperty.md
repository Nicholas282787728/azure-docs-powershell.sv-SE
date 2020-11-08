---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269573"
---
# <span data-ttu-id="31e53-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="31e53-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="31e53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31e53-102">SYNOPSIS</span></span>
<span data-ttu-id="31e53-103">Hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="31e53-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="31e53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31e53-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31e53-105">DESCRIPTION</span></span>
<span data-ttu-id="31e53-106">Cmdleten **Get-AzStorageServiceLoggingProperty** hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="31e53-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="31e53-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31e53-107">EXAMPLES</span></span>

### <span data-ttu-id="31e53-108">Exempel 1: Hämta loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="31e53-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="31e53-109">Det här kommandot får loggnings egenskaper för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="31e53-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="31e53-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31e53-110">PARAMETERS</span></span>

### <span data-ttu-id="31e53-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="31e53-111">-Context</span></span>
<span data-ttu-id="31e53-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="31e53-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="31e53-113">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="31e53-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="31e53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e53-114">-DefaultProfile</span></span>
<span data-ttu-id="31e53-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31e53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e53-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="31e53-116">-ServiceType</span></span>
<span data-ttu-id="31e53-117">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="31e53-117">Specifies the storage service type.</span></span>
<span data-ttu-id="31e53-118">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="31e53-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="31e53-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="31e53-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="31e53-120">Object</span><span class="sxs-lookup"><span data-stu-id="31e53-120">Blob</span></span> 
- <span data-ttu-id="31e53-121">Tabell</span><span class="sxs-lookup"><span data-stu-id="31e53-121">Table</span></span>
- <span data-ttu-id="31e53-122">Svarskö</span><span class="sxs-lookup"><span data-stu-id="31e53-122">Queue</span></span>
- <span data-ttu-id="31e53-123">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="31e53-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="31e53-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e53-124">CommonParameters</span></span>
<span data-ttu-id="31e53-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e53-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e53-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e53-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e53-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31e53-127">INPUTS</span></span>

### <span data-ttu-id="31e53-128">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="31e53-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="31e53-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31e53-129">OUTPUTS</span></span>

### <span data-ttu-id="31e53-130">Microsoft. Azure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="31e53-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="31e53-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31e53-131">NOTES</span></span>

## <span data-ttu-id="31e53-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31e53-132">RELATED LINKS</span></span>

[<span data-ttu-id="31e53-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="31e53-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="31e53-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="31e53-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


