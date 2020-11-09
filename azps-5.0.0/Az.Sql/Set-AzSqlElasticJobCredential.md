---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322311"
---
# <span data-ttu-id="3ca5e-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="3ca5e-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="3ca5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ca5e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca5e-103">Uppdaterar autentiseringsuppgifterna för jobbet</span><span class="sxs-lookup"><span data-stu-id="3ca5e-103">Updates a job credential</span></span>

## <span data-ttu-id="3ca5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ca5e-104">SYNTAX</span></span>

### <span data-ttu-id="3ca5e-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3ca5e-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca5e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ca5e-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3ca5e-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca5e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ca5e-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca5e-109">Set-AzSqlElasticJobCredential cmdlet uppdaterar autentiseringsuppgifter för en jobb</span><span class="sxs-lookup"><span data-stu-id="3ca5e-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="3ca5e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ca5e-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca5e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3ca5e-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="3ca5e-112">Uppdaterar autentiseringsuppgifterna för jobbet</span><span class="sxs-lookup"><span data-stu-id="3ca5e-112">Updates a job credential</span></span>

## <span data-ttu-id="3ca5e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ca5e-113">PARAMETERS</span></span>

### <span data-ttu-id="3ca5e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3ca5e-114">-AgentName</span></span>
<span data-ttu-id="3ca5e-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="3ca5e-115">The agent name</span></span>

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

### <span data-ttu-id="3ca5e-116">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="3ca5e-116">-Credential</span></span>
<span data-ttu-id="3ca5e-117">Autentiseringsuppgifterna</span><span class="sxs-lookup"><span data-stu-id="3ca5e-117">The credential</span></span>

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

### <span data-ttu-id="3ca5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca5e-118">-DefaultProfile</span></span>
<span data-ttu-id="3ca5e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca5e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca5e-120">-InputObject</span></span>
<span data-ttu-id="3ca5e-121">Objektet jobb referens</span><span class="sxs-lookup"><span data-stu-id="3ca5e-121">The job credential object</span></span>

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

### <span data-ttu-id="3ca5e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ca5e-122">-Name</span></span>
<span data-ttu-id="3ca5e-123">Namnet på jobbet</span><span class="sxs-lookup"><span data-stu-id="3ca5e-123">The job credential name</span></span>

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

### <span data-ttu-id="3ca5e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca5e-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ca5e-125">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="3ca5e-125">The resource group name</span></span>

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

### <span data-ttu-id="3ca5e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca5e-126">-ResourceId</span></span>
<span data-ttu-id="3ca5e-127">Resurs-ID för jobb uppgifter</span><span class="sxs-lookup"><span data-stu-id="3ca5e-127">The job credential resource id</span></span>

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

### <span data-ttu-id="3ca5e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ca5e-128">-ServerName</span></span>
<span data-ttu-id="3ca5e-129">Server namnet</span><span class="sxs-lookup"><span data-stu-id="3ca5e-129">The server name</span></span>

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

### <span data-ttu-id="3ca5e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ca5e-130">-Confirm</span></span>
<span data-ttu-id="3ca5e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca5e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca5e-132">-WhatIf</span></span>
<span data-ttu-id="3ca5e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca5e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca5e-135">CommonParameters</span></span>
<span data-ttu-id="3ca5e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca5e-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ca5e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca5e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ca5e-138">INPUTS</span></span>

### <span data-ttu-id="3ca5e-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3ca5e-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="3ca5e-140">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="3ca5e-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3ca5e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ca5e-141">OUTPUTS</span></span>

### <span data-ttu-id="3ca5e-142">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="3ca5e-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3ca5e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ca5e-143">NOTES</span></span>

## <span data-ttu-id="3ca5e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ca5e-144">RELATED LINKS</span></span>
