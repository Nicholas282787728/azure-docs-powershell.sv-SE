---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099336"
---
# <span data-ttu-id="cc5f1-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc5f1-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="cc5f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5f1-103">Tar bort en brand Väggs regel från en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="cc5f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc5f1-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc5f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="cc5f1-106">Cmdleten **Remove-AzureSqlDatabaseServerFirewallRule** tar bort en brand Väggs regel från en instans av en Azure SQL Database-Server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="cc5f1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc5f1-107">EXAMPLES</span></span>

### <span data-ttu-id="cc5f1-108">Exempel 1: ta bort en regel</span><span class="sxs-lookup"><span data-stu-id="cc5f1-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="cc5f1-109">Det här kommandot tar bort brand Väggs regeln med namnet FirewallRule24 från SQL-serverdatabasen med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="cc5f1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc5f1-110">PARAMETERS</span></span>

### <span data-ttu-id="cc5f1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cc5f1-111">-Force</span></span>
<span data-ttu-id="cc5f1-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5f1-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="cc5f1-113">-Profile</span></span>
<span data-ttu-id="cc5f1-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc5f1-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5f1-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="cc5f1-116">-RuleName</span></span>
<span data-ttu-id="cc5f1-117">Anger namnet på den brand Väggs regel som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5f1-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc5f1-118">-ServerName</span></span>
<span data-ttu-id="cc5f1-119">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-119">Specifies the name of a server.</span></span>
<span data-ttu-id="cc5f1-120">Denna cmdlet tar bort en brand Väggs regel från den server som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5f1-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc5f1-121">-Confirm</span></span>
<span data-ttu-id="cc5f1-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5f1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5f1-123">-WhatIf</span></span>
<span data-ttu-id="cc5f1-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5f1-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5f1-126">CommonParameters</span></span>
<span data-ttu-id="cc5f1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5f1-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5f1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5f1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc5f1-129">INPUTS</span></span>

### <span data-ttu-id="cc5f1-130">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="cc5f1-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="cc5f1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc5f1-131">OUTPUTS</span></span>

## <span data-ttu-id="cc5f1-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc5f1-132">NOTES</span></span>

## <span data-ttu-id="cc5f1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc5f1-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc5f1-134">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="cc5f1-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="cc5f1-135">Ta bort brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="cc5f1-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="cc5f1-136">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="cc5f1-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="cc5f1-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc5f1-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="cc5f1-138">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc5f1-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="cc5f1-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc5f1-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


