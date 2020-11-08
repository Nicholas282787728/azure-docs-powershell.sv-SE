---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089241"
---
# <span data-ttu-id="7d505-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="7d505-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="7d505-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d505-102">SYNOPSIS</span></span>
<span data-ttu-id="7d505-103">Får ett eller flera jobb</span><span class="sxs-lookup"><span data-stu-id="7d505-103">Gets one or more jobs</span></span>

## <span data-ttu-id="7d505-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d505-104">SYNTAX</span></span>

### <span data-ttu-id="7d505-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7d505-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d505-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d505-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d505-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d505-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d505-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d505-108">DESCRIPTION</span></span>
<span data-ttu-id="7d505-109">Get-AzSqlElasticJob-cmdleten får ett eller flera jobb</span><span class="sxs-lookup"><span data-stu-id="7d505-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="7d505-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d505-110">EXAMPLES</span></span>

### <span data-ttu-id="7d505-111">Exempel 1-har ett jobb</span><span class="sxs-lookup"><span data-stu-id="7d505-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="7d505-112">Hämtar ett jobb</span><span class="sxs-lookup"><span data-stu-id="7d505-112">Gets a job</span></span>

## <span data-ttu-id="7d505-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d505-113">PARAMETERS</span></span>

### <span data-ttu-id="7d505-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7d505-114">-AgentName</span></span>
<span data-ttu-id="7d505-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="7d505-115">The agent name</span></span>

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

### <span data-ttu-id="7d505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d505-116">-DefaultProfile</span></span>
<span data-ttu-id="7d505-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d505-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d505-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d505-118">-Name</span></span>
<span data-ttu-id="7d505-119">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="7d505-119">The job name</span></span>

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

### <span data-ttu-id="7d505-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7d505-120">-ParentObject</span></span>
<span data-ttu-id="7d505-121">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="7d505-121">The agent input object</span></span>

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

### <span data-ttu-id="7d505-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7d505-122">-ParentResourceId</span></span>
<span data-ttu-id="7d505-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="7d505-123">The agent resource id</span></span>

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

### <span data-ttu-id="7d505-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d505-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d505-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="7d505-125">The resource group name</span></span>

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

### <span data-ttu-id="7d505-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7d505-126">-ServerName</span></span>
<span data-ttu-id="7d505-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="7d505-127">The server name</span></span>

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

### <span data-ttu-id="7d505-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d505-128">CommonParameters</span></span>
<span data-ttu-id="7d505-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d505-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d505-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d505-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d505-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d505-131">INPUTS</span></span>

### <span data-ttu-id="7d505-132">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7d505-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7d505-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d505-133">OUTPUTS</span></span>

### <span data-ttu-id="7d505-134">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7d505-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7d505-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d505-135">NOTES</span></span>

## <span data-ttu-id="7d505-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d505-136">RELATED LINKS</span></span>