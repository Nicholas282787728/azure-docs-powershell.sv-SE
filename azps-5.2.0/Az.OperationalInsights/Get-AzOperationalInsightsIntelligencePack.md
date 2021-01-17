---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416651"
---
# <span data-ttu-id="f5ce6-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f5ce6-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="f5ce6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ce6-103">Hämtar tillgängliga intelligens paket.</span><span class="sxs-lookup"><span data-stu-id="f5ce6-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="f5ce6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5ce6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ce6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5ce6-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ce6-106">Cmdleten **Get-AzOperationalInsightsIntelligencePack** hämtar de tillgängliga intelligens paketen.</span><span class="sxs-lookup"><span data-stu-id="f5ce6-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="f5ce6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5ce6-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ce6-108">Exempel 1: skaffa paketlösningar</span><span class="sxs-lookup"><span data-stu-id="f5ce6-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="f5ce6-109">Det här kommandot får de tillgängliga intelligens-paketen.</span><span class="sxs-lookup"><span data-stu-id="f5ce6-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="f5ce6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5ce6-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ce6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ce6-111">-DefaultProfile</span></span>
<span data-ttu-id="f5ce6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f5ce6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5ce6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ce6-113">-ResourceGroupName</span></span>
<span data-ttu-id="f5ce6-114">Anger namnet på en Azure-adressresurs som innehåller en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="f5ce6-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="f5ce6-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5ce6-115">-WorkspaceName</span></span>
<span data-ttu-id="f5ce6-116">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="f5ce6-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ce6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ce6-117">CommonParameters</span></span>
<span data-ttu-id="f5ce6-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ce6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ce6-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ce6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ce6-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5ce6-120">INPUTS</span></span>

### <span data-ttu-id="f5ce6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f5ce6-121">System.String</span></span>

## <span data-ttu-id="f5ce6-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5ce6-122">OUTPUTS</span></span>

### <span data-ttu-id="f5ce6-123">Microsoft. Azure. commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="f5ce6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="f5ce6-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5ce6-124">NOTES</span></span>

## <span data-ttu-id="f5ce6-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5ce6-125">RELATED LINKS</span></span>

[<span data-ttu-id="f5ce6-126">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="f5ce6-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


