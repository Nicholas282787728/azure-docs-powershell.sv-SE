---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103174"
---
# <span data-ttu-id="3f4fe-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f4fe-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="3f4fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4fe-103">Få nycklar till konton med spatiala ankare</span><span class="sxs-lookup"><span data-stu-id="3f4fe-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="3f4fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f4fe-104">SYNTAX</span></span>

### <span data-ttu-id="3f4fe-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f4fe-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f4fe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4fe-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f4fe-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4fe-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f4fe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f4fe-108">DESCRIPTION</span></span>
<span data-ttu-id="3f4fe-109">Få till gång till utvecklings nycklar för konton med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="3f4fe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f4fe-110">EXAMPLES</span></span>

### <span data-ttu-id="3f4fe-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f4fe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="3f4fe-112">Få till gång till utvecklings nycklar för konton med spatiala ankare "exempel" från aktuell prenumeration och resurs grupp "RG1".</span><span class="sxs-lookup"><span data-stu-id="3f4fe-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="3f4fe-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3f4fe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="3f4fe-114">Få till gång till utvecklings nycklar för konton med spatiala ankare "exempel" från aktuell prenumeration och resurs grupp "RG1" med rör.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="3f4fe-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f4fe-115">PARAMETERS</span></span>

### <span data-ttu-id="3f4fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4fe-116">-DefaultProfile</span></span>
<span data-ttu-id="3f4fe-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4fe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f4fe-118">-InputObject</span></span>
<span data-ttu-id="3f4fe-119">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4fe-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f4fe-120">-Name</span></span>
<span data-ttu-id="3f4fe-121">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f4fe-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4fe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f4fe-124">-ResourceId</span></span>
<span data-ttu-id="3f4fe-125">Resurs-ID för konton med Spatial ankare.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-125">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4fe-126">CommonParameters</span></span>
<span data-ttu-id="3f4fe-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3f4fe-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4fe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4fe-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f4fe-129">INPUTS</span></span>

### <span data-ttu-id="3f4fe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3f4fe-130">System.String</span></span>

### <span data-ttu-id="3f4fe-131">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="3f4fe-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="3f4fe-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f4fe-132">OUTPUTS</span></span>

### <span data-ttu-id="3f4fe-133">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3f4fe-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="3f4fe-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f4fe-134">NOTES</span></span>

## <span data-ttu-id="3f4fe-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f4fe-135">RELATED LINKS</span></span>
