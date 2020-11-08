---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: c1054e8dfb9a9133da740c5162c8e8f60c9df5d1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100505"
---
# <span data-ttu-id="7d33a-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="7d33a-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="7d33a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d33a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d33a-103">Hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7d33a-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="7d33a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d33a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d33a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d33a-105">DESCRIPTION</span></span>
<span data-ttu-id="7d33a-106">Cmdleten **Get-AzOperationalInsightsWorkspaceUsage** hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="7d33a-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="7d33a-107">Detta visar hur många data som analyseras av arbets ytan under en viss tids period.</span><span class="sxs-lookup"><span data-stu-id="7d33a-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="7d33a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d33a-108">EXAMPLES</span></span>

### <span data-ttu-id="7d33a-109">Exempel 1: Hämta användnings data efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="7d33a-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="7d33a-110">Det här kommandot får användnings information för arbets ytan med namnet min arbets yta i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7d33a-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="7d33a-111">Exempel 2: Hämta användnings data med pipeline</span><span class="sxs-lookup"><span data-stu-id="7d33a-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="7d33a-112">Det här kommandot hämtar arbets ytan med namnet min arbets yta med Get-AzOperationalInsightsWorkspace cmdlet och skickar sedan arbets ytan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d33a-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="7d33a-113">Kommandot får användnings informationen för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="7d33a-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="7d33a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d33a-114">PARAMETERS</span></span>

### <span data-ttu-id="7d33a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d33a-115">-DefaultProfile</span></span>
<span data-ttu-id="7d33a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7d33a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d33a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d33a-117">-Name</span></span>
<span data-ttu-id="7d33a-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="7d33a-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d33a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d33a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d33a-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="7d33a-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="7d33a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d33a-121">CommonParameters</span></span>
<span data-ttu-id="7d33a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d33a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d33a-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d33a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d33a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d33a-124">INPUTS</span></span>

### <span data-ttu-id="7d33a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7d33a-125">System.String</span></span>

## <span data-ttu-id="7d33a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d33a-126">OUTPUTS</span></span>

### <span data-ttu-id="7d33a-127">Microsoft. Azure. commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="7d33a-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="7d33a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d33a-128">NOTES</span></span>

## <span data-ttu-id="7d33a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d33a-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d33a-130">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="7d33a-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="7d33a-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d33a-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


