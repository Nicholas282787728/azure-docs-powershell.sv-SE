---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: dc13bdaf737985f6769b3bb326201100204c6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575467"
---
# <span data-ttu-id="05884-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="05884-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="05884-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05884-102">SYNOPSIS</span></span>
<span data-ttu-id="05884-103">Tar bort DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05884-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05884-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05884-104">SYNTAX</span></span>

### <span data-ttu-id="05884-105">Ta bort ett DNS-alias för servrar från cmdlet-indataparametrar</span><span class="sxs-lookup"><span data-stu-id="05884-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05884-106">Ta bort ett DNS-alias för servrar från instans definitionen för AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="05884-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05884-107">Ta bort ett DNS-alias för servrar från ett Azure Resource-ID</span><span class="sxs-lookup"><span data-stu-id="05884-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05884-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05884-108">DESCRIPTION</span></span>
<span data-ttu-id="05884-109">De här kommandona tar bort DNS-aliaset för Azure SQL Server från servern som lämnar servern intakt.</span><span class="sxs-lookup"><span data-stu-id="05884-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="05884-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05884-110">EXAMPLES</span></span>

### <span data-ttu-id="05884-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="05884-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="05884-112">Tar bort DNS-aliaset för Azure SQL Server med namnet aliasName från servern med namnet serverName</span><span class="sxs-lookup"><span data-stu-id="05884-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="05884-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05884-113">PARAMETERS</span></span>

### <span data-ttu-id="05884-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05884-114">-AsJob</span></span>
<span data-ttu-id="05884-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="05884-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05884-116">-DefaultProfile</span></span>
<span data-ttu-id="05884-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05884-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-118">-Force</span><span class="sxs-lookup"><span data-stu-id="05884-118">-Force</span></span>
<span data-ttu-id="05884-119">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="05884-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05884-120">-InputObject</span></span>
<span data-ttu-id="05884-121">Server-DNS-Alisystemet-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="05884-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05884-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="05884-122">-Name</span></span>
<span data-ttu-id="05884-123">Namn på DNS-alias för Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="05884-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05884-124">-ResourceGroupName</span></span>
<span data-ttu-id="05884-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="05884-125">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05884-126">-ResourceId</span></span>
<span data-ttu-id="05884-127">Resurs-ID för serverns DNS-aliasresurspost som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="05884-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05884-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05884-128">-ServerName</span></span>
<span data-ttu-id="05884-129">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="05884-129">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05884-130">-Confirm</span></span>
<span data-ttu-id="05884-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05884-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05884-132">-WhatIf</span></span>
<span data-ttu-id="05884-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05884-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05884-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05884-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05884-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05884-135">CommonParameters</span></span>
<span data-ttu-id="05884-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05884-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05884-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05884-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05884-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05884-138">INPUTS</span></span>

### <span data-ttu-id="05884-139">System. String</span><span class="sxs-lookup"><span data-stu-id="05884-139">System.String</span></span>
<span data-ttu-id="05884-140">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="05884-140">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="05884-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05884-141">OUTPUTS</span></span>

### <span data-ttu-id="05884-142">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="05884-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="05884-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05884-143">NOTES</span></span>

## <span data-ttu-id="05884-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05884-144">RELATED LINKS</span></span>
