---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 0f17d30b6f47effab5b0039bd56172cbe580392c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922141"
---
# <span data-ttu-id="3bd73-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3bd73-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3bd73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bd73-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd73-103">Skapar en ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3bd73-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="3bd73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bd73-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bd73-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bd73-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd73-106">Cmdleten **New-AzExpressRouteCircuitAuthorization** skapar ett krets godkännande som kan läggas till i en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3bd73-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="3bd73-107">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="3bd73-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3bd73-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta ett nätverk till kretsen.</span><span class="sxs-lookup"><span data-stu-id="3bd73-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="3bd73-109">Det kan bara finnas en auktorisering per virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="3bd73-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="3bd73-110">När du har skapat en ExpressRoute-krets kan du använda **Add-AzExpressRouteCircuitAuthorization** för att lägga till ett godkännande till kretsen.</span><span class="sxs-lookup"><span data-stu-id="3bd73-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="3bd73-111">Alternativt kan du använda **New-AzExpressRouteCircuitAuthorization** för att skapa ett godkännande som kan läggas till i en ny krets samtidigt som kretsen skapas.</span><span class="sxs-lookup"><span data-stu-id="3bd73-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="3bd73-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bd73-112">EXAMPLES</span></span>

### <span data-ttu-id="3bd73-113">Exempel 1: skapa en ny krets auktorisering</span><span class="sxs-lookup"><span data-stu-id="3bd73-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="3bd73-114">Det här kommandot skapar en ny auktorisering av kretsen med namnet ContosoCircuitAuthorization och lagrar sedan objektet i en variabel som heter $Authorization.</span><span class="sxs-lookup"><span data-stu-id="3bd73-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="3bd73-115">Det är viktigt att spara objektet till en variabel: även om det inte går att skapa en **AzExpressRouteCircuitAuthorization** kan du inte lägga till auktorisationen i ett kretsar.</span><span class="sxs-lookup"><span data-stu-id="3bd73-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="3bd73-116">I stället används variabel $Authorization New-AzExpressRouteCircuit när du skapar en helt ny ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="3bd73-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="3bd73-117">Mer information finns i dokumentationen för New-AzExpressRouteCircuit-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bd73-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="3bd73-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bd73-118">PARAMETERS</span></span>

### <span data-ttu-id="3bd73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd73-119">-DefaultProfile</span></span>
<span data-ttu-id="3bd73-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd73-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd73-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bd73-121">-Name</span></span>
<span data-ttu-id="3bd73-122">Anger ett unikt namn för den nya ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3bd73-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="3bd73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd73-123">CommonParameters</span></span>
<span data-ttu-id="3bd73-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd73-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd73-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd73-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bd73-126">INPUTS</span></span>

### <span data-ttu-id="3bd73-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="3bd73-127">None</span></span>
<span data-ttu-id="3bd73-128">Denna cmdlet accepterar inte förloppet.</span><span class="sxs-lookup"><span data-stu-id="3bd73-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="3bd73-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bd73-129">OUTPUTS</span></span>

### <span data-ttu-id="3bd73-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3bd73-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="3bd73-131">Denna cmdlet skapar instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization** -objektet.</span><span class="sxs-lookup"><span data-stu-id="3bd73-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="3bd73-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bd73-132">NOTES</span></span>

## <span data-ttu-id="3bd73-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bd73-133">RELATED LINKS</span></span>

[<span data-ttu-id="3bd73-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3bd73-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3bd73-135">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3bd73-135">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3bd73-136">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3bd73-136">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

