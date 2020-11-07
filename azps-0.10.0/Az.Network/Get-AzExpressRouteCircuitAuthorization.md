---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922284"
---
# <span data-ttu-id="9a101-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9a101-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="9a101-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a101-102">SYNOPSIS</span></span>
<span data-ttu-id="9a101-103">Hämtar information om ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9a101-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="9a101-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a101-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a101-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a101-105">DESCRIPTION</span></span>
<span data-ttu-id="9a101-106">Cmdleten **Get-AzExpressRouteCircuitAuthorization** hämtar information om de godkännanden som tilldelats en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="9a101-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="9a101-107">ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet.</span><span class="sxs-lookup"><span data-stu-id="9a101-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="9a101-108">Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk).</span><span class="sxs-lookup"><span data-stu-id="9a101-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="9a101-109">Auktoriseringsregler, samt annan information om auktoriseringen, kan visas när som helst genom att köra **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="9a101-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="9a101-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a101-110">EXAMPLES</span></span>

### <span data-ttu-id="9a101-111">Exempel 1: skaffa alla ExpressRoute-godkännanden</span><span class="sxs-lookup"><span data-stu-id="9a101-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="9a101-112">De här kommandona returnerar information om alla ExpressRoute-godkännanden som är associerade med en ExpressRoute-krets.</span><span class="sxs-lookup"><span data-stu-id="9a101-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="9a101-113">I det första kommandot används cmdleten **Get-AzExpressRouteCircuit** för att skapa en objekt referens med en krets som heter ContosoCircuit; objekt referensen lagras i variabeln $Circuit.</span><span class="sxs-lookup"><span data-stu-id="9a101-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="9a101-114">Det andra kommandot använder då objekt referensen och cmdleten **Get-AzExpressRouteCircuitAuthorization** för att returnera information om godkännanden som är associerade med ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="9a101-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="9a101-115">Exempel 2: Hämta alla ExpressRoute-tillstånd med Where-Object cmdlet</span><span class="sxs-lookup"><span data-stu-id="9a101-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="9a101-116">De här kommandona representerar en variant av kommandona som används i exempel 1.</span><span class="sxs-lookup"><span data-stu-id="9a101-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="9a101-117">I det här fallet returneras informationen endast för de godkännanden som är tillgängliga för användning (det vill säga för godkännanden som inte har tilldelats ett virtuellt nätverk).</span><span class="sxs-lookup"><span data-stu-id="9a101-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="9a101-118">För att göra det här returneras information om kretsen i kommando 2 och är piped till cmdleten **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="9a101-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="9a101-119">**WHERE-objekt** gör sedan endast för de godkännanden där egenskapen *AuthorizationUseStatus* är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="9a101-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="9a101-120">Om du bara vill lista de godkännanden som inte är tillgängliga använder du denna syntax för WHERE-satsen:</span><span class="sxs-lookup"><span data-stu-id="9a101-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="9a101-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a101-121">PARAMETERS</span></span>

### <span data-ttu-id="9a101-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a101-122">-DefaultProfile</span></span>
<span data-ttu-id="9a101-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a101-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a101-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9a101-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9a101-125">Anger ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9a101-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="9a101-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a101-126">-Name</span></span>
<span data-ttu-id="9a101-127">Anger namnet på den ExpressRoute som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9a101-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="9a101-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="9a101-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="9a101-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a101-129">CommonParameters</span></span>
<span data-ttu-id="9a101-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a101-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a101-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a101-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a101-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a101-132">INPUTS</span></span>

### <span data-ttu-id="9a101-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9a101-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="9a101-134">**Get-AzExpressRouteCircuitAuthorization** accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="9a101-134">**Get-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="9a101-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a101-135">OUTPUTS</span></span>

### <span data-ttu-id="9a101-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9a101-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="9a101-137">**Get-AzExpressRouteCircuitAuthorization** returnerar instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="9a101-137">**Get-AzExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="9a101-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a101-138">NOTES</span></span>

## <span data-ttu-id="9a101-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a101-139">RELATED LINKS</span></span>

[<span data-ttu-id="9a101-140">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9a101-140">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9a101-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9a101-141">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9a101-142">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9a101-142">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9a101-143">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9a101-143">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
