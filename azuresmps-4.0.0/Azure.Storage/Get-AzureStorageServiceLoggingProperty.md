---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572363"
---
# <span data-ttu-id="50f4e-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="50f4e-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="50f4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="50f4e-103">Hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="50f4e-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="50f4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50f4e-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f4e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50f4e-105">DESCRIPTION</span></span>
<span data-ttu-id="50f4e-106">Cmdleten **Get-AzureStorageServiceLoggingProperty** hämtar loggnings egenskaper för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="50f4e-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="50f4e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50f4e-107">EXAMPLES</span></span>

### <span data-ttu-id="50f4e-108">Exempel 1: Hämta loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="50f4e-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="50f4e-109">Det här kommandot får loggnings egenskaper för blob-lagring.</span><span class="sxs-lookup"><span data-stu-id="50f4e-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="50f4e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50f4e-110">PARAMETERS</span></span>

### <span data-ttu-id="50f4e-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="50f4e-111">-Context</span></span>
<span data-ttu-id="50f4e-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="50f4e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="50f4e-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="50f4e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="50f4e-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="50f4e-114">-ServiceType</span></span>
<span data-ttu-id="50f4e-115">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="50f4e-115">Specifies the storage service type.</span></span>
<span data-ttu-id="50f4e-116">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="50f4e-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="50f4e-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="50f4e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50f4e-118">Object</span><span class="sxs-lookup"><span data-stu-id="50f4e-118">Blob</span></span> 
- <span data-ttu-id="50f4e-119">Tabell</span><span class="sxs-lookup"><span data-stu-id="50f4e-119">Table</span></span>
- <span data-ttu-id="50f4e-120">Svarskö</span><span class="sxs-lookup"><span data-stu-id="50f4e-120">Queue</span></span>
- <span data-ttu-id="50f4e-121">Fil</span><span class="sxs-lookup"><span data-stu-id="50f4e-121">File</span></span>

<span data-ttu-id="50f4e-122">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="50f4e-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="50f4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f4e-123">CommonParameters</span></span>
<span data-ttu-id="50f4e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f4e-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f4e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f4e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50f4e-126">INPUTS</span></span>

## <span data-ttu-id="50f4e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50f4e-127">OUTPUTS</span></span>

## <span data-ttu-id="50f4e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50f4e-128">NOTES</span></span>

## <span data-ttu-id="50f4e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50f4e-129">RELATED LINKS</span></span>

[<span data-ttu-id="50f4e-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="50f4e-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="50f4e-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="50f4e-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


