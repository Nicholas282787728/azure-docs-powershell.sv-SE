---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103276"
---
# <span data-ttu-id="36b74-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="36b74-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="36b74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36b74-102">SYNOPSIS</span></span>
<span data-ttu-id="36b74-103">Uppdatera noden Transaction.</span><span class="sxs-lookup"><span data-stu-id="36b74-103">Update the transaction node.</span></span>

## <span data-ttu-id="36b74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36b74-104">SYNTAX</span></span>

### <span data-ttu-id="36b74-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="36b74-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36b74-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36b74-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36b74-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36b74-107">DESCRIPTION</span></span>
<span data-ttu-id="36b74-108">Uppdatera noden Transaction.</span><span class="sxs-lookup"><span data-stu-id="36b74-108">Update the transaction node.</span></span>

## <span data-ttu-id="36b74-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36b74-109">EXAMPLES</span></span>

### <span data-ttu-id="36b74-110">Exempel 1: uppdatera en transcation-nod</span><span class="sxs-lookup"><span data-stu-id="36b74-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="36b74-111">Det här kommandot uppdaterar en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="36b74-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="36b74-112">Exempel 2: uppdatera en transcation-nod</span><span class="sxs-lookup"><span data-stu-id="36b74-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="36b74-113">Det här kommandot uppdaterar en Transaction-nod.</span><span class="sxs-lookup"><span data-stu-id="36b74-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="36b74-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36b74-114">PARAMETERS</span></span>

### <span data-ttu-id="36b74-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="36b74-115">-BlockchainMemberName</span></span>
<span data-ttu-id="36b74-116">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="36b74-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="36b74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b74-117">-DefaultProfile</span></span>
<span data-ttu-id="36b74-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36b74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b74-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="36b74-119">-FirewallRule</span></span>
<span data-ttu-id="36b74-120">Hämtar eller anger brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="36b74-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="36b74-121">För att konstruera kan du läsa avsnittet anteckningar för FIREWALLRULE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="36b74-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="36b74-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b74-122">-InputObject</span></span>
<span data-ttu-id="36b74-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="36b74-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36b74-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="36b74-124">-Name</span></span>
<span data-ttu-id="36b74-125">Nodnamn för transaktion.</span><span class="sxs-lookup"><span data-stu-id="36b74-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b74-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="36b74-126">-Password</span></span>
<span data-ttu-id="36b74-127">Ställer in DNS Endpoint Basic auth-lösenordet för noden Transaction Node.</span><span class="sxs-lookup"><span data-stu-id="36b74-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="36b74-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b74-128">-ResourceGroupName</span></span>
<span data-ttu-id="36b74-129">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="36b74-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="36b74-130">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="36b74-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="36b74-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36b74-131">-SubscriptionId</span></span>
<span data-ttu-id="36b74-132">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="36b74-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="36b74-133">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="36b74-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="36b74-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36b74-134">-Confirm</span></span>
<span data-ttu-id="36b74-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36b74-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b74-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b74-136">-WhatIf</span></span>
<span data-ttu-id="36b74-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36b74-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36b74-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36b74-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b74-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b74-139">CommonParameters</span></span>
<span data-ttu-id="36b74-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b74-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b74-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36b74-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b74-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36b74-142">INPUTS</span></span>

### <span data-ttu-id="36b74-143">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="36b74-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="36b74-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36b74-144">OUTPUTS</span></span>

### <span data-ttu-id="36b74-145">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="36b74-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="36b74-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36b74-146">NOTES</span></span>

<span data-ttu-id="36b74-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="36b74-147">ALIASES</span></span>

<span data-ttu-id="36b74-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="36b74-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36b74-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="36b74-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36b74-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36b74-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36b74-151">FIREWALLRULE <IFirewallRule [] >: hämtar eller anger brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="36b74-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="36b74-152">`[EndIPAddress <String>]`: Hämtar eller anger den sista IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="36b74-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="36b74-153">`[RuleName <String>]`: Hämtar eller anger namnet på brand Väggs reglerna.</span><span class="sxs-lookup"><span data-stu-id="36b74-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="36b74-154">`[StartIPAddress <String>]`: Hämtar eller anger Start-IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="36b74-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="36b74-155">INPUTOBJECT <IBlockchainIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="36b74-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36b74-156">`[BlockchainMemberName <String>]`: Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="36b74-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="36b74-157">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="36b74-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36b74-158">`[Location <String>]`: Plats namn.</span><span class="sxs-lookup"><span data-stu-id="36b74-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="36b74-159">`[OperationId <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="36b74-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="36b74-160">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="36b74-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="36b74-161">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="36b74-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="36b74-162">`[SubscriptionId <String>]`: Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="36b74-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="36b74-163">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="36b74-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="36b74-164">`[TransactionNodeName <String>]`: Namn på nodnamn.</span><span class="sxs-lookup"><span data-stu-id="36b74-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="36b74-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36b74-165">RELATED LINKS</span></span>

