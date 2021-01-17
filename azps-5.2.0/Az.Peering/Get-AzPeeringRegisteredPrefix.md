---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408355"
---
# <span data-ttu-id="f2538-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="f2538-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="f2538-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2538-102">SYNOPSIS</span></span>
<span data-ttu-id="f2538-103">Hämtar eller visar det registrerade prefixet för peers.</span><span class="sxs-lookup"><span data-stu-id="f2538-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="f2538-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2538-104">SYNTAX</span></span>

### <span data-ttu-id="f2538-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="f2538-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2538-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f2538-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2538-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2538-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2538-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2538-108">DESCRIPTION</span></span>
<span data-ttu-id="f2538-109">Hämtar eller visar det registrerade prefixet för peers.</span><span class="sxs-lookup"><span data-stu-id="f2538-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="f2538-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2538-110">EXAMPLES</span></span>

### <span data-ttu-id="f2538-111">Lista över registrerade ASNs för peering</span><span class="sxs-lookup"><span data-stu-id="f2538-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="f2538-112">Listor registrerade ASN.</span><span class="sxs-lookup"><span data-stu-id="f2538-112">Lists registered asn.</span></span>

### <span data-ttu-id="f2538-113">Hämtar registrerade ASN för peering efter namn</span><span class="sxs-lookup"><span data-stu-id="f2538-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="f2538-114">Får registrerade peering-ASN.</span><span class="sxs-lookup"><span data-stu-id="f2538-114">Gets registered peering asn.</span></span>

<span data-ttu-id="f2538-115">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="f2538-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="f2538-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2538-116">PARAMETERS</span></span>

### <span data-ttu-id="f2538-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2538-117">-DefaultProfile</span></span>
<span data-ttu-id="f2538-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2538-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2538-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2538-119">-InputObject</span></span>
<span data-ttu-id="f2538-120">Använda en Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f2538-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="f2538-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2538-121">-Name</span></span>
<span data-ttu-id="f2538-122">Prefixets namn.</span><span class="sxs-lookup"><span data-stu-id="f2538-122">The name of prefix.</span></span>

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

### <span data-ttu-id="f2538-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="f2538-123">-PeeringName</span></span>
<span data-ttu-id="f2538-124">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f2538-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f2538-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2538-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2538-126">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="f2538-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f2538-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2538-127">-ResourceId</span></span>
<span data-ttu-id="f2538-128">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f2538-128">The resource id string name.</span></span>

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

### <span data-ttu-id="f2538-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2538-129">CommonParameters</span></span>
<span data-ttu-id="f2538-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2538-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2538-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2538-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2538-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2538-132">INPUTS</span></span>

### <span data-ttu-id="f2538-133">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f2538-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="f2538-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2538-134">System.String</span></span>

## <span data-ttu-id="f2538-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2538-135">OUTPUTS</span></span>

### <span data-ttu-id="f2538-136">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="f2538-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="f2538-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2538-137">NOTES</span></span>

## <span data-ttu-id="f2538-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2538-138">RELATED LINKS</span></span>
