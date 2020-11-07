---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 45192b6b24719bb793e3f443cf2a8cb42abd78ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931553"
---
# <span data-ttu-id="20536-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="20536-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="20536-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20536-102">SYNOPSIS</span></span>
<span data-ttu-id="20536-103">Ändrar mått för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20536-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20536-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20536-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20536-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20536-105">DESCRIPTION</span></span>
<span data-ttu-id="20536-106">Cmdleten **set-AzureStorageServiceMetricsProperty** ändrar måtten för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20536-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="20536-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20536-107">EXAMPLES</span></span>

### <span data-ttu-id="20536-108">Exempel 1: ändra mått egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="20536-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="20536-109">Det här kommandot ändrar version 1,0-värden för blob-lagring till en tjänst nivå.</span><span class="sxs-lookup"><span data-stu-id="20536-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="20536-110">Mått för Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="20536-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="20536-111">Eftersom det här kommandot anger parametern *Passthru* visas egenskaperna för de ändrade måtten.</span><span class="sxs-lookup"><span data-stu-id="20536-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="20536-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20536-112">PARAMETERS</span></span>

### <span data-ttu-id="20536-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="20536-113">-Context</span></span>
<span data-ttu-id="20536-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="20536-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="20536-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="20536-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="20536-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20536-116">-DefaultProfile</span></span>
<span data-ttu-id="20536-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20536-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20536-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="20536-118">-MetricsLevel</span></span>
<span data-ttu-id="20536-119">Anger den mått nivå som Azure-lagring använder för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="20536-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="20536-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="20536-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20536-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="20536-121">None</span></span>
- <span data-ttu-id="20536-122">Serv</span><span class="sxs-lookup"><span data-stu-id="20536-122">Service</span></span>
- <span data-ttu-id="20536-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="20536-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20536-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="20536-124">-MetricsType</span></span>
<span data-ttu-id="20536-125">Anger en typ av mått.</span><span class="sxs-lookup"><span data-stu-id="20536-125">Specifies a metrics type.</span></span>
<span data-ttu-id="20536-126">Den här cmldet ställer in värdet för Azure Storage Service-värden på det värde som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="20536-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="20536-127">De acceptabla värdena för den här parametern är: timme och minut.</span><span class="sxs-lookup"><span data-stu-id="20536-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="20536-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20536-128">-PassThru</span></span>
<span data-ttu-id="20536-129">Anger att den här cmdleten returnerar de uppdaterade måtten.</span><span class="sxs-lookup"><span data-stu-id="20536-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="20536-130">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="20536-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="20536-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="20536-131">-RetentionDays</span></span>
<span data-ttu-id="20536-132">Anger antalet dagar som Azure Storage-tjänsten behåller statistik information.</span><span class="sxs-lookup"><span data-stu-id="20536-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="20536-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="20536-133">-ServiceType</span></span>
<span data-ttu-id="20536-134">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="20536-134">Specifies the storage service type.</span></span>
<span data-ttu-id="20536-135">Denna cmdlet ändrar egenskaperna för de tjänst typer som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="20536-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="20536-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="20536-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20536-137">Object</span><span class="sxs-lookup"><span data-stu-id="20536-137">Blob</span></span> 
- <span data-ttu-id="20536-138">Tabell</span><span class="sxs-lookup"><span data-stu-id="20536-138">Table</span></span>
- <span data-ttu-id="20536-139">Svarskö</span><span class="sxs-lookup"><span data-stu-id="20536-139">Queue</span></span>
- <span data-ttu-id="20536-140">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="20536-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="20536-141">-Version</span><span class="sxs-lookup"><span data-stu-id="20536-141">-Version</span></span>
<span data-ttu-id="20536-142">Anger versionen för Azure lagrings mått.</span><span class="sxs-lookup"><span data-stu-id="20536-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="20536-143">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="20536-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="20536-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20536-144">CommonParameters</span></span>
<span data-ttu-id="20536-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20536-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20536-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20536-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20536-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20536-147">INPUTS</span></span>

### <span data-ttu-id="20536-148">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20536-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="20536-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20536-149">OUTPUTS</span></span>

### <span data-ttu-id="20536-150">Microsoft. WindowsAzure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="20536-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="20536-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20536-151">NOTES</span></span>

## <span data-ttu-id="20536-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20536-152">RELATED LINKS</span></span>

[<span data-ttu-id="20536-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="20536-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="20536-154">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="20536-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


