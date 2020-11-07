---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 80835d33f75517bea6a91e65f110f441d20ab59c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920474"
---
# <span data-ttu-id="df067-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="df067-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="df067-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df067-102">SYNOPSIS</span></span>
<span data-ttu-id="df067-103">Hämtar en agent för en elastisk Azure SQL-jobb</span><span class="sxs-lookup"><span data-stu-id="df067-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="df067-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df067-104">SYNTAX</span></span>

### <span data-ttu-id="df067-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="df067-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df067-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="df067-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df067-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df067-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df067-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df067-108">DESCRIPTION</span></span>
<span data-ttu-id="df067-109">Get-AzSqlElasticJobAgent-cmdleten får en eller flera elastiska jobb agenter</span><span class="sxs-lookup"><span data-stu-id="df067-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="df067-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df067-110">EXAMPLES</span></span>

### <span data-ttu-id="df067-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="df067-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="df067-112">Hämtar en elastisk jobb agent</span><span class="sxs-lookup"><span data-stu-id="df067-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="df067-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df067-113">PARAMETERS</span></span>

### <span data-ttu-id="df067-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df067-114">-DefaultProfile</span></span>
<span data-ttu-id="df067-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df067-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df067-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="df067-116">-Name</span></span>
<span data-ttu-id="df067-117">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="df067-117">The agent name</span></span>

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

### <span data-ttu-id="df067-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df067-118">-ParentObject</span></span>
<span data-ttu-id="df067-119">Serverobjektet för servern</span><span class="sxs-lookup"><span data-stu-id="df067-119">The server input object</span></span>

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

### <span data-ttu-id="df067-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="df067-120">-ParentResourceId</span></span>
<span data-ttu-id="df067-121">Server resurs-ID</span><span class="sxs-lookup"><span data-stu-id="df067-121">The server resource id</span></span>

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

### <span data-ttu-id="df067-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df067-122">-ResourceGroupName</span></span>
<span data-ttu-id="df067-123">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="df067-123">The resource group name</span></span>

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

### <span data-ttu-id="df067-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df067-124">-ServerName</span></span>
<span data-ttu-id="df067-125">Server namnet</span><span class="sxs-lookup"><span data-stu-id="df067-125">The server name</span></span>

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

### <span data-ttu-id="df067-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df067-126">CommonParameters</span></span>
<span data-ttu-id="df067-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df067-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df067-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df067-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df067-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df067-129">INPUTS</span></span>

### <span data-ttu-id="df067-130">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="df067-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="df067-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df067-131">OUTPUTS</span></span>

### <span data-ttu-id="df067-132">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="df067-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="df067-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df067-133">NOTES</span></span>

## <span data-ttu-id="df067-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df067-134">RELATED LINKS</span></span>
