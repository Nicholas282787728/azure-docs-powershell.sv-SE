---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575169"
---
# <span data-ttu-id="7fbf4-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="7fbf4-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="7fbf4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fbf4-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbf4-103">Hämtar konton som inte är kopplade till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fbf4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fbf4-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fbf4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fbf4-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbf4-106">Cmdleten **Get-AzureRmOperationalInsightsLinkTargets** innehåller befintliga konton som inte är associerade med en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="7fbf4-107">Om du vill länka en ny arbets yta till ett befintligt konto använder du ett kund-ID som returneras av den här åtgärden i egenskapen kund-ID för en ny arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="7fbf4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fbf4-108">EXAMPLES</span></span>

### <span data-ttu-id="7fbf4-109">Exempel 1: Hämta olänkade konton</span><span class="sxs-lookup"><span data-stu-id="7fbf4-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="7fbf4-110">Det här kommandot får olänkade konton som ägs av anroparens ID.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="7fbf4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fbf4-111">PARAMETERS</span></span>

### <span data-ttu-id="7fbf4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbf4-112">-DefaultProfile</span></span>
<span data-ttu-id="7fbf4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7fbf4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fbf4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbf4-114">CommonParameters</span></span>
<span data-ttu-id="7fbf4-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbf4-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbf4-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbf4-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fbf4-117">INPUTS</span></span>

### <span data-ttu-id="7fbf4-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="7fbf4-118">None</span></span>

## <span data-ttu-id="7fbf4-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fbf4-119">OUTPUTS</span></span>

### <span data-ttu-id="7fbf4-120">Microsoft. Azure. commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="7fbf4-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="7fbf4-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fbf4-121">NOTES</span></span>

## <span data-ttu-id="7fbf4-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fbf4-122">RELATED LINKS</span></span>

[<span data-ttu-id="7fbf4-123">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="7fbf4-123">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


