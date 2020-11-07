---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: 810dc3246e1b1d49db491c030446117dbabfb548
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931554"
---
# <span data-ttu-id="21377-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="21377-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="21377-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21377-102">SYNOPSIS</span></span>
<span data-ttu-id="21377-103">Ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="21377-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21377-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21377-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21377-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21377-105">DESCRIPTION</span></span>
<span data-ttu-id="21377-106">Cmdleten **set-AzureStorageServiceLoggingProperty** ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="21377-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="21377-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21377-107">EXAMPLES</span></span>

### <span data-ttu-id="21377-108">Exempel 1: ändra loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="21377-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="21377-109">Det här kommandot ändrar version 1,0-loggning för Blob Storage för att omfatta Läs-och skriv åtgärder.</span><span class="sxs-lookup"><span data-stu-id="21377-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="21377-110">Loggning av Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="21377-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="21377-111">Eftersom det här kommandot anger parametern *Passthru* visas de ändrade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="21377-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="21377-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21377-112">PARAMETERS</span></span>

### <span data-ttu-id="21377-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="21377-113">-Context</span></span>
<span data-ttu-id="21377-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="21377-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="21377-115">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="21377-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="21377-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21377-116">-DefaultProfile</span></span>
<span data-ttu-id="21377-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21377-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21377-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="21377-118">-LoggingOperations</span></span>
<span data-ttu-id="21377-119">Anger en matris med Azure Storage Service-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="21377-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="21377-120">Azure Storage Services loggar de åtgärder som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="21377-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="21377-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21377-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21377-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="21377-122">None</span></span>
- <span data-ttu-id="21377-123">Läst</span><span class="sxs-lookup"><span data-stu-id="21377-123">Read</span></span>
- <span data-ttu-id="21377-124">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="21377-124">Write</span></span>
- <span data-ttu-id="21377-125">Ta bort</span><span class="sxs-lookup"><span data-stu-id="21377-125">Delete</span></span>
- <span data-ttu-id="21377-126">Alla</span><span class="sxs-lookup"><span data-stu-id="21377-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21377-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21377-127">-PassThru</span></span>
<span data-ttu-id="21377-128">Anger att den här cmdleten returnerar de uppdaterade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="21377-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="21377-129">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="21377-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="21377-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="21377-130">-RetentionDays</span></span>
<span data-ttu-id="21377-131">Anger antalet dagar som Azure Storage-tjänsten behåller loggad information.</span><span class="sxs-lookup"><span data-stu-id="21377-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="21377-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="21377-132">-ServiceType</span></span>
<span data-ttu-id="21377-133">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="21377-133">Specifies the storage service type.</span></span>
<span data-ttu-id="21377-134">Denna cmdlet ändrar loggnings egenskaperna för tjänste typen som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="21377-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="21377-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21377-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21377-136">Object</span><span class="sxs-lookup"><span data-stu-id="21377-136">Blob</span></span> 
- <span data-ttu-id="21377-137">Tabell</span><span class="sxs-lookup"><span data-stu-id="21377-137">Table</span></span>
- <span data-ttu-id="21377-138">Svarskö</span><span class="sxs-lookup"><span data-stu-id="21377-138">Queue</span></span>
- <span data-ttu-id="21377-139">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="21377-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="21377-140">-Version</span><span class="sxs-lookup"><span data-stu-id="21377-140">-Version</span></span>
<span data-ttu-id="21377-141">Anger versionen för loggning av Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="21377-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="21377-142">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="21377-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="21377-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21377-143">CommonParameters</span></span>
<span data-ttu-id="21377-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21377-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21377-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21377-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21377-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21377-146">INPUTS</span></span>

### <span data-ttu-id="21377-147">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="21377-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="21377-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21377-148">OUTPUTS</span></span>

### <span data-ttu-id="21377-149">Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="21377-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="21377-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21377-150">NOTES</span></span>

## <span data-ttu-id="21377-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21377-151">RELATED LINKS</span></span>

[<span data-ttu-id="21377-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="21377-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="21377-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="21377-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


