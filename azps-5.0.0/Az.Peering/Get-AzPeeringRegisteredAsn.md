---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269611"
---
# <span data-ttu-id="24928-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="24928-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="24928-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24928-102">SYNOPSIS</span></span>
<span data-ttu-id="24928-103">Hämtar det registrerade ASN för Internet Exchange routing Server types.</span><span class="sxs-lookup"><span data-stu-id="24928-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="24928-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24928-104">SYNTAX</span></span>

### <span data-ttu-id="24928-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="24928-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24928-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="24928-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24928-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24928-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24928-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24928-108">DESCRIPTION</span></span>
<span data-ttu-id="24928-109">Skaffa eller Visa en lista över ASN.</span><span class="sxs-lookup"><span data-stu-id="24928-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="24928-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24928-110">EXAMPLES</span></span>

### <span data-ttu-id="24928-111">Lista över registrerade ASNs för peering</span><span class="sxs-lookup"><span data-stu-id="24928-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="24928-112">Listor registrerade ASN.</span><span class="sxs-lookup"><span data-stu-id="24928-112">Lists registered asn.</span></span>

### <span data-ttu-id="24928-113">Hämtar registrerade ASN för peering efter namn</span><span class="sxs-lookup"><span data-stu-id="24928-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="24928-114">Får registrerade peering-ASN.</span><span class="sxs-lookup"><span data-stu-id="24928-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="24928-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24928-115">PARAMETERS</span></span>

### <span data-ttu-id="24928-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24928-116">-DefaultProfile</span></span>
<span data-ttu-id="24928-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24928-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24928-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24928-118">-InputObject</span></span>
<span data-ttu-id="24928-119">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="24928-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="24928-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="24928-120">-Name</span></span>
<span data-ttu-id="24928-121">Namnet på det registrerade ASN</span><span class="sxs-lookup"><span data-stu-id="24928-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="24928-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="24928-122">-PeeringName</span></span>
<span data-ttu-id="24928-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="24928-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="24928-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24928-124">-ResourceGroupName</span></span>
<span data-ttu-id="24928-125">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="24928-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="24928-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24928-126">-ResourceId</span></span>
<span data-ttu-id="24928-127">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="24928-127">The resource id string name.</span></span>

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

### <span data-ttu-id="24928-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24928-128">CommonParameters</span></span>
<span data-ttu-id="24928-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24928-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24928-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24928-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24928-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24928-131">INPUTS</span></span>

### <span data-ttu-id="24928-132">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="24928-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="24928-133">System. String</span><span class="sxs-lookup"><span data-stu-id="24928-133">System.String</span></span>

## <span data-ttu-id="24928-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24928-134">OUTPUTS</span></span>

### <span data-ttu-id="24928-135">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="24928-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="24928-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24928-136">NOTES</span></span>

## <span data-ttu-id="24928-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24928-137">RELATED LINKS</span></span>