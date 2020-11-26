---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262023"
---
# <span data-ttu-id="35517-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="35517-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="35517-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35517-102">SYNOPSIS</span></span>
<span data-ttu-id="35517-103">Hämtar det registrerade ASN för Internet Exchange routing Server types.</span><span class="sxs-lookup"><span data-stu-id="35517-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="35517-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35517-104">SYNTAX</span></span>

### <span data-ttu-id="35517-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="35517-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35517-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="35517-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35517-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35517-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35517-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35517-108">DESCRIPTION</span></span>
<span data-ttu-id="35517-109">Skaffa eller Visa en lista över ASN.</span><span class="sxs-lookup"><span data-stu-id="35517-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="35517-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35517-110">EXAMPLES</span></span>

### <span data-ttu-id="35517-111">Lista över registrerade ASNs för peering</span><span class="sxs-lookup"><span data-stu-id="35517-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="35517-112">Listor registrerade ASN.</span><span class="sxs-lookup"><span data-stu-id="35517-112">Lists registered asn.</span></span>

### <span data-ttu-id="35517-113">Hämtar registrerade ASN för peering efter namn</span><span class="sxs-lookup"><span data-stu-id="35517-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="35517-114">Får registrerade peering-ASN.</span><span class="sxs-lookup"><span data-stu-id="35517-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="35517-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35517-115">PARAMETERS</span></span>

### <span data-ttu-id="35517-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35517-116">-DefaultProfile</span></span>
<span data-ttu-id="35517-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35517-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35517-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35517-118">-InputObject</span></span>
<span data-ttu-id="35517-119">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="35517-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35517-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="35517-120">-Name</span></span>
<span data-ttu-id="35517-121">Namnet på det registrerade ASN</span><span class="sxs-lookup"><span data-stu-id="35517-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35517-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="35517-122">-PeeringName</span></span>
<span data-ttu-id="35517-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="35517-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35517-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35517-124">-ResourceGroupName</span></span>
<span data-ttu-id="35517-125">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="35517-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35517-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35517-126">-ResourceId</span></span>
<span data-ttu-id="35517-127">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="35517-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35517-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35517-128">CommonParameters</span></span>
<span data-ttu-id="35517-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35517-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35517-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35517-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35517-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35517-131">INPUTS</span></span>

### <span data-ttu-id="35517-132">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="35517-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="35517-133">System. String</span><span class="sxs-lookup"><span data-stu-id="35517-133">System.String</span></span>

## <span data-ttu-id="35517-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35517-134">OUTPUTS</span></span>

### <span data-ttu-id="35517-135">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="35517-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="35517-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35517-136">NOTES</span></span>

## <span data-ttu-id="35517-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35517-137">RELATED LINKS</span></span>