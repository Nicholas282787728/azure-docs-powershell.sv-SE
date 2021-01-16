---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: f7e0f511c42dd6eda730380a02e0d46239bf045e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390681"
---
# <span data-ttu-id="97934-101">New-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97934-101">New-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="97934-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97934-102">SYNOPSIS</span></span>
<span data-ttu-id="97934-103">Skapar en ny brand Väggs regel för MySQL-flexibel Server</span><span class="sxs-lookup"><span data-stu-id="97934-103">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="97934-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97934-104">SYNTAX</span></span>

### <span data-ttu-id="97934-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="97934-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97934-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="97934-106">AllowAll</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97934-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="97934-107">ClientIPAddress</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97934-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97934-108">DESCRIPTION</span></span>
<span data-ttu-id="97934-109">Skapar en ny brand Väggs regel för MySQL-flexibel Server</span><span class="sxs-lookup"><span data-stu-id="97934-109">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="97934-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97934-110">EXAMPLES</span></span>

### <span data-ttu-id="97934-111">Exempel 1: skapa en ny server brand Väggs regel för MySql</span><span class="sxs-lookup"><span data-stu-id="97934-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="97934-112">Denna cmdlets skapar en server brand Väggs regel för MySql.</span><span class="sxs-lookup"><span data-stu-id="97934-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="97934-113">Exempel 2: skapa en ny MySql Firewall-regel med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="97934-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="97934-114">Denna cmdletar skapar en MySql-brandväggsregel med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="97934-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="97934-115">Exempel 3: skapa en ny MySql Firewall-regel för att tillåta alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="97934-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="97934-116">Denna cmdlets skapar en ny MySql Firewall-regel som tillåter alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="97934-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="97934-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97934-117">PARAMETERS</span></span>

### <span data-ttu-id="97934-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="97934-118">-AllowAll</span></span>
<span data-ttu-id="97934-119">Finns för att tillåta alla IP-adresser, från 0.0.0.0 till 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="97934-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="97934-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97934-120">-AsJob</span></span>
<span data-ttu-id="97934-121">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="97934-121">Run the command as a job</span></span>

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

### <span data-ttu-id="97934-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="97934-122">-ClientIPAddress</span></span>
<span data-ttu-id="97934-123">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="97934-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="97934-124">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="97934-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="97934-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97934-125">-DefaultProfile</span></span>
<span data-ttu-id="97934-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97934-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97934-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="97934-127">-EndIPAddress</span></span>
<span data-ttu-id="97934-128">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="97934-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="97934-129">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="97934-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="97934-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="97934-130">-Name</span></span>
<span data-ttu-id="97934-131">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="97934-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="97934-132">Om inget anges är standardvärdet odefinierat.</span><span class="sxs-lookup"><span data-stu-id="97934-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="97934-133">Om AllowAll finns är standard namnet AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="97934-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="97934-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="97934-134">-NoWait</span></span>
<span data-ttu-id="97934-135">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="97934-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="97934-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97934-136">-ResourceGroupName</span></span>
<span data-ttu-id="97934-137">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="97934-137">The name of the resource group.</span></span>
<span data-ttu-id="97934-138">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="97934-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="97934-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97934-139">-ServerName</span></span>
<span data-ttu-id="97934-140">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="97934-140">The name of the server.</span></span>

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

### <span data-ttu-id="97934-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="97934-141">-StartIPAddress</span></span>
<span data-ttu-id="97934-142">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="97934-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="97934-143">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="97934-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="97934-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97934-144">-SubscriptionId</span></span>
<span data-ttu-id="97934-145">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="97934-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="97934-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97934-146">-Confirm</span></span>
<span data-ttu-id="97934-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97934-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97934-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97934-148">-WhatIf</span></span>
<span data-ttu-id="97934-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97934-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97934-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97934-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97934-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97934-151">CommonParameters</span></span>
<span data-ttu-id="97934-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97934-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97934-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97934-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97934-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97934-154">INPUTS</span></span>

## <span data-ttu-id="97934-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97934-155">OUTPUTS</span></span>

### <span data-ttu-id="97934-156">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97934-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="97934-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97934-157">NOTES</span></span>

<span data-ttu-id="97934-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="97934-158">ALIASES</span></span>

## <span data-ttu-id="97934-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97934-159">RELATED LINKS</span></span>

