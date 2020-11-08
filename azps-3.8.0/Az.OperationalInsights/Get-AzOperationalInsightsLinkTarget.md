---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: 72841dc8ecc90c14bb41ae8f0f207d990afec9a8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100501"
---
# <span data-ttu-id="54b08-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="54b08-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="54b08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54b08-102">SYNOPSIS</span></span>
<span data-ttu-id="54b08-103">Hämtar konton som inte är kopplade till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="54b08-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="54b08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54b08-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54b08-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54b08-105">DESCRIPTION</span></span>
<span data-ttu-id="54b08-106">Cmdleten **Get-AzOperationalInsightsLinkTarget** innehåller befintliga konton som inte är associerade med en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="54b08-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="54b08-107">Om du vill länka en ny arbets yta till ett befintligt konto använder du ett kund-ID som returneras av den här åtgärden i egenskapen kund-ID för en ny arbets yta.</span><span class="sxs-lookup"><span data-stu-id="54b08-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="54b08-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54b08-108">EXAMPLES</span></span>

### <span data-ttu-id="54b08-109">Exempel 1: Hämta olänkade konton</span><span class="sxs-lookup"><span data-stu-id="54b08-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="54b08-110">Det här kommandot får olänkade konton som ägs av anroparens ID.</span><span class="sxs-lookup"><span data-stu-id="54b08-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="54b08-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54b08-111">PARAMETERS</span></span>

### <span data-ttu-id="54b08-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b08-112">-DefaultProfile</span></span>
<span data-ttu-id="54b08-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54b08-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54b08-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b08-114">CommonParameters</span></span>
<span data-ttu-id="54b08-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54b08-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b08-116">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b08-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b08-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54b08-117">INPUTS</span></span>

### <span data-ttu-id="54b08-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="54b08-118">None</span></span>

## <span data-ttu-id="54b08-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54b08-119">OUTPUTS</span></span>

### <span data-ttu-id="54b08-120">Microsoft. Azure. commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="54b08-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="54b08-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54b08-121">NOTES</span></span>

## <span data-ttu-id="54b08-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54b08-122">RELATED LINKS</span></span>

[<span data-ttu-id="54b08-123">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="54b08-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


