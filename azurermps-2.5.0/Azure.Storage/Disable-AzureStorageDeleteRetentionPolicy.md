---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930037"
---
# <span data-ttu-id="a6f98-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6f98-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a6f98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6f98-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f98-103">Inaktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a6f98-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6f98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6f98-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6f98-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6f98-105">DESCRIPTION</span></span>
<span data-ttu-id="a6f98-106">Cmdleten **disable-AzureStorageDeleteRetentionPolicy** inaktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a6f98-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="a6f98-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6f98-107">EXAMPLES</span></span>

### <span data-ttu-id="a6f98-108">Exempel 1: inaktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="a6f98-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="a6f98-109">Det här kommandot inaktiverar borttagning av princip för bevarande av Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a6f98-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="a6f98-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6f98-110">PARAMETERS</span></span>

### <span data-ttu-id="a6f98-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a6f98-111">-Context</span></span>
<span data-ttu-id="a6f98-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="a6f98-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a6f98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f98-113">-DefaultProfile</span></span>
<span data-ttu-id="a6f98-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6f98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f98-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6f98-115">-PassThru</span></span>
<span data-ttu-id="a6f98-116">Visa DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="a6f98-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="a6f98-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6f98-117">-Confirm</span></span>
<span data-ttu-id="a6f98-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6f98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6f98-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f98-119">-WhatIf</span></span>
<span data-ttu-id="a6f98-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6f98-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6f98-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6f98-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6f98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f98-122">CommonParameters</span></span>
<span data-ttu-id="a6f98-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f98-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f98-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f98-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6f98-125">INPUTS</span></span>

### <span data-ttu-id="a6f98-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6f98-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6f98-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6f98-127">OUTPUTS</span></span>

### <span data-ttu-id="a6f98-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a6f98-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a6f98-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6f98-129">NOTES</span></span>

## <span data-ttu-id="a6f98-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6f98-130">RELATED LINKS</span></span>
