---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 5afd12ac027b19f888eb6a5110db2179dd6df24d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584860"
---
# <span data-ttu-id="f9240-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="f9240-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="f9240-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9240-102">SYNOPSIS</span></span>
<span data-ttu-id="f9240-103">Tar bort DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f9240-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9240-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9240-104">SYNTAX</span></span>

### <span data-ttu-id="f9240-105">Ta bort ett DNS-alias för servrar från cmdlet-indataparametrar</span><span class="sxs-lookup"><span data-stu-id="f9240-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9240-106">Ta bort ett DNS-alias för servrar från instans definitionen för AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f9240-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9240-107">Ta bort ett DNS-alias för servrar från ett Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="f9240-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9240-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9240-108">DESCRIPTION</span></span>
<span data-ttu-id="f9240-109">De här kommandona tar bort DNS-aliaset för Azure SQL Server från servern som lämnar servern intakt.</span><span class="sxs-lookup"><span data-stu-id="f9240-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="f9240-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9240-110">EXAMPLES</span></span>

### <span data-ttu-id="f9240-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9240-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="f9240-112">Tar bort DNS-aliaset för Azure SQL Server med namnet aliasName från servern med namnet serverName</span><span class="sxs-lookup"><span data-stu-id="f9240-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="f9240-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9240-113">PARAMETERS</span></span>

### <span data-ttu-id="f9240-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9240-114">-AsJob</span></span>
<span data-ttu-id="f9240-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f9240-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9240-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9240-116">-DefaultProfile</span></span>
<span data-ttu-id="f9240-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9240-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9240-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f9240-118">-Force</span></span>
<span data-ttu-id="f9240-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="f9240-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f9240-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9240-120">-InputObject</span></span>
<span data-ttu-id="f9240-121">Server-DNS-Alisystemet-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f9240-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="f9240-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9240-122">-Name</span></span>
<span data-ttu-id="f9240-123">Namn på DNS-alias för Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f9240-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="f9240-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9240-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9240-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f9240-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9240-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9240-126">-ResourceId</span></span>
<span data-ttu-id="f9240-127">Resurs-ID för serverns DNS-aliasresurspost som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f9240-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="f9240-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9240-128">-ServerName</span></span>
<span data-ttu-id="f9240-129">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="f9240-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f9240-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9240-130">-Confirm</span></span>
<span data-ttu-id="f9240-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9240-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9240-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9240-132">-WhatIf</span></span>
<span data-ttu-id="f9240-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9240-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9240-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9240-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9240-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9240-135">CommonParameters</span></span>
<span data-ttu-id="f9240-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9240-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9240-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9240-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9240-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9240-138">INPUTS</span></span>

### <span data-ttu-id="f9240-139">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f9240-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>
<span data-ttu-id="f9240-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f9240-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f9240-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f9240-141">System.String</span></span>

## <span data-ttu-id="f9240-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9240-142">OUTPUTS</span></span>

### <span data-ttu-id="f9240-143">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f9240-143">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="f9240-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9240-144">NOTES</span></span>

## <span data-ttu-id="f9240-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9240-145">RELATED LINKS</span></span>
