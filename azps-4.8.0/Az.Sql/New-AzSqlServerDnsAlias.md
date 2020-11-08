---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100787"
---
# <span data-ttu-id="cee59-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="cee59-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="cee59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cee59-102">SYNOPSIS</span></span>
<span data-ttu-id="cee59-103">Det här kommandot skapar ett nytt DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cee59-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="cee59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cee59-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cee59-105">DESCRIPTION</span></span>
<span data-ttu-id="cee59-106">Skapar ett nytt DNS-alias för Azure SQL Server som pekar på angiven server.</span><span class="sxs-lookup"><span data-stu-id="cee59-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="cee59-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cee59-107">EXAMPLES</span></span>

### <span data-ttu-id="cee59-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cee59-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="cee59-109">Det här kommandot skapar DNS-aliaset för Azure SQL Server med namnet aliasName som pekar på Server namn</span><span class="sxs-lookup"><span data-stu-id="cee59-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="cee59-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cee59-110">PARAMETERS</span></span>

### <span data-ttu-id="cee59-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cee59-111">-AsJob</span></span>
<span data-ttu-id="cee59-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cee59-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cee59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee59-113">-DefaultProfile</span></span>
<span data-ttu-id="cee59-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cee59-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee59-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="cee59-115">-Name</span></span>
<span data-ttu-id="cee59-116">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cee59-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="cee59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee59-117">-ResourceGroupName</span></span>
<span data-ttu-id="cee59-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cee59-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cee59-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cee59-119">-ServerName</span></span>
<span data-ttu-id="cee59-120">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="cee59-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cee59-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cee59-121">-Confirm</span></span>
<span data-ttu-id="cee59-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cee59-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee59-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee59-123">-WhatIf</span></span>
<span data-ttu-id="cee59-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cee59-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee59-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cee59-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee59-126">CommonParameters</span></span>
<span data-ttu-id="cee59-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee59-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cee59-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee59-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cee59-129">INPUTS</span></span>

### <span data-ttu-id="cee59-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cee59-130">System.String</span></span>

## <span data-ttu-id="cee59-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cee59-131">OUTPUTS</span></span>

### <span data-ttu-id="cee59-132">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="cee59-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="cee59-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cee59-133">NOTES</span></span>

## <span data-ttu-id="cee59-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cee59-134">RELATED LINKS</span></span>
