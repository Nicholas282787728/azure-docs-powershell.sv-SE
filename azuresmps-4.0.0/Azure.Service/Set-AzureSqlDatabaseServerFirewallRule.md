---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099093"
---
# <span data-ttu-id="b024e-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b024e-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="b024e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b024e-102">SYNOPSIS</span></span>
<span data-ttu-id="b024e-103">Ändrar en befintlig brand Väggs regel i en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="b024e-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="b024e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b024e-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b024e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b024e-105">DESCRIPTION</span></span>
<span data-ttu-id="b024e-106">Cmdleten **set-AzureSqlDatabaseServerFirewallRule** ändrar värdena för Start-IP-adress och slut-IP-adress för en befintlig brand Väggs regel i den angivna instansen av Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="b024e-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="b024e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b024e-107">EXAMPLES</span></span>

### <span data-ttu-id="b024e-108">Exempel 1: ändra en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b024e-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="b024e-109">Det här kommandot ändrar Start-IP-adress och slut-IP-adress för brand Väggs regeln som heter FirewallRule24 på din Azure SQL-databasserver med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b024e-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="b024e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b024e-110">PARAMETERS</span></span>

### <span data-ttu-id="b024e-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="b024e-111">-EndIpAddress</span></span>
<span data-ttu-id="b024e-112">Anger slutvärdet för IP-adressintervallet för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="b024e-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b024e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b024e-113">-Force</span></span>
<span data-ttu-id="b024e-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b024e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b024e-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="b024e-115">-Profile</span></span>
<span data-ttu-id="b024e-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b024e-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b024e-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b024e-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b024e-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b024e-118">-RuleName</span></span>
<span data-ttu-id="b024e-119">Anger namnet på brand Väggs regeln som ändras av den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b024e-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b024e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b024e-120">-ServerName</span></span>
<span data-ttu-id="b024e-121">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="b024e-121">Specifies the name of a server.</span></span>
<span data-ttu-id="b024e-122">Denna cmdlet skapar en brand Väggs regel på den server som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="b024e-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="b024e-123">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="b024e-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="b024e-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="b024e-124">-StartIpAddress</span></span>
<span data-ttu-id="b024e-125">Anger startvärdet för IP-adressintervallet för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="b024e-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b024e-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b024e-126">-Confirm</span></span>
<span data-ttu-id="b024e-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b024e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b024e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b024e-128">-WhatIf</span></span>
<span data-ttu-id="b024e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b024e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b024e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b024e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b024e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b024e-131">CommonParameters</span></span>
<span data-ttu-id="b024e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b024e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b024e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b024e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b024e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b024e-134">INPUTS</span></span>

### <span data-ttu-id="b024e-135">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="b024e-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="b024e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b024e-136">OUTPUTS</span></span>

### <span data-ttu-id="b024e-137">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="b024e-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="b024e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b024e-138">NOTES</span></span>

## <span data-ttu-id="b024e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b024e-139">RELATED LINKS</span></span>

[<span data-ttu-id="b024e-140">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="b024e-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b024e-141">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b024e-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b024e-142">Ange brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="b024e-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="b024e-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b024e-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="b024e-144">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b024e-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="b024e-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b024e-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


