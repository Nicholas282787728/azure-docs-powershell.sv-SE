---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 338e54a602391f1c7234445fa9b27713859d0089
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754700"
---
# <span data-ttu-id="7d69c-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="7d69c-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="7d69c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d69c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d69c-103">Hämtar värdet för batch-tjänsten för din prenumeration på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="7d69c-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="7d69c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d69c-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d69c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d69c-105">DESCRIPTION</span></span>
<span data-ttu-id="7d69c-106">Hämtar värdet för batch-tjänsten för angiven prenumeration på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="7d69c-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="7d69c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d69c-107">EXAMPLES</span></span>

### <span data-ttu-id="7d69c-108">Exempel 1: Hämta värdet för batch-tjänsten för abonnemanget i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="7d69c-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="7d69c-109">Det här kommandot får kvoterna för det aktuella abonnemanget i västra USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="7d69c-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="7d69c-110">Returvärdet visar att denna prenumeration endast kan skapa ett batch-konto i den regionen.</span><span class="sxs-lookup"><span data-stu-id="7d69c-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="7d69c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d69c-111">PARAMETERS</span></span>

### <span data-ttu-id="7d69c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d69c-112">-DefaultProfile</span></span>
<span data-ttu-id="7d69c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d69c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d69c-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="7d69c-114">-Location</span></span>
<span data-ttu-id="7d69c-115">Anger den region som denna cmdlet kontrollerar kvoterna för.</span><span class="sxs-lookup"><span data-stu-id="7d69c-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="7d69c-116">Mer information finns i Azure-regioner ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="7d69c-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d69c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d69c-117">CommonParameters</span></span>
<span data-ttu-id="7d69c-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d69c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d69c-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d69c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d69c-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d69c-120">INPUTS</span></span>

### <span data-ttu-id="7d69c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7d69c-121">System.String</span></span>

## <span data-ttu-id="7d69c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d69c-122">OUTPUTS</span></span>

### <span data-ttu-id="7d69c-123">Microsoft.Azure.Commands.BatCH. Modeller. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="7d69c-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="7d69c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d69c-124">NOTES</span></span>

## <span data-ttu-id="7d69c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d69c-125">RELATED LINKS</span></span>
