---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928030"
---
# <span data-ttu-id="9eb7d-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="9eb7d-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="9eb7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9eb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb7d-103">Hämtar en agent för en elastisk Azure SQL-jobb</span><span class="sxs-lookup"><span data-stu-id="9eb7d-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="9eb7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9eb7d-104">SYNTAX</span></span>

### <span data-ttu-id="9eb7d-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9eb7d-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eb7d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9eb7d-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eb7d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9eb7d-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eb7d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9eb7d-108">DESCRIPTION</span></span>
<span data-ttu-id="9eb7d-109">Get-AzSqlElasticJobAgent-cmdleten får en eller flera elastiska jobb agenter</span><span class="sxs-lookup"><span data-stu-id="9eb7d-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="9eb7d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9eb7d-110">EXAMPLES</span></span>

### <span data-ttu-id="9eb7d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9eb7d-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="9eb7d-112">Hämtar en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="9eb7d-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="9eb7d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9eb7d-113">PARAMETERS</span></span>

### <span data-ttu-id="9eb7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb7d-114">-DefaultProfile</span></span>
<span data-ttu-id="9eb7d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb7d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eb7d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9eb7d-116">-Name</span></span>
<span data-ttu-id="9eb7d-117">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="9eb7d-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb7d-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9eb7d-118">-ParentObject</span></span>
<span data-ttu-id="9eb7d-119">Serverobjektet för servern</span><span class="sxs-lookup"><span data-stu-id="9eb7d-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb7d-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9eb7d-120">-ParentResourceId</span></span>
<span data-ttu-id="9eb7d-121">Server resurs-ID</span><span class="sxs-lookup"><span data-stu-id="9eb7d-121">The server resource id</span></span>

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

### <span data-ttu-id="9eb7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9eb7d-123">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="9eb7d-123">The resource group name</span></span>

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

### <span data-ttu-id="9eb7d-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9eb7d-124">-ServerName</span></span>
<span data-ttu-id="9eb7d-125">Server namnet</span><span class="sxs-lookup"><span data-stu-id="9eb7d-125">The server name</span></span>

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

### <span data-ttu-id="9eb7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb7d-126">CommonParameters</span></span>
<span data-ttu-id="9eb7d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb7d-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9eb7d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb7d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9eb7d-129">INPUTS</span></span>

### <span data-ttu-id="9eb7d-130">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="9eb7d-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="9eb7d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9eb7d-131">OUTPUTS</span></span>

### <span data-ttu-id="9eb7d-132">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="9eb7d-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9eb7d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9eb7d-133">NOTES</span></span>

## <span data-ttu-id="9eb7d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9eb7d-134">RELATED LINKS</span></span>
