---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 5b277ca35071c3639a3c7b341451cea78c024901
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584948"
---
# <span data-ttu-id="4bc92-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4bc92-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="4bc92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bc92-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc92-103">Hämtar information om ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4bc92-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bc92-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bc92-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bc92-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc92-106">Cmdleten **Get-AzureRmExpressRouteCircuitAuthorization** hämtar information om de godkännanden som tilldelats en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="4bc92-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="4bc92-107">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="4bc92-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="4bc92-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk).</span><span class="sxs-lookup"><span data-stu-id="4bc92-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="4bc92-109">Auktoriseringsregler, samt annan information om auktoriseringen, kan visas när som helst genom att köra **Get-AzureRmExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="4bc92-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="4bc92-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bc92-110">EXAMPLES</span></span>

### <span data-ttu-id="4bc92-111">Exempel 1: skaffa alla ExpressRoute-godkännanden</span><span class="sxs-lookup"><span data-stu-id="4bc92-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="4bc92-112">De här kommandona returnerar information om alla ExpressRoute-godkännanden som är associerade med en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="4bc92-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="4bc92-113">I det första kommandot används cmdleten **Get-AzureRmExpressRouteCircuit** för att skapa en objekt referens med en krets som heter ContosoCircuit; objekt referensen lagras i variabeln $Circuit.</span><span class="sxs-lookup"><span data-stu-id="4bc92-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="4bc92-114">Det andra kommandot använder då objekt referensen och cmdleten **Get-AzureRmExpressRouteCircuitAuthorization** för att returnera information om godkännanden som är associerade med ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="4bc92-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="4bc92-115">Exempel 2: Hämta alla ExpressRoute-tillstånd med Where-Object cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bc92-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="4bc92-116">De här kommandona representerar en variant av kommandona som används i exempel 1.</span><span class="sxs-lookup"><span data-stu-id="4bc92-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="4bc92-117">I det här fallet returneras informationen endast för de godkännanden som är tillgängliga för användning (det vill säga för godkännanden som inte har tilldelats ett virtuellt nätverk).</span><span class="sxs-lookup"><span data-stu-id="4bc92-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="4bc92-118">För att göra det här returneras information om kretsen i kommando 2 och är piped till cmdleten **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="4bc92-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="4bc92-119">**WHERE-objekt** gör sedan endast för de godkännanden där egenskapen *AuthorizationUseStatus* är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="4bc92-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="4bc92-120">Om du bara vill lista de godkännanden som inte är tillgängliga använder du denna syntax för WHERE-satsen: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="4bc92-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="4bc92-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bc92-121">PARAMETERS</span></span>

### <span data-ttu-id="4bc92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc92-122">-DefaultProfile</span></span>
<span data-ttu-id="4bc92-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc92-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bc92-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bc92-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4bc92-125">Anger ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4bc92-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="4bc92-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="4bc92-126">-Name</span></span>
<span data-ttu-id="4bc92-127">Anger namnet på den ExpressRoute som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="4bc92-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="4bc92-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="4bc92-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="4bc92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc92-129">CommonParameters</span></span>
<span data-ttu-id="4bc92-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc92-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc92-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc92-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bc92-132">INPUTS</span></span>

### <span data-ttu-id="4bc92-133">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bc92-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="4bc92-134">Parametrar: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bc92-134">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="4bc92-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bc92-135">OUTPUTS</span></span>

### <span data-ttu-id="4bc92-136">Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4bc92-136">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="4bc92-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bc92-137">NOTES</span></span>

## <span data-ttu-id="4bc92-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bc92-138">RELATED LINKS</span></span>

[<span data-ttu-id="4bc92-139">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4bc92-139">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4bc92-140">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bc92-140">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4bc92-141">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4bc92-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="4bc92-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="4bc92-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
