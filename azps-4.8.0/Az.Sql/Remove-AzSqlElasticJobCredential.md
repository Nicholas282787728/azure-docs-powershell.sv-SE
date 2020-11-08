---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259042"
---
# <span data-ttu-id="ecfdc-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="ecfdc-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="ecfdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecfdc-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfdc-103">Tar bort den Elastic Job-autentiseringsuppgiften</span><span class="sxs-lookup"><span data-stu-id="ecfdc-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="ecfdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecfdc-104">SYNTAX</span></span>

### <span data-ttu-id="ecfdc-105">DefaultSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ecfdc-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfdc-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecfdc-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfdc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ecfdc-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfdc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecfdc-108">DESCRIPTION</span></span>
<span data-ttu-id="ecfdc-109">Remove-AzSqlElasticJobCredential cmdlet tar bort en autentiseringsuppgifter för jobbet</span><span class="sxs-lookup"><span data-stu-id="ecfdc-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="ecfdc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecfdc-110">EXAMPLES</span></span>

### <span data-ttu-id="ecfdc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecfdc-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="ecfdc-112">Tar bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ecfdc-112">Removes a job credential</span></span>

## <span data-ttu-id="ecfdc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecfdc-113">PARAMETERS</span></span>

### <span data-ttu-id="ecfdc-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ecfdc-114">-AgentName</span></span>
<span data-ttu-id="ecfdc-115">Ombudets namn</span><span class="sxs-lookup"><span data-stu-id="ecfdc-115">The agent name</span></span>

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

### <span data-ttu-id="ecfdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfdc-116">-DefaultProfile</span></span>
<span data-ttu-id="ecfdc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecfdc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfdc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecfdc-118">-InputObject</span></span>
<span data-ttu-id="ecfdc-119">Objektet jobb referens</span><span class="sxs-lookup"><span data-stu-id="ecfdc-119">The job credential object</span></span>

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

### <span data-ttu-id="ecfdc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecfdc-120">-Name</span></span>
<span data-ttu-id="ecfdc-121">Namnet på jobbet</span><span class="sxs-lookup"><span data-stu-id="ecfdc-121">The job credential name</span></span>

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

### <span data-ttu-id="ecfdc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfdc-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecfdc-123">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="ecfdc-123">The resource group name</span></span>

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

### <span data-ttu-id="ecfdc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfdc-124">-ResourceId</span></span>
<span data-ttu-id="ecfdc-125">Resurs-ID för jobb uppgifter</span><span class="sxs-lookup"><span data-stu-id="ecfdc-125">The job credential resource id</span></span>

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

### <span data-ttu-id="ecfdc-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ecfdc-126">-ServerName</span></span>
<span data-ttu-id="ecfdc-127">Server namnet</span><span class="sxs-lookup"><span data-stu-id="ecfdc-127">The server name</span></span>

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

### <span data-ttu-id="ecfdc-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecfdc-128">-Confirm</span></span>
<span data-ttu-id="ecfdc-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecfdc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfdc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfdc-130">-WhatIf</span></span>
<span data-ttu-id="ecfdc-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecfdc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecfdc-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecfdc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfdc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfdc-133">CommonParameters</span></span>
<span data-ttu-id="ecfdc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfdc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfdc-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecfdc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfdc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecfdc-136">INPUTS</span></span>

### <span data-ttu-id="ecfdc-137">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="ecfdc-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="ecfdc-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecfdc-138">OUTPUTS</span></span>

### <span data-ttu-id="ecfdc-139">Microsoft. Azure. commands. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="ecfdc-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="ecfdc-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecfdc-140">NOTES</span></span>

## <span data-ttu-id="ecfdc-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecfdc-141">RELATED LINKS</span></span>
