---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 656fe09054b1cfae90175cc4ea55370f80dfd8e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574106"
---
# <span data-ttu-id="bea55-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bea55-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bea55-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bea55-102">SYNOPSIS</span></span>
<span data-ttu-id="bea55-103">Inaktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bea55-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea55-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bea55-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea55-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bea55-105">DESCRIPTION</span></span>
<span data-ttu-id="bea55-106">Cmdleten **disable-AzureStorageDeleteRetentionPolicy** inaktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bea55-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bea55-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bea55-107">EXAMPLES</span></span>

### <span data-ttu-id="bea55-108">Exempel 1: inaktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="bea55-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="bea55-109">Det här kommandot inaktiverar borttagning av princip för bevarande av Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bea55-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="bea55-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bea55-110">PARAMETERS</span></span>

### <span data-ttu-id="bea55-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bea55-111">-Context</span></span>
<span data-ttu-id="bea55-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="bea55-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bea55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea55-113">-DefaultProfile</span></span>
<span data-ttu-id="bea55-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bea55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea55-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bea55-115">-PassThru</span></span>
<span data-ttu-id="bea55-116">Visa DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="bea55-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="bea55-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bea55-117">-Confirm</span></span>
<span data-ttu-id="bea55-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bea55-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea55-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea55-119">-WhatIf</span></span>
<span data-ttu-id="bea55-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bea55-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea55-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bea55-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea55-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea55-122">CommonParameters</span></span>
<span data-ttu-id="bea55-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea55-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea55-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea55-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea55-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bea55-125">INPUTS</span></span>

### <span data-ttu-id="bea55-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bea55-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bea55-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bea55-127">OUTPUTS</span></span>

### <span data-ttu-id="bea55-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bea55-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bea55-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bea55-129">NOTES</span></span>

## <span data-ttu-id="bea55-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bea55-130">RELATED LINKS</span></span>
