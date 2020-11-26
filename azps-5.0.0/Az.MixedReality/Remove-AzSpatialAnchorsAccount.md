---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270527"
---
# <span data-ttu-id="1110e-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="1110e-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="1110e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1110e-102">SYNOPSIS</span></span>
<span data-ttu-id="1110e-103">Ta bort konton för spatialdata</span><span class="sxs-lookup"><span data-stu-id="1110e-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="1110e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1110e-104">SYNTAX</span></span>

### <span data-ttu-id="1110e-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1110e-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1110e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1110e-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1110e-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="1110e-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1110e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1110e-108">DESCRIPTION</span></span>
<span data-ttu-id="1110e-109">Ta bort det angivna kontot för spatiala ankare från vissa abonnemang och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="1110e-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="1110e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1110e-110">EXAMPLES</span></span>

### <span data-ttu-id="1110e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1110e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="1110e-112">Ta bort kontot för spatialdata "exempel" från aktuell prenumeration och resurs grupp "RG1".</span><span class="sxs-lookup"><span data-stu-id="1110e-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="1110e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1110e-113">PARAMETERS</span></span>

### <span data-ttu-id="1110e-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1110e-114">-Confirm</span></span>
<span data-ttu-id="1110e-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1110e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1110e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1110e-116">-DefaultProfile</span></span>
<span data-ttu-id="1110e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1110e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1110e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1110e-118">-InputObject</span></span>
<span data-ttu-id="1110e-119">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="1110e-119">The custom domain object.</span></span>

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

### <span data-ttu-id="1110e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1110e-120">-Name</span></span>
<span data-ttu-id="1110e-121">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="1110e-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="1110e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1110e-122">-PassThru</span></span>
<span data-ttu-id="1110e-123">Returnera objekt om det anges.</span><span class="sxs-lookup"><span data-stu-id="1110e-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1110e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1110e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1110e-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1110e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1110e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1110e-126">-ResourceId</span></span>
<span data-ttu-id="1110e-127">Resurs-ID för konton med Spatial ankare.</span><span class="sxs-lookup"><span data-stu-id="1110e-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="1110e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1110e-128">-WhatIf</span></span>
<span data-ttu-id="1110e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1110e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1110e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1110e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1110e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1110e-131">CommonParameters</span></span>
<span data-ttu-id="1110e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1110e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1110e-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1110e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1110e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1110e-134">INPUTS</span></span>

### <span data-ttu-id="1110e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1110e-135">System.String</span></span>

### <span data-ttu-id="1110e-136">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="1110e-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="1110e-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1110e-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1110e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1110e-138">OUTPUTS</span></span>

### <span data-ttu-id="1110e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1110e-139">System.Boolean</span></span>

## <span data-ttu-id="1110e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1110e-140">NOTES</span></span>

## <span data-ttu-id="1110e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1110e-141">RELATED LINKS</span></span>