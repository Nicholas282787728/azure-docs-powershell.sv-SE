---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755412"
---
# <span data-ttu-id="b9041-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b9041-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b9041-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9041-102">SYNOPSIS</span></span>
<span data-ttu-id="b9041-103">Inaktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b9041-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9041-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9041-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9041-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9041-105">DESCRIPTION</span></span>
<span data-ttu-id="b9041-106">Cmdleten **disable-AzureStorageDeleteRetentionPolicy** inaktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b9041-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9041-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9041-107">EXAMPLES</span></span>

### <span data-ttu-id="b9041-108">Exempel 1: inaktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="b9041-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="b9041-109">Det här kommandot inaktiverar borttagning av princip för bevarande av Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b9041-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="b9041-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9041-110">PARAMETERS</span></span>

### <span data-ttu-id="b9041-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b9041-111">-Context</span></span>
<span data-ttu-id="b9041-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="b9041-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b9041-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9041-113">-PassThru</span></span>
<span data-ttu-id="b9041-114">Visa DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="b9041-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="b9041-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9041-115">-Confirm</span></span>
<span data-ttu-id="b9041-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9041-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9041-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9041-117">-WhatIf</span></span>
<span data-ttu-id="b9041-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9041-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9041-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9041-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9041-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9041-120">CommonParameters</span></span>
<span data-ttu-id="b9041-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9041-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9041-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9041-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9041-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9041-123">INPUTS</span></span>

### <span data-ttu-id="b9041-124">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b9041-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b9041-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9041-125">OUTPUTS</span></span>

### <span data-ttu-id="b9041-126">Microsoft. WindowsAzure. commands. Storage. Model. ResourceMode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="b9041-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="b9041-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9041-127">NOTES</span></span>

## <span data-ttu-id="b9041-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9041-128">RELATED LINKS</span></span>

