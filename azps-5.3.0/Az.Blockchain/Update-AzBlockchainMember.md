---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524662"
---
# <span data-ttu-id="6a6ce-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="6a6ce-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="6a6ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a6ce-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6ce-103">Uppdatera en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-103">Update a blockchain member.</span></span>

## <span data-ttu-id="6a6ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a6ce-104">SYNTAX</span></span>

### <span data-ttu-id="6a6ce-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="6a6ce-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6a6ce-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a6ce-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6a6ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a6ce-107">DESCRIPTION</span></span>
<span data-ttu-id="6a6ce-108">Uppdatera en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-108">Update a blockchain member.</span></span>

## <span data-ttu-id="6a6ce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a6ce-109">EXAMPLES</span></span>

### <span data-ttu-id="6a6ce-110">Exempel 1: uppdatera en blockchain medlem</span><span class="sxs-lookup"><span data-stu-id="6a6ce-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="6a6ce-111">Det här kommandot uppdaterar en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="6a6ce-112">Exempel 2: uppdatera en blockchain-medlem</span><span class="sxs-lookup"><span data-stu-id="6a6ce-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="6a6ce-113">Det här kommandot uppdaterar en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="6a6ce-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a6ce-114">PARAMETERS</span></span>

### <span data-ttu-id="6a6ce-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="6a6ce-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="6a6ce-116">Anger lösen ordet för hanterings konto för hanterade konsortier.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-116">Sets the managed consortium management account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6ce-117">-DefaultProfile</span></span>
<span data-ttu-id="6a6ce-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a6ce-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="6a6ce-119">-FirewallRule</span></span>
<span data-ttu-id="6a6ce-120">Hämtar eller anger brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="6a6ce-121">För att konstruera kan du läsa avsnittet anteckningar för FIREWALLRULE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6ce-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a6ce-122">-InputObject</span></span>
<span data-ttu-id="6a6ce-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a6ce-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a6ce-124">-Name</span></span>
<span data-ttu-id="6a6ce-125">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6ce-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="6a6ce-126">-Password</span></span>
<span data-ttu-id="6a6ce-127">Ställer in DNS Endpoint Basic auth-lösenordet för noden Transaction Node.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-127">Sets the transaction node dns endpoint basic auth password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a6ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a6ce-129">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6a6ce-130">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6a6ce-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a6ce-131">-SubscriptionId</span></span>
<span data-ttu-id="6a6ce-132">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a6ce-133">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a6ce-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6a6ce-134">-Tag</span></span>
<span data-ttu-id="6a6ce-135">Taggar för tjänsten som är en lista över viktiga värde par som beskriver resursen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a6ce-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a6ce-136">-Confirm</span></span>
<span data-ttu-id="6a6ce-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a6ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a6ce-138">-WhatIf</span></span>
<span data-ttu-id="6a6ce-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a6ce-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a6ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6ce-141">CommonParameters</span></span>
<span data-ttu-id="6a6ce-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6ce-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a6ce-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6ce-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a6ce-144">INPUTS</span></span>

### <span data-ttu-id="6a6ce-145">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="6a6ce-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="6a6ce-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a6ce-146">OUTPUTS</span></span>

### <span data-ttu-id="6a6ce-147">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="6a6ce-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="6a6ce-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a6ce-148">NOTES</span></span>

<span data-ttu-id="6a6ce-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6a6ce-149">ALIASES</span></span>

<span data-ttu-id="6a6ce-150">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="6a6ce-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a6ce-151">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a6ce-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a6ce-153">FIREWALLRULE <IFirewallRule [] >: hämtar eller anger brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="6a6ce-154">`[EndIPAddress <String>]`: Hämtar eller anger den sista IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="6a6ce-155">`[RuleName <String>]`: Hämtar eller anger namnet på brand Väggs reglerna.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="6a6ce-156">`[StartIPAddress <String>]`: Hämtar eller anger Start-IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="6a6ce-157">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6a6ce-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a6ce-158">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="6a6ce-159">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6a6ce-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a6ce-160">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="6a6ce-161">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="6a6ce-162">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6a6ce-163">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6a6ce-164">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="6a6ce-165">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="6a6ce-166">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="6a6ce-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="6a6ce-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a6ce-167">RELATED LINKS</span></span>

