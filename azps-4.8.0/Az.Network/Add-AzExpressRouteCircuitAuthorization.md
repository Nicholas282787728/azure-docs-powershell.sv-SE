---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262630"
---
# <span data-ttu-id="a62c5-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a62c5-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="a62c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a62c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a62c5-103">Lägger till en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a62c5-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="a62c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a62c5-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a62c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a62c5-105">DESCRIPTION</span></span>
<span data-ttu-id="a62c5-106">Cmdleten **Add-AzExpressRouteCircuitAuthorization** lägger till ett godkännande till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="a62c5-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="a62c5-107">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="a62c5-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a62c5-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk).</span><span class="sxs-lookup"><span data-stu-id="a62c5-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="a62c5-109">**Add-AzExpressRouteCircuitAuthorization** lägger till ett nytt tillstånd för en krets och på samma gång genererar motsvarande auktoriseringspost.</span><span class="sxs-lookup"><span data-stu-id="a62c5-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="a62c5-110">Dessa nycklar kan visas när som helst genom att köra Get-AzExpressRouteCircuitAuthorization cmdlet och, om det behövs, och sedan kopieras och vidarebefordras till en lämplig nätverks ägare.</span><span class="sxs-lookup"><span data-stu-id="a62c5-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="a62c5-111">Observera att när du har kört **Add-AzExpressRouteCircuitAuthorization** måste du anropa Set-AzExpressRouteCircuit cmdlet för att aktivera den.</span><span class="sxs-lookup"><span data-stu-id="a62c5-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="a62c5-112">Om du inte anropar **set-AzExpressRouteCircuit** kommer tillståndet att läggas till i kretsen men inte aktive ras för användning.</span><span class="sxs-lookup"><span data-stu-id="a62c5-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="a62c5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a62c5-113">EXAMPLES</span></span>

### <span data-ttu-id="a62c5-114">Exempel 1: lägga till ett godkännande för den angivna ExpressRoute-kretsen</span><span class="sxs-lookup"><span data-stu-id="a62c5-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="a62c5-115">Kommandona i det här exemplet lägger till ett nytt godkännande i en befintlig ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="a62c5-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="a62c5-116">Det första kommandot använder funktionen **Get-AzExpressRouteCircuit** för att skapa en objekt referens till en krets med namnet ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="a62c5-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="a62c5-117">Objekt referensen lagras i en variabel som heter $Circuit.</span><span class="sxs-lookup"><span data-stu-id="a62c5-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="a62c5-118">I det andra kommandot används cmdleten **Add-AzExpressRouteCircuitAuthorization** för att lägga till en ny auktorisering (ContosoCircuitAuthorization) i ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="a62c5-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="a62c5-119">Det här kommandot lägger till auktoriseringen men aktiverar inte den auktoriseringen.</span><span class="sxs-lookup"><span data-stu-id="a62c5-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="a62c5-120">Om du aktiverar ett godkännande krävs **set-AzExpressRouteCircuit** som visas i det sista kommandot i exemplet.</span><span class="sxs-lookup"><span data-stu-id="a62c5-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="a62c5-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a62c5-121">PARAMETERS</span></span>

### <span data-ttu-id="a62c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62c5-122">-DefaultProfile</span></span>
<span data-ttu-id="a62c5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a62c5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a62c5-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a62c5-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a62c5-125">Anger den ExpressRoute-krets som den här cmdleten lägger till för auktoriseringen.</span><span class="sxs-lookup"><span data-stu-id="a62c5-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="a62c5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a62c5-126">-Name</span></span>
<span data-ttu-id="a62c5-127">Anger namnet på den krets som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a62c5-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="a62c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62c5-128">CommonParameters</span></span>
<span data-ttu-id="a62c5-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62c5-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62c5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62c5-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a62c5-131">INPUTS</span></span>

### <span data-ttu-id="a62c5-132">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a62c5-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a62c5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a62c5-133">OUTPUTS</span></span>

### <span data-ttu-id="a62c5-134">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a62c5-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a62c5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a62c5-135">NOTES</span></span>

## <span data-ttu-id="a62c5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a62c5-136">RELATED LINKS</span></span>

[<span data-ttu-id="a62c5-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a62c5-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a62c5-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a62c5-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a62c5-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a62c5-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a62c5-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a62c5-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a62c5-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a62c5-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
