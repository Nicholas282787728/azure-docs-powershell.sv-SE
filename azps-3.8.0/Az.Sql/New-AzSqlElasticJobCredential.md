---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091983"
---
# <span data-ttu-id="1c0b0-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="1c0b0-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="1c0b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0b0-103">Skapar ett nytt jobb-autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="1c0b0-103">Creates a new job credential</span></span>

## <span data-ttu-id="1c0b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c0b0-104">SYNTAX</span></span>

### <span data-ttu-id="1c0b0-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1c0b0-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c0b0-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1c0b0-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c0b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1c0b0-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c0b0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c0b0-108">DESCRIPTION</span></span>
<span data-ttu-id="1c0b0-109">New-AzSqlElasticJobCredential cmdlet skapar ett nytt jobb-autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="1c0b0-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="1c0b0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c0b0-110">EXAMPLES</span></span>

### <span data-ttu-id="1c0b0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1c0b0-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="1c0b0-112">Skapar ett nytt jobb-autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="1c0b0-112">Creates a new job credential</span></span>

## <span data-ttu-id="1c0b0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c0b0-113">PARAMETERS</span></span>

### <span data-ttu-id="1c0b0-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1c0b0-114">-AgentName</span></span>
<span data-ttu-id="1c0b0-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="1c0b0-115">The agent name</span></span>

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

### <span data-ttu-id="1c0b0-116">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="1c0b0-116">-Credential</span></span>
<span data-ttu-id="1c0b0-117">Autentiseringsuppgifterna</span><span class="sxs-lookup"><span data-stu-id="1c0b0-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0b0-118">-DefaultProfile</span></span>
<span data-ttu-id="1c0b0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0b0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c0b0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c0b0-120">-Name</span></span>
<span data-ttu-id="1c0b0-121">Namnet på jobbet</span><span class="sxs-lookup"><span data-stu-id="1c0b0-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0b0-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1c0b0-122">-ParentObject</span></span>
<span data-ttu-id="1c0b0-123">Agent-objektet</span><span class="sxs-lookup"><span data-stu-id="1c0b0-123">The agent object</span></span>

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

### <span data-ttu-id="1c0b0-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1c0b0-124">-ParentResourceId</span></span>
<span data-ttu-id="1c0b0-125">Agent resurs-ID</span><span class="sxs-lookup"><span data-stu-id="1c0b0-125">The agent resource id</span></span>

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

### <span data-ttu-id="1c0b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c0b0-127">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="1c0b0-127">The resource group name</span></span>

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

### <span data-ttu-id="1c0b0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c0b0-128">-ServerName</span></span>
<span data-ttu-id="1c0b0-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="1c0b0-129">The server name</span></span>

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

### <span data-ttu-id="1c0b0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c0b0-130">-Confirm</span></span>
<span data-ttu-id="1c0b0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c0b0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0b0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0b0-132">-WhatIf</span></span>
<span data-ttu-id="1c0b0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c0b0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c0b0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c0b0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c0b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0b0-135">CommonParameters</span></span>
<span data-ttu-id="1c0b0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0b0-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c0b0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0b0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c0b0-138">INPUTS</span></span>

### <span data-ttu-id="1c0b0-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1c0b0-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="1c0b0-140">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="1c0b0-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="1c0b0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c0b0-141">OUTPUTS</span></span>

### <span data-ttu-id="1c0b0-142">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="1c0b0-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="1c0b0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c0b0-143">NOTES</span></span>

## <span data-ttu-id="1c0b0-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c0b0-144">RELATED LINKS</span></span>
