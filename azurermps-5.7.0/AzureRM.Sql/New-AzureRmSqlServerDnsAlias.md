---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 897911a4f13b2453d0e814828000309ad8865ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579304"
---
# <span data-ttu-id="34b97-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="34b97-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="34b97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34b97-102">SYNOPSIS</span></span>
<span data-ttu-id="34b97-103">Det här kommandot skapar ett nytt DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="34b97-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34b97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34b97-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34b97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34b97-105">DESCRIPTION</span></span>
<span data-ttu-id="34b97-106">Skapar ett nytt DNS-alias för Azure SQL Server som pekar på angiven server.</span><span class="sxs-lookup"><span data-stu-id="34b97-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="34b97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34b97-107">EXAMPLES</span></span>

### <span data-ttu-id="34b97-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34b97-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="34b97-109">Det här kommandot skapar DNS-aliaset för Azure SQL Server med namnet aliasName som pekar på Server namn</span><span class="sxs-lookup"><span data-stu-id="34b97-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="34b97-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34b97-110">PARAMETERS</span></span>

### <span data-ttu-id="34b97-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34b97-111">-AsJob</span></span>
<span data-ttu-id="34b97-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="34b97-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="34b97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b97-113">-DefaultProfile</span></span>
<span data-ttu-id="34b97-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34b97-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34b97-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="34b97-115">-Name</span></span>
<span data-ttu-id="34b97-116">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="34b97-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b97-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b97-117">-ResourceGroupName</span></span>
<span data-ttu-id="34b97-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34b97-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b97-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34b97-119">-ServerName</span></span>
<span data-ttu-id="34b97-120">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="34b97-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b97-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34b97-121">-Confirm</span></span>
<span data-ttu-id="34b97-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34b97-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b97-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b97-123">-WhatIf</span></span>
<span data-ttu-id="34b97-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34b97-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34b97-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34b97-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b97-126">CommonParameters</span></span>
<span data-ttu-id="34b97-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b97-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b97-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b97-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34b97-129">INPUTS</span></span>

### <span data-ttu-id="34b97-130">System. String</span><span class="sxs-lookup"><span data-stu-id="34b97-130">System.String</span></span>

## <span data-ttu-id="34b97-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34b97-131">OUTPUTS</span></span>

### <span data-ttu-id="34b97-132">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="34b97-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="34b97-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34b97-133">NOTES</span></span>

## <span data-ttu-id="34b97-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34b97-134">RELATED LINKS</span></span>