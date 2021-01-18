---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522250"
---
# <span data-ttu-id="fa9e1-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="fa9e1-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="fa9e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9e1-103">Skapar en ny elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="fa9e1-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="fa9e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa9e1-104">SYNTAX</span></span>

### <span data-ttu-id="fa9e1-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fa9e1-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa9e1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa9e1-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9e1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa9e1-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9e1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa9e1-108">DESCRIPTION</span></span>
<span data-ttu-id="fa9e1-109">New-AzSqlElasticJobAgent-cmdleten skapar en ny elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="fa9e1-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="fa9e1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa9e1-110">EXAMPLES</span></span>

### <span data-ttu-id="fa9e1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa9e1-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="fa9e1-112">Skapar en ny elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="fa9e1-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="fa9e1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa9e1-113">PARAMETERS</span></span>

### <span data-ttu-id="fa9e1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa9e1-114">-DatabaseName</span></span>
<span data-ttu-id="fa9e1-115">Databasens namn</span><span class="sxs-lookup"><span data-stu-id="fa9e1-115">The database name</span></span>

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

### <span data-ttu-id="fa9e1-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fa9e1-116">-DatabaseObject</span></span>
<span data-ttu-id="fa9e1-117">Serverobjektet för agent kontroll</span><span class="sxs-lookup"><span data-stu-id="fa9e1-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e1-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="fa9e1-118">-DatabaseResourceId</span></span>
<span data-ttu-id="fa9e1-119">Resurs-ID för agent kontroll databas</span><span class="sxs-lookup"><span data-stu-id="fa9e1-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="fa9e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9e1-120">-DefaultProfile</span></span>
<span data-ttu-id="fa9e1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa9e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa9e1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa9e1-122">-Name</span></span>
<span data-ttu-id="fa9e1-123">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="fa9e1-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa9e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa9e1-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="fa9e1-125">The resource group name</span></span>

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

### <span data-ttu-id="fa9e1-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa9e1-126">-ServerName</span></span>
<span data-ttu-id="fa9e1-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="fa9e1-127">The server name</span></span>

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

### <span data-ttu-id="fa9e1-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fa9e1-128">-Tag</span></span>
<span data-ttu-id="fa9e1-129">Agent-taggarna</span><span class="sxs-lookup"><span data-stu-id="fa9e1-129">The Agent Tags</span></span>

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

### <span data-ttu-id="fa9e1-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa9e1-130">-Confirm</span></span>
<span data-ttu-id="fa9e1-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa9e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9e1-132">-WhatIf</span></span>
<span data-ttu-id="fa9e1-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa9e1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9e1-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa9e1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9e1-135">CommonParameters</span></span>
<span data-ttu-id="fa9e1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa9e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9e1-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa9e1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9e1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa9e1-138">INPUTS</span></span>

### <span data-ttu-id="fa9e1-139">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fa9e1-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fa9e1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa9e1-140">OUTPUTS</span></span>

### <span data-ttu-id="fa9e1-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="fa9e1-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="fa9e1-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa9e1-142">NOTES</span></span>

## <span data-ttu-id="fa9e1-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa9e1-143">RELATED LINKS</span></span>
