---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 679a6c434b037913ab5abb68f65b48c324d49b8b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928617"
---
# <span data-ttu-id="960be-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="960be-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="960be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="960be-102">SYNOPSIS</span></span>
<span data-ttu-id="960be-103">Hämtar information om hanterings grupper som är anslutna till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="960be-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="960be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="960be-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="960be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="960be-105">DESCRIPTION</span></span>
<span data-ttu-id="960be-106">Cmdleten **Get-AzOperationalInsightsWorkspaceManagementGroup** visar de hanterings grupper som är anslutna till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="960be-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="960be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="960be-107">EXAMPLES</span></span>

### <span data-ttu-id="960be-108">Exempel 1: Hämta hanterings grupper efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="960be-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="960be-109">Det här kommandot får hanterings grupperna för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="960be-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="960be-110">Exempel 2: få hanterings grupper genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="960be-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="960be-111">Det här kommandot använder cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och skickar sedan arbets ytan till den aktuella cmdleten, som hämtar hanterings grupperna för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="960be-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="960be-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="960be-112">PARAMETERS</span></span>

### <span data-ttu-id="960be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="960be-113">-DefaultProfile</span></span>
<span data-ttu-id="960be-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="960be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="960be-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="960be-115">-Name</span></span>
<span data-ttu-id="960be-116">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="960be-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="960be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="960be-117">-ResourceGroupName</span></span>
<span data-ttu-id="960be-118">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="960be-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="960be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="960be-119">CommonParameters</span></span>
<span data-ttu-id="960be-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="960be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="960be-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="960be-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="960be-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="960be-122">INPUTS</span></span>

### <span data-ttu-id="960be-123">System. String</span><span class="sxs-lookup"><span data-stu-id="960be-123">System.String</span></span>

## <span data-ttu-id="960be-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="960be-124">OUTPUTS</span></span>

### <span data-ttu-id="960be-125">Microsoft. Azure. commands. OperationalInsights. Models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="960be-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="960be-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="960be-126">NOTES</span></span>

## <span data-ttu-id="960be-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="960be-127">RELATED LINKS</span></span>

[<span data-ttu-id="960be-128">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="960be-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="960be-129">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="960be-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


