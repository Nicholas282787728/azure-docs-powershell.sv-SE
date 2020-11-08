---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259043"
---
# <span data-ttu-id="38bb1-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="38bb1-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="38bb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="38bb1-103">Tar bort jobb steget</span><span class="sxs-lookup"><span data-stu-id="38bb1-103">Removes the job step</span></span>

## <span data-ttu-id="38bb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38bb1-104">SYNTAX</span></span>

### <span data-ttu-id="38bb1-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="38bb1-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38bb1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="38bb1-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bb1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38bb1-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bb1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38bb1-108">DESCRIPTION</span></span>
<span data-ttu-id="38bb1-109">Remove-AzSqlElasticJobStep cmdlet tar bort ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="38bb1-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="38bb1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38bb1-110">EXAMPLES</span></span>

### <span data-ttu-id="38bb1-111">Exempel 1: tar bort ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="38bb1-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="38bb1-112">Tar bort ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="38bb1-112">Removes a job step from a job</span></span>

### <span data-ttu-id="38bb1-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="38bb1-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="38bb1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38bb1-114">PARAMETERS</span></span>

### <span data-ttu-id="38bb1-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="38bb1-115">-AgentName</span></span>
<span data-ttu-id="38bb1-116">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="38bb1-116">The agent name</span></span>

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

### <span data-ttu-id="38bb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bb1-117">-DefaultProfile</span></span>
<span data-ttu-id="38bb1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="38bb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38bb1-119">-InputObject</span></span>
<span data-ttu-id="38bb1-120">Jobbobjektet för jobb</span><span class="sxs-lookup"><span data-stu-id="38bb1-120">The job step input object</span></span>

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

### <span data-ttu-id="38bb1-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="38bb1-121">-JobName</span></span>
<span data-ttu-id="38bb1-122">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="38bb1-122">The job name</span></span>

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

### <span data-ttu-id="38bb1-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="38bb1-123">-Name</span></span>
<span data-ttu-id="38bb1-124">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="38bb1-124">The job step name</span></span>

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

### <span data-ttu-id="38bb1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bb1-125">-ResourceGroupName</span></span>
<span data-ttu-id="38bb1-126">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="38bb1-126">The resource group name</span></span>

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

### <span data-ttu-id="38bb1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38bb1-127">-ResourceId</span></span>
<span data-ttu-id="38bb1-128">Resurs-ID för jobb steg</span><span class="sxs-lookup"><span data-stu-id="38bb1-128">The job step resource id</span></span>

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

### <span data-ttu-id="38bb1-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38bb1-129">-ServerName</span></span>
<span data-ttu-id="38bb1-130">Server namnet</span><span class="sxs-lookup"><span data-stu-id="38bb1-130">The server name</span></span>

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

### <span data-ttu-id="38bb1-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38bb1-131">-Confirm</span></span>
<span data-ttu-id="38bb1-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38bb1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38bb1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bb1-133">-WhatIf</span></span>
<span data-ttu-id="38bb1-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38bb1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bb1-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38bb1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38bb1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bb1-136">CommonParameters</span></span>
<span data-ttu-id="38bb1-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bb1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bb1-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38bb1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bb1-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38bb1-139">INPUTS</span></span>

### <span data-ttu-id="38bb1-140">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="38bb1-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="38bb1-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38bb1-141">OUTPUTS</span></span>

### <span data-ttu-id="38bb1-142">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="38bb1-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="38bb1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38bb1-143">NOTES</span></span>

## <span data-ttu-id="38bb1-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38bb1-144">RELATED LINKS</span></span>
