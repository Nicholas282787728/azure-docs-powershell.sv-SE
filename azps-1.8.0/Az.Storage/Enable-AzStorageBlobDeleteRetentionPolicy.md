---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: fdac081aa6edc5ac43c98800ad2d857cb8f62b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746421"
---
# <span data-ttu-id="5ee06-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee06-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="5ee06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ee06-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee06-103">Aktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5ee06-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="5ee06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ee06-104">SYNTAX</span></span>

### <span data-ttu-id="5ee06-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="5ee06-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ee06-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5ee06-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ee06-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="5ee06-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee06-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ee06-108">DESCRIPTION</span></span>
<span data-ttu-id="5ee06-109">Cmdleten **Enable-AzStorageBlobDeleteRetentionPolicy** aktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5ee06-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="5ee06-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ee06-110">EXAMPLES</span></span>

### <span data-ttu-id="5ee06-111">Exempel 1: Aktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="5ee06-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="5ee06-112">Med det här kommandot kan du ta bort bevarande princip för Blob-tjänsten och ange rader för borttagna BLOB-bevarande till 4.</span><span class="sxs-lookup"><span data-stu-id="5ee06-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="5ee06-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ee06-113">PARAMETERS</span></span>

### <span data-ttu-id="5ee06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee06-114">-DefaultProfile</span></span>
<span data-ttu-id="5ee06-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee06-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ee06-116">-PassThru</span></span>
<span data-ttu-id="5ee06-117">Visa ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="5ee06-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="5ee06-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee06-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ee06-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5ee06-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee06-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ee06-120">-ResourceId</span></span>
<span data-ttu-id="5ee06-121">Ange ett resurs-ID för lagrings-ID eller egenskaper för Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5ee06-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee06-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="5ee06-122">-RetentionDays</span></span>
<span data-ttu-id="5ee06-123">Anger antalet bevarande dagar för DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="5ee06-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee06-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee06-124">-StorageAccount</span></span>
<span data-ttu-id="5ee06-125">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="5ee06-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee06-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5ee06-126">-StorageAccountName</span></span>
<span data-ttu-id="5ee06-127">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5ee06-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee06-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ee06-128">-Confirm</span></span>
<span data-ttu-id="5ee06-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ee06-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee06-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee06-130">-WhatIf</span></span>
<span data-ttu-id="5ee06-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ee06-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee06-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ee06-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee06-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee06-133">CommonParameters</span></span>
<span data-ttu-id="5ee06-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee06-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee06-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee06-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee06-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ee06-136">INPUTS</span></span>

### <span data-ttu-id="5ee06-137">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee06-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5ee06-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee06-138">System.String</span></span>

## <span data-ttu-id="5ee06-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ee06-139">OUTPUTS</span></span>

### <span data-ttu-id="5ee06-140">Microsoft. Azure. commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="5ee06-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="5ee06-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ee06-141">NOTES</span></span>

## <span data-ttu-id="5ee06-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ee06-142">RELATED LINKS</span></span>
