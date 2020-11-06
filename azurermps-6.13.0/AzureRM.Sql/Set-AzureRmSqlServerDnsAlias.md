---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 6c18639e3c717ced8ed107ce3604e20639d87682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576040"
---
# <span data-ttu-id="18801-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="18801-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="18801-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18801-102">SYNOPSIS</span></span>
<span data-ttu-id="18801-103">Ändrar den server som DNS-aliaset för Azure SQL Server pekar på</span><span class="sxs-lookup"><span data-stu-id="18801-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18801-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18801-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18801-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18801-105">DESCRIPTION</span></span>
<span data-ttu-id="18801-106">Det här kommandot uppdaterar servern som aliaset pekar på.</span><span class="sxs-lookup"><span data-stu-id="18801-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="18801-107">Det här kommandot måste utfärdas när du är inloggad i ett abonnemang där den nya server som aliaset ska pekas på finns.</span><span class="sxs-lookup"><span data-stu-id="18801-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="18801-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18801-108">EXAMPLES</span></span>

### <span data-ttu-id="18801-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="18801-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="18801-110">Det här kommandot uppdaterar alias som tidigare pekade på oldServer för att peka på Server newServer</span><span class="sxs-lookup"><span data-stu-id="18801-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="18801-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18801-111">PARAMETERS</span></span>

### <span data-ttu-id="18801-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18801-112">-AsJob</span></span>
<span data-ttu-id="18801-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18801-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18801-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18801-114">-DefaultProfile</span></span>
<span data-ttu-id="18801-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18801-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18801-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="18801-116">-Name</span></span>
<span data-ttu-id="18801-117">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="18801-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="18801-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18801-118">-ResourceGroupName</span></span>
<span data-ttu-id="18801-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="18801-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="18801-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="18801-120">-SourceServerName</span></span>
<span data-ttu-id="18801-121">Namnet på Azure SQL Server som aliaset för närvarande pekar på.</span><span class="sxs-lookup"><span data-stu-id="18801-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="18801-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18801-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="18801-123">Namnet på resurs gruppen för käll servern.</span><span class="sxs-lookup"><span data-stu-id="18801-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="18801-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18801-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="18801-125">Abonnemangs-ID för käll servern</span><span class="sxs-lookup"><span data-stu-id="18801-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="18801-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="18801-126">-TargetServerName</span></span>
<span data-ttu-id="18801-127">Namnet på Azure SQL Server som alias ska peka på.</span><span class="sxs-lookup"><span data-stu-id="18801-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="18801-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18801-128">-Confirm</span></span>
<span data-ttu-id="18801-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18801-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18801-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18801-130">-WhatIf</span></span>
<span data-ttu-id="18801-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18801-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18801-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18801-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18801-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18801-133">CommonParameters</span></span>
<span data-ttu-id="18801-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18801-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18801-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18801-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18801-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18801-136">INPUTS</span></span>

### <span data-ttu-id="18801-137">System. String</span><span class="sxs-lookup"><span data-stu-id="18801-137">System.String</span></span>

## <span data-ttu-id="18801-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18801-138">OUTPUTS</span></span>

### <span data-ttu-id="18801-139">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="18801-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="18801-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18801-140">NOTES</span></span>

## <span data-ttu-id="18801-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18801-141">RELATED LINKS</span></span>
