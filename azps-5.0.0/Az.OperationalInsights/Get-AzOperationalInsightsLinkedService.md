---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270806"
---
# <span data-ttu-id="e2721-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="e2721-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="e2721-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2721-102">SYNOPSIS</span></span>
<span data-ttu-id="e2721-103">Hämta eller lista den länkade tjänsten för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="e2721-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="e2721-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2721-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2721-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2721-105">DESCRIPTION</span></span>
<span data-ttu-id="e2721-106">Hämta eller lista den länkade tjänsten för arbets ytan, lista när "-LinkedServiceName" inte tillhandahölls</span><span class="sxs-lookup"><span data-stu-id="e2721-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="e2721-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2721-107">EXAMPLES</span></span>

### <span data-ttu-id="e2721-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e2721-108">Example 1</span></span>
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

<span data-ttu-id="e2721-109">Hämta den länkade tjänsten för arbets ytan</span><span class="sxs-lookup"><span data-stu-id="e2721-109">Get linked service for workspace</span></span>

## <span data-ttu-id="e2721-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2721-110">PARAMETERS</span></span>

### <span data-ttu-id="e2721-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2721-111">-DefaultProfile</span></span>
<span data-ttu-id="e2721-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2721-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2721-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="e2721-113">-LinkedServiceName</span></span>
<span data-ttu-id="e2721-114">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e2721-114">The linked service name.</span></span>

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

### <span data-ttu-id="e2721-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2721-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2721-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e2721-116">The resource group name.</span></span>

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

### <span data-ttu-id="e2721-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2721-117">-WorkspaceName</span></span>
<span data-ttu-id="e2721-118">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="e2721-118">The workspace name.</span></span>

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

### <span data-ttu-id="e2721-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2721-119">CommonParameters</span></span>
<span data-ttu-id="e2721-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2721-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2721-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2721-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2721-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2721-122">INPUTS</span></span>

### <span data-ttu-id="e2721-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e2721-123">System.String</span></span>

## <span data-ttu-id="e2721-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2721-124">OUTPUTS</span></span>

### <span data-ttu-id="e2721-125">Microsoft. Azure. commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="e2721-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="e2721-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2721-126">NOTES</span></span>

## <span data-ttu-id="e2721-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2721-127">RELATED LINKS</span></span>
