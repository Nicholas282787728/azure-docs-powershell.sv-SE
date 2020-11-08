---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920566"
---
# <span data-ttu-id="71c9c-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="71c9c-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="71c9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="71c9c-103">Skapar en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="71c9c-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="71c9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71c9c-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71c9c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="71c9c-106">Skapar en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="71c9c-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="71c9c-107">Regler för virtuella nätverk används för att ansluta Azure SQL-servern till ett specifikt virtuellt nätverk för att begränsa åtkomsten på Azure SQL-servern så att den endast är tillgänglig i det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="71c9c-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="71c9c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71c9c-108">EXAMPLES</span></span>

### <span data-ttu-id="71c9c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71c9c-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="71c9c-110">Skapar en regel för ett Azure SQL Server-nätverk</span><span class="sxs-lookup"><span data-stu-id="71c9c-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="71c9c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71c9c-111">PARAMETERS</span></span>

### <span data-ttu-id="71c9c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71c9c-112">-AsJob</span></span>
<span data-ttu-id="71c9c-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="71c9c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71c9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c9c-114">-DefaultProfile</span></span>
<span data-ttu-id="71c9c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="71c9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71c9c-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="71c9c-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="71c9c-117">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="71c9c-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="71c9c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c9c-118">-ResourceGroupName</span></span>
<span data-ttu-id="71c9c-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="71c9c-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="71c9c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71c9c-120">-ServerName</span></span>
<span data-ttu-id="71c9c-121">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="71c9c-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="71c9c-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="71c9c-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="71c9c-123">Namn på en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="71c9c-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="71c9c-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="71c9c-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="71c9c-125">Det virtuella nätverkets nät-ID som anger Microsoft. Network-uppgifter</span><span class="sxs-lookup"><span data-stu-id="71c9c-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="71c9c-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71c9c-126">-Confirm</span></span>
<span data-ttu-id="71c9c-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71c9c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71c9c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71c9c-128">-WhatIf</span></span>
<span data-ttu-id="71c9c-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71c9c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71c9c-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71c9c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71c9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c9c-131">CommonParameters</span></span>
<span data-ttu-id="71c9c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c9c-133">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71c9c-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c9c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71c9c-134">INPUTS</span></span>

### <span data-ttu-id="71c9c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="71c9c-135">System.String</span></span>

## <span data-ttu-id="71c9c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71c9c-136">OUTPUTS</span></span>

### <span data-ttu-id="71c9c-137">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="71c9c-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="71c9c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71c9c-138">NOTES</span></span>

## <span data-ttu-id="71c9c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71c9c-139">RELATED LINKS</span></span>