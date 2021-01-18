---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522955"
---
# <span data-ttu-id="51fce-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="51fce-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="51fce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51fce-102">SYNOPSIS</span></span>
<span data-ttu-id="51fce-103">Ändrar konfigurationen för en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="51fce-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="51fce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51fce-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51fce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51fce-105">DESCRIPTION</span></span>
<span data-ttu-id="51fce-106">Det här kommandot ändrar konfigurationen för en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="51fce-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="51fce-107">Använd "Add-AzSqlServerVirtualNetworkRule" och "Remove-AzSqlServerVirtualNetworkRule" i stället för att styra uppsättningen med regler för virtuella nätverk på servern.</span><span class="sxs-lookup"><span data-stu-id="51fce-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="51fce-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51fce-108">EXAMPLES</span></span>

### <span data-ttu-id="51fce-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51fce-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="51fce-110">Ändrar en befintlig virtuell nätverks regel med det nya virtuella nätverkets undernät-ID som innehåller information om det nya virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="51fce-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="51fce-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51fce-111">PARAMETERS</span></span>

### <span data-ttu-id="51fce-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51fce-112">-AsJob</span></span>
<span data-ttu-id="51fce-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="51fce-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51fce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fce-114">-DefaultProfile</span></span>
<span data-ttu-id="51fce-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="51fce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51fce-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="51fce-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="51fce-117">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="51fce-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="51fce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fce-118">-ResourceGroupName</span></span>
<span data-ttu-id="51fce-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51fce-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="51fce-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51fce-120">-ServerName</span></span>
<span data-ttu-id="51fce-121">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="51fce-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="51fce-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="51fce-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="51fce-123">Namnet på den virtuella nätverks regeln för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="51fce-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="51fce-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="51fce-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="51fce-125">ID för den virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="51fce-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="51fce-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51fce-126">-Confirm</span></span>
<span data-ttu-id="51fce-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51fce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51fce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fce-128">-WhatIf</span></span>
<span data-ttu-id="51fce-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51fce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fce-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51fce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51fce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fce-131">CommonParameters</span></span>
<span data-ttu-id="51fce-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51fce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fce-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51fce-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fce-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51fce-134">INPUTS</span></span>

### <span data-ttu-id="51fce-135">System. String</span><span class="sxs-lookup"><span data-stu-id="51fce-135">System.String</span></span>

## <span data-ttu-id="51fce-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51fce-136">OUTPUTS</span></span>

### <span data-ttu-id="51fce-137">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="51fce-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="51fce-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51fce-138">NOTES</span></span>

## <span data-ttu-id="51fce-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51fce-139">RELATED LINKS</span></span>
