---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 3e0f7e021f6ddf2f9b18873dda4f9d482a4db1da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757822"
---
# <span data-ttu-id="263d4-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="263d4-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="263d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="263d4-102">SYNOPSIS</span></span>
<span data-ttu-id="263d4-103">Tar bort en brand Väggs regel från en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="263d4-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="263d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="263d4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="263d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="263d4-105">DESCRIPTION</span></span>
<span data-ttu-id="263d4-106">Cmdleten **Remove-AzureRmSqlServerFirewallRule** tar bort en brand Väggs regel från den angivna Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="263d4-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="263d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="263d4-107">EXAMPLES</span></span>

### <span data-ttu-id="263d4-108">Exempel 1: ta bort en regel</span><span class="sxs-lookup"><span data-stu-id="263d4-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="263d4-109">Det här kommandot tar bort en brand Väggs regel med namnet Rule01 på servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="263d4-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="263d4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="263d4-110">PARAMETERS</span></span>

### <span data-ttu-id="263d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263d4-111">-DefaultProfile</span></span>
<span data-ttu-id="263d4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="263d4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="263d4-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="263d4-113">-FirewallRuleName</span></span>
<span data-ttu-id="263d4-114">Anger namnet på brand Väggs regeln som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="263d4-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263d4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="263d4-115">-Force</span></span>
<span data-ttu-id="263d4-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="263d4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="263d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="263d4-118">Anger namnet på en resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="263d4-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="263d4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="263d4-119">-ServerName</span></span>
<span data-ttu-id="263d4-120">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="263d4-120">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263d4-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="263d4-121">-Confirm</span></span>
<span data-ttu-id="263d4-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="263d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="263d4-123">-WhatIf</span></span>
<span data-ttu-id="263d4-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="263d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="263d4-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="263d4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263d4-126">CommonParameters</span></span>
<span data-ttu-id="263d4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263d4-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="263d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263d4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="263d4-129">INPUTS</span></span>

### <span data-ttu-id="263d4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="263d4-130">System.String</span></span>

## <span data-ttu-id="263d4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="263d4-131">OUTPUTS</span></span>

### <span data-ttu-id="263d4-132">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="263d4-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="263d4-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="263d4-133">NOTES</span></span>

## <span data-ttu-id="263d4-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="263d4-134">RELATED LINKS</span></span>

[<span data-ttu-id="263d4-135">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="263d4-135">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="263d4-136">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="263d4-136">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="263d4-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="263d4-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="263d4-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="263d4-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


