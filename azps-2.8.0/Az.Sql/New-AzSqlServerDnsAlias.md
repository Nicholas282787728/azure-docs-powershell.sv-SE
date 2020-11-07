---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 60790af3396177e2885b4a83fda4d24db8c4e4d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920569"
---
# <span data-ttu-id="0eda9-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="0eda9-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="0eda9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0eda9-102">SYNOPSIS</span></span>
<span data-ttu-id="0eda9-103">Det här kommandot skapar ett nytt DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0eda9-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="0eda9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0eda9-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eda9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0eda9-105">DESCRIPTION</span></span>
<span data-ttu-id="0eda9-106">Skapar ett nytt DNS-alias för Azure SQL Server som pekar på angiven server.</span><span class="sxs-lookup"><span data-stu-id="0eda9-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="0eda9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0eda9-107">EXAMPLES</span></span>

### <span data-ttu-id="0eda9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0eda9-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="0eda9-109">Det här kommandot skapar DNS-aliaset för Azure SQL Server med namnet aliasName som pekar på Server namn</span><span class="sxs-lookup"><span data-stu-id="0eda9-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="0eda9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0eda9-110">PARAMETERS</span></span>

### <span data-ttu-id="0eda9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eda9-111">-AsJob</span></span>
<span data-ttu-id="0eda9-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0eda9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0eda9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eda9-113">-DefaultProfile</span></span>
<span data-ttu-id="0eda9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0eda9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eda9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0eda9-115">-Name</span></span>
<span data-ttu-id="0eda9-116">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0eda9-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eda9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eda9-117">-ResourceGroupName</span></span>
<span data-ttu-id="0eda9-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0eda9-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eda9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0eda9-119">-ServerName</span></span>
<span data-ttu-id="0eda9-120">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="0eda9-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0eda9-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0eda9-121">-Confirm</span></span>
<span data-ttu-id="0eda9-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0eda9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eda9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eda9-123">-WhatIf</span></span>
<span data-ttu-id="0eda9-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0eda9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eda9-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0eda9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eda9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eda9-126">CommonParameters</span></span>
<span data-ttu-id="0eda9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eda9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eda9-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eda9-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eda9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0eda9-129">INPUTS</span></span>

### <span data-ttu-id="0eda9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0eda9-130">System.String</span></span>

## <span data-ttu-id="0eda9-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0eda9-131">OUTPUTS</span></span>

### <span data-ttu-id="0eda9-132">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="0eda9-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="0eda9-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0eda9-133">NOTES</span></span>

## <span data-ttu-id="0eda9-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0eda9-134">RELATED LINKS</span></span>
