---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322191"
---
# <span data-ttu-id="a6c39-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a6c39-101">New-AzPeering</span></span>

## <span data-ttu-id="a6c39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6c39-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c39-103">Skapar en ny peering ARM-resurs</span><span class="sxs-lookup"><span data-stu-id="a6c39-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="a6c39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6c39-104">SYNTAX</span></span>

### <span data-ttu-id="a6c39-105">Exchange (standard)</span><span class="sxs-lookup"><span data-stu-id="a6c39-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c39-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="a6c39-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c39-107">Utdata</span><span class="sxs-lookup"><span data-stu-id="a6c39-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6c39-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6c39-108">DESCRIPTION</span></span>
<span data-ttu-id="a6c39-109">Skapar en ARM peering för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6c39-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="a6c39-110">Mer information om hur du skapar ett Connection-objekt finns i [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) eller [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) .</span><span class="sxs-lookup"><span data-stu-id="a6c39-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="a6c39-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6c39-111">EXAMPLES</span></span>

### <span data-ttu-id="a6c39-112">Skapa ny direkt peering</span><span class="sxs-lookup"><span data-stu-id="a6c39-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="a6c39-113">Skapa en ny direkt peering med en enda anslutning vid Malmö med PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="a6c39-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="a6c39-114">Skapa ny Exchange-peering</span><span class="sxs-lookup"><span data-stu-id="a6c39-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a6c39-115">Skapa en ny Exchange-peering</span><span class="sxs-lookup"><span data-stu-id="a6c39-115">Create a new exchange peering</span></span>

### <span data-ttu-id="a6c39-116">Konvertera bakåtkompatibel peering till ARM-peering</span><span class="sxs-lookup"><span data-stu-id="a6c39-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="a6c39-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6c39-117">PARAMETERS</span></span>

### <span data-ttu-id="a6c39-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6c39-118">-AsJob</span></span>
<span data-ttu-id="a6c39-119">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="a6c39-119">Run in the background.</span></span>

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

### <span data-ttu-id="a6c39-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c39-120">-DefaultProfile</span></span>
<span data-ttu-id="a6c39-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c39-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="a6c39-122">-DirectConnection</span></span>
<span data-ttu-id="a6c39-123">Skapa en ny direkt förbindelse med New-AzExchangePeeringConnection och pipe till det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="a6c39-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a6c39-124">-ExchangeConnection</span></span>
<span data-ttu-id="a6c39-125">Skapa en ny Exchange-anslutning med New-AzExchangePeeringConnection och pipe till det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="a6c39-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6c39-126">-InputObject</span></span>
<span data-ttu-id="a6c39-127">Använd Get-AzLegacyPeering för att hämta det här objektet.</span><span class="sxs-lookup"><span data-stu-id="a6c39-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="a6c39-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="a6c39-129">Välj det Microsoft-nätverk du vill använda.</span><span class="sxs-lookup"><span data-stu-id="a6c39-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6c39-130">-Name</span></span>
<span data-ttu-id="a6c39-131">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a6c39-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c39-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="a6c39-133">Resurs-ID för peer-PNRP. Använd Get-AzPeerAsn för att hämta ID.</span><span class="sxs-lookup"><span data-stu-id="a6c39-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a6c39-134">-PeeringLocation</span></span>
<span data-ttu-id="a6c39-135">Den fysiska platsen skiljer sig från Azure-regionen.</span><span class="sxs-lookup"><span data-stu-id="a6c39-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="a6c39-136">Använd \<kind\> Orts namn Get-AzPeeringLocation-as-tangenten.</span><span class="sxs-lookup"><span data-stu-id="a6c39-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c39-137">-ResourceGroupName</span></span>
<span data-ttu-id="a6c39-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a6c39-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="a6c39-139">-Sku</span></span>
<span data-ttu-id="a6c39-140">Välj Basic_Direct_Free eller Premium_Direct_Free såvida det inte uttryckligen anges att välja ett annat alternativ.</span><span class="sxs-lookup"><span data-stu-id="a6c39-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c39-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a6c39-141">-Tag</span></span>
<span data-ttu-id="a6c39-142">De taggar som ska kopplas till Microsofts peering service.</span><span class="sxs-lookup"><span data-stu-id="a6c39-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="a6c39-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6c39-143">-Confirm</span></span>
<span data-ttu-id="a6c39-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6c39-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c39-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c39-145">-WhatIf</span></span>
<span data-ttu-id="a6c39-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6c39-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6c39-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6c39-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c39-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c39-148">CommonParameters</span></span>
<span data-ttu-id="a6c39-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c39-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c39-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6c39-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c39-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6c39-151">INPUTS</span></span>

### <span data-ttu-id="a6c39-152">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a6c39-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a6c39-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6c39-153">OUTPUTS</span></span>

### <span data-ttu-id="a6c39-154">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a6c39-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a6c39-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6c39-155">NOTES</span></span>

## <span data-ttu-id="a6c39-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6c39-156">RELATED LINKS</span></span>
