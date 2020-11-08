---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099199"
---
# <span data-ttu-id="c28c4-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c28c4-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="c28c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c28c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c28c4-103">Skapar en brand Väggs regel i Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="c28c4-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="c28c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c28c4-104">SYNTAX</span></span>

### <span data-ttu-id="c28c4-105">IpRange (standard)</span><span class="sxs-lookup"><span data-stu-id="c28c4-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c28c4-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="c28c4-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c28c4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c28c4-107">DESCRIPTION</span></span>
<span data-ttu-id="c28c4-108">Cmdleten **New-AzureSqlDatabaseServerFirewallRule** skapar en brand Väggs regel i den angivna instansen av Azure SQL Database Server i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c28c4-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="c28c4-109">Använd parametrarna *StartIpAddress* och *EndIpAddress* för att ange ett intervall med IP-adresser som den här regeln tillåter att ansluta till Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="c28c4-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="c28c4-110">Ange parametern *AllowAllAzureServices* om du vill skapa en regel som tillåter Azure-anslutningar till servern.</span><span class="sxs-lookup"><span data-stu-id="c28c4-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="c28c4-111">Regeln har start-och slut värden för IP-adresserna 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="c28c4-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="c28c4-112">Om du inte anger något namn för en brand Väggs regel tilldelar denna cmdlet standard namnet AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="c28c4-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="c28c4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c28c4-113">EXAMPLES</span></span>

### <span data-ttu-id="c28c4-114">Exempel 1: skapa en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="c28c4-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="c28c4-115">Det här kommandot skapar en brand Väggs regel FirewallRule24 på en Azure SQL-databasserver med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c28c4-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="c28c4-116">Kommandot anger ett IP-adressintervall.</span><span class="sxs-lookup"><span data-stu-id="c28c4-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="c28c4-117">Exempel 2: skapa en regel som tillåter alla Azure-tjänster</span><span class="sxs-lookup"><span data-stu-id="c28c4-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="c28c4-118">Det här kommandot skapar en brand Väggs regel med namnet AzureConnections på servern med namnet lpqd0zbr8y som tillåter Azure-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="c28c4-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="c28c4-119">Exempel 3: skapa en regel som gör att alla Azure-tjänster som använder standard namnet skapar en regel som tillåter alla Azure-tjänster som använder standard namnet</span><span class="sxs-lookup"><span data-stu-id="c28c4-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="c28c4-120">Det här kommandot skapar en brand Väggs regel på den angivna servern med namnet lpqd0zbr8y som tillåter Azure-anslutningar.</span><span class="sxs-lookup"><span data-stu-id="c28c4-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="c28c4-121">Kommandot tilldelar standard regel namnet AllowAllAzureServices.</span><span class="sxs-lookup"><span data-stu-id="c28c4-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="c28c4-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c28c4-122">PARAMETERS</span></span>

### <span data-ttu-id="c28c4-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="c28c4-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="c28c4-124">Visar att den här brand Väggs regeln gör att alla Azure IP-adresser kan komma åt servern.</span><span class="sxs-lookup"><span data-stu-id="c28c4-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28c4-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c28c4-125">-EndIpAddress</span></span>
<span data-ttu-id="c28c4-126">Anger slutvärdet för IP-adressintervallet för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="c28c4-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28c4-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c28c4-127">-Force</span></span>
<span data-ttu-id="c28c4-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c28c4-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c28c4-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="c28c4-129">-Profile</span></span>
<span data-ttu-id="c28c4-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c28c4-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c28c4-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c28c4-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c28c4-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="c28c4-132">-RuleName</span></span>
<span data-ttu-id="c28c4-133">Anger namnet på den nya brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="c28c4-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28c4-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c28c4-134">-ServerName</span></span>
<span data-ttu-id="c28c4-135">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="c28c4-135">Specifies the name of a server.</span></span>
<span data-ttu-id="c28c4-136">Denna cmdlet skapar en brand Väggs regel på den server som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="c28c4-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="c28c4-137">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="c28c4-137">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="c28c4-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c28c4-138">-StartIpAddress</span></span>
<span data-ttu-id="c28c4-139">Anger startvärdet för IP-adressintervallet för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="c28c4-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28c4-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c28c4-140">-Confirm</span></span>
<span data-ttu-id="c28c4-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c28c4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28c4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28c4-142">-WhatIf</span></span>
<span data-ttu-id="c28c4-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c28c4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28c4-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c28c4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28c4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28c4-145">CommonParameters</span></span>
<span data-ttu-id="c28c4-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c28c4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28c4-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c28c4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28c4-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c28c4-148">INPUTS</span></span>

## <span data-ttu-id="c28c4-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c28c4-149">OUTPUTS</span></span>

### <span data-ttu-id="c28c4-150">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="c28c4-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="c28c4-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c28c4-151">NOTES</span></span>

## <span data-ttu-id="c28c4-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c28c4-152">RELATED LINKS</span></span>

[<span data-ttu-id="c28c4-153">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="c28c4-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c28c4-154">Skapa brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="c28c4-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="c28c4-155">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c28c4-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c28c4-156">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c28c4-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c28c4-157">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c28c4-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="c28c4-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c28c4-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


