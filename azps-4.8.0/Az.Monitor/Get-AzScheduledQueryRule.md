---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102228"
---
# <span data-ttu-id="df5e5-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="df5e5-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="df5e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="df5e5-103">Hämtar schemalagda frågor</span><span class="sxs-lookup"><span data-stu-id="df5e5-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="df5e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df5e5-104">SYNTAX</span></span>

### <span data-ttu-id="df5e5-105">BySubscriptionOrResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="df5e5-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df5e5-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="df5e5-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df5e5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df5e5-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df5e5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df5e5-108">DESCRIPTION</span></span>
<span data-ttu-id="df5e5-109">Hämtar schemalagda frågor</span><span class="sxs-lookup"><span data-stu-id="df5e5-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="df5e5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df5e5-110">EXAMPLES</span></span>

### <span data-ttu-id="df5e5-111">Exempel 1: lista efter abonnemang eller resurs grupp</span><span class="sxs-lookup"><span data-stu-id="df5e5-111">Example 1: List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="df5e5-112">Exempel 2: get efter regel namn</span><span class="sxs-lookup"><span data-stu-id="df5e5-112">Example 2: Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="df5e5-113">Exempel 3: get efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="df5e5-113">Example 3: Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="df5e5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df5e5-114">PARAMETERS</span></span>

### <span data-ttu-id="df5e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5e5-115">-DefaultProfile</span></span>
<span data-ttu-id="df5e5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df5e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df5e5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="df5e5-117">-Name</span></span>
<span data-ttu-id="df5e5-118">Namnet på notifieringsregeln</span><span class="sxs-lookup"><span data-stu-id="df5e5-118">The alert rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df5e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="df5e5-120">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="df5e5-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df5e5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df5e5-121">-ResourceId</span></span>
<span data-ttu-id="df5e5-122">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="df5e5-122">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df5e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5e5-123">CommonParameters</span></span>
<span data-ttu-id="df5e5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5e5-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df5e5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5e5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df5e5-126">INPUTS</span></span>

### <span data-ttu-id="df5e5-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="df5e5-127">None</span></span>

## <span data-ttu-id="df5e5-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df5e5-128">OUTPUTS</span></span>

### <span data-ttu-id="df5e5-129">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="df5e5-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="df5e5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df5e5-130">NOTES</span></span>

## <span data-ttu-id="df5e5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df5e5-131">RELATED LINKS</span></span>
