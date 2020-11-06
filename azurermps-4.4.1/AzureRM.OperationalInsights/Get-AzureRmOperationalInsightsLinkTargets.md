---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582276"
---
# <span data-ttu-id="b6a99-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="b6a99-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="b6a99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6a99-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a99-103">Hämtar konton som inte är kopplade till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="b6a99-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6a99-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a99-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6a99-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a99-106">Cmdleten **Get-AzureRmOperationalInsightsLinkTargets** innehåller befintliga konton som inte är associerade med en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b6a99-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="b6a99-107">Om du vill länka en ny arbets yta till ett befintligt konto använder du ett kund-ID som returneras av den här åtgärden i egenskapen kund-ID för en ny arbets yta.</span><span class="sxs-lookup"><span data-stu-id="b6a99-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="b6a99-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6a99-108">EXAMPLES</span></span>

### <span data-ttu-id="b6a99-109">Exempel 1: Hämta olänkade konton</span><span class="sxs-lookup"><span data-stu-id="b6a99-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="b6a99-110">Det här kommandot får olänkade konton som ägs av anroparens ID.</span><span class="sxs-lookup"><span data-stu-id="b6a99-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="b6a99-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6a99-111">PARAMETERS</span></span>

### <span data-ttu-id="b6a99-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a99-112">-DefaultProfile</span></span>
<span data-ttu-id="b6a99-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a99-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a99-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a99-114">CommonParameters</span></span>
<span data-ttu-id="b6a99-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a99-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a99-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a99-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a99-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6a99-117">INPUTS</span></span>

## <span data-ttu-id="b6a99-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6a99-118">OUTPUTS</span></span>

### <span data-ttu-id="b6a99-119">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="b6a99-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="b6a99-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6a99-120">NOTES</span></span>

## <span data-ttu-id="b6a99-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6a99-121">RELATED LINKS</span></span>

[<span data-ttu-id="b6a99-122">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="b6a99-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


