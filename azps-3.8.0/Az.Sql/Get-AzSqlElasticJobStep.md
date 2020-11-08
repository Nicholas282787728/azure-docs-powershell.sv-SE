---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 2b202fd2cff8ae12425c1e41807126798eb9944e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928017"
---
# <span data-ttu-id="3c2a1-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="3c2a1-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="3c2a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c2a1-103">Får ett eller flera jobb steg</span><span class="sxs-lookup"><span data-stu-id="3c2a1-103">Gets one or more job steps</span></span>

## <span data-ttu-id="3c2a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c2a1-104">SYNTAX</span></span>

### <span data-ttu-id="3c2a1-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3c2a1-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c2a1-106">Version</span><span class="sxs-lookup"><span data-stu-id="3c2a1-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c2a1-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c2a1-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c2a1-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="3c2a1-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c2a1-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3c2a1-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c2a1-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3c2a1-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c2a1-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c2a1-111">DESCRIPTION</span></span>
<span data-ttu-id="3c2a1-112">Med Get-AzSqlElasticJobStep cmdlet hämtas en eller flera jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="3c2a1-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="3c2a1-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c2a1-113">EXAMPLES</span></span>

### <span data-ttu-id="3c2a1-114">Exempel 1-hämtar ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="3c2a1-114">Example 1 - Gets a job step from a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="3c2a1-115">Hämtar ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="3c2a1-115">Gets a job step from a job</span></span>

## <span data-ttu-id="3c2a1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c2a1-116">PARAMETERS</span></span>

### <span data-ttu-id="3c2a1-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3c2a1-117">-AgentName</span></span>
<span data-ttu-id="3c2a1-118">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="3c2a1-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c2a1-119">-DefaultProfile</span></span>
<span data-ttu-id="3c2a1-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c2a1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c2a1-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="3c2a1-121">-JobName</span></span>
<span data-ttu-id="3c2a1-122">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="3c2a1-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c2a1-123">-Name</span></span>
<span data-ttu-id="3c2a1-124">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="3c2a1-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3c2a1-125">-ParentObject</span></span>
<span data-ttu-id="3c2a1-126">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="3c2a1-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3c2a1-127">-ParentResourceId</span></span>
<span data-ttu-id="3c2a1-128">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3c2a1-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c2a1-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c2a1-130">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="3c2a1-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c2a1-131">-ServerName</span></span>
<span data-ttu-id="3c2a1-132">Server namnet</span><span class="sxs-lookup"><span data-stu-id="3c2a1-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-133">-Version</span><span class="sxs-lookup"><span data-stu-id="3c2a1-133">-Version</span></span>
<span data-ttu-id="3c2a1-134">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="3c2a1-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c2a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c2a1-135">CommonParameters</span></span>
<span data-ttu-id="3c2a1-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c2a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c2a1-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c2a1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c2a1-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c2a1-138">INPUTS</span></span>

### <span data-ttu-id="3c2a1-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="3c2a1-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="3c2a1-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c2a1-140">OUTPUTS</span></span>

### <span data-ttu-id="3c2a1-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="3c2a1-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="3c2a1-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c2a1-142">NOTES</span></span>

## <span data-ttu-id="3c2a1-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c2a1-143">RELATED LINKS</span></span>