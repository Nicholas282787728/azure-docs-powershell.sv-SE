---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: c24793273e4da59b487702fb4d147bb6a7fb3ecb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269072"
---
# <span data-ttu-id="6df3a-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6df3a-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="6df3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6df3a-102">SYNOPSIS</span></span>
<span data-ttu-id="6df3a-103">Får ett eller flera jobb</span><span class="sxs-lookup"><span data-stu-id="6df3a-103">Gets one or more jobs</span></span>

## <span data-ttu-id="6df3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6df3a-104">SYNTAX</span></span>

### <span data-ttu-id="6df3a-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6df3a-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6df3a-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6df3a-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6df3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6df3a-108">DESCRIPTION</span></span>
<span data-ttu-id="6df3a-109">Get-AzSqlElasticJob-cmdleten får ett eller flera jobb</span><span class="sxs-lookup"><span data-stu-id="6df3a-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="6df3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6df3a-110">EXAMPLES</span></span>

### <span data-ttu-id="6df3a-111">Exempel 1: hämtar ett jobb</span><span class="sxs-lookup"><span data-stu-id="6df3a-111">Example 1: Gets a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="6df3a-112">Hämtar ett jobb</span><span class="sxs-lookup"><span data-stu-id="6df3a-112">Gets a job</span></span>

### <span data-ttu-id="6df3a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6df3a-113">Example 2</span></span>

<span data-ttu-id="6df3a-114">Får ett eller flera jobb.</span><span class="sxs-lookup"><span data-stu-id="6df3a-114">Gets one or more jobs.</span></span> <span data-ttu-id="6df3a-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="6df3a-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJob -AgentName agent -Name job1 -ResourceGroupName rg -ServerName elasticjobserver
```

## <span data-ttu-id="6df3a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6df3a-116">PARAMETERS</span></span>

### <span data-ttu-id="6df3a-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6df3a-117">-AgentName</span></span>
<span data-ttu-id="6df3a-118">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="6df3a-118">The agent name</span></span>

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

### <span data-ttu-id="6df3a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df3a-119">-DefaultProfile</span></span>
<span data-ttu-id="6df3a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6df3a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df3a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6df3a-121">-Name</span></span>
<span data-ttu-id="6df3a-122">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="6df3a-122">The job name</span></span>

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

### <span data-ttu-id="6df3a-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6df3a-123">-ParentObject</span></span>
<span data-ttu-id="6df3a-124">Agent-indatavärdet</span><span class="sxs-lookup"><span data-stu-id="6df3a-124">The agent input object</span></span>

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

### <span data-ttu-id="6df3a-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6df3a-125">-ParentResourceId</span></span>
<span data-ttu-id="6df3a-126">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="6df3a-126">The agent resource id</span></span>

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

### <span data-ttu-id="6df3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="6df3a-128">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="6df3a-128">The resource group name</span></span>

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

### <span data-ttu-id="6df3a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6df3a-129">-ServerName</span></span>
<span data-ttu-id="6df3a-130">Server namnet</span><span class="sxs-lookup"><span data-stu-id="6df3a-130">The server name</span></span>

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

### <span data-ttu-id="6df3a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df3a-131">CommonParameters</span></span>
<span data-ttu-id="6df3a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df3a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df3a-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6df3a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df3a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6df3a-134">INPUTS</span></span>

### <span data-ttu-id="6df3a-135">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="6df3a-135">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="6df3a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6df3a-136">OUTPUTS</span></span>

### <span data-ttu-id="6df3a-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6df3a-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6df3a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6df3a-138">NOTES</span></span>

## <span data-ttu-id="6df3a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6df3a-139">RELATED LINKS</span></span>