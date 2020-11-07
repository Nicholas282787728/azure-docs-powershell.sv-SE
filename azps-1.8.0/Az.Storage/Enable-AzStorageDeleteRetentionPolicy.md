---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: e9825c0efe0f54788cb074c862d51b747c6fbb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746420"
---
# <span data-ttu-id="e0b50-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0b50-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e0b50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0b50-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b50-103">Aktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e0b50-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e0b50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0b50-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b50-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0b50-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b50-106">Cmdleten **Enable-AzStorageDeleteRetentionPolicy** aktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e0b50-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e0b50-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0b50-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b50-108">Exempel 1: Aktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="e0b50-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="e0b50-109">Med det här kommandot kan du ta bort bevarande princip för Blob-tjänsten och ange rader för borttagna BLOB-bevarande till 3.</span><span class="sxs-lookup"><span data-stu-id="e0b50-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="e0b50-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0b50-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b50-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e0b50-111">-Context</span></span>
<span data-ttu-id="e0b50-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="e0b50-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e0b50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b50-113">-DefaultProfile</span></span>
<span data-ttu-id="e0b50-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b50-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0b50-115">-PassThru</span></span>
<span data-ttu-id="e0b50-116">Visa DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="e0b50-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="e0b50-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="e0b50-117">-RetentionDays</span></span>
<span data-ttu-id="e0b50-118">Anger antalet bevarande dagar för DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="e0b50-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0b50-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0b50-119">-Confirm</span></span>
<span data-ttu-id="e0b50-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0b50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b50-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b50-121">-WhatIf</span></span>
<span data-ttu-id="e0b50-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0b50-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0b50-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0b50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b50-124">CommonParameters</span></span>
<span data-ttu-id="e0b50-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b50-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b50-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b50-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0b50-127">INPUTS</span></span>

### <span data-ttu-id="e0b50-128">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e0b50-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e0b50-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0b50-129">OUTPUTS</span></span>

### <span data-ttu-id="e0b50-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e0b50-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e0b50-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0b50-131">NOTES</span></span>

## <span data-ttu-id="e0b50-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0b50-132">RELATED LINKS</span></span>
