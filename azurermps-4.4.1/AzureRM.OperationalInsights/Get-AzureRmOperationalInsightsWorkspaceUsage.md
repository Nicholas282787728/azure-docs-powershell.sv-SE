---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: dfbf5833bd045c40315cb06d2e954688229ac557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577583"
---
# <span data-ttu-id="9d2d6-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="9d2d6-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="9d2d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2d6-103">Hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d2d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d2d6-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d2d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d2d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9d2d6-106">Cmdleten **Get-AzureRmOperationalInsightsWorkspaceUsage** hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="9d2d6-107">Detta visar hur många data som analyseras av arbets ytan under en viss tids period.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="9d2d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d2d6-108">EXAMPLES</span></span>

### <span data-ttu-id="9d2d6-109">Exempel 1: Hämta användnings data efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="9d2d6-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="9d2d6-110">Det här kommandot får användnings information för arbets ytan med namnet min arbets yta i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="9d2d6-111">Exempel 2: Hämta användnings data med pipeline</span><span class="sxs-lookup"><span data-stu-id="9d2d6-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="9d2d6-112">Det här kommandot hämtar arbets ytan med namnet min arbets yta med Get-AzureRmOperationalInsightsWorkspace cmdlet och skickar sedan arbets ytan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="9d2d6-113">Kommandot får användnings informationen för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="9d2d6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d2d6-114">PARAMETERS</span></span>

### <span data-ttu-id="9d2d6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d2d6-115">-Name</span></span>
<span data-ttu-id="9d2d6-116">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="9d2d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d2d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d2d6-118">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="9d2d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2d6-119">-DefaultProfile</span></span>
<span data-ttu-id="9d2d6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d2d6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2d6-121">CommonParameters</span></span>
<span data-ttu-id="9d2d6-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d2d6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2d6-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d2d6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2d6-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d2d6-124">INPUTS</span></span>

## <span data-ttu-id="9d2d6-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d2d6-125">OUTPUTS</span></span>

### <span data-ttu-id="9d2d6-126">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="9d2d6-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="9d2d6-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d2d6-127">NOTES</span></span>

## <span data-ttu-id="9d2d6-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d2d6-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d2d6-129">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="9d2d6-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="9d2d6-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9d2d6-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


