---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572476"
---
# <span data-ttu-id="d859c-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d859c-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="d859c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d859c-102">SYNOPSIS</span></span>
<span data-ttu-id="d859c-103">Ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="d859c-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="d859c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d859c-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="d859c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d859c-105">DESCRIPTION</span></span>
<span data-ttu-id="d859c-106">Cmdleten **set-AzureStorageServiceLoggingProperty** ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="d859c-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="d859c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d859c-107">EXAMPLES</span></span>

### <span data-ttu-id="d859c-108">Exempel 1: ändra loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="d859c-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="d859c-109">Det här kommandot ändrar version 1,0-loggning för Blob Storage för att omfatta Läs-och skriv åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d859c-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="d859c-110">Loggning av Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="d859c-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="d859c-111">Eftersom det här kommandot anger parametern *Passthru* visas de ändrade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="d859c-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="d859c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d859c-112">PARAMETERS</span></span>

### <span data-ttu-id="d859c-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d859c-113">-Context</span></span>
<span data-ttu-id="d859c-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="d859c-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d859c-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="d859c-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d859c-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="d859c-116">-LoggingOperations</span></span>
<span data-ttu-id="d859c-117">Anger en matris med Azure Storage Service-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d859c-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="d859c-118">Azure Storage Services loggar de åtgärder som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d859c-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="d859c-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d859c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d859c-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="d859c-120">None</span></span>
- <span data-ttu-id="d859c-121">Läst</span><span class="sxs-lookup"><span data-stu-id="d859c-121">Read</span></span>
- <span data-ttu-id="d859c-122">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="d859c-122">Write</span></span>
- <span data-ttu-id="d859c-123">Ta bort</span><span class="sxs-lookup"><span data-stu-id="d859c-123">Delete</span></span>
- <span data-ttu-id="d859c-124">Alla</span><span class="sxs-lookup"><span data-stu-id="d859c-124">All</span></span>

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

### <span data-ttu-id="d859c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d859c-125">-PassThru</span></span>
<span data-ttu-id="d859c-126">Anger att den här cmdleten returnerar de uppdaterade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="d859c-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="d859c-127">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="d859c-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d859c-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="d859c-128">-RetentionDays</span></span>
<span data-ttu-id="d859c-129">Anger antalet dagar som Azure Storage-tjänsten behåller loggad information.</span><span class="sxs-lookup"><span data-stu-id="d859c-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="d859c-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d859c-130">-ServiceType</span></span>
<span data-ttu-id="d859c-131">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="d859c-131">Specifies the storage service type.</span></span>
<span data-ttu-id="d859c-132">Denna cmdlet ändrar loggnings egenskaperna för tjänste typen som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="d859c-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d859c-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d859c-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d859c-134">Object</span><span class="sxs-lookup"><span data-stu-id="d859c-134">Blob</span></span> 
- <span data-ttu-id="d859c-135">Tabell</span><span class="sxs-lookup"><span data-stu-id="d859c-135">Table</span></span>
- <span data-ttu-id="d859c-136">Svarskö</span><span class="sxs-lookup"><span data-stu-id="d859c-136">Queue</span></span>
- <span data-ttu-id="d859c-137">Fil</span><span class="sxs-lookup"><span data-stu-id="d859c-137">File</span></span>

<span data-ttu-id="d859c-138">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="d859c-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="d859c-139">-Version</span><span class="sxs-lookup"><span data-stu-id="d859c-139">-Version</span></span>
<span data-ttu-id="d859c-140">Anger versionen för loggning av Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d859c-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="d859c-141">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="d859c-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="d859c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d859c-142">CommonParameters</span></span>
<span data-ttu-id="d859c-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d859c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d859c-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d859c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d859c-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d859c-145">INPUTS</span></span>

## <span data-ttu-id="d859c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d859c-146">OUTPUTS</span></span>

## <span data-ttu-id="d859c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d859c-147">NOTES</span></span>

## <span data-ttu-id="d859c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d859c-148">RELATED LINKS</span></span>

[<span data-ttu-id="d859c-149">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d859c-149">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="d859c-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d859c-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


