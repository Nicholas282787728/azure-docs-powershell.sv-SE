---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 5c079adea8079807374d4538f6259cd995103694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920485"
---
# <span data-ttu-id="478b6-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="478b6-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="478b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="478b6-102">SYNOPSIS</span></span>
<span data-ttu-id="478b6-103">Ändrar en brand Väggs regel i Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="478b6-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="478b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="478b6-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="478b6-105">DESCRIPTION</span></span>
<span data-ttu-id="478b6-106">Cmdleten **set-AzSqlServerFirewallRule** ändrar en brand Väggs regel i en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="478b6-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="478b6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="478b6-107">EXAMPLES</span></span>

### <span data-ttu-id="478b6-108">Exempel 1: ändra en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="478b6-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="478b6-109">Det här kommandot ändrar en brand Väggs regel som heter Rule01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="478b6-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="478b6-110">Kommandot ändrar Start-och slut-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="478b6-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="478b6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="478b6-111">PARAMETERS</span></span>

### <span data-ttu-id="478b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478b6-112">-DefaultProfile</span></span>
<span data-ttu-id="478b6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="478b6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="478b6-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="478b6-114">-EndIpAddress</span></span>
<span data-ttu-id="478b6-115">Anger slutvärdet för IP-adressintervallet för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="478b6-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="478b6-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="478b6-116">-FirewallRuleName</span></span>
<span data-ttu-id="478b6-117">Anger namnet på brand Väggs regeln som ändras av den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="478b6-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="478b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="478b6-119">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="478b6-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="478b6-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="478b6-120">-ServerName</span></span>
<span data-ttu-id="478b6-121">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="478b6-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="478b6-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="478b6-122">-StartIpAddress</span></span>
<span data-ttu-id="478b6-123">Anger startvärdet för IP-adressintervallet för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="478b6-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="478b6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="478b6-124">-Confirm</span></span>
<span data-ttu-id="478b6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="478b6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478b6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478b6-126">-WhatIf</span></span>
<span data-ttu-id="478b6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="478b6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478b6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="478b6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478b6-129">CommonParameters</span></span>
<span data-ttu-id="478b6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478b6-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="478b6-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478b6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="478b6-132">INPUTS</span></span>

### <span data-ttu-id="478b6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="478b6-133">System.String</span></span>

## <span data-ttu-id="478b6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="478b6-134">OUTPUTS</span></span>

### <span data-ttu-id="478b6-135">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="478b6-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="478b6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="478b6-136">NOTES</span></span>

## <span data-ttu-id="478b6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="478b6-137">RELATED LINKS</span></span>

[<span data-ttu-id="478b6-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="478b6-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="478b6-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="478b6-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="478b6-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="478b6-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="478b6-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="478b6-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


