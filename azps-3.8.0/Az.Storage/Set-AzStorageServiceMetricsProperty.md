---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090658"
---
# <span data-ttu-id="26007-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="26007-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="26007-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26007-102">SYNOPSIS</span></span>
<span data-ttu-id="26007-103">Ändrar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26007-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="26007-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26007-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26007-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26007-105">DESCRIPTION</span></span>
<span data-ttu-id="26007-106">Cmdleten **set-AzStorageServiceMetricsProperty** ändrar måtten för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26007-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="26007-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26007-107">EXAMPLES</span></span>

### <span data-ttu-id="26007-108">Exempel 1: ändra mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="26007-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="26007-109">Det här kommandot ändrar version 1,0-värden för blob-lagring till en tjänst nivå.</span><span class="sxs-lookup"><span data-stu-id="26007-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="26007-110">Mått för Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="26007-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="26007-111">Eftersom det här kommandot anger parametern *Passthru* visas egenskaperna för de ändrade måtten.</span><span class="sxs-lookup"><span data-stu-id="26007-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="26007-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26007-112">PARAMETERS</span></span>

### <span data-ttu-id="26007-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="26007-113">-Context</span></span>
<span data-ttu-id="26007-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="26007-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="26007-115">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="26007-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="26007-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26007-116">-DefaultProfile</span></span>
<span data-ttu-id="26007-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26007-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26007-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="26007-118">-MetricsLevel</span></span>
<span data-ttu-id="26007-119">Anger den mått nivå som Azure-lagring använder för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="26007-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="26007-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="26007-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26007-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="26007-121">None</span></span>
- <span data-ttu-id="26007-122">Serv</span><span class="sxs-lookup"><span data-stu-id="26007-122">Service</span></span>
- <span data-ttu-id="26007-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="26007-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26007-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="26007-124">-MetricsType</span></span>
<span data-ttu-id="26007-125">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="26007-125">Specifies a metrics type.</span></span>
<span data-ttu-id="26007-126">Denna cmdlet anger måttet för Azure Storage Service-värden till det värde som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="26007-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="26007-127">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="26007-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="26007-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26007-128">-PassThru</span></span>
<span data-ttu-id="26007-129">Anger att den här cmdleten returnerar de uppdaterade måtten.</span><span class="sxs-lookup"><span data-stu-id="26007-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="26007-130">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="26007-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26007-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="26007-131">-RetentionDays</span></span>
<span data-ttu-id="26007-132">Anger antalet dagar som Azure Storage-tjänsten behåller statistik information.</span><span class="sxs-lookup"><span data-stu-id="26007-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26007-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="26007-133">-ServiceType</span></span>
<span data-ttu-id="26007-134">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="26007-134">Specifies the storage service type.</span></span>
<span data-ttu-id="26007-135">Denna cmdlet ändrar egenskaperna för de tjänst typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="26007-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="26007-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="26007-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26007-137">Object</span><span class="sxs-lookup"><span data-stu-id="26007-137">Blob</span></span> 
- <span data-ttu-id="26007-138">Tabell</span><span class="sxs-lookup"><span data-stu-id="26007-138">Table</span></span>
- <span data-ttu-id="26007-139">Svarskö</span><span class="sxs-lookup"><span data-stu-id="26007-139">Queue</span></span>
- <span data-ttu-id="26007-140">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="26007-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="26007-141">-Version</span><span class="sxs-lookup"><span data-stu-id="26007-141">-Version</span></span>
<span data-ttu-id="26007-142">Anger versionen för Azure lagrings mått.</span><span class="sxs-lookup"><span data-stu-id="26007-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="26007-143">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="26007-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26007-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26007-144">CommonParameters</span></span>
<span data-ttu-id="26007-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26007-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26007-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26007-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26007-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26007-147">INPUTS</span></span>

### <span data-ttu-id="26007-148">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="26007-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="26007-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26007-149">OUTPUTS</span></span>

### <span data-ttu-id="26007-150">Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="26007-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="26007-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26007-151">NOTES</span></span>

## <span data-ttu-id="26007-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26007-152">RELATED LINKS</span></span>

[<span data-ttu-id="26007-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="26007-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="26007-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="26007-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

