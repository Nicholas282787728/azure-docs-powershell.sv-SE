---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523740"
---
# <span data-ttu-id="af874-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="af874-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="af874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af874-102">SYNOPSIS</span></span>
<span data-ttu-id="af874-103">Hämtar eller visar regeln för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="af874-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="af874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af874-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af874-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af874-105">DESCRIPTION</span></span>
<span data-ttu-id="af874-106">Det här kommandot får en specifik regel för Azure SQL Server-nätverket eller en lista med nätverks regler för Azure SQL Server under en server.</span><span class="sxs-lookup"><span data-stu-id="af874-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="af874-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af874-107">EXAMPLES</span></span>

### <span data-ttu-id="af874-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af874-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="af874-109">Hämtar en enda regel för ett enskilt Azure SQL Server-nätverk</span><span class="sxs-lookup"><span data-stu-id="af874-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="af874-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="af874-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="af874-111">Hämtar listan över Azure SQL Server-regler för virtuella nätverk under den angivna servern</span><span class="sxs-lookup"><span data-stu-id="af874-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="af874-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="af874-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="af874-113">Hämtar listan över Azure SQL Server-regler för virtuella nätverk under den angivna servern som börjar med "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="af874-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="af874-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af874-114">PARAMETERS</span></span>

### <span data-ttu-id="af874-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af874-115">-DefaultProfile</span></span>
<span data-ttu-id="af874-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="af874-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af874-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af874-117">-ResourceGroupName</span></span>
<span data-ttu-id="af874-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af874-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="af874-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af874-119">-ServerName</span></span>
<span data-ttu-id="af874-120">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="af874-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="af874-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="af874-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="af874-122">Namnet på den virtuella nätverks regeln för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af874-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af874-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af874-123">CommonParameters</span></span>
<span data-ttu-id="af874-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af874-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af874-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af874-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af874-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af874-126">INPUTS</span></span>

### <span data-ttu-id="af874-127">System. String</span><span class="sxs-lookup"><span data-stu-id="af874-127">System.String</span></span>

## <span data-ttu-id="af874-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af874-128">OUTPUTS</span></span>

### <span data-ttu-id="af874-129">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="af874-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="af874-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af874-130">NOTES</span></span>

## <span data-ttu-id="af874-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af874-131">RELATED LINKS</span></span>
