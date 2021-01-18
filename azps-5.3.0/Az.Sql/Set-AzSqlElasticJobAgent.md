---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522806"
---
# <span data-ttu-id="75244-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="75244-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="75244-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75244-102">SYNOPSIS</span></span>
<span data-ttu-id="75244-103">Uppdaterar en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="75244-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="75244-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75244-104">SYNTAX</span></span>

### <span data-ttu-id="75244-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="75244-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75244-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="75244-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75244-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="75244-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75244-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75244-108">DESCRIPTION</span></span>
<span data-ttu-id="75244-109">Set-AzSqlElasticJobAgent cmdlet uppdaterar en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="75244-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="75244-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75244-110">EXAMPLES</span></span>

### <span data-ttu-id="75244-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75244-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="75244-112">Uppdaterar en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="75244-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="75244-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75244-113">PARAMETERS</span></span>

### <span data-ttu-id="75244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75244-114">-DefaultProfile</span></span>
<span data-ttu-id="75244-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75244-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75244-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75244-116">-InputObject</span></span>
<span data-ttu-id="75244-117">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="75244-117">The agent input object</span></span>

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

### <span data-ttu-id="75244-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="75244-118">-Name</span></span>
<span data-ttu-id="75244-119">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="75244-119">The agent name</span></span>

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

### <span data-ttu-id="75244-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75244-120">-ResourceGroupName</span></span>
<span data-ttu-id="75244-121">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="75244-121">The resource group name</span></span>

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

### <span data-ttu-id="75244-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75244-122">-ResourceId</span></span>
<span data-ttu-id="75244-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="75244-123">The agent resource id</span></span>

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

### <span data-ttu-id="75244-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="75244-124">-ServerName</span></span>
<span data-ttu-id="75244-125">Server namnet</span><span class="sxs-lookup"><span data-stu-id="75244-125">The server name</span></span>

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

### <span data-ttu-id="75244-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="75244-126">-Tag</span></span>
<span data-ttu-id="75244-127">De taggar som ska kopplas till Azure SQL Database-agenten</span><span class="sxs-lookup"><span data-stu-id="75244-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75244-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75244-128">-Confirm</span></span>
<span data-ttu-id="75244-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75244-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75244-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75244-130">-WhatIf</span></span>
<span data-ttu-id="75244-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75244-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75244-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75244-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75244-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75244-133">CommonParameters</span></span>
<span data-ttu-id="75244-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75244-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75244-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75244-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75244-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75244-136">INPUTS</span></span>

### <span data-ttu-id="75244-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="75244-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="75244-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75244-138">OUTPUTS</span></span>

### <span data-ttu-id="75244-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="75244-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="75244-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75244-140">NOTES</span></span>

## <span data-ttu-id="75244-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75244-141">RELATED LINKS</span></span>
