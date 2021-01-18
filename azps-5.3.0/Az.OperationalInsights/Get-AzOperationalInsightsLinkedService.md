---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527387"
---
# <span data-ttu-id="08bc2-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="08bc2-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="08bc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="08bc2-103">Hämta eller lista den länkade tjänsten för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="08bc2-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="08bc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08bc2-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08bc2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="08bc2-106">Hämta eller lista den länkade tjänsten för arbets ytan, lista när "-LinkedServiceName" inte tillhandahölls</span><span class="sxs-lookup"><span data-stu-id="08bc2-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="08bc2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="08bc2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08bc2-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="08bc2-109">Hämta den länkade tjänsten för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="08bc2-109">Get linked service for workspace</span></span>

## <span data-ttu-id="08bc2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08bc2-110">PARAMETERS</span></span>

### <span data-ttu-id="08bc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bc2-111">-DefaultProfile</span></span>
<span data-ttu-id="08bc2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08bc2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bc2-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="08bc2-113">-LinkedServiceName</span></span>
<span data-ttu-id="08bc2-114">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="08bc2-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bc2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08bc2-115">-ResourceGroupName</span></span>
<span data-ttu-id="08bc2-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="08bc2-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bc2-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08bc2-117">-WorkspaceName</span></span>
<span data-ttu-id="08bc2-118">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="08bc2-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bc2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bc2-119">CommonParameters</span></span>
<span data-ttu-id="08bc2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bc2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bc2-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08bc2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bc2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08bc2-122">INPUTS</span></span>

### <span data-ttu-id="08bc2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="08bc2-123">System.String</span></span>

## <span data-ttu-id="08bc2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08bc2-124">OUTPUTS</span></span>

### <span data-ttu-id="08bc2-125">Microsoft. Azure. commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="08bc2-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="08bc2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08bc2-126">NOTES</span></span>

## <span data-ttu-id="08bc2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08bc2-127">RELATED LINKS</span></span>
