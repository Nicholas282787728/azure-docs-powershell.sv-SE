---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 808c92e987d30e97ee0ad2ed56b24be9b0f92a1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755484"
---
# <span data-ttu-id="775a8-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="775a8-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="775a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="775a8-102">SYNOPSIS</span></span>
<span data-ttu-id="775a8-103">Hämtar information om hanterings grupper som är anslutna till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="775a8-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="775a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="775a8-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="775a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="775a8-105">DESCRIPTION</span></span>
<span data-ttu-id="775a8-106">Cmdleten **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** visar de hanterings grupper som är anslutna till en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="775a8-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="775a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="775a8-107">EXAMPLES</span></span>

### <span data-ttu-id="775a8-108">Exempel 1: Hämta hanterings grupper efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="775a8-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="775a8-109">Det här kommandot får hanterings grupperna för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="775a8-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="775a8-110">Exempel 2: få hanterings grupper genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="775a8-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="775a8-111">Det här kommandot använder cmdleten Get-AzureRmOperationalInsightsWorkspace för att hämta arbets ytan med namnet min arbets yta och skickar sedan arbets ytan till den aktuella cmdleten, som hämtar hanterings grupperna för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="775a8-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="775a8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="775a8-112">PARAMETERS</span></span>

### <span data-ttu-id="775a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775a8-113">-DefaultProfile</span></span>
<span data-ttu-id="775a8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="775a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="775a8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="775a8-115">-Name</span></span>
<span data-ttu-id="775a8-116">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="775a8-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="775a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="775a8-118">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="775a8-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="775a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775a8-119">CommonParameters</span></span>
<span data-ttu-id="775a8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775a8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775a8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775a8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="775a8-122">INPUTS</span></span>

### <span data-ttu-id="775a8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="775a8-123">None</span></span>
<span data-ttu-id="775a8-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="775a8-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="775a8-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="775a8-125">OUTPUTS</span></span>

### <span data-ttu-id="775a8-126">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. Models. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="775a8-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="775a8-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="775a8-127">NOTES</span></span>

## <span data-ttu-id="775a8-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="775a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="775a8-129">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="775a8-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="775a8-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="775a8-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

