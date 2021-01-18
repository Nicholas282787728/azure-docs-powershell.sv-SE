---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523945"
---
# <span data-ttu-id="edac9-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="edac9-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="edac9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edac9-102">SYNOPSIS</span></span>
<span data-ttu-id="edac9-103">Hämtar brand Väggs regler för en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="edac9-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="edac9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edac9-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edac9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edac9-105">DESCRIPTION</span></span>
<span data-ttu-id="edac9-106">Cmdleten **Get-AzSqlServerFirewallRule** hämtar brand Väggs regler för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="edac9-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="edac9-107">Om du anger namnet på en brand Väggs regel får denna cmdlet information om den specifika brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="edac9-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="edac9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edac9-108">EXAMPLES</span></span>

### <span data-ttu-id="edac9-109">Exempel 1: Hämta alla regler för en server</span><span class="sxs-lookup"><span data-stu-id="edac9-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="edac9-110">Det här kommandot får alla brand Väggs regler för servern som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="edac9-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="edac9-111">Exempel 2: Hämta alla regler för en server med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="edac9-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="edac9-112">Det här kommandot får alla brand Väggs regler för servern med namnet Server01 som börjar med "Rule".</span><span class="sxs-lookup"><span data-stu-id="edac9-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="edac9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edac9-113">PARAMETERS</span></span>

### <span data-ttu-id="edac9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edac9-114">-DefaultProfile</span></span>
<span data-ttu-id="edac9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="edac9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edac9-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="edac9-116">-FirewallRuleName</span></span>
<span data-ttu-id="edac9-117">Anger namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="edac9-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edac9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edac9-118">-ResourceGroupName</span></span>
<span data-ttu-id="edac9-119">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="edac9-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="edac9-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edac9-120">-ServerName</span></span>
<span data-ttu-id="edac9-121">Anger namnet på SQL Server.</span><span class="sxs-lookup"><span data-stu-id="edac9-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="edac9-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="edac9-122">-Confirm</span></span>
<span data-ttu-id="edac9-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="edac9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edac9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edac9-124">-WhatIf</span></span>
<span data-ttu-id="edac9-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="edac9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edac9-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="edac9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edac9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edac9-127">CommonParameters</span></span>
<span data-ttu-id="edac9-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edac9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edac9-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edac9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edac9-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edac9-130">INPUTS</span></span>

### <span data-ttu-id="edac9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="edac9-131">System.String</span></span>

## <span data-ttu-id="edac9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edac9-132">OUTPUTS</span></span>

### <span data-ttu-id="edac9-133">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="edac9-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="edac9-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edac9-134">NOTES</span></span>

## <span data-ttu-id="edac9-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edac9-135">RELATED LINKS</span></span>

[<span data-ttu-id="edac9-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="edac9-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="edac9-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="edac9-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="edac9-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="edac9-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="edac9-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="edac9-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


