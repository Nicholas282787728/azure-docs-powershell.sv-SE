---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 6a8c81f8c130f322e868c91e18c7fff7b1175d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584116"
---
# <span data-ttu-id="c496b-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c496b-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="c496b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c496b-102">SYNOPSIS</span></span>
<span data-ttu-id="c496b-103">Tar bort en befintlig ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c496b-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c496b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c496b-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c496b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c496b-105">DESCRIPTION</span></span>
<span data-ttu-id="c496b-106">Cmdleten **Remove-AzureRmExpressRouteCircuitAuthorization** tar bort ett godkännande som tilldelats en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="c496b-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="c496b-107">ExpressRoute kretsar Anslut ditt lokala nätverk till Azure med hjälp av en anslutnings tjänst i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="c496b-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="c496b-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen.</span><span class="sxs-lookup"><span data-stu-id="c496b-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="c496b-109">Det kan bara finnas en auktorisering per virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="c496b-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="c496b-110">Du kan när som helst använda **Remove-AzureRmExpressRouteCircuitAuthorization** för att ta bort auktoriseringen som tilldelats ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="c496b-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="c496b-111">När det gäller det motsvarande virtuella nätverket kan du inte längre använda ExpressRoute-kretsen för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="c496b-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="c496b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c496b-112">EXAMPLES</span></span>

### <span data-ttu-id="c496b-113">Exempel 1: ta bort en krets godkännande från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="c496b-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="c496b-114">I det här exemplet tas en krets bort från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="c496b-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="c496b-115">I det första kommandot används cmdleten **Get-AzureRmExpressRouteCircuit** för att skapa en objekt referens till en ExpressRoute-krets som heter ContosoCircuit och lagrar resultatet i variabeln som heter $Circuit.</span><span class="sxs-lookup"><span data-stu-id="c496b-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="c496b-116">Det andra kommandot markerar det ContosoCircuitAuthorization som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c496b-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="c496b-117">Det tredje kommandot använder cmdleten Set-AzureRmExpressRouteCircuit för att bekräfta borttagningen av ExpressRoute-kretsen som lagras i $Circuit-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c496b-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="c496b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c496b-118">PARAMETERS</span></span>

### <span data-ttu-id="c496b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c496b-119">-DefaultProfile</span></span>
<span data-ttu-id="c496b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c496b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c496b-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c496b-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c496b-122">Anger det ExpressRouteCircuit-objekt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c496b-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c496b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c496b-123">-Name</span></span>
<span data-ttu-id="c496b-124">Anger namnet på den krets verifiering som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c496b-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c496b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c496b-125">CommonParameters</span></span>
<span data-ttu-id="c496b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c496b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c496b-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c496b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c496b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c496b-128">INPUTS</span></span>

### <span data-ttu-id="c496b-129">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c496b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="c496b-130">Parametrar: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c496b-130">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="c496b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c496b-131">OUTPUTS</span></span>

### <span data-ttu-id="c496b-132">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c496b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c496b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c496b-133">NOTES</span></span>

## <span data-ttu-id="c496b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c496b-134">RELATED LINKS</span></span>

[<span data-ttu-id="c496b-135">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c496b-135">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c496b-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c496b-136">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c496b-137">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c496b-137">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c496b-138">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c496b-138">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c496b-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c496b-139">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
