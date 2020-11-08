---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269752"
---
# <span data-ttu-id="5dfa0-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5dfa0-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="5dfa0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5dfa0-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfa0-103">Tar bort en brand Väggs regel från en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="5dfa0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5dfa0-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dfa0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5dfa0-105">DESCRIPTION</span></span>
<span data-ttu-id="5dfa0-106">Cmdleten **Remove-AzSqlServerFirewallRule** tar bort en brand Väggs regel från den angivna Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="5dfa0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5dfa0-107">EXAMPLES</span></span>

### <span data-ttu-id="5dfa0-108">Exempel 1: ta bort en regel</span><span class="sxs-lookup"><span data-stu-id="5dfa0-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="5dfa0-109">Det här kommandot tar bort en brand Väggs regel med namnet Rule01 på servern med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="5dfa0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5dfa0-110">PARAMETERS</span></span>

### <span data-ttu-id="5dfa0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfa0-111">-DefaultProfile</span></span>
<span data-ttu-id="5dfa0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5dfa0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5dfa0-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5dfa0-113">-FirewallRuleName</span></span>
<span data-ttu-id="5dfa0-114">Anger namnet på brand Väggs regeln som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="5dfa0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5dfa0-115">-Force</span></span>
<span data-ttu-id="5dfa0-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5dfa0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfa0-117">-ResourceGroupName</span></span>
<span data-ttu-id="5dfa0-118">Anger namnet på en resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5dfa0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5dfa0-119">-ServerName</span></span>
<span data-ttu-id="5dfa0-120">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5dfa0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5dfa0-121">-Confirm</span></span>
<span data-ttu-id="5dfa0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dfa0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dfa0-123">-WhatIf</span></span>
<span data-ttu-id="5dfa0-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfa0-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dfa0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfa0-126">CommonParameters</span></span>
<span data-ttu-id="5dfa0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfa0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfa0-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dfa0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfa0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5dfa0-129">INPUTS</span></span>

### <span data-ttu-id="5dfa0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5dfa0-130">System.String</span></span>

## <span data-ttu-id="5dfa0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5dfa0-131">OUTPUTS</span></span>

### <span data-ttu-id="5dfa0-132">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5dfa0-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5dfa0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5dfa0-133">NOTES</span></span>

## <span data-ttu-id="5dfa0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5dfa0-134">RELATED LINKS</span></span>

[<span data-ttu-id="5dfa0-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5dfa0-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5dfa0-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5dfa0-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5dfa0-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5dfa0-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5dfa0-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5dfa0-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


