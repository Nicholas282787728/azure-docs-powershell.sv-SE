---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272860"
---
# <span data-ttu-id="db376-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="db376-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="db376-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db376-102">SYNOPSIS</span></span>
<span data-ttu-id="db376-103">Ta bort en virtuell enhets webbplats från en virtuell enhets resurs för nätverk.</span><span class="sxs-lookup"><span data-stu-id="db376-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="db376-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db376-104">SYNTAX</span></span>

### <span data-ttu-id="db376-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db376-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db376-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db376-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db376-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db376-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db376-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db376-108">DESCRIPTION</span></span>
<span data-ttu-id="db376-109">Med kommandot Remove-AzVirtualApplianceSite tas en virtuell enhet bort från en virtuell enhets resurs för nätverk.</span><span class="sxs-lookup"><span data-stu-id="db376-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="db376-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db376-110">EXAMPLES</span></span>

### <span data-ttu-id="db376-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db376-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="db376-112">Ta bort en webbplats resurs för en virtuell enhet.</span><span class="sxs-lookup"><span data-stu-id="db376-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="db376-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db376-113">PARAMETERS</span></span>

### <span data-ttu-id="db376-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db376-114">-AsJob</span></span>
<span data-ttu-id="db376-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="db376-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db376-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db376-116">-DefaultProfile</span></span>
<span data-ttu-id="db376-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db376-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db376-118">-Force</span><span class="sxs-lookup"><span data-stu-id="db376-118">-Force</span></span>
<span data-ttu-id="db376-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="db376-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="db376-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="db376-120">-Name</span></span>
<span data-ttu-id="db376-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="db376-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="db376-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="db376-123">Resurs-ID för den virtuella nätverks enhet som är kopplad till den här webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="db376-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db376-124">-PassThru</span></span>
<span data-ttu-id="db376-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="db376-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="db376-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="db376-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db376-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db376-127">-ResourceGroupName</span></span>
<span data-ttu-id="db376-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="db376-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db376-129">-ResourceId</span></span>
<span data-ttu-id="db376-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="db376-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="db376-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="db376-132">Objektet för den virtuella apparaten.</span><span class="sxs-lookup"><span data-stu-id="db376-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db376-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db376-133">-Confirm</span></span>
<span data-ttu-id="db376-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db376-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db376-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db376-135">-WhatIf</span></span>
<span data-ttu-id="db376-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db376-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db376-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db376-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db376-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db376-138">CommonParameters</span></span>
<span data-ttu-id="db376-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db376-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db376-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db376-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db376-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db376-141">INPUTS</span></span>

### <span data-ttu-id="db376-142">System. String</span><span class="sxs-lookup"><span data-stu-id="db376-142">System.String</span></span>

### <span data-ttu-id="db376-143">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="db376-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="db376-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db376-144">OUTPUTS</span></span>

### <span data-ttu-id="db376-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db376-145">System.Boolean</span></span>

## <span data-ttu-id="db376-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db376-146">NOTES</span></span>

## <span data-ttu-id="db376-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db376-147">RELATED LINKS</span></span>
