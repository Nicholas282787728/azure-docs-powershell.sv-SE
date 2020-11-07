---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 16899acb35270e01b80e267aab6fe6ab03827c02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920365"
---
# <span data-ttu-id="b4c0f-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="b4c0f-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="b4c0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c0f-103">Får ett eller flera jobb steg</span><span class="sxs-lookup"><span data-stu-id="b4c0f-103">Gets one or more job steps</span></span>

## <span data-ttu-id="b4c0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4c0f-104">SYNTAX</span></span>

### <span data-ttu-id="b4c0f-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b4c0f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c0f-106">Version</span><span class="sxs-lookup"><span data-stu-id="b4c0f-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4c0f-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4c0f-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c0f-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="b4c0f-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c0f-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4c0f-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4c0f-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b4c0f-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4c0f-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4c0f-111">DESCRIPTION</span></span>
<span data-ttu-id="b4c0f-112">Med Get-AzSqlElasticJobStep cmdlet hämtas en eller flera jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="b4c0f-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="b4c0f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4c0f-113">EXAMPLES</span></span>

### <span data-ttu-id="b4c0f-114">Exempel 1-hämtar ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="b4c0f-114">Example 1 - Gets a job step from a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="b4c0f-115">Hämtar ett jobb steg från ett jobb</span><span class="sxs-lookup"><span data-stu-id="b4c0f-115">Gets a job step from a job</span></span>

## <span data-ttu-id="b4c0f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4c0f-116">PARAMETERS</span></span>

### <span data-ttu-id="b4c0f-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b4c0f-117">-AgentName</span></span>
<span data-ttu-id="b4c0f-118">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="b4c0f-118">The agent name</span></span>

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

### <span data-ttu-id="b4c0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c0f-119">-DefaultProfile</span></span>
<span data-ttu-id="b4c0f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4c0f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c0f-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="b4c0f-121">-JobName</span></span>
<span data-ttu-id="b4c0f-122">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="b4c0f-122">The job name</span></span>

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

### <span data-ttu-id="b4c0f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4c0f-123">-Name</span></span>
<span data-ttu-id="b4c0f-124">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="b4c0f-124">The job step name</span></span>

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

### <span data-ttu-id="b4c0f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4c0f-125">-ParentObject</span></span>
<span data-ttu-id="b4c0f-126">Jobbobjektet</span><span class="sxs-lookup"><span data-stu-id="b4c0f-126">The job input object</span></span>

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

### <span data-ttu-id="b4c0f-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b4c0f-127">-ParentResourceId</span></span>
<span data-ttu-id="b4c0f-128">Jobb resurs-ID</span><span class="sxs-lookup"><span data-stu-id="b4c0f-128">The job resource id</span></span>

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

### <span data-ttu-id="b4c0f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c0f-129">-ResourceGroupName</span></span>
<span data-ttu-id="b4c0f-130">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="b4c0f-130">The resource group name</span></span>

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

### <span data-ttu-id="b4c0f-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4c0f-131">-ServerName</span></span>
<span data-ttu-id="b4c0f-132">Server namnet</span><span class="sxs-lookup"><span data-stu-id="b4c0f-132">The server name</span></span>

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

### <span data-ttu-id="b4c0f-133">-Version</span><span class="sxs-lookup"><span data-stu-id="b4c0f-133">-Version</span></span>
<span data-ttu-id="b4c0f-134">Namn på projekt steget</span><span class="sxs-lookup"><span data-stu-id="b4c0f-134">The job step name</span></span>

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

### <span data-ttu-id="b4c0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c0f-135">CommonParameters</span></span>
<span data-ttu-id="b4c0f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4c0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c0f-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4c0f-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c0f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4c0f-138">INPUTS</span></span>

### <span data-ttu-id="b4c0f-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="b4c0f-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="b4c0f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4c0f-140">OUTPUTS</span></span>

### <span data-ttu-id="b4c0f-141">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="b4c0f-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b4c0f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4c0f-142">NOTES</span></span>

## <span data-ttu-id="b4c0f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4c0f-143">RELATED LINKS</span></span>
