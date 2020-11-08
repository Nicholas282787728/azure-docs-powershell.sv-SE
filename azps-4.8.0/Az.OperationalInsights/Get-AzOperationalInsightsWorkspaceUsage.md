---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260682"
---
# <span data-ttu-id="22d56-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="22d56-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="22d56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22d56-102">SYNOPSIS</span></span>
<span data-ttu-id="22d56-103">Hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="22d56-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="22d56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22d56-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22d56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22d56-105">DESCRIPTION</span></span>
<span data-ttu-id="22d56-106">Cmdleten **Get-AzOperationalInsightsWorkspaceUsage** hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="22d56-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="22d56-107">Detta visar hur många data som analyseras av arbets ytan under en viss tids period.</span><span class="sxs-lookup"><span data-stu-id="22d56-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="22d56-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22d56-108">EXAMPLES</span></span>

### <span data-ttu-id="22d56-109">Exempel 1: Hämta användnings data efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="22d56-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="22d56-110">Det här kommandot får användnings information för arbets ytan med namnet min arbets yta i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="22d56-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="22d56-111">Exempel 2: Hämta användnings data med pipeline</span><span class="sxs-lookup"><span data-stu-id="22d56-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="22d56-112">Det här kommandot hämtar arbets ytan med namnet min arbets yta med Get-AzOperationalInsightsWorkspace cmdlet och skickar sedan arbets ytan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22d56-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="22d56-113">Kommandot får användnings informationen för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="22d56-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="22d56-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22d56-114">PARAMETERS</span></span>

### <span data-ttu-id="22d56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d56-115">-DefaultProfile</span></span>
<span data-ttu-id="22d56-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="22d56-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22d56-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="22d56-117">-Name</span></span>
<span data-ttu-id="22d56-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="22d56-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="22d56-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d56-119">-ResourceGroupName</span></span>
<span data-ttu-id="22d56-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="22d56-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="22d56-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d56-121">CommonParameters</span></span>
<span data-ttu-id="22d56-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d56-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d56-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d56-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d56-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22d56-124">INPUTS</span></span>

### <span data-ttu-id="22d56-125">System. String</span><span class="sxs-lookup"><span data-stu-id="22d56-125">System.String</span></span>

## <span data-ttu-id="22d56-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22d56-126">OUTPUTS</span></span>

### <span data-ttu-id="22d56-127">Microsoft. Azure. commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="22d56-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="22d56-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22d56-128">NOTES</span></span>

## <span data-ttu-id="22d56-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22d56-129">RELATED LINKS</span></span>

[<span data-ttu-id="22d56-130">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="22d56-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="22d56-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="22d56-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


