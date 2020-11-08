---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262178"
---
# <span data-ttu-id="a0223-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0223-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="a0223-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0223-102">SYNOPSIS</span></span>
<span data-ttu-id="a0223-103">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="a0223-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a0223-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0223-104">SYNTAX</span></span>

### <span data-ttu-id="a0223-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="a0223-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0223-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a0223-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a0223-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0223-107">DESCRIPTION</span></span>
<span data-ttu-id="a0223-108">Skapar eller uppdaterar en befintlig virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="a0223-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a0223-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0223-109">EXAMPLES</span></span>

### <span data-ttu-id="a0223-110">Exempel 1: uppdatera MariaDB för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="a0223-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="a0223-111">Det här kommandot uppdaterar en virtuell nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="a0223-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="a0223-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0223-112">PARAMETERS</span></span>

### <span data-ttu-id="a0223-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0223-113">-AsJob</span></span>
<span data-ttu-id="a0223-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="a0223-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a0223-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0223-115">-DefaultProfile</span></span>
<span data-ttu-id="a0223-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0223-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0223-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0223-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a0223-118">Skapa brand Väggs regel innan slut punkts tjänst för virtuellt nätverk har Aktiver ATS för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a0223-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a0223-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0223-119">-InputObject</span></span>
<span data-ttu-id="a0223-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a0223-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0223-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0223-121">-Name</span></span>
<span data-ttu-id="a0223-122">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="a0223-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0223-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a0223-123">-NoWait</span></span>
<span data-ttu-id="a0223-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="a0223-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0223-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0223-125">-PassThru</span></span>
<span data-ttu-id="a0223-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="a0223-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a0223-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0223-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0223-128">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="a0223-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a0223-129">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="a0223-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0223-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0223-130">-ServerName</span></span>
<span data-ttu-id="a0223-131">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a0223-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0223-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a0223-132">-SubnetId</span></span>
<span data-ttu-id="a0223-133">ARM-resurs-ID för det virtuella nätverkets undernät.</span><span class="sxs-lookup"><span data-stu-id="a0223-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0223-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0223-134">-SubscriptionId</span></span>
<span data-ttu-id="a0223-135">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a0223-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0223-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0223-136">-Confirm</span></span>
<span data-ttu-id="a0223-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0223-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0223-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0223-138">-WhatIf</span></span>
<span data-ttu-id="a0223-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0223-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0223-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0223-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0223-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0223-141">CommonParameters</span></span>
<span data-ttu-id="a0223-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0223-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0223-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0223-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0223-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0223-144">INPUTS</span></span>

### <span data-ttu-id="a0223-145">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a0223-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a0223-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0223-146">OUTPUTS</span></span>

### <span data-ttu-id="a0223-147">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0223-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="a0223-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0223-148">NOTES</span></span>

<span data-ttu-id="a0223-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a0223-149">ALIASES</span></span>

<span data-ttu-id="a0223-150">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a0223-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0223-151">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a0223-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0223-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0223-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0223-153">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a0223-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0223-154">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="a0223-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a0223-155">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="a0223-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a0223-156">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="a0223-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a0223-157">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a0223-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0223-158">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="a0223-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a0223-159">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="a0223-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a0223-160">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="a0223-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a0223-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="a0223-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a0223-162">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a0223-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a0223-163">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a0223-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a0223-164">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="a0223-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a0223-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0223-165">RELATED LINKS</span></span>

