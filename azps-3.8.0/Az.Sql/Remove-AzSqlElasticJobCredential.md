---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090918"
---
# <span data-ttu-id="128ee-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="128ee-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="128ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="128ee-102">SYNOPSIS</span></span>
<span data-ttu-id="128ee-103">Tar bort den Elastic Job-autentiseringsuppgiften</span><span class="sxs-lookup"><span data-stu-id="128ee-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="128ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="128ee-104">SYNTAX</span></span>

### <span data-ttu-id="128ee-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="128ee-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="128ee-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="128ee-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="128ee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="128ee-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="128ee-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="128ee-108">DESCRIPTION</span></span>
<span data-ttu-id="128ee-109">Remove-AzSqlElasticJobCredential cmdlet tar bort en autentiseringsuppgifter för jobbet</span><span class="sxs-lookup"><span data-stu-id="128ee-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="128ee-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="128ee-110">EXAMPLES</span></span>

### <span data-ttu-id="128ee-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="128ee-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="128ee-112">Tar bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="128ee-112">Removes a job credential</span></span>

## <span data-ttu-id="128ee-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="128ee-113">PARAMETERS</span></span>

### <span data-ttu-id="128ee-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="128ee-114">-AgentName</span></span>
<span data-ttu-id="128ee-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="128ee-115">The agent name</span></span>

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

### <span data-ttu-id="128ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128ee-116">-DefaultProfile</span></span>
<span data-ttu-id="128ee-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="128ee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128ee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="128ee-118">-InputObject</span></span>
<span data-ttu-id="128ee-119">Objektet jobb referens</span><span class="sxs-lookup"><span data-stu-id="128ee-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="128ee-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="128ee-120">-Name</span></span>
<span data-ttu-id="128ee-121">Namnet på jobbet</span><span class="sxs-lookup"><span data-stu-id="128ee-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="128ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="128ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="128ee-123">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="128ee-123">The resource group name</span></span>

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

### <span data-ttu-id="128ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="128ee-124">-ResourceId</span></span>
<span data-ttu-id="128ee-125">Resurs-ID för jobb uppgifter</span><span class="sxs-lookup"><span data-stu-id="128ee-125">The job credential resource id</span></span>

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

### <span data-ttu-id="128ee-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="128ee-126">-ServerName</span></span>
<span data-ttu-id="128ee-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="128ee-127">The server name</span></span>

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

### <span data-ttu-id="128ee-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="128ee-128">-Confirm</span></span>
<span data-ttu-id="128ee-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="128ee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="128ee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="128ee-130">-WhatIf</span></span>
<span data-ttu-id="128ee-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="128ee-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="128ee-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="128ee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="128ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128ee-133">CommonParameters</span></span>
<span data-ttu-id="128ee-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="128ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128ee-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="128ee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128ee-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="128ee-136">INPUTS</span></span>

### <span data-ttu-id="128ee-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="128ee-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="128ee-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="128ee-138">OUTPUTS</span></span>

### <span data-ttu-id="128ee-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="128ee-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="128ee-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="128ee-140">NOTES</span></span>

## <span data-ttu-id="128ee-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="128ee-141">RELATED LINKS</span></span>
