---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 4a2b7de83036e274b9d53b701615e3c348c5f4df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573191"
---
# <span data-ttu-id="741b3-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="741b3-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="741b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="741b3-102">SYNOPSIS</span></span>
<span data-ttu-id="741b3-103">Hämtar eller visar DNS-alias för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="741b3-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="741b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="741b3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="741b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="741b3-105">DESCRIPTION</span></span>
<span data-ttu-id="741b3-106">Hämta det specifika DNS-aliaset för Azure SQL Server eller en lista över alla Server-DNS-alias för servern</span><span class="sxs-lookup"><span data-stu-id="741b3-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="741b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="741b3-107">EXAMPLES</span></span>

### <span data-ttu-id="741b3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="741b3-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="741b3-109">Visar alla DNS-alias för servrar för den specifika servern</span><span class="sxs-lookup"><span data-stu-id="741b3-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="741b3-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="741b3-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="741b3-111">Hämtar Server-DNS-alias som anges av Server-och aliasnamn</span><span class="sxs-lookup"><span data-stu-id="741b3-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="741b3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="741b3-112">PARAMETERS</span></span>

### <span data-ttu-id="741b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741b3-113">-DefaultProfile</span></span>
<span data-ttu-id="741b3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="741b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="741b3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="741b3-115">-Name</span></span>
<span data-ttu-id="741b3-116">DNS-aliasnamnet för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="741b3-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="741b3-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="741b3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="741b3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="741b3-119">-ServerName</span></span>
<span data-ttu-id="741b3-120">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="741b3-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="741b3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="741b3-121">-Confirm</span></span>
<span data-ttu-id="741b3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="741b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741b3-123">-WhatIf</span></span>
<span data-ttu-id="741b3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="741b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="741b3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="741b3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741b3-126">CommonParameters</span></span>
<span data-ttu-id="741b3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741b3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="741b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741b3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="741b3-129">INPUTS</span></span>

### <span data-ttu-id="741b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="741b3-130">System.String</span></span>

## <span data-ttu-id="741b3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="741b3-131">OUTPUTS</span></span>

### <span data-ttu-id="741b3-132">Microsoft. Azure. commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="741b3-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="741b3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="741b3-133">NOTES</span></span>

## <span data-ttu-id="741b3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="741b3-134">RELATED LINKS</span></span>
