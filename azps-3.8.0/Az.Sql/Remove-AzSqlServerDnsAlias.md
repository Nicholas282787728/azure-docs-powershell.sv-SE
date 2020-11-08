---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090907"
---
# <span data-ttu-id="a74ff-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="a74ff-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="a74ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a74ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a74ff-103">Tar bort DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a74ff-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="a74ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a74ff-104">SYNTAX</span></span>

### <span data-ttu-id="a74ff-105">Ta bort ett DNS-alias för servrar från cmdlet-indataparametrar</span><span class="sxs-lookup"><span data-stu-id="a74ff-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a74ff-106">Ta bort ett DNS-alias för servrar från instans definitionen för AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="a74ff-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a74ff-107">Ta bort ett DNS-alias för servrar från ett Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="a74ff-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a74ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a74ff-108">DESCRIPTION</span></span>
<span data-ttu-id="a74ff-109">De här kommandona tar bort DNS-aliaset för Azure SQL Server från servern som lämnar servern intakt.</span><span class="sxs-lookup"><span data-stu-id="a74ff-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="a74ff-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a74ff-110">EXAMPLES</span></span>

### <span data-ttu-id="a74ff-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a74ff-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="a74ff-112">Tar bort DNS-aliaset för Azure SQL Server med namnet aliasName från servern med namnet serverName</span><span class="sxs-lookup"><span data-stu-id="a74ff-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="a74ff-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a74ff-113">PARAMETERS</span></span>

### <span data-ttu-id="a74ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a74ff-114">-AsJob</span></span>
<span data-ttu-id="a74ff-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a74ff-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74ff-116">-DefaultProfile</span></span>
<span data-ttu-id="a74ff-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a74ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a74ff-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a74ff-118">-Force</span></span>
<span data-ttu-id="a74ff-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="a74ff-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a74ff-120">-InputObject</span></span>
<span data-ttu-id="a74ff-121">Server-DNS-Alisystemet-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="a74ff-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a74ff-122">-Name</span></span>
<span data-ttu-id="a74ff-123">Namn på DNS-alias för Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="a74ff-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="a74ff-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a74ff-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a74ff-126">-ResourceId</span></span>
<span data-ttu-id="a74ff-127">Resurs-ID för serverns DNS-aliasresurspost som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="a74ff-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a74ff-128">-ServerName</span></span>
<span data-ttu-id="a74ff-129">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="a74ff-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a74ff-130">-Confirm</span></span>
<span data-ttu-id="a74ff-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a74ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74ff-132">-WhatIf</span></span>
<span data-ttu-id="a74ff-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a74ff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a74ff-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a74ff-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74ff-135">CommonParameters</span></span>
<span data-ttu-id="a74ff-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74ff-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a74ff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74ff-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a74ff-138">INPUTS</span></span>

### <span data-ttu-id="a74ff-139">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="a74ff-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="a74ff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a74ff-140">System.String</span></span>

## <span data-ttu-id="a74ff-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a74ff-141">OUTPUTS</span></span>

### <span data-ttu-id="a74ff-142">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="a74ff-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="a74ff-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a74ff-143">NOTES</span></span>

## <span data-ttu-id="a74ff-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a74ff-144">RELATED LINKS</span></span>
