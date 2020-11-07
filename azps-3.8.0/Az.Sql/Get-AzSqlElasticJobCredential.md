---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928022"
---
# <span data-ttu-id="7d399-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="7d399-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="7d399-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d399-102">SYNOPSIS</span></span>
<span data-ttu-id="7d399-103">Får en eller flera autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="7d399-103">Gets one or more credentials</span></span>

## <span data-ttu-id="7d399-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d399-104">SYNTAX</span></span>

### <span data-ttu-id="7d399-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7d399-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d399-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d399-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d399-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d399-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d399-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d399-108">DESCRIPTION</span></span>
<span data-ttu-id="7d399-109">Get-AzSqlElasticJobCredential cmdlet får en eller flera autentiseringsuppgifter för jobbet</span><span class="sxs-lookup"><span data-stu-id="7d399-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="7d399-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d399-110">EXAMPLES</span></span>

### <span data-ttu-id="7d399-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d399-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="7d399-112">Hämtar autentiseringsuppgifter för jobbet</span><span class="sxs-lookup"><span data-stu-id="7d399-112">Gets a job credential</span></span>

## <span data-ttu-id="7d399-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d399-113">PARAMETERS</span></span>

### <span data-ttu-id="7d399-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7d399-114">-AgentName</span></span>
<span data-ttu-id="7d399-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="7d399-115">The agent name</span></span>

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

### <span data-ttu-id="7d399-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d399-116">-DefaultProfile</span></span>
<span data-ttu-id="7d399-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d399-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d399-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d399-118">-Name</span></span>
<span data-ttu-id="7d399-119">Namnet på jobbet</span><span class="sxs-lookup"><span data-stu-id="7d399-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d399-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7d399-120">-ParentObject</span></span>
<span data-ttu-id="7d399-121">Agent-objektet</span><span class="sxs-lookup"><span data-stu-id="7d399-121">The agent object</span></span>

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

### <span data-ttu-id="7d399-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7d399-122">-ParentResourceId</span></span>
<span data-ttu-id="7d399-123">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="7d399-123">The agent resource id</span></span>

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

### <span data-ttu-id="7d399-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d399-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d399-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="7d399-125">The resource group name</span></span>

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

### <span data-ttu-id="7d399-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7d399-126">-ServerName</span></span>
<span data-ttu-id="7d399-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="7d399-127">The server name</span></span>

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

### <span data-ttu-id="7d399-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d399-128">CommonParameters</span></span>
<span data-ttu-id="7d399-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d399-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d399-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d399-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d399-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d399-131">INPUTS</span></span>

### <span data-ttu-id="7d399-132">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="7d399-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7d399-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d399-133">OUTPUTS</span></span>

### <span data-ttu-id="7d399-134">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="7d399-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="7d399-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d399-135">NOTES</span></span>

## <span data-ttu-id="7d399-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d399-136">RELATED LINKS</span></span>
