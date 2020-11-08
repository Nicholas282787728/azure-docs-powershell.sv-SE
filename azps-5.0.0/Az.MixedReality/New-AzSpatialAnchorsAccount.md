---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270538"
---
# <span data-ttu-id="a2d27-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a2d27-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a2d27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2d27-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d27-103">Konto för att skapa spatiala ankare</span><span class="sxs-lookup"><span data-stu-id="a2d27-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="a2d27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2d27-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2d27-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d27-106">Skapa ett nytt konto för spatialdata i vissa abonnemang, resurs grupper och region.</span><span class="sxs-lookup"><span data-stu-id="a2d27-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="a2d27-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2d27-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d27-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2d27-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="a2d27-109">Skapa ett nytt konto med spatiala ankare "exempel" i aktuell prenumeration, resurs grupp "RG1" och Central.</span><span class="sxs-lookup"><span data-stu-id="a2d27-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="a2d27-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2d27-110">PARAMETERS</span></span>

### <span data-ttu-id="a2d27-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2d27-111">-Confirm</span></span>
<span data-ttu-id="a2d27-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2d27-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d27-113">-DefaultProfile</span></span>
<span data-ttu-id="a2d27-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d27-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="a2d27-115">-Location</span></span>
<span data-ttu-id="a2d27-116">Placering av fäst punkter.</span><span class="sxs-lookup"><span data-stu-id="a2d27-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="a2d27-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2d27-117">-Name</span></span>
<span data-ttu-id="a2d27-118">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="a2d27-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d27-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d27-119">-ResourceGroupName</span></span>
<span data-ttu-id="a2d27-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a2d27-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d27-121">-WhatIf</span></span>
<span data-ttu-id="a2d27-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2d27-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d27-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2d27-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d27-124">CommonParameters</span></span>
<span data-ttu-id="a2d27-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a2d27-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d27-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d27-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2d27-127">INPUTS</span></span>

### <span data-ttu-id="a2d27-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="a2d27-128">None</span></span>

## <span data-ttu-id="a2d27-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2d27-129">OUTPUTS</span></span>

### <span data-ttu-id="a2d27-130">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a2d27-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a2d27-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2d27-131">NOTES</span></span>

## <span data-ttu-id="a2d27-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2d27-132">RELATED LINKS</span></span>
