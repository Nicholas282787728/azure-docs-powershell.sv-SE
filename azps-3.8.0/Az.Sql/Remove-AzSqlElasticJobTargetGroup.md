---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: a20de2c2431e1ab6aea5da4d6dd61e6c745a3c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090189"
---
# <span data-ttu-id="c699e-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="c699e-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="c699e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c699e-102">SYNOPSIS</span></span>
<span data-ttu-id="c699e-103">Tar bort mål gruppen</span><span class="sxs-lookup"><span data-stu-id="c699e-103">Removes the target group</span></span>

## <span data-ttu-id="c699e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c699e-104">SYNTAX</span></span>

### <span data-ttu-id="c699e-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c699e-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c699e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c699e-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c699e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c699e-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c699e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c699e-108">DESCRIPTION</span></span>
<span data-ttu-id="c699e-109">Med den här Remove-AzSqlElasticJobTargetGroup cmdleten tas en mål grupp bort och dess mål</span><span class="sxs-lookup"><span data-stu-id="c699e-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="c699e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c699e-110">EXAMPLES</span></span>

### <span data-ttu-id="c699e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c699e-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="c699e-112">Tar bort en mål grupp och mål gruppen</span><span class="sxs-lookup"><span data-stu-id="c699e-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="c699e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c699e-113">PARAMETERS</span></span>

### <span data-ttu-id="c699e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c699e-114">-AgentName</span></span>
<span data-ttu-id="c699e-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="c699e-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c699e-116">-DefaultProfile</span></span>
<span data-ttu-id="c699e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c699e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c699e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c699e-118">-Force</span></span>
<span data-ttu-id="c699e-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="c699e-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c699e-120">-InputObject</span></span>
<span data-ttu-id="c699e-121">Mål grupps objekt</span><span class="sxs-lookup"><span data-stu-id="c699e-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c699e-122">-Name</span></span>
<span data-ttu-id="c699e-123">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="c699e-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c699e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c699e-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="c699e-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c699e-126">-ResourceId</span></span>
<span data-ttu-id="c699e-127">Resurs-ID för mål grupp</span><span class="sxs-lookup"><span data-stu-id="c699e-127">The target group resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c699e-128">-ServerName</span></span>
<span data-ttu-id="c699e-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="c699e-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c699e-130">-Confirm</span></span>
<span data-ttu-id="c699e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c699e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c699e-132">-WhatIf</span></span>
<span data-ttu-id="c699e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c699e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c699e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c699e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c699e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c699e-135">CommonParameters</span></span>
<span data-ttu-id="c699e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c699e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c699e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c699e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c699e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c699e-138">INPUTS</span></span>

### <span data-ttu-id="c699e-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="c699e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="c699e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c699e-140">OUTPUTS</span></span>

### <span data-ttu-id="c699e-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="c699e-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="c699e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c699e-142">NOTES</span></span>

## <span data-ttu-id="c699e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c699e-143">RELATED LINKS</span></span>
