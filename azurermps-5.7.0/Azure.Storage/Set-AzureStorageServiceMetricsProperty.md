---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 3cbe0a4e0276f2b62a0e0aed5b6168a5b81f8d7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758244"
---
# <span data-ttu-id="6e408-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6e408-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="6e408-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e408-102">SYNOPSIS</span></span>
<span data-ttu-id="6e408-103">Ändrar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6e408-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e408-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e408-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="6e408-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e408-105">DESCRIPTION</span></span>
<span data-ttu-id="6e408-106">Cmdleten **set-AzureStorageServiceMetricsProperty** ändrar måtten för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6e408-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6e408-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e408-107">EXAMPLES</span></span>

### <span data-ttu-id="6e408-108">Exempel 1: ändra mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="6e408-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="6e408-109">Det här kommandot ändrar version 1,0-värden för blob-lagring till en tjänst nivå.</span><span class="sxs-lookup"><span data-stu-id="6e408-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="6e408-110">Mått för Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="6e408-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="6e408-111">Eftersom det här kommandot anger parametern *Passthru* visas egenskaperna för de ändrade måtten.</span><span class="sxs-lookup"><span data-stu-id="6e408-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="6e408-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e408-112">PARAMETERS</span></span>

### <span data-ttu-id="6e408-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6e408-113">-Context</span></span>
<span data-ttu-id="6e408-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="6e408-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e408-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="6e408-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e408-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="6e408-116">-MetricsLevel</span></span>
<span data-ttu-id="6e408-117">Anger den mått nivå som Azure-lagring använder för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6e408-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="6e408-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6e408-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e408-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="6e408-119">None</span></span>
- <span data-ttu-id="6e408-120">Serv</span><span class="sxs-lookup"><span data-stu-id="6e408-120">Service</span></span>
- <span data-ttu-id="6e408-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="6e408-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e408-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="6e408-122">-MetricsType</span></span>
<span data-ttu-id="6e408-123">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="6e408-123">Specifies a metrics type.</span></span>
<span data-ttu-id="6e408-124">Den här cmldet ställer in värdet för Azure Storage Service-värden på det värde som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6e408-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="6e408-125">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="6e408-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="6e408-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e408-126">-PassThru</span></span>
<span data-ttu-id="6e408-127">Anger att den här cmdleten returnerar de uppdaterade måtten.</span><span class="sxs-lookup"><span data-stu-id="6e408-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="6e408-128">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="6e408-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6e408-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6e408-129">-RetentionDays</span></span>
<span data-ttu-id="6e408-130">Anger antalet dagar som Azure Storage-tjänsten behåller statistik information.</span><span class="sxs-lookup"><span data-stu-id="6e408-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="6e408-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6e408-131">-ServiceType</span></span>
<span data-ttu-id="6e408-132">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="6e408-132">Specifies the storage service type.</span></span>
<span data-ttu-id="6e408-133">Denna cmdlet ändrar egenskaperna för de tjänst typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6e408-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6e408-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6e408-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e408-135">Object</span><span class="sxs-lookup"><span data-stu-id="6e408-135">Blob</span></span> 
- <span data-ttu-id="6e408-136">Tabell</span><span class="sxs-lookup"><span data-stu-id="6e408-136">Table</span></span>
- <span data-ttu-id="6e408-137">Svarskö</span><span class="sxs-lookup"><span data-stu-id="6e408-137">Queue</span></span>
- <span data-ttu-id="6e408-138">Fil</span><span class="sxs-lookup"><span data-stu-id="6e408-138">File</span></span>

<span data-ttu-id="6e408-139">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="6e408-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6e408-140">-Version</span><span class="sxs-lookup"><span data-stu-id="6e408-140">-Version</span></span>
<span data-ttu-id="6e408-141">Anger versionen för Azure lagrings mått.</span><span class="sxs-lookup"><span data-stu-id="6e408-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="6e408-142">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="6e408-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="6e408-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e408-143">CommonParameters</span></span>
<span data-ttu-id="6e408-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e408-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e408-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e408-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e408-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e408-146">INPUTS</span></span>

### <span data-ttu-id="6e408-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e408-147">IStorageContext</span></span>

<span data-ttu-id="6e408-148">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6e408-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6e408-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e408-149">OUTPUTS</span></span>

### <span data-ttu-id="6e408-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="6e408-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="6e408-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e408-151">NOTES</span></span>

## <span data-ttu-id="6e408-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e408-152">RELATED LINKS</span></span>

[<span data-ttu-id="6e408-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6e408-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="6e408-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e408-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


