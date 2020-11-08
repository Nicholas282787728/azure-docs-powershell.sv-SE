---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102391"
---
# <span data-ttu-id="87638-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="87638-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="87638-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87638-102">SYNOPSIS</span></span>
<span data-ttu-id="87638-103">Skapa en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="87638-103">Create a blockchain member.</span></span>

## <span data-ttu-id="87638-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87638-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87638-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87638-105">DESCRIPTION</span></span>
<span data-ttu-id="87638-106">Skapa en blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="87638-106">Create a blockchain member.</span></span>

## <span data-ttu-id="87638-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87638-107">EXAMPLES</span></span>

### <span data-ttu-id="87638-108">Exempel 1: skapa en ny blockchain-medlem</span><span class="sxs-lookup"><span data-stu-id="87638-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="87638-109">Det här kommandot skapar en ny blockchain-medlem.</span><span class="sxs-lookup"><span data-stu-id="87638-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="87638-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87638-110">PARAMETERS</span></span>

### <span data-ttu-id="87638-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87638-111">-AsJob</span></span>
<span data-ttu-id="87638-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="87638-112">Run the command as a job</span></span>

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

### <span data-ttu-id="87638-113">-Konsortium</span><span class="sxs-lookup"><span data-stu-id="87638-113">-Consortium</span></span>
<span data-ttu-id="87638-114">Hämtar eller anger konsortiet för blockchain-medlemmen.</span><span class="sxs-lookup"><span data-stu-id="87638-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="87638-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="87638-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="87638-116">Anger lösen ordet för hanterings konto för hanterade konsortier.</span><span class="sxs-lookup"><span data-stu-id="87638-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="87638-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="87638-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="87638-118">Hämtar visnings namnet för medlemmen i konsortiet.</span><span class="sxs-lookup"><span data-stu-id="87638-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="87638-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="87638-119">-ConsortiumRole</span></span>
<span data-ttu-id="87638-120">Får rollen som medlem i konsortiet.</span><span class="sxs-lookup"><span data-stu-id="87638-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="87638-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87638-121">-DefaultProfile</span></span>
<span data-ttu-id="87638-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87638-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87638-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="87638-123">-FirewallRule</span></span>
<span data-ttu-id="87638-124">Hämtar eller anger brand Väggs regler att skapa, se avsnittet anteckningar för FIREWALLRULE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="87638-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="87638-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="87638-125">-Location</span></span>
<span data-ttu-id="87638-126">GEO-platsen för blockchain-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="87638-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="87638-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="87638-127">-Name</span></span>
<span data-ttu-id="87638-128">Blockchain medlems namn.</span><span class="sxs-lookup"><span data-stu-id="87638-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87638-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="87638-129">-NoWait</span></span>
<span data-ttu-id="87638-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="87638-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87638-131">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="87638-131">-Password</span></span>
<span data-ttu-id="87638-132">Anger lösen ordet för grundläggande autentisering för blockchain medlem.</span><span class="sxs-lookup"><span data-stu-id="87638-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="87638-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="87638-133">-Protocol</span></span>
<span data-ttu-id="87638-134">Hämtar eller anger protokollet blockchain.</span><span class="sxs-lookup"><span data-stu-id="87638-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87638-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87638-135">-ResourceGroupName</span></span>
<span data-ttu-id="87638-136">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="87638-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="87638-137">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="87638-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="87638-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="87638-138">-Sku</span></span>
<span data-ttu-id="87638-139">Hämtar eller anger SKU-namn</span><span class="sxs-lookup"><span data-stu-id="87638-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="87638-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="87638-140">-SkuTier</span></span>
<span data-ttu-id="87638-141">Hämtar eller anger SKU-nivå</span><span class="sxs-lookup"><span data-stu-id="87638-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="87638-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87638-142">-SubscriptionId</span></span>
<span data-ttu-id="87638-143">Hämtar det prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="87638-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="87638-144">Prenumerations-ID är en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="87638-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="87638-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="87638-145">-Tag</span></span>
<span data-ttu-id="87638-146">Taggar för tjänsten som är en lista över viktiga värde par som beskriver resursen.</span><span class="sxs-lookup"><span data-stu-id="87638-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="87638-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="87638-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="87638-148">Hämtar eller anger nodernas kapacitet.</span><span class="sxs-lookup"><span data-stu-id="87638-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87638-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87638-149">-Confirm</span></span>
<span data-ttu-id="87638-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87638-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87638-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87638-151">-WhatIf</span></span>
<span data-ttu-id="87638-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87638-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87638-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87638-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87638-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87638-154">CommonParameters</span></span>
<span data-ttu-id="87638-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87638-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87638-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87638-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87638-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87638-157">INPUTS</span></span>

## <span data-ttu-id="87638-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87638-158">OUTPUTS</span></span>

### <span data-ttu-id="87638-159">Microsoft. Azure. PowerShell. cmdletar. blockchain. Models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="87638-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="87638-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87638-160">NOTES</span></span>

<span data-ttu-id="87638-161">ALIAS</span><span class="sxs-lookup"><span data-stu-id="87638-161">ALIASES</span></span>

<span data-ttu-id="87638-162">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="87638-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87638-163">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="87638-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87638-164">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87638-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87638-165">FIREWALLRULE <IFirewallRule [] >: hämtar eller anger brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="87638-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="87638-166">`[EndIPAddress <String>]`: Hämtar eller anger den sista IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="87638-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="87638-167">`[RuleName <String>]`: Hämtar eller anger namnet på brand Väggs reglerna.</span><span class="sxs-lookup"><span data-stu-id="87638-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="87638-168">`[StartIPAddress <String>]`: Hämtar eller anger Start-IP-adressen för brand Väggs regel området.</span><span class="sxs-lookup"><span data-stu-id="87638-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="87638-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87638-169">RELATED LINKS</span></span>

