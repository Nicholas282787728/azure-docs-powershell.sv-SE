---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271516"
---
# <span data-ttu-id="b6e6b-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="b6e6b-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="b6e6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e6b-103">Stoppar ett jobb får det jobb körnings-ID</span><span class="sxs-lookup"><span data-stu-id="b6e6b-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="b6e6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6e6b-104">SYNTAX</span></span>

### <span data-ttu-id="b6e6b-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b6e6b-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6e6b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6e6b-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6e6b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6e6b-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6e6b-108">DESCRIPTION</span></span>
<span data-ttu-id="b6e6b-109">Stop-AzSqlElasticJob-cmdleten stoppar ett jobb med pågående körning.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="b6e6b-110">Returnerar aktuell status för jobb körningen</span><span class="sxs-lookup"><span data-stu-id="b6e6b-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="b6e6b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-111">EXAMPLES</span></span>

### <span data-ttu-id="b6e6b-112">Exempel 1: stoppar ett jobb med körnings jobb</span><span class="sxs-lookup"><span data-stu-id="b6e6b-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="b6e6b-113">Stoppar en pågående jobb körning och returnerar den aktuella statusen</span><span class="sxs-lookup"><span data-stu-id="b6e6b-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="b6e6b-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b6e6b-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="b6e6b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6e6b-115">PARAMETERS</span></span>

### <span data-ttu-id="b6e6b-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b6e6b-116">-AgentName</span></span>
<span data-ttu-id="b6e6b-117">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="b6e6b-117">The agent name</span></span>

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

### <span data-ttu-id="b6e6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e6b-118">-DefaultProfile</span></span>
<span data-ttu-id="b6e6b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e6b-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="b6e6b-120">-JobExecutionId</span></span>
<span data-ttu-id="b6e6b-121">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-121">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e6b-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="b6e6b-122">-JobName</span></span>
<span data-ttu-id="b6e6b-123">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="b6e6b-123">The job name</span></span>

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

### <span data-ttu-id="b6e6b-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b6e6b-124">-ParentObject</span></span>
<span data-ttu-id="b6e6b-125">Serverobjektet för agent kontroll</span><span class="sxs-lookup"><span data-stu-id="b6e6b-125">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e6b-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e6b-126">-ParentResourceId</span></span>
<span data-ttu-id="b6e6b-127">Resurs-ID för jobb körning</span><span class="sxs-lookup"><span data-stu-id="b6e6b-127">The job execution resource id</span></span>

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

### <span data-ttu-id="b6e6b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e6b-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6e6b-129">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="b6e6b-129">The resource group name</span></span>

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

### <span data-ttu-id="b6e6b-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6e6b-130">-ServerName</span></span>
<span data-ttu-id="b6e6b-131">Server namnet</span><span class="sxs-lookup"><span data-stu-id="b6e6b-131">The server name</span></span>

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

### <span data-ttu-id="b6e6b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6e6b-132">-Confirm</span></span>
<span data-ttu-id="b6e6b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6e6b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e6b-134">-WhatIf</span></span>
<span data-ttu-id="b6e6b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e6b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6e6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e6b-137">CommonParameters</span></span>
<span data-ttu-id="b6e6b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e6b-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6e6b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e6b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6e6b-140">INPUTS</span></span>

### <span data-ttu-id="b6e6b-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="b6e6b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b6e6b-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6e6b-142">OUTPUTS</span></span>

### <span data-ttu-id="b6e6b-143">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="b6e6b-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b6e6b-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6e6b-144">NOTES</span></span>

## <span data-ttu-id="b6e6b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6e6b-145">RELATED LINKS</span></span>