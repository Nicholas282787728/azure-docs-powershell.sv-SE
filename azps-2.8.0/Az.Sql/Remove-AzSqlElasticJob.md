---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: b758c3a76c27fb2a1f06c7b6c940d3c3a7ef1c11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920282"
---
# <span data-ttu-id="7e457-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="7e457-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="7e457-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e457-102">SYNOPSIS</span></span>
<span data-ttu-id="7e457-103">Tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="7e457-103">Removes a job</span></span>

## <span data-ttu-id="7e457-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e457-104">SYNTAX</span></span>

### <span data-ttu-id="7e457-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7e457-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e457-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7e457-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e457-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7e457-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e457-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e457-108">DESCRIPTION</span></span>
<span data-ttu-id="7e457-109">Remove-AzSqlElasticJob cmdlet tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="7e457-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="7e457-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e457-110">EXAMPLES</span></span>

### <span data-ttu-id="7e457-111">Exempel 1-tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="7e457-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="7e457-112">Tar bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="7e457-112">Removes a job</span></span>

## <span data-ttu-id="7e457-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e457-113">PARAMETERS</span></span>

### <span data-ttu-id="7e457-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7e457-114">-AgentName</span></span>
<span data-ttu-id="7e457-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="7e457-115">The agent name</span></span>

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

### <span data-ttu-id="7e457-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e457-116">-DefaultProfile</span></span>
<span data-ttu-id="7e457-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e457-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e457-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7e457-118">-Force</span></span>
<span data-ttu-id="7e457-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="7e457-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7e457-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e457-120">-InputObject</span></span>
<span data-ttu-id="7e457-121">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="7e457-121">The job input object</span></span>

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

### <span data-ttu-id="7e457-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e457-122">-Name</span></span>
<span data-ttu-id="7e457-123">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="7e457-123">The job name</span></span>

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

### <span data-ttu-id="7e457-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e457-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e457-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="7e457-125">The resource group name</span></span>

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

### <span data-ttu-id="7e457-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e457-126">-ResourceId</span></span>
<span data-ttu-id="7e457-127">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="7e457-127">The agent resource id</span></span>

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

### <span data-ttu-id="7e457-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e457-128">-ServerName</span></span>
<span data-ttu-id="7e457-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="7e457-129">The server name</span></span>

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

### <span data-ttu-id="7e457-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e457-130">-Confirm</span></span>
<span data-ttu-id="7e457-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e457-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e457-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e457-132">-WhatIf</span></span>
<span data-ttu-id="7e457-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e457-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e457-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e457-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e457-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e457-135">CommonParameters</span></span>
<span data-ttu-id="7e457-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e457-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e457-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e457-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e457-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e457-138">INPUTS</span></span>

### <span data-ttu-id="7e457-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7e457-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7e457-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e457-140">OUTPUTS</span></span>

### <span data-ttu-id="7e457-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7e457-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7e457-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e457-142">NOTES</span></span>

## <span data-ttu-id="7e457-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e457-143">RELATED LINKS</span></span>
