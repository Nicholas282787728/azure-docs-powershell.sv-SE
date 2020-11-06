---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 091f9b57d7e40c20b52f82ec9d6c17e6d90dad3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574877"
---
# <span data-ttu-id="d6110-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="d6110-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="d6110-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6110-102">SYNOPSIS</span></span>
<span data-ttu-id="d6110-103">Hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="d6110-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6110-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6110-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6110-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6110-105">DESCRIPTION</span></span>
<span data-ttu-id="d6110-106">Cmdleten **Get-AzureRmOperationalInsightsWorkspaceUsage** hämtar användnings data för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="d6110-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="d6110-107">Detta visar hur många data som analyseras av arbets ytan under en viss tids period.</span><span class="sxs-lookup"><span data-stu-id="d6110-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="d6110-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6110-108">EXAMPLES</span></span>

### <span data-ttu-id="d6110-109">Exempel 1: Hämta användnings data efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="d6110-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="d6110-110">Det här kommandot får användnings information för arbets ytan med namnet min arbets yta i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6110-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="d6110-111">Exempel 2: Hämta användnings data med pipeline</span><span class="sxs-lookup"><span data-stu-id="d6110-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="d6110-112">Det här kommandot hämtar arbets ytan med namnet min arbets yta med Get-AzureRmOperationalInsightsWorkspace cmdlet och skickar sedan arbets ytan till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6110-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="d6110-113">Kommandot får användnings informationen för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="d6110-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="d6110-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6110-114">PARAMETERS</span></span>

### <span data-ttu-id="d6110-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6110-115">-DefaultProfile</span></span>
<span data-ttu-id="d6110-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d6110-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6110-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6110-117">-Name</span></span>
<span data-ttu-id="d6110-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="d6110-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6110-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6110-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6110-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d6110-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="d6110-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6110-121">CommonParameters</span></span>
<span data-ttu-id="d6110-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6110-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6110-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6110-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6110-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6110-124">INPUTS</span></span>

### <span data-ttu-id="d6110-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="d6110-125">None</span></span>
<span data-ttu-id="d6110-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d6110-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6110-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6110-127">OUTPUTS</span></span>

### <span data-ttu-id="d6110-128">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="d6110-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="d6110-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6110-129">NOTES</span></span>

## <span data-ttu-id="d6110-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6110-130">RELATED LINKS</span></span>

[<span data-ttu-id="d6110-131">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="d6110-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="d6110-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6110-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


