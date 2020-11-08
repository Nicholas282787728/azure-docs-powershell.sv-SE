---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091982"
---
# <span data-ttu-id="fdbc6-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="fdbc6-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="fdbc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbc6-103">Skapar en ny mål grupp</span><span class="sxs-lookup"><span data-stu-id="fdbc6-103">Creates a new target group</span></span>

## <span data-ttu-id="fdbc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdbc6-104">SYNTAX</span></span>

### <span data-ttu-id="fdbc6-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fdbc6-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdbc6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fdbc6-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdbc6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fdbc6-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdbc6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdbc6-108">DESCRIPTION</span></span>
<span data-ttu-id="fdbc6-109">New-AzSqlElasticJobTargetGroup cmdlet skapar en ny mål grupp</span><span class="sxs-lookup"><span data-stu-id="fdbc6-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="fdbc6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdbc6-110">EXAMPLES</span></span>

### <span data-ttu-id="fdbc6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fdbc6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="fdbc6-112">Skapar en tom mål grupp</span><span class="sxs-lookup"><span data-stu-id="fdbc6-112">Creates an empty target group</span></span>

## <span data-ttu-id="fdbc6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdbc6-113">PARAMETERS</span></span>

### <span data-ttu-id="fdbc6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fdbc6-114">-AgentName</span></span>
<span data-ttu-id="fdbc6-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="fdbc6-115">The agent name</span></span>

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

### <span data-ttu-id="fdbc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbc6-116">-DefaultProfile</span></span>
<span data-ttu-id="fdbc6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fdbc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdbc6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdbc6-118">-Name</span></span>
<span data-ttu-id="fdbc6-119">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="fdbc6-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdbc6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fdbc6-120">-ParentObject</span></span>
<span data-ttu-id="fdbc6-121">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="fdbc6-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbc6-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fdbc6-122">-ParentResourceId</span></span>
<span data-ttu-id="fdbc6-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="fdbc6-123">The agent resource id</span></span>

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

### <span data-ttu-id="fdbc6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdbc6-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdbc6-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="fdbc6-125">The resource group name</span></span>

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

### <span data-ttu-id="fdbc6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fdbc6-126">-ServerName</span></span>
<span data-ttu-id="fdbc6-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="fdbc6-127">The server name</span></span>

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

### <span data-ttu-id="fdbc6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fdbc6-128">-Confirm</span></span>
<span data-ttu-id="fdbc6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fdbc6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdbc6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdbc6-130">-WhatIf</span></span>
<span data-ttu-id="fdbc6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fdbc6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdbc6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fdbc6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdbc6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbc6-133">CommonParameters</span></span>
<span data-ttu-id="fdbc6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdbc6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbc6-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdbc6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbc6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdbc6-136">INPUTS</span></span>

### <span data-ttu-id="fdbc6-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="fdbc6-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="fdbc6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdbc6-138">OUTPUTS</span></span>

### <span data-ttu-id="fdbc6-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="fdbc6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="fdbc6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdbc6-140">NOTES</span></span>

## <span data-ttu-id="fdbc6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdbc6-141">RELATED LINKS</span></span>