---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920674"
---
# <span data-ttu-id="10d8c-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="10d8c-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="10d8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="10d8c-103">Stoppar ett jobb får det jobb körnings-ID</span><span class="sxs-lookup"><span data-stu-id="10d8c-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="10d8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10d8c-104">SYNTAX</span></span>

### <span data-ttu-id="10d8c-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="10d8c-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10d8c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="10d8c-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10d8c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10d8c-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10d8c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10d8c-108">DESCRIPTION</span></span>
<span data-ttu-id="10d8c-109">Stop-AzSqlElasticJob-cmdleten stoppar ett jobb med pågående körning.</span><span class="sxs-lookup"><span data-stu-id="10d8c-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="10d8c-110">Returnerar aktuell status för jobb körningen</span><span class="sxs-lookup"><span data-stu-id="10d8c-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="10d8c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10d8c-111">EXAMPLES</span></span>

### <span data-ttu-id="10d8c-112">Exempel 1 – stoppar ett jobb med körnings jobb</span><span class="sxs-lookup"><span data-stu-id="10d8c-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="10d8c-113">Stoppar en pågående jobb körning och returnerar den aktuella statusen</span><span class="sxs-lookup"><span data-stu-id="10d8c-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="10d8c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10d8c-114">PARAMETERS</span></span>

### <span data-ttu-id="10d8c-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="10d8c-115">-AgentName</span></span>
<span data-ttu-id="10d8c-116">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="10d8c-116">The agent name</span></span>

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

### <span data-ttu-id="10d8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d8c-117">-DefaultProfile</span></span>
<span data-ttu-id="10d8c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10d8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d8c-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="10d8c-119">-JobExecutionId</span></span>
<span data-ttu-id="10d8c-120">Kör-ID för jobb.</span><span class="sxs-lookup"><span data-stu-id="10d8c-120">The job execution id.</span></span>

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

### <span data-ttu-id="10d8c-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="10d8c-121">-JobName</span></span>
<span data-ttu-id="10d8c-122">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="10d8c-122">The job name</span></span>

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

### <span data-ttu-id="10d8c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="10d8c-123">-ParentObject</span></span>
<span data-ttu-id="10d8c-124">Serverobjektet för agent kontroll</span><span class="sxs-lookup"><span data-stu-id="10d8c-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="10d8c-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="10d8c-125">-ParentResourceId</span></span>
<span data-ttu-id="10d8c-126">Resurs-ID för jobb körning</span><span class="sxs-lookup"><span data-stu-id="10d8c-126">The job execution resource id</span></span>

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

### <span data-ttu-id="10d8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d8c-127">-ResourceGroupName</span></span>
<span data-ttu-id="10d8c-128">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="10d8c-128">The resource group name</span></span>

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

### <span data-ttu-id="10d8c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10d8c-129">-ServerName</span></span>
<span data-ttu-id="10d8c-130">Server namnet</span><span class="sxs-lookup"><span data-stu-id="10d8c-130">The server name</span></span>

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

### <span data-ttu-id="10d8c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10d8c-131">-Confirm</span></span>
<span data-ttu-id="10d8c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10d8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d8c-133">-WhatIf</span></span>
<span data-ttu-id="10d8c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10d8c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d8c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10d8c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d8c-136">CommonParameters</span></span>
<span data-ttu-id="10d8c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d8c-138">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10d8c-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d8c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10d8c-139">INPUTS</span></span>

### <span data-ttu-id="10d8c-140">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="10d8c-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="10d8c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10d8c-141">OUTPUTS</span></span>

### <span data-ttu-id="10d8c-142">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="10d8c-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="10d8c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10d8c-143">NOTES</span></span>

## <span data-ttu-id="10d8c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10d8c-144">RELATED LINKS</span></span>

## <span data-ttu-id="10d8c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10d8c-145">RELATED LINKS</span></span>
