---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 14eb3de52c08c276638c5079a1e64c65da6669f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582915"
---
# <span data-ttu-id="67200-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="67200-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="67200-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67200-102">SYNOPSIS</span></span>
<span data-ttu-id="67200-103">Hämtar eller visar regeln för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="67200-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67200-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67200-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67200-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67200-105">DESCRIPTION</span></span>
<span data-ttu-id="67200-106">Det här kommandot får en specifik regel för Azure SQL Server-nätverket eller en lista med nätverks regler för Azure SQL Server under en server.</span><span class="sxs-lookup"><span data-stu-id="67200-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="67200-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67200-107">EXAMPLES</span></span>

### <span data-ttu-id="67200-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67200-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="67200-109">Hämtar en enda regel för ett enskilt Azure SQL Server-nätverk</span><span class="sxs-lookup"><span data-stu-id="67200-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="67200-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="67200-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="67200-111">Hämtar listan över Azure SQL Server-regler för virtuella nätverk under den angivna servern</span><span class="sxs-lookup"><span data-stu-id="67200-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="67200-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67200-112">PARAMETERS</span></span>

### <span data-ttu-id="67200-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67200-113">-DefaultProfile</span></span>
<span data-ttu-id="67200-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="67200-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67200-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67200-115">-ResourceGroupName</span></span>
<span data-ttu-id="67200-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="67200-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="67200-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67200-117">-ServerName</span></span>
<span data-ttu-id="67200-118">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="67200-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="67200-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="67200-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="67200-120">Namnet på den virtuella nätverks regeln för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="67200-120">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67200-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67200-121">CommonParameters</span></span>
<span data-ttu-id="67200-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67200-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67200-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67200-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67200-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67200-124">INPUTS</span></span>

### <span data-ttu-id="67200-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67200-125">System.String</span></span>

## <span data-ttu-id="67200-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67200-126">OUTPUTS</span></span>

### <span data-ttu-id="67200-127">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="67200-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="67200-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67200-128">NOTES</span></span>

## <span data-ttu-id="67200-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67200-129">RELATED LINKS</span></span>
