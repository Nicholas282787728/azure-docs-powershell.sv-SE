---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103469"
---
# <span data-ttu-id="0256c-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="0256c-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="0256c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0256c-102">SYNOPSIS</span></span>
<span data-ttu-id="0256c-103">Skapar en ny mål grupp</span><span class="sxs-lookup"><span data-stu-id="0256c-103">Creates a new target group</span></span>

## <span data-ttu-id="0256c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0256c-104">SYNTAX</span></span>

### <span data-ttu-id="0256c-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0256c-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0256c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0256c-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0256c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0256c-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0256c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0256c-108">DESCRIPTION</span></span>
<span data-ttu-id="0256c-109">New-AzSqlElasticJobTargetGroup cmdlet skapar en ny mål grupp</span><span class="sxs-lookup"><span data-stu-id="0256c-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="0256c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0256c-110">EXAMPLES</span></span>

### <span data-ttu-id="0256c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0256c-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="0256c-112">Skapar en tom mål grupp</span><span class="sxs-lookup"><span data-stu-id="0256c-112">Creates an empty target group</span></span>

## <span data-ttu-id="0256c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0256c-113">PARAMETERS</span></span>

### <span data-ttu-id="0256c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0256c-114">-AgentName</span></span>
<span data-ttu-id="0256c-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="0256c-115">The agent name</span></span>

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

### <span data-ttu-id="0256c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0256c-116">-DefaultProfile</span></span>
<span data-ttu-id="0256c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0256c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0256c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="0256c-118">-Name</span></span>
<span data-ttu-id="0256c-119">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="0256c-119">The target group name</span></span>

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

### <span data-ttu-id="0256c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0256c-120">-ParentObject</span></span>
<span data-ttu-id="0256c-121">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="0256c-121">The agent input object</span></span>

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

### <span data-ttu-id="0256c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0256c-122">-ParentResourceId</span></span>
<span data-ttu-id="0256c-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="0256c-123">The agent resource id</span></span>

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

### <span data-ttu-id="0256c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0256c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0256c-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="0256c-125">The resource group name</span></span>

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

### <span data-ttu-id="0256c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0256c-126">-ServerName</span></span>
<span data-ttu-id="0256c-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="0256c-127">The server name</span></span>

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

### <span data-ttu-id="0256c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0256c-128">-Confirm</span></span>
<span data-ttu-id="0256c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0256c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0256c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0256c-130">-WhatIf</span></span>
<span data-ttu-id="0256c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0256c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0256c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0256c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0256c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0256c-133">CommonParameters</span></span>
<span data-ttu-id="0256c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0256c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0256c-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0256c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0256c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0256c-136">INPUTS</span></span>

### <span data-ttu-id="0256c-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="0256c-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0256c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0256c-138">OUTPUTS</span></span>

### <span data-ttu-id="0256c-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="0256c-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="0256c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0256c-140">NOTES</span></span>

## <span data-ttu-id="0256c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0256c-141">RELATED LINKS</span></span>
