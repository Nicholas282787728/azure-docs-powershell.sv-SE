---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090917"
---
# <span data-ttu-id="f1586-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="f1586-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="f1586-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1586-102">SYNOPSIS</span></span>
<span data-ttu-id="f1586-103">Tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="f1586-103">Removes a job</span></span>

## <span data-ttu-id="f1586-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1586-104">SYNTAX</span></span>

### <span data-ttu-id="f1586-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1586-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1586-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f1586-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1586-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f1586-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1586-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1586-108">DESCRIPTION</span></span>
<span data-ttu-id="f1586-109">Remove-AzSqlElasticJob cmdlet tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="f1586-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="f1586-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1586-110">EXAMPLES</span></span>

### <span data-ttu-id="f1586-111">Exempel 1-tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="f1586-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="f1586-112">Tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="f1586-112">Removes a job</span></span>

## <span data-ttu-id="f1586-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1586-113">PARAMETERS</span></span>

### <span data-ttu-id="f1586-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f1586-114">-AgentName</span></span>
<span data-ttu-id="f1586-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="f1586-115">The agent name</span></span>

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

### <span data-ttu-id="f1586-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1586-116">-DefaultProfile</span></span>
<span data-ttu-id="f1586-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1586-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1586-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f1586-118">-Force</span></span>
<span data-ttu-id="f1586-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="f1586-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f1586-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1586-120">-InputObject</span></span>
<span data-ttu-id="f1586-121">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="f1586-121">The job input object</span></span>

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

### <span data-ttu-id="f1586-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1586-122">-Name</span></span>
<span data-ttu-id="f1586-123">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="f1586-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1586-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1586-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1586-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="f1586-125">The resource group name</span></span>

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

### <span data-ttu-id="f1586-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1586-126">-ResourceId</span></span>
<span data-ttu-id="f1586-127">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="f1586-127">The agent resource id</span></span>

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

### <span data-ttu-id="f1586-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1586-128">-ServerName</span></span>
<span data-ttu-id="f1586-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="f1586-129">The server name</span></span>

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

### <span data-ttu-id="f1586-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1586-130">-Confirm</span></span>
<span data-ttu-id="f1586-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1586-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1586-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1586-132">-WhatIf</span></span>
<span data-ttu-id="f1586-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1586-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1586-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1586-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1586-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1586-135">CommonParameters</span></span>
<span data-ttu-id="f1586-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1586-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1586-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1586-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1586-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1586-138">INPUTS</span></span>

### <span data-ttu-id="f1586-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f1586-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f1586-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1586-140">OUTPUTS</span></span>

### <span data-ttu-id="f1586-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f1586-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f1586-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1586-142">NOTES</span></span>

## <span data-ttu-id="f1586-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1586-143">RELATED LINKS</span></span>
