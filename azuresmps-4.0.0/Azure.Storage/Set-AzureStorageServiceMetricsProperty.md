---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572472"
---
# <span data-ttu-id="ddfc9-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ddfc9-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="ddfc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfc9-103">Ändrar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ddfc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddfc9-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ddfc9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddfc9-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfc9-106">Cmdleten **set-AzureStorageServiceMetricsProperty** ändrar måtten för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ddfc9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddfc9-107">EXAMPLES</span></span>

### <span data-ttu-id="ddfc9-108">Exempel 1: ändra mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="ddfc9-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="ddfc9-109">Det här kommandot ändrar version 1,0-värden för blob-lagring till en tjänst nivå.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="ddfc9-110">Mått för Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="ddfc9-111">Eftersom det här kommandot anger parametern *Passthru* visas egenskaperna för de ändrade måtten.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="ddfc9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddfc9-112">PARAMETERS</span></span>

### <span data-ttu-id="ddfc9-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ddfc9-113">-Context</span></span>
<span data-ttu-id="ddfc9-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ddfc9-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ddfc9-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="ddfc9-116">-MetricsLevel</span></span>
<span data-ttu-id="ddfc9-117">Anger den mått nivå som Azure-lagring använder för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="ddfc9-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ddfc9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ddfc9-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="ddfc9-119">None</span></span>
- <span data-ttu-id="ddfc9-120">Serv</span><span class="sxs-lookup"><span data-stu-id="ddfc9-120">Service</span></span>
- <span data-ttu-id="ddfc9-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="ddfc9-121">ServiceAndApi</span></span>

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

### <span data-ttu-id="ddfc9-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="ddfc9-122">-MetricsType</span></span>
<span data-ttu-id="ddfc9-123">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-123">Specifies a metrics type.</span></span>
<span data-ttu-id="ddfc9-124">Den här cmldet ställer in värdet för Azure Storage Service-värden på det värde som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="ddfc9-125">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="ddfc9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddfc9-126">-PassThru</span></span>
<span data-ttu-id="ddfc9-127">Anger att den här cmdleten returnerar de uppdaterade måtten.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="ddfc9-128">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ddfc9-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="ddfc9-129">-RetentionDays</span></span>
<span data-ttu-id="ddfc9-130">Anger antalet dagar som Azure Storage-tjänsten behåller statistik information.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="ddfc9-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ddfc9-131">-ServiceType</span></span>
<span data-ttu-id="ddfc9-132">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-132">Specifies the storage service type.</span></span>
<span data-ttu-id="ddfc9-133">Denna cmdlet ändrar egenskaperna för de tjänst typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ddfc9-134">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ddfc9-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ddfc9-135">Object</span><span class="sxs-lookup"><span data-stu-id="ddfc9-135">Blob</span></span> 
- <span data-ttu-id="ddfc9-136">Tabell</span><span class="sxs-lookup"><span data-stu-id="ddfc9-136">Table</span></span>
- <span data-ttu-id="ddfc9-137">Svarskö</span><span class="sxs-lookup"><span data-stu-id="ddfc9-137">Queue</span></span>
- <span data-ttu-id="ddfc9-138">Fil</span><span class="sxs-lookup"><span data-stu-id="ddfc9-138">File</span></span>

<span data-ttu-id="ddfc9-139">Värdet för File stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ddfc9-140">-Version</span><span class="sxs-lookup"><span data-stu-id="ddfc9-140">-Version</span></span>
<span data-ttu-id="ddfc9-141">Anger versionen för Azure lagrings mått.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="ddfc9-142">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="ddfc9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfc9-143">CommonParameters</span></span>
<span data-ttu-id="ddfc9-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfc9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfc9-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddfc9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfc9-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddfc9-146">INPUTS</span></span>

## <span data-ttu-id="ddfc9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddfc9-147">OUTPUTS</span></span>

## <span data-ttu-id="ddfc9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddfc9-148">NOTES</span></span>

## <span data-ttu-id="ddfc9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddfc9-149">RELATED LINKS</span></span>

[<span data-ttu-id="ddfc9-150">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ddfc9-150">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="ddfc9-151">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ddfc9-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


