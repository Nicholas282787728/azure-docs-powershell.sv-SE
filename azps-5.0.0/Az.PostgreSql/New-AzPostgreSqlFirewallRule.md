---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270800"
---
# <span data-ttu-id="1e135-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1e135-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="1e135-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e135-102">SYNOPSIS</span></span>
<span data-ttu-id="1e135-103">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="1e135-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="1e135-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e135-104">SYNTAX</span></span>

### <span data-ttu-id="1e135-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="1e135-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e135-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="1e135-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1e135-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e135-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e135-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e135-108">DESCRIPTION</span></span>
<span data-ttu-id="1e135-109">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="1e135-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="1e135-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e135-110">EXAMPLES</span></span>

### <span data-ttu-id="1e135-111">Exempel 1: skapa en ny PostgreSql</span><span class="sxs-lookup"><span data-stu-id="1e135-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="1e135-112">Denna cmdlets skapar en PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="1e135-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="1e135-113">Exempel 2: skapa en ny PostgreSql brand Väggs regel med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="1e135-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="1e135-114">Denna cmdlets skapar en PostgreSql med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="1e135-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="1e135-115">Exempel 3: skapa en ny PostgreSql för att tillåta alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="1e135-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="1e135-116">Denna cmdlets skapar en ny PostgreSql för att tillåta alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="1e135-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="1e135-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e135-117">PARAMETERS</span></span>

### <span data-ttu-id="1e135-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="1e135-118">-AllowAll</span></span>
<span data-ttu-id="1e135-119">Finns för att tillåta alla IP-adresser, från 0.0.0.0 till 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="1e135-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e135-120">-AsJob</span></span>
<span data-ttu-id="1e135-121">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1e135-121">Run the command as a job</span></span>

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

### <span data-ttu-id="1e135-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e135-122">-ClientIPAddress</span></span>
<span data-ttu-id="1e135-123">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1e135-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="1e135-124">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="1e135-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e135-125">-DefaultProfile</span></span>
<span data-ttu-id="1e135-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e135-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e135-127">-EndIPAddress</span></span>
<span data-ttu-id="1e135-128">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1e135-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="1e135-129">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="1e135-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e135-130">-Name</span></span>
<span data-ttu-id="1e135-131">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1e135-131">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1e135-132">-NoWait</span></span>
<span data-ttu-id="1e135-133">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1e135-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e135-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e135-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e135-135">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1e135-135">The name of the resource group.</span></span>
<span data-ttu-id="1e135-136">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1e135-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1e135-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e135-137">-ServerName</span></span>
<span data-ttu-id="1e135-138">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="1e135-138">The name of the server.</span></span>

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

### <span data-ttu-id="1e135-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="1e135-139">-StartIPAddress</span></span>
<span data-ttu-id="1e135-140">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="1e135-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="1e135-141">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="1e135-141">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e135-142">-SubscriptionId</span></span>
<span data-ttu-id="1e135-143">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1e135-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e135-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e135-144">-Confirm</span></span>
<span data-ttu-id="1e135-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e135-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e135-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e135-146">-WhatIf</span></span>
<span data-ttu-id="1e135-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e135-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e135-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e135-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e135-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e135-149">CommonParameters</span></span>
<span data-ttu-id="1e135-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e135-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e135-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e135-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e135-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e135-152">INPUTS</span></span>

## <span data-ttu-id="1e135-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e135-153">OUTPUTS</span></span>

### <span data-ttu-id="1e135-154">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1e135-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="1e135-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e135-155">NOTES</span></span>

<span data-ttu-id="1e135-156">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1e135-156">ALIASES</span></span>

## <span data-ttu-id="1e135-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e135-157">RELATED LINKS</span></span>
