---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929310"
---
# <span data-ttu-id="52ae7-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="52ae7-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="52ae7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="52ae7-103">Tar bort en befintlig ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="52ae7-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ae7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52ae7-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52ae7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52ae7-105">DESCRIPTION</span></span>
<span data-ttu-id="52ae7-106">Cmdleten **Remove-AzureRmExpressRouteCircuitAuthorization** tar bort ett godkännande som tilldelats en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="52ae7-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="52ae7-107">ExpressRoute kretsar Anslut ditt lokala nätverk till Azure med hjälp av en anslutnings tjänst i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="52ae7-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="52ae7-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen.</span><span class="sxs-lookup"><span data-stu-id="52ae7-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="52ae7-109">Det kan bara finnas en auktorisering per virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="52ae7-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="52ae7-110">Du kan när som helst använda **Remove-AzureRmExpressRouteCircuitAuthorization** för att ta bort auktoriseringen som tilldelats ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="52ae7-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="52ae7-111">När det gäller det motsvarande virtuella nätverket kan du inte längre använda ExpressRoute-kretsen för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="52ae7-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="52ae7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52ae7-112">EXAMPLES</span></span>

### <span data-ttu-id="52ae7-113">Exempel 1: ta bort en krets godkännande från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="52ae7-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="52ae7-114">I det här exemplet tas en krets bort från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="52ae7-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="52ae7-115">I det första kommandot används cmdleten **Get-AzureRmExpressRouteCircuit** för att skapa en objekt referens till en ExpressRoute-krets som heter ContosoCircuit och lagrar resultatet i variabeln som heter $Circuit.</span><span class="sxs-lookup"><span data-stu-id="52ae7-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="52ae7-116">Det andra kommandot markerar det ContosoCircuitAuthorization som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="52ae7-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="52ae7-117">Det tredje kommandot använder cmdleten Set-AzureRmExpressRouteCircuit för att bekräfta borttagningen av ExpressRoute-kretsen som lagras i $Circuit-variabeln.</span><span class="sxs-lookup"><span data-stu-id="52ae7-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="52ae7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52ae7-118">PARAMETERS</span></span>

### <span data-ttu-id="52ae7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ae7-119">-DefaultProfile</span></span>
<span data-ttu-id="52ae7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52ae7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ae7-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52ae7-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="52ae7-122">Anger det ExpressRouteCircuit-objekt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="52ae7-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52ae7-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="52ae7-123">-Name</span></span>
<span data-ttu-id="52ae7-124">Anger namnet på den krets verifiering som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ae7-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ae7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ae7-125">CommonParameters</span></span>
<span data-ttu-id="52ae7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ae7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ae7-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ae7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ae7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52ae7-128">INPUTS</span></span>

### <span data-ttu-id="52ae7-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52ae7-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="52ae7-130">Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** -objektet.</span><span class="sxs-lookup"><span data-stu-id="52ae7-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="52ae7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52ae7-131">OUTPUTS</span></span>

### <span data-ttu-id="52ae7-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52ae7-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="52ae7-133">Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** -objektet.</span><span class="sxs-lookup"><span data-stu-id="52ae7-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="52ae7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52ae7-134">NOTES</span></span>

## <span data-ttu-id="52ae7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52ae7-135">RELATED LINKS</span></span>

[<span data-ttu-id="52ae7-136">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="52ae7-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="52ae7-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52ae7-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="52ae7-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="52ae7-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="52ae7-139">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="52ae7-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="52ae7-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="52ae7-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
