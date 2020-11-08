---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273328"
---
# <span data-ttu-id="83753-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="83753-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="83753-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83753-102">SYNOPSIS</span></span>
<span data-ttu-id="83753-103">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="83753-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="83753-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83753-104">SYNTAX</span></span>

### <span data-ttu-id="83753-105">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="83753-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83753-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="83753-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="83753-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="83753-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83753-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83753-108">DESCRIPTION</span></span>
<span data-ttu-id="83753-109">Skapar en ny brand Väggs regel eller uppdaterar en befintlig brand Väggs regel.</span><span class="sxs-lookup"><span data-stu-id="83753-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="83753-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83753-110">EXAMPLES</span></span>

### <span data-ttu-id="83753-111">Exempel 1: skapa en brand Väggs regel under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="83753-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="83753-112">Det här kommandot skapar en brand Väggs regel under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="83753-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="83753-113">Exempel 2: skapa en ny MariaDB brand Väggs regel med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="83753-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="83753-114">Denna cmdlets skapar en MariaDB med-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="83753-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="83753-115">Exempel 3: skapa en ny MariaDB för att tillåta alla IP-adresser</span><span class="sxs-lookup"><span data-stu-id="83753-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="83753-116">Denna cmdlets skapar en ny MariaDB för att tillåta alla IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="83753-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="83753-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83753-117">PARAMETERS</span></span>

### <span data-ttu-id="83753-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="83753-118">-AllowAll</span></span>
<span data-ttu-id="83753-119">Finns för att tillåta alla IP-adresser, från 0.0.0.0 till 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="83753-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="83753-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83753-120">-AsJob</span></span>
<span data-ttu-id="83753-121">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="83753-121">Run the command as a job</span></span>

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

### <span data-ttu-id="83753-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="83753-122">-ClientIPAddress</span></span>
<span data-ttu-id="83753-123">Klienten angav en IP-adress för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="83753-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="83753-124">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="83753-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="83753-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83753-125">-DefaultProfile</span></span>
<span data-ttu-id="83753-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83753-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83753-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="83753-127">-EndIPAddress</span></span>
<span data-ttu-id="83753-128">Sista IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="83753-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="83753-129">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="83753-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="83753-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="83753-130">-Name</span></span>
<span data-ttu-id="83753-131">Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="83753-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="83753-132">Om inget anges är standardvärdet odefinierat.</span><span class="sxs-lookup"><span data-stu-id="83753-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="83753-133">Om AllowAll finns är standard namnet AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="83753-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="83753-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="83753-134">-NoWait</span></span>
<span data-ttu-id="83753-135">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="83753-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83753-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83753-136">-ResourceGroupName</span></span>
<span data-ttu-id="83753-137">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="83753-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83753-138">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="83753-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="83753-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83753-139">-ServerName</span></span>
<span data-ttu-id="83753-140">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="83753-140">The name of the server.</span></span>

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

### <span data-ttu-id="83753-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="83753-141">-StartIPAddress</span></span>
<span data-ttu-id="83753-142">Den första IP-adressen för Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="83753-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="83753-143">Måste vara IPv4-format.</span><span class="sxs-lookup"><span data-stu-id="83753-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="83753-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83753-144">-SubscriptionId</span></span>
<span data-ttu-id="83753-145">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="83753-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="83753-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83753-146">-Confirm</span></span>
<span data-ttu-id="83753-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83753-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83753-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83753-148">-WhatIf</span></span>
<span data-ttu-id="83753-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83753-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83753-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83753-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83753-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83753-151">CommonParameters</span></span>
<span data-ttu-id="83753-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83753-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83753-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83753-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83753-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83753-154">INPUTS</span></span>

## <span data-ttu-id="83753-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83753-155">OUTPUTS</span></span>

### <span data-ttu-id="83753-156">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="83753-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="83753-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83753-157">NOTES</span></span>

<span data-ttu-id="83753-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83753-158">ALIASES</span></span>

## <span data-ttu-id="83753-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83753-159">RELATED LINKS</span></span>

