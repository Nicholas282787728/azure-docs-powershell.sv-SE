---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400803"
---
# <span data-ttu-id="6851e-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="6851e-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="6851e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6851e-102">SYNOPSIS</span></span>
<span data-ttu-id="6851e-103">Skapa om nyckeln för spatialdata</span><span class="sxs-lookup"><span data-stu-id="6851e-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="6851e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6851e-104">SYNTAX</span></span>

### <span data-ttu-id="6851e-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6851e-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6851e-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6851e-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6851e-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6851e-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6851e-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6851e-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6851e-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6851e-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6851e-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6851e-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6851e-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6851e-111">DESCRIPTION</span></span>
<span data-ttu-id="6851e-112">Återskapa primär nyckeln eller sekundär nyckeln för konton med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="6851e-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="6851e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6851e-113">EXAMPLES</span></span>

### <span data-ttu-id="6851e-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6851e-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="6851e-115">Återskapa sekundär nyckeln för konton med spatiala ankare "exempel" i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="6851e-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="6851e-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6851e-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6851e-117">Återskapa sekundär nyckeln för konton med spatiala ankare "exempel" från aktuell prenumeration och resurs grupp "RG1" med rör.</span><span class="sxs-lookup"><span data-stu-id="6851e-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="6851e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6851e-118">PARAMETERS</span></span>

### <span data-ttu-id="6851e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6851e-119">-DefaultProfile</span></span>
<span data-ttu-id="6851e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6851e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6851e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6851e-121">-Force</span></span>
<span data-ttu-id="6851e-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6851e-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6851e-123">-InputObject</span></span>
<span data-ttu-id="6851e-124">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="6851e-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="6851e-125">-Name</span></span>
<span data-ttu-id="6851e-126">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="6851e-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="6851e-127">-Primary</span></span>
<span data-ttu-id="6851e-128">Återskapa primär nyckeln för ett konto med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="6851e-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6851e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6851e-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6851e-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6851e-131">-ResourceId</span></span>
<span data-ttu-id="6851e-132">Resurs-ID för konton med Spatial ankare.</span><span class="sxs-lookup"><span data-stu-id="6851e-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-133">-Sekundär</span><span class="sxs-lookup"><span data-stu-id="6851e-133">-Secondary</span></span>
<span data-ttu-id="6851e-134">Återskapa primär nyckeln för ett konto med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="6851e-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6851e-135">-Confirm</span></span>
<span data-ttu-id="6851e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6851e-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6851e-137">-WhatIf</span></span>
<span data-ttu-id="6851e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6851e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6851e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6851e-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6851e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6851e-140">CommonParameters</span></span>
<span data-ttu-id="6851e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6851e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6851e-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6851e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6851e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6851e-143">INPUTS</span></span>

### <span data-ttu-id="6851e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6851e-144">System.String</span></span>

### <span data-ttu-id="6851e-145">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="6851e-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="6851e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6851e-146">OUTPUTS</span></span>

### <span data-ttu-id="6851e-147">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6851e-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="6851e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6851e-148">NOTES</span></span>

## <span data-ttu-id="6851e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6851e-149">RELATED LINKS</span></span>
