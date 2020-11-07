---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929721"
---
# <span data-ttu-id="7ec7e-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7ec7e-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="7ec7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ec7e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec7e-103">Skapar en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ec7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ec7e-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ec7e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ec7e-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec7e-106">Cmdleten **New-AzureRmExpressRouteCircuitAuthorization** skapar ett krets godkännande som kan läggas till i en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="7ec7e-107">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="7ec7e-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta ett nätverk till kretsen.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="7ec7e-109">Det kan bara finnas en auktorisering per virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="7ec7e-110">När du har skapat en ExpressRoute-krets kan du använda **Add-AzureRmExpressRouteCircuitAuthorization** för att lägga till ett godkännande till kretsen.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="7ec7e-111">Alternativt kan du använda **New-AzureRmExpressRouteCircuitAuthorization** för att skapa ett godkännande som kan läggas till i en ny krets samtidigt som kretsen skapas.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="7ec7e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ec7e-112">EXAMPLES</span></span>

### <span data-ttu-id="7ec7e-113">Exempel 1: skapa en ny krets auktorisering</span><span class="sxs-lookup"><span data-stu-id="7ec7e-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="7ec7e-114">Det här kommandot skapar en ny auktorisering av kretsen med namnet ContosoCircuitAuthorization och lagrar sedan objektet i en variabel som heter $Authorization.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="7ec7e-115">Det är viktigt att spara objektet till en variabel: även om det inte går att skapa en **AzureRmExpressRouteCircuitAuthorization** kan du inte lägga till auktorisationen i ett kretsar.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="7ec7e-116">I stället används variabel $Authorization New-AzureRmExpressRouteCircuit när du skapar en helt ny ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="7ec7e-117">Mer information finns i dokumentationen för New-AzureRmExpressRouteCircuit-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="7ec7e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ec7e-118">PARAMETERS</span></span>

### <span data-ttu-id="7ec7e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec7e-119">-DefaultProfile</span></span>
<span data-ttu-id="7ec7e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ec7e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ec7e-121">-Name</span></span>
<span data-ttu-id="7ec7e-122">Anger ett unikt namn för den nya ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ec7e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec7e-123">CommonParameters</span></span>
<span data-ttu-id="7ec7e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec7e-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec7e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec7e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ec7e-126">INPUTS</span></span>

### <span data-ttu-id="7ec7e-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="7ec7e-127">None</span></span>
<span data-ttu-id="7ec7e-128">Denna cmdlet accepterar inte förloppet.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="7ec7e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ec7e-129">OUTPUTS</span></span>

### <span data-ttu-id="7ec7e-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7ec7e-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="7ec7e-131">Denna cmdlet skapar instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization** -objektet.</span><span class="sxs-lookup"><span data-stu-id="7ec7e-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="7ec7e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ec7e-132">NOTES</span></span>

## <span data-ttu-id="7ec7e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ec7e-133">RELATED LINKS</span></span>

[<span data-ttu-id="7ec7e-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7ec7e-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7ec7e-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7ec7e-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7ec7e-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7ec7e-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

