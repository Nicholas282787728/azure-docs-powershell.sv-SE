---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319788"
---
# <span data-ttu-id="6f47c-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="6f47c-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="6f47c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f47c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f47c-103">Hämtar en eller flera jobb mål grupper</span><span class="sxs-lookup"><span data-stu-id="6f47c-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="6f47c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f47c-104">SYNTAX</span></span>

### <span data-ttu-id="6f47c-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f47c-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f47c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f47c-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f47c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f47c-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f47c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f47c-108">DESCRIPTION</span></span>
<span data-ttu-id="6f47c-109">Get-AzSqlElasticJobTargetGroup-cmdleten får en mål grupp och är mål</span><span class="sxs-lookup"><span data-stu-id="6f47c-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="6f47c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f47c-110">EXAMPLES</span></span>

### <span data-ttu-id="6f47c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f47c-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="6f47c-112">Hämtar en mål grupp och är mål</span><span class="sxs-lookup"><span data-stu-id="6f47c-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="6f47c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f47c-113">PARAMETERS</span></span>

### <span data-ttu-id="6f47c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6f47c-114">-AgentName</span></span>
<span data-ttu-id="6f47c-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="6f47c-115">The agent name</span></span>

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

### <span data-ttu-id="6f47c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f47c-116">-DefaultProfile</span></span>
<span data-ttu-id="6f47c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f47c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f47c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f47c-118">-Name</span></span>
<span data-ttu-id="6f47c-119">Namnet på mål gruppen</span><span class="sxs-lookup"><span data-stu-id="6f47c-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f47c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f47c-120">-ParentObject</span></span>
<span data-ttu-id="6f47c-121">Agent-objektet</span><span class="sxs-lookup"><span data-stu-id="6f47c-121">The agent object</span></span>

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

### <span data-ttu-id="6f47c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6f47c-122">-ParentResourceId</span></span>
<span data-ttu-id="6f47c-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="6f47c-123">The agent resource id</span></span>

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

### <span data-ttu-id="6f47c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f47c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f47c-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="6f47c-125">The resource group name</span></span>

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

### <span data-ttu-id="6f47c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f47c-126">-ServerName</span></span>
<span data-ttu-id="6f47c-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="6f47c-127">The server name</span></span>

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

### <span data-ttu-id="6f47c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f47c-128">CommonParameters</span></span>
<span data-ttu-id="6f47c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f47c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f47c-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f47c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f47c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f47c-131">INPUTS</span></span>

### <span data-ttu-id="6f47c-132">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="6f47c-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="6f47c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f47c-133">OUTPUTS</span></span>

### <span data-ttu-id="6f47c-134">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="6f47c-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="6f47c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f47c-135">NOTES</span></span>

## <span data-ttu-id="6f47c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f47c-136">RELATED LINKS</span></span>
