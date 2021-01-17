---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399000"
---
# <span data-ttu-id="47dbd-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="47dbd-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="47dbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="47dbd-103">Skapa eller uppdatera Transaction-noden.</span><span class="sxs-lookup"><span data-stu-id="47dbd-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="47dbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47dbd-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47dbd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="47dbd-106">Skapa eller uppdatera Transaction-noden.</span><span class="sxs-lookup"><span data-stu-id="47dbd-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="47dbd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47dbd-107">EXAMPLES</span></span>

### <span data-ttu-id="47dbd-108">Exempel 1: skapa en blockchain</span><span class="sxs-lookup"><span data-stu-id="47dbd-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="47dbd-109">Det här kommandot skapar en blockchain.</span><span class="sxs-lookup"><span data-stu-id="47dbd-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="47dbd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47dbd-110">PARAMETERS</span></span>

### <span data-ttu-id="47dbd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47dbd-111">-AsJob</span></span>
<span data-ttu-id="47dbd-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="47dbd-112">Run the command as a job</span></span>

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

### <span data-ttu-id="47dbd-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="47dbd-113">-BlockchainMemberName</span></span>
<span data-ttu-id="47dbd-114">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="47dbd-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="47dbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dbd-115">-DefaultProfile</span></span>
<span data-ttu-id="47dbd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47dbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47dbd-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="47dbd-117">-FirewallRule</span></span>
<span data-ttu-id="47dbd-118">Hämtar eller anger brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="47dbd-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="47dbd-119">För att konstruera kan du läsa avsnittet anteckningar för FIREWALLRULE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="47dbd-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="47dbd-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="47dbd-120">-Location</span></span>
<span data-ttu-id="47dbd-121">Hämtar eller anger noden för transaktionsloggfiler.</span><span class="sxs-lookup"><span data-stu-id="47dbd-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="47dbd-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="47dbd-122">-Name</span></span>
<span data-ttu-id="47dbd-123">Nodnamn för transaktion.</span><span class="sxs-lookup"><span data-stu-id="47dbd-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dbd-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="47dbd-124">-NoWait</span></span>
<span data-ttu-id="47dbd-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="47dbd-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47dbd-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="47dbd-126">-Password</span></span>
<span data-ttu-id="47dbd-127">Ställer in DNS Endpoint Basic auth-lösenordet för noden Transaction Node.</span><span class="sxs-lookup"><span data-stu-id="47dbd-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="47dbd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47dbd-128">-ResourceGroupName</span></span>
<span data-ttu-id="47dbd-129">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="47dbd-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="47dbd-130">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="47dbd-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="47dbd-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47dbd-131">-SubscriptionId</span></span>
<span data-ttu-id="47dbd-132">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="47dbd-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47dbd-133">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="47dbd-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47dbd-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47dbd-134">-Confirm</span></span>
<span data-ttu-id="47dbd-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47dbd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47dbd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dbd-136">-WhatIf</span></span>
<span data-ttu-id="47dbd-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47dbd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47dbd-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47dbd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47dbd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dbd-139">CommonParameters</span></span>
<span data-ttu-id="47dbd-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47dbd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dbd-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47dbd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dbd-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47dbd-142">INPUTS</span></span>

## <span data-ttu-id="47dbd-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47dbd-143">OUTPUTS</span></span>

### <span data-ttu-id="47dbd-144">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="47dbd-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="47dbd-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47dbd-145">NOTES</span></span>

<span data-ttu-id="47dbd-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="47dbd-146">ALIASES</span></span>

<span data-ttu-id="47dbd-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="47dbd-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47dbd-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="47dbd-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47dbd-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47dbd-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47dbd-150">FIREWALLRULE <IFirewallRule [] >: hämtar eller anger brand Väggs regler.</span><span class="sxs-lookup"><span data-stu-id="47dbd-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="47dbd-151">`[EndIPAddress <String>]`: Hämtar eller anger den sista IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="47dbd-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="47dbd-152">`[RuleName <String>]`: Hämtar eller anger namnet på brand Väggs reglerna.</span><span class="sxs-lookup"><span data-stu-id="47dbd-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="47dbd-153">`[StartIPAddress <String>]`: Hämtar eller anger Start-IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="47dbd-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="47dbd-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47dbd-154">RELATED LINKS</span></span>

