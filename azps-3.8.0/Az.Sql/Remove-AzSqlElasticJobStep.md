---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: c0ebc561a047ffe6a62722012fd7ecd3d42e472a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090914"
---
# <span data-ttu-id="2b34e-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="2b34e-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="2b34e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b34e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b34e-103">Tar bort jobb steget</span><span class="sxs-lookup"><span data-stu-id="2b34e-103">Removes the job step</span></span>

## <span data-ttu-id="2b34e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b34e-104">SYNTAX</span></span>

### <span data-ttu-id="2b34e-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2b34e-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b34e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b34e-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b34e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b34e-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b34e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b34e-108">DESCRIPTION</span></span>
<span data-ttu-id="2b34e-109">Remove-AzSqlElasticJobStep cmdlet tar bort ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="2b34e-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="2b34e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b34e-110">EXAMPLES</span></span>

### <span data-ttu-id="2b34e-111">Exempel 1 – tar bort ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="2b34e-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="2b34e-112">Tar bort ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="2b34e-112">Removes a job step from a job</span></span>

## <span data-ttu-id="2b34e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b34e-113">PARAMETERS</span></span>

### <span data-ttu-id="2b34e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2b34e-114">-AgentName</span></span>
<span data-ttu-id="2b34e-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="2b34e-115">The agent name</span></span>

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

### <span data-ttu-id="2b34e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b34e-116">-DefaultProfile</span></span>
<span data-ttu-id="2b34e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b34e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b34e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b34e-118">-InputObject</span></span>
<span data-ttu-id="2b34e-119">Jobbobjektet för jobb</span><span class="sxs-lookup"><span data-stu-id="2b34e-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b34e-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="2b34e-120">-JobName</span></span>
<span data-ttu-id="2b34e-121">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="2b34e-121">The job name</span></span>

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

### <span data-ttu-id="2b34e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b34e-122">-Name</span></span>
<span data-ttu-id="2b34e-123">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="2b34e-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b34e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b34e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b34e-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="2b34e-125">The resource group name</span></span>

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

### <span data-ttu-id="2b34e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b34e-126">-ResourceId</span></span>
<span data-ttu-id="2b34e-127">Resurs-ID för jobb steg</span><span class="sxs-lookup"><span data-stu-id="2b34e-127">The job step resource id</span></span>

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

### <span data-ttu-id="2b34e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b34e-128">-ServerName</span></span>
<span data-ttu-id="2b34e-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="2b34e-129">The server name</span></span>

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

### <span data-ttu-id="2b34e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b34e-130">-Confirm</span></span>
<span data-ttu-id="2b34e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b34e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b34e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b34e-132">-WhatIf</span></span>
<span data-ttu-id="2b34e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b34e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b34e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b34e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b34e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b34e-135">CommonParameters</span></span>
<span data-ttu-id="2b34e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b34e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b34e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b34e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b34e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b34e-138">INPUTS</span></span>

### <span data-ttu-id="2b34e-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2b34e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2b34e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b34e-140">OUTPUTS</span></span>

### <span data-ttu-id="2b34e-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2b34e-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2b34e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b34e-142">NOTES</span></span>

## <span data-ttu-id="2b34e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b34e-143">RELATED LINKS</span></span>
