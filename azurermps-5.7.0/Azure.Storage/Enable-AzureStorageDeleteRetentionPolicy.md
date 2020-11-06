---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574465"
---
# <span data-ttu-id="64e2c-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="64e2c-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="64e2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="64e2c-103">Aktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="64e2c-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64e2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64e2c-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64e2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="64e2c-106">Cmdleten **Enable-AzureStorageDeleteRetentionPolicy** aktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="64e2c-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="64e2c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64e2c-107">EXAMPLES</span></span>

### <span data-ttu-id="64e2c-108">Exempel 1: Aktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="64e2c-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="64e2c-109">Med det här kommandot kan du ta bort bevarande princip för Blob-tjänsten och ange rader för borttagna BLOB-bevarande till 3.</span><span class="sxs-lookup"><span data-stu-id="64e2c-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="64e2c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64e2c-110">PARAMETERS</span></span>

### <span data-ttu-id="64e2c-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="64e2c-111">-Context</span></span>
<span data-ttu-id="64e2c-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="64e2c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="64e2c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64e2c-113">-PassThru</span></span>
<span data-ttu-id="64e2c-114">Visa DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="64e2c-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="64e2c-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="64e2c-115">-RetentionDays</span></span>
<span data-ttu-id="64e2c-116">Anger antalet bevarande dagar för DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="64e2c-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64e2c-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64e2c-117">-Confirm</span></span>
<span data-ttu-id="64e2c-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64e2c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64e2c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e2c-119">-WhatIf</span></span>
<span data-ttu-id="64e2c-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64e2c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e2c-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64e2c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64e2c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e2c-122">CommonParameters</span></span>
<span data-ttu-id="64e2c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64e2c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e2c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64e2c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e2c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64e2c-125">INPUTS</span></span>

### <span data-ttu-id="64e2c-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="64e2c-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="64e2c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64e2c-127">OUTPUTS</span></span>

### <span data-ttu-id="64e2c-128">Microsoft. WindowsAzure. Storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="64e2c-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="64e2c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64e2c-129">NOTES</span></span>

## <span data-ttu-id="64e2c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64e2c-130">RELATED LINKS</span></span>

