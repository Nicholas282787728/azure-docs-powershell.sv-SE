---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258549"
---
# <span data-ttu-id="e2d68-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="e2d68-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="e2d68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2d68-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d68-103">Hämtar eller visar DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e2d68-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="e2d68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2d68-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d68-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2d68-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d68-106">Hämta det specifika DNS-aliaset för Azure SQL Server eller en lista över alla Server-DNS-alias för servern</span><span class="sxs-lookup"><span data-stu-id="e2d68-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="e2d68-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2d68-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d68-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e2d68-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="e2d68-109">Visar alla DNS-alias för servrar för den specifika servern</span><span class="sxs-lookup"><span data-stu-id="e2d68-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="e2d68-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e2d68-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="e2d68-111">Hämtar Server-DNS-alias som anges av Server-och aliasnamn</span><span class="sxs-lookup"><span data-stu-id="e2d68-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="e2d68-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="e2d68-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="e2d68-113">Visar alla DNS-alias för servrar för den specifika server som börjar med "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="e2d68-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="e2d68-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2d68-114">PARAMETERS</span></span>

### <span data-ttu-id="e2d68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d68-115">-DefaultProfile</span></span>
<span data-ttu-id="e2d68-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d68-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2d68-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2d68-117">-Name</span></span>
<span data-ttu-id="e2d68-118">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e2d68-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d68-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d68-119">-ResourceGroupName</span></span>
<span data-ttu-id="e2d68-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e2d68-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2d68-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2d68-121">-ServerName</span></span>
<span data-ttu-id="e2d68-122">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="e2d68-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e2d68-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2d68-123">-Confirm</span></span>
<span data-ttu-id="e2d68-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2d68-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d68-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d68-125">-WhatIf</span></span>
<span data-ttu-id="e2d68-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2d68-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d68-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2d68-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d68-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d68-128">CommonParameters</span></span>
<span data-ttu-id="e2d68-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d68-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d68-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2d68-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d68-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2d68-131">INPUTS</span></span>

### <span data-ttu-id="e2d68-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e2d68-132">System.String</span></span>

## <span data-ttu-id="e2d68-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2d68-133">OUTPUTS</span></span>

### <span data-ttu-id="e2d68-134">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="e2d68-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="e2d68-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2d68-135">NOTES</span></span>

## <span data-ttu-id="e2d68-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2d68-136">RELATED LINKS</span></span>
