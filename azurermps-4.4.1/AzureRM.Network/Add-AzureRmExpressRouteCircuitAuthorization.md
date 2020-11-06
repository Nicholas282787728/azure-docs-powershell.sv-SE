---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 03b9e64970be7f3d3876a3d04f26b11ac24dd8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583256"
---
# <span data-ttu-id="ac38a-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ac38a-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ac38a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac38a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac38a-103">Lägger till en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ac38a-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac38a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac38a-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac38a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac38a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac38a-106">Cmdleten **Add-AzureRmExpressRouteCircuitAuthorization** lägger till ett godkännande till en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ac38a-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="ac38a-107">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="ac38a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ac38a-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk).</span><span class="sxs-lookup"><span data-stu-id="ac38a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="ac38a-109">**Add-AzureRmExpressRouteCircuitAuthorization** lägger till ett nytt tillstånd för en krets och på samma gång genererar motsvarande auktoriseringspost.</span><span class="sxs-lookup"><span data-stu-id="ac38a-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="ac38a-110">Dessa nycklar kan visas när som helst genom att köra Get-AzureRmExpressRouteCircuitAuthorization cmdlet och, om det behövs, och sedan kopieras och vidarebefordras till en lämplig nätverks ägare.</span><span class="sxs-lookup"><span data-stu-id="ac38a-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="ac38a-111">Observera att när du har kört **Add-AzureRmExpressRouteCircuitAuthorization** måste du anropa Set-AzureRmExpressRouteCircuit cmdlet för att aktivera den.</span><span class="sxs-lookup"><span data-stu-id="ac38a-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="ac38a-112">Om du inte anropar **set-AzureRmExpressRouteCircuit** kommer tillståndet att läggas till i kretsen men inte aktive ras för användning.</span><span class="sxs-lookup"><span data-stu-id="ac38a-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="ac38a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac38a-113">EXAMPLES</span></span>

### <span data-ttu-id="ac38a-114">Exempel 1: lägga till ett godkännande för den angivna ExpressRoute-kretsen</span><span class="sxs-lookup"><span data-stu-id="ac38a-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="ac38a-115">Kommandona i det här exemplet lägger till ett nytt godkännande i en befintlig ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="ac38a-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="ac38a-116">Det första kommandot använder funktionen **Get-AzureRmExpressRouteCircuit** för att skapa en objekt referens till en krets med namnet ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="ac38a-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="ac38a-117">Objekt referensen lagras i en variabel som heter $Circuit.</span><span class="sxs-lookup"><span data-stu-id="ac38a-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="ac38a-118">I det andra kommandot används cmdleten **Add-AzureRmExpressRouteCircuitAuthorization** för att lägga till en ny auktorisering (ContosoCircuitAuthorization) i ExpressRoute-kretsen.</span><span class="sxs-lookup"><span data-stu-id="ac38a-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="ac38a-119">Det här kommandot lägger till auktoriseringen men aktiverar inte den auktoriseringen.</span><span class="sxs-lookup"><span data-stu-id="ac38a-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="ac38a-120">Om du aktiverar ett godkännande krävs **set-AzureRmExpressRouteCircuit** som visas i det sista kommandot i exemplet.</span><span class="sxs-lookup"><span data-stu-id="ac38a-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="ac38a-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac38a-121">PARAMETERS</span></span>

### <span data-ttu-id="ac38a-122">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac38a-122">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ac38a-123">Anger den ExpressRoute-krets som den här cmdleten lägger till för auktoriseringen.</span><span class="sxs-lookup"><span data-stu-id="ac38a-123">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="ac38a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac38a-124">-Name</span></span>
<span data-ttu-id="ac38a-125">Anger namnet på den krets som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="ac38a-125">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="ac38a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac38a-126">-DefaultProfile</span></span>
<span data-ttu-id="ac38a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac38a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac38a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac38a-128">CommonParameters</span></span>
<span data-ttu-id="ac38a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac38a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac38a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac38a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac38a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac38a-131">INPUTS</span></span>

### <span data-ttu-id="ac38a-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac38a-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ac38a-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepterar pipeline-instanser av objektet **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="ac38a-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="ac38a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac38a-134">OUTPUTS</span></span>

### <span data-ttu-id="ac38a-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac38a-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ac38a-136">**Add-AzureRmExpressRouteCircuitAuthorization** ändrar instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="ac38a-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="ac38a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac38a-137">NOTES</span></span>

## <span data-ttu-id="ac38a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac38a-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac38a-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac38a-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ac38a-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ac38a-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ac38a-141">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ac38a-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ac38a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ac38a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ac38a-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac38a-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
