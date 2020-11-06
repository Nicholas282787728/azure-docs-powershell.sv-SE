---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c71f8284cc3b1a2648e3523c77f0e9e2dd2d3876
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576033"
---
# <span data-ttu-id="7eb80-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7eb80-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="7eb80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7eb80-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb80-103">Ändrar konfigurationen för en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="7eb80-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7eb80-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb80-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7eb80-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb80-106">Det här kommandot ändrar konfigurationen för en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="7eb80-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="7eb80-107">Använd "Add-AzureRmSqlServerVirtualNetworkRule" och "Remove-AzureRmSqlServerVirtualNetworkRule" i stället för att styra uppsättningen med regler för virtuella nätverk på servern.</span><span class="sxs-lookup"><span data-stu-id="7eb80-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="7eb80-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7eb80-108">EXAMPLES</span></span>

### <span data-ttu-id="7eb80-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7eb80-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="7eb80-110">Ändrar en befintlig virtuell nätverks regel med det nya virtuella nätverkets undernät-ID som innehåller information om det nya virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="7eb80-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="7eb80-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7eb80-111">PARAMETERS</span></span>

### <span data-ttu-id="7eb80-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7eb80-112">-AsJob</span></span>
<span data-ttu-id="7eb80-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7eb80-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eb80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb80-114">-DefaultProfile</span></span>
<span data-ttu-id="7eb80-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7eb80-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eb80-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7eb80-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="7eb80-117">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7eb80-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="7eb80-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb80-118">-ResourceGroupName</span></span>
<span data-ttu-id="7eb80-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7eb80-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="7eb80-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7eb80-120">-ServerName</span></span>
<span data-ttu-id="7eb80-121">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="7eb80-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7eb80-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="7eb80-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="7eb80-123">Namnet på den virtuella nätverks regeln för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7eb80-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="7eb80-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="7eb80-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="7eb80-125">ID för den virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="7eb80-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="7eb80-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7eb80-126">-Confirm</span></span>
<span data-ttu-id="7eb80-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7eb80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb80-128">-WhatIf</span></span>
<span data-ttu-id="7eb80-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7eb80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb80-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7eb80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb80-131">CommonParameters</span></span>
<span data-ttu-id="7eb80-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eb80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb80-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb80-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7eb80-134">INPUTS</span></span>

### <span data-ttu-id="7eb80-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb80-135">System.String</span></span>

## <span data-ttu-id="7eb80-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7eb80-136">OUTPUTS</span></span>

### <span data-ttu-id="7eb80-137">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="7eb80-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="7eb80-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7eb80-138">NOTES</span></span>

## <span data-ttu-id="7eb80-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7eb80-139">RELATED LINKS</span></span>
