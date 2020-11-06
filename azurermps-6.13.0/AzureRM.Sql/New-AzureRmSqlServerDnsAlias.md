---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573877"
---
# <span data-ttu-id="1b32d-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="1b32d-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="1b32d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b32d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b32d-103">Det här kommandot skapar ett nytt DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b32d-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b32d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b32d-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b32d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b32d-105">DESCRIPTION</span></span>
<span data-ttu-id="1b32d-106">Skapar ett nytt DNS-alias för Azure SQL Server som pekar på angiven server.</span><span class="sxs-lookup"><span data-stu-id="1b32d-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="1b32d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b32d-107">EXAMPLES</span></span>

### <span data-ttu-id="1b32d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b32d-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="1b32d-109">Det här kommandot skapar DNS-aliaset för Azure SQL Server med namnet aliasName som pekar på Server namn</span><span class="sxs-lookup"><span data-stu-id="1b32d-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="1b32d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b32d-110">PARAMETERS</span></span>

### <span data-ttu-id="1b32d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b32d-111">-AsJob</span></span>
<span data-ttu-id="1b32d-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1b32d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b32d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b32d-113">-DefaultProfile</span></span>
<span data-ttu-id="1b32d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b32d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b32d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b32d-115">-Name</span></span>
<span data-ttu-id="1b32d-116">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b32d-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="1b32d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b32d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b32d-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b32d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b32d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b32d-119">-ServerName</span></span>
<span data-ttu-id="1b32d-120">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="1b32d-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1b32d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b32d-121">-Confirm</span></span>
<span data-ttu-id="1b32d-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b32d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b32d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b32d-123">-WhatIf</span></span>
<span data-ttu-id="1b32d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b32d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b32d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b32d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b32d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b32d-126">CommonParameters</span></span>
<span data-ttu-id="1b32d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b32d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b32d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b32d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b32d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b32d-129">INPUTS</span></span>

### <span data-ttu-id="1b32d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1b32d-130">System.String</span></span>

## <span data-ttu-id="1b32d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b32d-131">OUTPUTS</span></span>

### <span data-ttu-id="1b32d-132">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1b32d-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="1b32d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b32d-133">NOTES</span></span>

## <span data-ttu-id="1b32d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b32d-134">RELATED LINKS</span></span>
