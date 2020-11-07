---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: 2f0c59acba56fb80a12df0c5df6c8168ebc91000
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931045"
---
# <span data-ttu-id="ff100-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ff100-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="ff100-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff100-102">SYNOPSIS</span></span>
<span data-ttu-id="ff100-103">Ändrar egenskaperna för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ff100-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff100-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff100-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff100-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff100-105">DESCRIPTION</span></span>
<span data-ttu-id="ff100-106">Cmdleten **Update-AzureStorageServiceProperty** ändrar egenskaperna för Azure Storage-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ff100-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="ff100-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff100-107">EXAMPLES</span></span>

### <span data-ttu-id="ff100-108">Exempel 1: Ange BLOB service-DefaultServiceVersion till 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="ff100-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="ff100-109">Det här kommandot anger DefaultServiceVersion för Blob-tjänsten till 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="ff100-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="ff100-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff100-110">PARAMETERS</span></span>

### <span data-ttu-id="ff100-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ff100-111">-Context</span></span>
<span data-ttu-id="ff100-112">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="ff100-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff100-113">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="ff100-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ff100-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff100-114">-DefaultProfile</span></span>
<span data-ttu-id="ff100-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff100-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff100-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="ff100-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="ff100-117">DefaultServiceVersion anger vilken standard version som ska användas för förfrågningar till Blob-tjänsten om en inkommande begärans version inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="ff100-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="ff100-118">Möjliga värden inkluderar version 2008-10-27 och alla nyare versioner.</span><span class="sxs-lookup"><span data-stu-id="ff100-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="ff100-119">Mer information finns i https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="ff100-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff100-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff100-120">-PassThru</span></span>
<span data-ttu-id="ff100-121">Visa ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="ff100-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="ff100-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ff100-122">-ServiceType</span></span>
<span data-ttu-id="ff100-123">Anger typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="ff100-123">Specifies the storage service type.</span></span>
<span data-ttu-id="ff100-124">Med den här cmdleten får du loggnings egenskaper för den typ av tjänst som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ff100-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ff100-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ff100-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff100-126">Object</span><span class="sxs-lookup"><span data-stu-id="ff100-126">Blob</span></span> 
- <span data-ttu-id="ff100-127">Tabell</span><span class="sxs-lookup"><span data-stu-id="ff100-127">Table</span></span>
- <span data-ttu-id="ff100-128">Svarskö</span><span class="sxs-lookup"><span data-stu-id="ff100-128">Queue</span></span>
- <span data-ttu-id="ff100-129">Fil</span><span class="sxs-lookup"><span data-stu-id="ff100-129">File</span></span>

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

### <span data-ttu-id="ff100-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff100-130">-Confirm</span></span>
<span data-ttu-id="ff100-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff100-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff100-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff100-132">-WhatIf</span></span>
<span data-ttu-id="ff100-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff100-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff100-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff100-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff100-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff100-135">CommonParameters</span></span>
<span data-ttu-id="ff100-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff100-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff100-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff100-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff100-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff100-138">INPUTS</span></span>

### <span data-ttu-id="ff100-139">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff100-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ff100-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff100-140">OUTPUTS</span></span>

### <span data-ttu-id="ff100-141">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="ff100-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="ff100-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff100-142">NOTES</span></span>

## <span data-ttu-id="ff100-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff100-143">RELATED LINKS</span></span>
