---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 64e74b2c9d4aa5f22d48bb6cb80c5a1952424c38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575587"
---
# <span data-ttu-id="c9440-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="c9440-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="c9440-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9440-102">SYNOPSIS</span></span>
<span data-ttu-id="c9440-103">Hämtar konton som inte är kopplade till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c9440-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9440-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9440-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9440-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9440-105">DESCRIPTION</span></span>
<span data-ttu-id="c9440-106">Cmdleten **Get-AzureRmOperationalInsightsLinkTargets** innehåller befintliga konton som inte är associerade med en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c9440-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="c9440-107">Om du vill länka en ny arbets yta till ett befintligt konto använder du ett kund-ID som returneras av den här åtgärden i egenskapen kund-ID för en ny arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c9440-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="c9440-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9440-108">EXAMPLES</span></span>

### <span data-ttu-id="c9440-109">Exempel 1: Hämta olänkade konton</span><span class="sxs-lookup"><span data-stu-id="c9440-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="c9440-110">Det här kommandot får olänkade konton som ägs av anroparens ID.</span><span class="sxs-lookup"><span data-stu-id="c9440-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="c9440-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9440-111">PARAMETERS</span></span>

### <span data-ttu-id="c9440-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9440-112">-DefaultProfile</span></span>
<span data-ttu-id="c9440-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9440-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9440-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9440-114">CommonParameters</span></span>
<span data-ttu-id="c9440-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9440-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9440-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9440-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9440-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9440-117">INPUTS</span></span>

### <span data-ttu-id="c9440-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="c9440-118">None</span></span>
<span data-ttu-id="c9440-119">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c9440-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9440-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9440-120">OUTPUTS</span></span>

### <span data-ttu-id="c9440-121">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="c9440-121">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="c9440-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9440-122">NOTES</span></span>

## <span data-ttu-id="c9440-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9440-123">RELATED LINKS</span></span>

[<span data-ttu-id="c9440-124">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="c9440-124">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

