---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: fbd7c691e2cfbef58bc59429f68740af00288906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757972"
---
# <span data-ttu-id="c7181-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c7181-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="c7181-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7181-102">SYNOPSIS</span></span>
<span data-ttu-id="c7181-103">Ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="c7181-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7181-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7181-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7181-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7181-105">DESCRIPTION</span></span>
<span data-ttu-id="c7181-106">Cmdleten **set-AzureStorageServiceLoggingProperty** ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="c7181-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="c7181-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7181-107">EXAMPLES</span></span>

### <span data-ttu-id="c7181-108">Exempel 1: ändra loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="c7181-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="c7181-109">Det här kommandot ändrar version 1,0-loggning för Blob Storage för att omfatta Läs-och skriv åtgärder.</span><span class="sxs-lookup"><span data-stu-id="c7181-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="c7181-110">Loggning av Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="c7181-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="c7181-111">Eftersom det här kommandot anger parametern *Passthru* visas de ändrade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="c7181-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="c7181-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7181-112">PARAMETERS</span></span>

### <span data-ttu-id="c7181-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c7181-113">-Context</span></span>
<span data-ttu-id="c7181-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="c7181-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c7181-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="c7181-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c7181-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="c7181-116">-LoggingOperations</span></span>
<span data-ttu-id="c7181-117">Anger en matris med Azure Storage Service-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="c7181-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="c7181-118">Azure Storage Services loggar de åtgärder som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c7181-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="c7181-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c7181-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7181-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="c7181-120">None</span></span>
- <span data-ttu-id="c7181-121">Läst</span><span class="sxs-lookup"><span data-stu-id="c7181-121">Read</span></span>
- <span data-ttu-id="c7181-122">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="c7181-122">Write</span></span>
- <span data-ttu-id="c7181-123">Ta bort</span><span class="sxs-lookup"><span data-stu-id="c7181-123">Delete</span></span>
- <span data-ttu-id="c7181-124">Alla</span><span class="sxs-lookup"><span data-stu-id="c7181-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7181-125">-PassThru</span></span>
<span data-ttu-id="c7181-126">Anger att den här cmdleten returnerar de uppdaterade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="c7181-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="c7181-127">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="c7181-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c7181-128">-RetentionDays</span></span>
<span data-ttu-id="c7181-129">Anger antalet dagar som Azure Storage-tjänsten behåller loggad information.</span><span class="sxs-lookup"><span data-stu-id="c7181-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c7181-130">-ServiceType</span></span>
<span data-ttu-id="c7181-131">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="c7181-131">Specifies the storage service type.</span></span>
<span data-ttu-id="c7181-132">Denna cmdlet ändrar loggnings egenskaperna för tjänste typen som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="c7181-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c7181-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c7181-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7181-134">Object</span><span class="sxs-lookup"><span data-stu-id="c7181-134">Blob</span></span> 
- <span data-ttu-id="c7181-135">Tabell</span><span class="sxs-lookup"><span data-stu-id="c7181-135">Table</span></span>
- <span data-ttu-id="c7181-136">Svarskö</span><span class="sxs-lookup"><span data-stu-id="c7181-136">Queue</span></span>
- <span data-ttu-id="c7181-137">Fil</span><span class="sxs-lookup"><span data-stu-id="c7181-137">File</span></span>

<span data-ttu-id="c7181-138">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="c7181-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c7181-139">-Version</span><span class="sxs-lookup"><span data-stu-id="c7181-139">-Version</span></span>
<span data-ttu-id="c7181-140">Anger versionen för loggning av Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c7181-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="c7181-141">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="c7181-141">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7181-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7181-142">CommonParameters</span></span>
<span data-ttu-id="c7181-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7181-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7181-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7181-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7181-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7181-145">INPUTS</span></span>

### <span data-ttu-id="c7181-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7181-146">IStorageContext</span></span>

<span data-ttu-id="c7181-147">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c7181-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="c7181-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7181-148">OUTPUTS</span></span>

### <span data-ttu-id="c7181-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="c7181-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="c7181-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7181-150">NOTES</span></span>

## <span data-ttu-id="c7181-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7181-151">RELATED LINKS</span></span>

[<span data-ttu-id="c7181-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c7181-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="c7181-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7181-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


