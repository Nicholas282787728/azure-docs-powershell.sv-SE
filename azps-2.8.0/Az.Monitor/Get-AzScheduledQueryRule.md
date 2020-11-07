---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 86559299a4711d95e1b5c94c455bdbb841e141e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918619"
---
# <span data-ttu-id="ebed1-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ebed1-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="ebed1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebed1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebed1-103">Hämtar schemalagda frågor</span><span class="sxs-lookup"><span data-stu-id="ebed1-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="ebed1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebed1-104">SYNTAX</span></span>

### <span data-ttu-id="ebed1-105">BySubscriptionOrResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="ebed1-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebed1-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="ebed1-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebed1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebed1-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebed1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebed1-108">DESCRIPTION</span></span>
<span data-ttu-id="ebed1-109">Hämtar schemalagda frågor</span><span class="sxs-lookup"><span data-stu-id="ebed1-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="ebed1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebed1-110">EXAMPLES</span></span>

### <span data-ttu-id="ebed1-111">Exempel 1-lista efter abonnemang eller resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ebed1-111">Example 1 - List by subscription or resource group</span></span>
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

### <span data-ttu-id="ebed1-112">Exempel 2 – Hämta efter regel namn</span><span class="sxs-lookup"><span data-stu-id="ebed1-112">Example 2 - Get by rule name</span></span>
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

### <span data-ttu-id="ebed1-113">Exempel 3-Se resurs-ID</span><span class="sxs-lookup"><span data-stu-id="ebed1-113">Example 3 - Get by resource Id</span></span>
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

## <span data-ttu-id="ebed1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebed1-114">PARAMETERS</span></span>

### <span data-ttu-id="ebed1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebed1-115">-DefaultProfile</span></span>
<span data-ttu-id="ebed1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ebed1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebed1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ebed1-117">-Name</span></span>
<span data-ttu-id="ebed1-118">Namnet på notifieringsregeln</span><span class="sxs-lookup"><span data-stu-id="ebed1-118">The alert rule name</span></span>

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

### <span data-ttu-id="ebed1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebed1-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebed1-120">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="ebed1-120">The resource group name</span></span>

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

### <span data-ttu-id="ebed1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebed1-121">-ResourceId</span></span>
<span data-ttu-id="ebed1-122">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="ebed1-122">The resource Id</span></span>

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

### <span data-ttu-id="ebed1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebed1-123">CommonParameters</span></span>
<span data-ttu-id="ebed1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebed1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebed1-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebed1-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebed1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebed1-126">INPUTS</span></span>

### <span data-ttu-id="ebed1-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="ebed1-127">None</span></span>

## <span data-ttu-id="ebed1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebed1-128">OUTPUTS</span></span>

### <span data-ttu-id="ebed1-129">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ebed1-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="ebed1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebed1-130">NOTES</span></span>

## <span data-ttu-id="ebed1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebed1-131">RELATED LINKS</span></span>
