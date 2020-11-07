---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 7022f8655e1b87bc55ddd90cbd0aca512eeec0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920248"
---
# <span data-ttu-id="e8424-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="e8424-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="e8424-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8424-102">SYNOPSIS</span></span>
<span data-ttu-id="e8424-103">Ändrar den server som DNS-aliaset för Azure SQL Server pekar på</span><span class="sxs-lookup"><span data-stu-id="e8424-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="e8424-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8424-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8424-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8424-105">DESCRIPTION</span></span>
<span data-ttu-id="e8424-106">Det här kommandot uppdaterar servern som aliaset pekar på.</span><span class="sxs-lookup"><span data-stu-id="e8424-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="e8424-107">Det här kommandot måste utfärdas när du är inloggad i ett abonnemang där den nya server som aliaset ska pekas på finns.</span><span class="sxs-lookup"><span data-stu-id="e8424-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="e8424-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8424-108">EXAMPLES</span></span>

### <span data-ttu-id="e8424-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e8424-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="e8424-110">Det här kommandot uppdaterar alias som tidigare pekade på oldServer för att peka på Server newServer</span><span class="sxs-lookup"><span data-stu-id="e8424-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="e8424-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8424-111">PARAMETERS</span></span>

### <span data-ttu-id="e8424-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8424-112">-AsJob</span></span>
<span data-ttu-id="e8424-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e8424-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8424-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8424-114">-DefaultProfile</span></span>
<span data-ttu-id="e8424-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8424-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8424-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8424-116">-Name</span></span>
<span data-ttu-id="e8424-117">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e8424-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8424-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8424-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8424-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e8424-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8424-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="e8424-120">-SourceServerName</span></span>
<span data-ttu-id="e8424-121">Namnet på Azure SQL Server som aliaset för närvarande pekar på.</span><span class="sxs-lookup"><span data-stu-id="e8424-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8424-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8424-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="e8424-123">Namnet på resurs gruppen för käll servern.</span><span class="sxs-lookup"><span data-stu-id="e8424-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8424-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8424-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="e8424-125">Abonnemangs-ID för käll servern</span><span class="sxs-lookup"><span data-stu-id="e8424-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8424-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="e8424-126">-TargetServerName</span></span>
<span data-ttu-id="e8424-127">Namnet på Azure SQL Server som alias ska peka på.</span><span class="sxs-lookup"><span data-stu-id="e8424-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8424-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8424-128">-Confirm</span></span>
<span data-ttu-id="e8424-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8424-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8424-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8424-130">-WhatIf</span></span>
<span data-ttu-id="e8424-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8424-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8424-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8424-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8424-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8424-133">CommonParameters</span></span>
<span data-ttu-id="e8424-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8424-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8424-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8424-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8424-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8424-136">INPUTS</span></span>

### <span data-ttu-id="e8424-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e8424-137">System.String</span></span>

## <span data-ttu-id="e8424-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8424-138">OUTPUTS</span></span>

### <span data-ttu-id="e8424-139">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="e8424-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="e8424-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8424-140">NOTES</span></span>

## <span data-ttu-id="e8424-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8424-141">RELATED LINKS</span></span>
