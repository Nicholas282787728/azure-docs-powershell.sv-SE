---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915730"
---
# <span data-ttu-id="f849b-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="f849b-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="f849b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f849b-102">SYNOPSIS</span></span>
<span data-ttu-id="f849b-103">Få nycklar till konton med spatiala ankare</span><span class="sxs-lookup"><span data-stu-id="f849b-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="f849b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f849b-104">SYNTAX</span></span>

### <span data-ttu-id="f849b-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f849b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f849b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f849b-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f849b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f849b-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f849b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f849b-108">DESCRIPTION</span></span>
<span data-ttu-id="f849b-109">Få till gång till utvecklings nycklar för konton med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="f849b-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="f849b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f849b-110">EXAMPLES</span></span>

### <span data-ttu-id="f849b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f849b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="f849b-112">Få till gång till utvecklings nycklar för konton med spatiala ankare "exempel" från aktuell prenumeration och resurs grupp "RG1".</span><span class="sxs-lookup"><span data-stu-id="f849b-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="f849b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f849b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="f849b-114">Få till gång till utvecklings nycklar för konton med spatiala ankare "exempel" från aktuell prenumeration och resurs grupp "RG1" med rör.</span><span class="sxs-lookup"><span data-stu-id="f849b-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="f849b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f849b-115">PARAMETERS</span></span>

### <span data-ttu-id="f849b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f849b-116">-DefaultProfile</span></span>
<span data-ttu-id="f849b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f849b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f849b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f849b-118">-InputObject</span></span>
<span data-ttu-id="f849b-119">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="f849b-119">The custom domain object.</span></span>

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

### <span data-ttu-id="f849b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f849b-120">-Name</span></span>
<span data-ttu-id="f849b-121">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="f849b-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="f849b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f849b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f849b-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f849b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f849b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f849b-124">-ResourceId</span></span>
<span data-ttu-id="f849b-125">Resurs-ID för konton med Spatial ankare.</span><span class="sxs-lookup"><span data-stu-id="f849b-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="f849b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f849b-126">CommonParameters</span></span>
<span data-ttu-id="f849b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f849b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f849b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f849b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f849b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f849b-129">INPUTS</span></span>

### <span data-ttu-id="f849b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f849b-130">System.String</span></span>

### <span data-ttu-id="f849b-131">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f849b-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f849b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f849b-132">OUTPUTS</span></span>

### <span data-ttu-id="f849b-133">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f849b-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="f849b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f849b-134">NOTES</span></span>

## <span data-ttu-id="f849b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f849b-135">RELATED LINKS</span></span>
