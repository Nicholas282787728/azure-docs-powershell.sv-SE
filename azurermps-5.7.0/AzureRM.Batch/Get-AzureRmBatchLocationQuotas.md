---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 1390efccef67e6bfb626e9b31d1a58c72c9fb36e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756807"
---
# <span data-ttu-id="bbe0a-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="bbe0a-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="bbe0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbe0a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe0a-103">Hämtar värdet för batch-tjänsten för din prenumeration på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbe0a-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbe0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbe0a-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe0a-106">Hämtar värdet för batch-tjänsten för angiven prenumeration på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="bbe0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbe0a-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe0a-108">Exempel 1: Hämta värdet för batch-tjänsten för abonnemanget i västra USA-regionen</span><span class="sxs-lookup"><span data-stu-id="bbe0a-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="bbe0a-109">Det här kommandot får kvoterna för det aktuella abonnemanget i västra USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="bbe0a-110">Returvärdet visar att denna prenumeration endast kan skapa ett batch-konto i den regionen.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="bbe0a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbe0a-111">PARAMETERS</span></span>

### <span data-ttu-id="bbe0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe0a-112">-DefaultProfile</span></span>
<span data-ttu-id="bbe0a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe0a-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="bbe0a-114">-Location</span></span>
<span data-ttu-id="bbe0a-115">Anger den region som denna cmdlet kontrollerar kvoterna för.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="bbe0a-116">Mer information finns i Azure-regioner ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="bbe0a-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe0a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe0a-117">CommonParameters</span></span>
<span data-ttu-id="bbe0a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe0a-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe0a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe0a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbe0a-120">INPUTS</span></span>

### <span data-ttu-id="bbe0a-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="bbe0a-121">None</span></span>
<span data-ttu-id="bbe0a-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bbe0a-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbe0a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbe0a-123">OUTPUTS</span></span>

### <span data-ttu-id="bbe0a-124">Microsoft.Azure.Commands.BatCH. Modeller. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="bbe0a-124">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="bbe0a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbe0a-125">NOTES</span></span>

## <span data-ttu-id="bbe0a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbe0a-126">RELATED LINKS</span></span>

