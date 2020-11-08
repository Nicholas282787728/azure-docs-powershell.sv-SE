---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090916"
---
# <span data-ttu-id="51b6a-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="51b6a-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="51b6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="51b6a-103">Tar bort agenten för elastiska jobb</span><span class="sxs-lookup"><span data-stu-id="51b6a-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="51b6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51b6a-104">SYNTAX</span></span>

### <span data-ttu-id="51b6a-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51b6a-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b6a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="51b6a-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b6a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="51b6a-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51b6a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51b6a-108">DESCRIPTION</span></span>
<span data-ttu-id="51b6a-109">Remove-AzSqlElasticJobAgent-cmdleten tar bort en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="51b6a-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="51b6a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51b6a-110">EXAMPLES</span></span>

### <span data-ttu-id="51b6a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51b6a-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="51b6a-112">Tar bort en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="51b6a-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="51b6a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51b6a-113">PARAMETERS</span></span>

### <span data-ttu-id="51b6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b6a-114">-DefaultProfile</span></span>
<span data-ttu-id="51b6a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51b6a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b6a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="51b6a-116">-Force</span></span>
<span data-ttu-id="51b6a-117">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="51b6a-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="51b6a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b6a-118">-InputObject</span></span>
<span data-ttu-id="51b6a-119">Agent-objektet</span><span class="sxs-lookup"><span data-stu-id="51b6a-119">The agent object</span></span>

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

### <span data-ttu-id="51b6a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="51b6a-120">-Name</span></span>
<span data-ttu-id="51b6a-121">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="51b6a-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="51b6a-123">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="51b6a-123">The resource group name</span></span>

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

### <span data-ttu-id="51b6a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b6a-124">-ResourceId</span></span>
<span data-ttu-id="51b6a-125">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="51b6a-125">The agent resource id</span></span>

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

### <span data-ttu-id="51b6a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51b6a-126">-ServerName</span></span>
<span data-ttu-id="51b6a-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="51b6a-127">The server name</span></span>

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

### <span data-ttu-id="51b6a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51b6a-128">-Confirm</span></span>
<span data-ttu-id="51b6a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51b6a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b6a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b6a-130">-WhatIf</span></span>
<span data-ttu-id="51b6a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51b6a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b6a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51b6a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b6a-133">CommonParameters</span></span>
<span data-ttu-id="51b6a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b6a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51b6a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b6a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51b6a-136">INPUTS</span></span>

### <span data-ttu-id="51b6a-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="51b6a-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="51b6a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51b6a-138">OUTPUTS</span></span>

### <span data-ttu-id="51b6a-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="51b6a-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="51b6a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51b6a-140">NOTES</span></span>

## <span data-ttu-id="51b6a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51b6a-141">RELATED LINKS</span></span>
