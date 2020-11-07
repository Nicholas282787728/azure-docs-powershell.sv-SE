---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 70f2a9a426ab5e2cb9a2083e6e645973c9ee743a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923445"
---
# <span data-ttu-id="2b771-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2b771-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="2b771-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b771-102">SYNOPSIS</span></span>
<span data-ttu-id="2b771-103">Ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="2b771-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="2b771-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b771-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b771-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b771-105">DESCRIPTION</span></span>
<span data-ttu-id="2b771-106">Cmdleten **set-AzStorageServiceLoggingProperty** ändrar loggning för Azure Storage-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="2b771-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="2b771-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b771-107">EXAMPLES</span></span>

### <span data-ttu-id="2b771-108">Exempel 1: ändra loggnings egenskaper för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="2b771-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="2b771-109">Det här kommandot ändrar version 1,0-loggning för Blob Storage för att omfatta Läs-och skriv åtgärder.</span><span class="sxs-lookup"><span data-stu-id="2b771-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="2b771-110">Loggning av Azure Storage-tjänsten bevarar poster i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="2b771-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="2b771-111">Eftersom det här kommandot anger parametern *Passthru* visas de ändrade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="2b771-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="2b771-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b771-112">PARAMETERS</span></span>

### <span data-ttu-id="2b771-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2b771-113">-Context</span></span>
<span data-ttu-id="2b771-114">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2b771-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2b771-115">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2b771-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2b771-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b771-116">-DefaultProfile</span></span>
<span data-ttu-id="2b771-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b771-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b771-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="2b771-118">-LoggingOperations</span></span>
<span data-ttu-id="2b771-119">Anger en matris med Azure Storage Service-åtgärder.</span><span class="sxs-lookup"><span data-stu-id="2b771-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="2b771-120">Azure Storage Services loggar de åtgärder som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2b771-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="2b771-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2b771-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b771-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="2b771-122">None</span></span>
- <span data-ttu-id="2b771-123">Läst</span><span class="sxs-lookup"><span data-stu-id="2b771-123">Read</span></span>
- <span data-ttu-id="2b771-124">Skrivcache</span><span class="sxs-lookup"><span data-stu-id="2b771-124">Write</span></span>
- <span data-ttu-id="2b771-125">Ta bort</span><span class="sxs-lookup"><span data-stu-id="2b771-125">Delete</span></span>
- <span data-ttu-id="2b771-126">Alla</span><span class="sxs-lookup"><span data-stu-id="2b771-126">All</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b771-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b771-127">-PassThru</span></span>
<span data-ttu-id="2b771-128">Anger att den här cmdleten returnerar de uppdaterade loggnings egenskaperna.</span><span class="sxs-lookup"><span data-stu-id="2b771-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="2b771-129">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="2b771-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2b771-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="2b771-130">-RetentionDays</span></span>
<span data-ttu-id="2b771-131">Anger antalet dagar som Azure Storage-tjänsten behåller loggad information.</span><span class="sxs-lookup"><span data-stu-id="2b771-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="2b771-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2b771-132">-ServiceType</span></span>
<span data-ttu-id="2b771-133">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="2b771-133">Specifies the storage service type.</span></span>
<span data-ttu-id="2b771-134">Denna cmdlet ändrar loggnings egenskaperna för tjänste typen som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="2b771-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="2b771-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2b771-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b771-136">Object</span><span class="sxs-lookup"><span data-stu-id="2b771-136">Blob</span></span> 
- <span data-ttu-id="2b771-137">Tabell</span><span class="sxs-lookup"><span data-stu-id="2b771-137">Table</span></span>
- <span data-ttu-id="2b771-138">Svarskö</span><span class="sxs-lookup"><span data-stu-id="2b771-138">Queue</span></span>
- <span data-ttu-id="2b771-139">Fil värdet stöds inte för närvarande.</span><span class="sxs-lookup"><span data-stu-id="2b771-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="2b771-140">-Version</span><span class="sxs-lookup"><span data-stu-id="2b771-140">-Version</span></span>
<span data-ttu-id="2b771-141">Anger versionen för loggning av Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2b771-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="2b771-142">Standardvärdet är 1,0.</span><span class="sxs-lookup"><span data-stu-id="2b771-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="2b771-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b771-143">CommonParameters</span></span>
<span data-ttu-id="2b771-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b771-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b771-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b771-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b771-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b771-146">INPUTS</span></span>

### <span data-ttu-id="2b771-147">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b771-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2b771-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b771-148">OUTPUTS</span></span>

### <span data-ttu-id="2b771-149">Microsoft. WindowsAz. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="2b771-149">Microsoft.WindowsAz.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="2b771-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b771-150">NOTES</span></span>

## <span data-ttu-id="2b771-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b771-151">RELATED LINKS</span></span>

[<span data-ttu-id="2b771-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2b771-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="2b771-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b771-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


