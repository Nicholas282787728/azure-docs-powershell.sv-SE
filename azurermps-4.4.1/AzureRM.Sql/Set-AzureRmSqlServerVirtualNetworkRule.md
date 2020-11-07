---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758258"
---
# <span data-ttu-id="5e9cf-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5e9cf-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="5e9cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9cf-103">Ändrar konfigurationen för en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e9cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e9cf-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e9cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e9cf-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9cf-106">Det här kommandot ändrar konfigurationen för en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="5e9cf-107">Använd "Add-AzureRmSqlServerVirtualNetworkRule" och "Remove-AzureRmSqlServerVirtualNetworkRule" i stället för att styra uppsättningen med regler för virtuella nätverk på servern.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="5e9cf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e9cf-108">EXAMPLES</span></span>

### <span data-ttu-id="5e9cf-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5e9cf-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="5e9cf-110">Ändrar en befintlig virtuell nätverks regel med det nya virtuella nätverkets undernät-ID som innehåller information om det nya virtuella nätverket</span><span class="sxs-lookup"><span data-stu-id="5e9cf-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="5e9cf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e9cf-111">PARAMETERS</span></span>

### <span data-ttu-id="5e9cf-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9cf-112">-ResourceGroupName</span></span>
<span data-ttu-id="5e9cf-113">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e9cf-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e9cf-114">-ServerName</span></span>
<span data-ttu-id="5e9cf-115">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5e9cf-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="5e9cf-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="5e9cf-117">Namnet på den virtuella nätverks regeln för Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="5e9cf-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="5e9cf-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="5e9cf-119">ID för den virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="5e9cf-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e9cf-120">-Confirm</span></span>
<span data-ttu-id="5e9cf-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9cf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9cf-122">-WhatIf</span></span>
<span data-ttu-id="5e9cf-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e9cf-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9cf-125">-DefaultProfile</span></span>
<span data-ttu-id="5e9cf-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e9cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9cf-127">CommonParameters</span></span>
<span data-ttu-id="5e9cf-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9cf-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9cf-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e9cf-130">INPUTS</span></span>

### <span data-ttu-id="5e9cf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e9cf-131">System.String</span></span>

## <span data-ttu-id="5e9cf-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e9cf-132">OUTPUTS</span></span>

### <span data-ttu-id="5e9cf-133">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="5e9cf-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="5e9cf-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e9cf-134">NOTES</span></span>

## <span data-ttu-id="5e9cf-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e9cf-135">RELATED LINKS</span></span>

