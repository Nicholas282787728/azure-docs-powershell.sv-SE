---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: e6c6d48cbef24977ae6e2411749efbd913787b33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746665"
---
# <span data-ttu-id="9771e-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9771e-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="9771e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9771e-102">SYNOPSIS</span></span>
<span data-ttu-id="9771e-103">Hämtar brand Väggs regler för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="9771e-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="9771e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9771e-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9771e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9771e-105">DESCRIPTION</span></span>
<span data-ttu-id="9771e-106">Cmdleten **Get-AzSqlServerFirewallRule** hämtar brand Väggs regler för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="9771e-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="9771e-107">Om du anger namnet på en brand Väggs regel får denna cmdlet information om den specifika brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="9771e-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="9771e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9771e-108">EXAMPLES</span></span>

### <span data-ttu-id="9771e-109">Exempel 1: Hämta alla regler för en server</span><span class="sxs-lookup"><span data-stu-id="9771e-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="9771e-110">Det här kommandot får alla brand Väggs regler för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="9771e-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="9771e-111">Exempel 2: Hämta alla regler för en server med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="9771e-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="9771e-112">Det här kommandot får alla brand Väggs regler för servern med namnet Server01 som börjar med "Rule".</span><span class="sxs-lookup"><span data-stu-id="9771e-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="9771e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9771e-113">PARAMETERS</span></span>

### <span data-ttu-id="9771e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9771e-114">-DefaultProfile</span></span>
<span data-ttu-id="9771e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9771e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9771e-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9771e-116">-FirewallRuleName</span></span>
<span data-ttu-id="9771e-117">Anger namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="9771e-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9771e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9771e-118">-ResourceGroupName</span></span>
<span data-ttu-id="9771e-119">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9771e-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="9771e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9771e-120">-ServerName</span></span>
<span data-ttu-id="9771e-121">Anger namnet på SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9771e-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="9771e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9771e-122">-Confirm</span></span>
<span data-ttu-id="9771e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9771e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9771e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9771e-124">-WhatIf</span></span>
<span data-ttu-id="9771e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9771e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9771e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9771e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9771e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9771e-127">CommonParameters</span></span>
<span data-ttu-id="9771e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9771e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9771e-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9771e-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9771e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9771e-130">INPUTS</span></span>

### <span data-ttu-id="9771e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9771e-131">System.String</span></span>

## <span data-ttu-id="9771e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9771e-132">OUTPUTS</span></span>

### <span data-ttu-id="9771e-133">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="9771e-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="9771e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9771e-134">NOTES</span></span>

## <span data-ttu-id="9771e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9771e-135">RELATED LINKS</span></span>

[<span data-ttu-id="9771e-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9771e-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9771e-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9771e-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9771e-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9771e-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="9771e-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9771e-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

