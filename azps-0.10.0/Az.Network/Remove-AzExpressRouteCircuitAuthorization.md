---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: ef00e209b030ed4a05ad29ccb3e768df090ea8ee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922041"
---
# <span data-ttu-id="5350f-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5350f-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="5350f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5350f-102">SYNOPSIS</span></span>
<span data-ttu-id="5350f-103">Tar bort en befintlig ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5350f-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="5350f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5350f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5350f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5350f-105">DESCRIPTION</span></span>
<span data-ttu-id="5350f-106">Cmdleten **Remove-AzExpressRouteCircuitAuthorization** tar bort ett godkännande som tilldelats en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="5350f-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="5350f-107">ExpressRoute kretsar Anslut ditt lokala nätverk till Azure med hjälp av en anslutnings tjänst i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="5350f-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="5350f-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen.</span><span class="sxs-lookup"><span data-stu-id="5350f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="5350f-109">Det kan bara finnas en auktorisering per virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5350f-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="5350f-110">Du kan när som helst använda **Remove-AzExpressRouteCircuitAuthorization** för att ta bort auktoriseringen som tilldelats ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="5350f-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="5350f-111">När det gäller det motsvarande virtuella nätverket kan du inte längre använda ExpressRoute-kretsen för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="5350f-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="5350f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5350f-112">EXAMPLES</span></span>

### <span data-ttu-id="5350f-113">Exempel 1: ta bort en krets godkännande från en ExpressRoute-krets</span><span class="sxs-lookup"><span data-stu-id="5350f-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="5350f-114">I det här exemplet tas en krets bort från en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="5350f-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="5350f-115">I det första kommandot används cmdleten **Get-AzExpressRouteCircuit** för att skapa en objekt referens till en ExpressRoute-krets som heter ContosoCircuit och lagrar resultatet i variabeln som heter $Circuit.</span><span class="sxs-lookup"><span data-stu-id="5350f-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="5350f-116">Det andra kommandot markerar det ContosoCircuitAuthorization som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5350f-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="5350f-117">Det tredje kommandot använder cmdleten Set-AzExpressRouteCircuit för att bekräfta borttagningen av ExpressRoute-kretsen som lagras i $Circuit-variabeln.</span><span class="sxs-lookup"><span data-stu-id="5350f-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="5350f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5350f-118">PARAMETERS</span></span>

### <span data-ttu-id="5350f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5350f-119">-DefaultProfile</span></span>
<span data-ttu-id="5350f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5350f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5350f-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5350f-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5350f-122">Anger det ExpressRouteCircuit-objekt som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="5350f-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5350f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5350f-123">-Name</span></span>
<span data-ttu-id="5350f-124">Anger namnet på den krets verifiering som tas bort av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5350f-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5350f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5350f-125">CommonParameters</span></span>
<span data-ttu-id="5350f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5350f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5350f-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5350f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5350f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5350f-128">INPUTS</span></span>

### <span data-ttu-id="5350f-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5350f-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5350f-130">Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** -objektet.</span><span class="sxs-lookup"><span data-stu-id="5350f-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="5350f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5350f-131">OUTPUTS</span></span>

### <span data-ttu-id="5350f-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5350f-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5350f-133">Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** -objektet.</span><span class="sxs-lookup"><span data-stu-id="5350f-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="5350f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5350f-134">NOTES</span></span>

## <span data-ttu-id="5350f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5350f-135">RELATED LINKS</span></span>

[<span data-ttu-id="5350f-136">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5350f-136">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5350f-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5350f-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5350f-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5350f-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5350f-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5350f-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5350f-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5350f-140">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)