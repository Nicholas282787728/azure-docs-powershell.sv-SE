---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 688926d05b56234ce11d4524afdcce326c5e09e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920370"
---
# <span data-ttu-id="02219-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="02219-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="02219-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02219-102">SYNOPSIS</span></span>
<span data-ttu-id="02219-103">Får ett eller flera jobb</span><span class="sxs-lookup"><span data-stu-id="02219-103">Gets one or more jobs</span></span>

## <span data-ttu-id="02219-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02219-104">SYNTAX</span></span>

### <span data-ttu-id="02219-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="02219-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02219-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="02219-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02219-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="02219-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02219-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02219-108">DESCRIPTION</span></span>
<span data-ttu-id="02219-109">Get-AzSqlElasticJob-cmdleten får ett eller flera jobb</span><span class="sxs-lookup"><span data-stu-id="02219-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="02219-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02219-110">EXAMPLES</span></span>

### <span data-ttu-id="02219-111">Exempel 1-har ett jobb</span><span class="sxs-lookup"><span data-stu-id="02219-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="02219-112">Hämtar ett jobb</span><span class="sxs-lookup"><span data-stu-id="02219-112">Gets a job</span></span>

## <span data-ttu-id="02219-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02219-113">PARAMETERS</span></span>

### <span data-ttu-id="02219-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="02219-114">-AgentName</span></span>
<span data-ttu-id="02219-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="02219-115">The agent name</span></span>

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

### <span data-ttu-id="02219-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02219-116">-DefaultProfile</span></span>
<span data-ttu-id="02219-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02219-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02219-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="02219-118">-Name</span></span>
<span data-ttu-id="02219-119">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="02219-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02219-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02219-120">-ParentObject</span></span>
<span data-ttu-id="02219-121">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="02219-121">The agent input object</span></span>

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

### <span data-ttu-id="02219-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="02219-122">-ParentResourceId</span></span>
<span data-ttu-id="02219-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="02219-123">The agent resource id</span></span>

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

### <span data-ttu-id="02219-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02219-124">-ResourceGroupName</span></span>
<span data-ttu-id="02219-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="02219-125">The resource group name</span></span>

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

### <span data-ttu-id="02219-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02219-126">-ServerName</span></span>
<span data-ttu-id="02219-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="02219-127">The server name</span></span>

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

### <span data-ttu-id="02219-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02219-128">CommonParameters</span></span>
<span data-ttu-id="02219-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02219-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02219-130">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02219-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02219-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02219-131">INPUTS</span></span>

### <span data-ttu-id="02219-132">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="02219-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="02219-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02219-133">OUTPUTS</span></span>

### <span data-ttu-id="02219-134">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="02219-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="02219-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02219-135">NOTES</span></span>

## <span data-ttu-id="02219-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02219-136">RELATED LINKS</span></span>
