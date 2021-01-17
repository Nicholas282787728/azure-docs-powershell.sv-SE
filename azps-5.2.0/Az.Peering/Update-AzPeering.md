---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405888"
---
# <span data-ttu-id="cb643-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="cb643-101">Update-AzPeering</span></span>

## <span data-ttu-id="cb643-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb643-102">SYNOPSIS</span></span>
<span data-ttu-id="cb643-103">Anger peering.</span><span class="sxs-lookup"><span data-stu-id="cb643-103">Sets the Peering.</span></span> <span data-ttu-id="cb643-104">Använd det här kommandot tillsammans med `Set-AzDirectPeeringConnectionObject` eller `Set-AzExchangePeeringConnectionObject` .</span><span class="sxs-lookup"><span data-stu-id="cb643-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="cb643-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb643-105">SYNTAX</span></span>

### <span data-ttu-id="cb643-106">DefaultExchange (standard)</span><span class="sxs-lookup"><span data-stu-id="cb643-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb643-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="cb643-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb643-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="cb643-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb643-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="cb643-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb643-110">Utdata</span><span class="sxs-lookup"><span data-stu-id="cb643-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb643-111">Exchanger</span><span class="sxs-lookup"><span data-stu-id="cb643-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb643-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb643-112">DESCRIPTION</span></span>
<span data-ttu-id="cb643-113">Ställer in PSPeering-objektet</span><span class="sxs-lookup"><span data-stu-id="cb643-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="cb643-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb643-114">EXAMPLES</span></span>

### <span data-ttu-id="cb643-115">Uppdatera Md5-autentiseringsnyckel</span><span class="sxs-lookup"><span data-stu-id="cb643-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="cb643-116">Anger Md5-autentiseringsnyckel</span><span class="sxs-lookup"><span data-stu-id="cb643-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="cb643-117">Uppdatera UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="cb643-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="cb643-118">Anger flaggan för användning av peering-tjänsten</span><span class="sxs-lookup"><span data-stu-id="cb643-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="cb643-119">Uppdatera IPv4-adress för Exchange-peering</span><span class="sxs-lookup"><span data-stu-id="cb643-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="cb643-120">Anger IPv4-adressen för en Exchange-peering med ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb643-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="cb643-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb643-121">PARAMETERS</span></span>

### <span data-ttu-id="cb643-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb643-122">-DefaultProfile</span></span>
<span data-ttu-id="cb643-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb643-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb643-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="cb643-124">-DirectConnection</span></span>
<span data-ttu-id="cb643-125">Skapa en ny direkt förbindelse med New-AzDirectPeeringConnectionObject och pipe till det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="cb643-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb643-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="cb643-126">-ExchangeConnection</span></span>
<span data-ttu-id="cb643-127">Skapa en ny Exchange-anslutning med New-AzExchangePeeringConnectionObject och pipe till det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="cb643-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb643-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb643-128">-InputObject</span></span>
<span data-ttu-id="cb643-129">Peering-objekt</span><span class="sxs-lookup"><span data-stu-id="cb643-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb643-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb643-130">-Name</span></span>
<span data-ttu-id="cb643-131">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="cb643-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb643-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb643-132">-ResourceGroupName</span></span>
<span data-ttu-id="cb643-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cb643-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb643-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb643-134">-ResourceId</span></span>
<span data-ttu-id="cb643-135">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cb643-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb643-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb643-136">-Confirm</span></span>
<span data-ttu-id="cb643-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb643-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb643-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb643-138">-WhatIf</span></span>
<span data-ttu-id="cb643-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb643-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb643-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb643-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb643-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb643-141">CommonParameters</span></span>
<span data-ttu-id="cb643-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb643-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb643-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb643-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb643-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb643-144">INPUTS</span></span>

### <span data-ttu-id="cb643-145">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="cb643-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="cb643-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cb643-146">System.String</span></span>

## <span data-ttu-id="cb643-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb643-147">OUTPUTS</span></span>

### <span data-ttu-id="cb643-148">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="cb643-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="cb643-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb643-149">NOTES</span></span>

## <span data-ttu-id="cb643-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb643-150">RELATED LINKS</span></span>
