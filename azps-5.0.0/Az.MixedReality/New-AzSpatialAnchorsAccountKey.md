---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270537"
---
# <span data-ttu-id="34e2f-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="34e2f-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="34e2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="34e2f-103">Skapa om nyckeln för spatialdata</span><span class="sxs-lookup"><span data-stu-id="34e2f-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="34e2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34e2f-104">SYNTAX</span></span>

### <span data-ttu-id="34e2f-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e2f-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e2f-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e2f-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e2f-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e2f-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e2f-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e2f-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e2f-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e2f-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e2f-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="34e2f-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e2f-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34e2f-111">DESCRIPTION</span></span>
<span data-ttu-id="34e2f-112">Återskapa primär nyckeln eller sekundär nyckeln för konton med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="34e2f-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="34e2f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34e2f-113">EXAMPLES</span></span>

### <span data-ttu-id="34e2f-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34e2f-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="34e2f-115">Återskapa sekundär nyckeln för konton med spatiala ankare "exempel" i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="34e2f-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="34e2f-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="34e2f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="34e2f-117">Återskapa sekundär nyckeln för konton med spatiala ankare "exempel" från aktuell prenumeration och resurs grupp "RG1" med rör.</span><span class="sxs-lookup"><span data-stu-id="34e2f-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="34e2f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34e2f-118">PARAMETERS</span></span>

### <span data-ttu-id="34e2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e2f-119">-DefaultProfile</span></span>
<span data-ttu-id="34e2f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34e2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34e2f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="34e2f-121">-Force</span></span>
<span data-ttu-id="34e2f-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="34e2f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34e2f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34e2f-123">-InputObject</span></span>
<span data-ttu-id="34e2f-124">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="34e2f-124">The custom domain object.</span></span>

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

### <span data-ttu-id="34e2f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="34e2f-125">-Name</span></span>
<span data-ttu-id="34e2f-126">Konto namn för spatialdata.</span><span class="sxs-lookup"><span data-stu-id="34e2f-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="34e2f-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="34e2f-127">-Primary</span></span>
<span data-ttu-id="34e2f-128">Återskapa primär nyckeln för ett konto med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="34e2f-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="34e2f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e2f-129">-ResourceGroupName</span></span>
<span data-ttu-id="34e2f-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="34e2f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="34e2f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34e2f-131">-ResourceId</span></span>
<span data-ttu-id="34e2f-132">Resurs-ID för konton med Spatial ankare.</span><span class="sxs-lookup"><span data-stu-id="34e2f-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="34e2f-133">-Sekundär</span><span class="sxs-lookup"><span data-stu-id="34e2f-133">-Secondary</span></span>
<span data-ttu-id="34e2f-134">Återskapa primär nyckeln för ett konto med spatiala ankare.</span><span class="sxs-lookup"><span data-stu-id="34e2f-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="34e2f-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34e2f-135">-Confirm</span></span>
<span data-ttu-id="34e2f-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34e2f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e2f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e2f-137">-WhatIf</span></span>
<span data-ttu-id="34e2f-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34e2f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34e2f-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34e2f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e2f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e2f-140">CommonParameters</span></span>
<span data-ttu-id="34e2f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e2f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="34e2f-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e2f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e2f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34e2f-143">INPUTS</span></span>

### <span data-ttu-id="34e2f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="34e2f-144">System.String</span></span>

### <span data-ttu-id="34e2f-145">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="34e2f-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="34e2f-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34e2f-146">OUTPUTS</span></span>

### <span data-ttu-id="34e2f-147">Microsoft. Azure. commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="34e2f-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="34e2f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34e2f-148">NOTES</span></span>

## <span data-ttu-id="34e2f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34e2f-149">RELATED LINKS</span></span>
