---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: fad4e01b06182d689e105f4b5e6c6a580e1b20b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746426"
---
# <span data-ttu-id="cdf0a-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cdf0a-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="cdf0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdf0a-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf0a-103">Inaktivera borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="cdf0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdf0a-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdf0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdf0a-105">DESCRIPTION</span></span>
<span data-ttu-id="cdf0a-106">Cmdleten **disable-AzStorageDeleteRetentionPolicy** inaktiverar borttagnings principer för Azure Storage Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="cdf0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdf0a-107">EXAMPLES</span></span>

### <span data-ttu-id="cdf0a-108">Exempel 1: inaktivera borttagnings principer för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="cdf0a-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="cdf0a-109">Det här kommandot inaktiverar borttagning av princip för bevarande av Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="cdf0a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdf0a-110">PARAMETERS</span></span>

### <span data-ttu-id="cdf0a-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cdf0a-111">-Context</span></span>
<span data-ttu-id="cdf0a-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="cdf0a-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="cdf0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf0a-113">-DefaultProfile</span></span>
<span data-ttu-id="cdf0a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdf0a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdf0a-115">-PassThru</span></span>
<span data-ttu-id="cdf0a-116">Visa DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="cdf0a-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="cdf0a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdf0a-117">-Confirm</span></span>
<span data-ttu-id="cdf0a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdf0a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdf0a-119">-WhatIf</span></span>
<span data-ttu-id="cdf0a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdf0a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdf0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf0a-122">CommonParameters</span></span>
<span data-ttu-id="cdf0a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf0a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdf0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf0a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdf0a-125">INPUTS</span></span>

### <span data-ttu-id="cdf0a-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cdf0a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cdf0a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdf0a-127">OUTPUTS</span></span>

### <span data-ttu-id="cdf0a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cdf0a-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="cdf0a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdf0a-129">NOTES</span></span>

## <span data-ttu-id="cdf0a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdf0a-130">RELATED LINKS</span></span>
