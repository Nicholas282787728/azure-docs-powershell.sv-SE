---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259835"
---
# <span data-ttu-id="53874-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="53874-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="53874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53874-102">SYNOPSIS</span></span>
<span data-ttu-id="53874-103">Startar ett jobb och returnerar ett ID för jobb körning som kan avsökas för att visa att det är status</span><span class="sxs-lookup"><span data-stu-id="53874-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="53874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53874-104">SYNTAX</span></span>

### <span data-ttu-id="53874-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="53874-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53874-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="53874-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53874-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53874-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53874-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53874-108">DESCRIPTION</span></span>
<span data-ttu-id="53874-109">Start-AzSqlElasticJob-cmdleten startar ett jobb som returnerar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="53874-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="53874-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53874-110">EXAMPLES</span></span>

### <span data-ttu-id="53874-111">Exempel 1 – startar ett jobb som returnerar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="53874-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="53874-112">Startar ett jobb som returnerar ett nytt jobb</span><span class="sxs-lookup"><span data-stu-id="53874-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="53874-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53874-113">PARAMETERS</span></span>

### <span data-ttu-id="53874-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="53874-114">-AgentName</span></span>
<span data-ttu-id="53874-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="53874-115">The agent name</span></span>

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

### <span data-ttu-id="53874-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53874-116">-AsJob</span></span>
<span data-ttu-id="53874-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="53874-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53874-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53874-118">-DefaultProfile</span></span>
<span data-ttu-id="53874-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53874-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53874-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="53874-120">-JobName</span></span>
<span data-ttu-id="53874-121">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="53874-121">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53874-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="53874-122">-ParentObject</span></span>
<span data-ttu-id="53874-123">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="53874-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53874-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="53874-124">-ParentResourceId</span></span>
<span data-ttu-id="53874-125">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="53874-125">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53874-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53874-126">-ResourceGroupName</span></span>
<span data-ttu-id="53874-127">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="53874-127">The resource group name</span></span>

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

### <span data-ttu-id="53874-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="53874-128">-ServerName</span></span>
<span data-ttu-id="53874-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="53874-129">The server name</span></span>

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

### <span data-ttu-id="53874-130">-Vänta</span><span class="sxs-lookup"><span data-stu-id="53874-130">-Wait</span></span>
<span data-ttu-id="53874-131">Flaggan wait för att indikera att vänta tills jobbets utförande är klar</span><span class="sxs-lookup"><span data-stu-id="53874-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="53874-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53874-132">-Confirm</span></span>
<span data-ttu-id="53874-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53874-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53874-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53874-134">-WhatIf</span></span>
<span data-ttu-id="53874-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53874-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53874-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53874-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53874-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53874-137">CommonParameters</span></span>
<span data-ttu-id="53874-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53874-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53874-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53874-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53874-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53874-140">INPUTS</span></span>

### <span data-ttu-id="53874-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="53874-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="53874-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53874-142">OUTPUTS</span></span>

### <span data-ttu-id="53874-143">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="53874-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="53874-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53874-144">NOTES</span></span>

## <span data-ttu-id="53874-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53874-145">RELATED LINKS</span></span>
