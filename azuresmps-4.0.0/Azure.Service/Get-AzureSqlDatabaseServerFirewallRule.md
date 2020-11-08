---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093298"
---
# <span data-ttu-id="325eb-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="325eb-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="325eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="325eb-102">SYNOPSIS</span></span>
<span data-ttu-id="325eb-103">Hämtar brand Väggs regler för Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="325eb-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="325eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="325eb-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="325eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="325eb-105">DESCRIPTION</span></span>
<span data-ttu-id="325eb-106">Cmdleten **Get-AzureSqlDatabaseServerFirewallRule** hämtar brand Väggs regler för en instans av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="325eb-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="325eb-107">Om du anger en brand Väggs regel efter namn returnerar denna cmdlet information om den brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="325eb-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="325eb-108">Annars returnerar cmdleten information om alla brand Väggs regler på den angivna Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="325eb-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="325eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="325eb-109">EXAMPLES</span></span>

### <span data-ttu-id="325eb-110">Exempel 1: Hämta alla brand Väggs regler på en server</span><span class="sxs-lookup"><span data-stu-id="325eb-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="325eb-111">Det här kommandot får alla brand Väggs regler på en Azure SQL Database-Server med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="325eb-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="325eb-112">Exempel 2: skaffa en brand Väggs regel genom att använda dess namn</span><span class="sxs-lookup"><span data-stu-id="325eb-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="325eb-113">Det här kommandot får brand Väggs regeln som heter FirewallRule24 på den server som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="325eb-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="325eb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="325eb-114">PARAMETERS</span></span>

### <span data-ttu-id="325eb-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="325eb-115">-Profile</span></span>
<span data-ttu-id="325eb-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="325eb-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="325eb-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="325eb-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="325eb-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="325eb-118">-RuleName</span></span>
<span data-ttu-id="325eb-119">Anger namnet på den brand Väggs regel som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="325eb-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="325eb-120">-ServerName</span></span>
<span data-ttu-id="325eb-121">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="325eb-121">Specifies the name of a server.</span></span>
<span data-ttu-id="325eb-122">Denna cmdlet tar Brand Väggs regler från den server som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="325eb-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="325eb-123">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="325eb-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="325eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325eb-124">CommonParameters</span></span>
<span data-ttu-id="325eb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325eb-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325eb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325eb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="325eb-127">INPUTS</span></span>

### <span data-ttu-id="325eb-128">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="325eb-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="325eb-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="325eb-129">OUTPUTS</span></span>

### <span data-ttu-id="325eb-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="325eb-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="325eb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="325eb-131">NOTES</span></span>

## <span data-ttu-id="325eb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="325eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="325eb-133">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="325eb-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="325eb-134">List brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="325eb-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="325eb-135">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="325eb-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="325eb-136">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="325eb-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="325eb-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="325eb-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="325eb-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="325eb-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


