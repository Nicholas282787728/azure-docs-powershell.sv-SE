---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523187"
---
# <span data-ttu-id="3124d-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3124d-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="3124d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3124d-102">SYNOPSIS</span></span>
<span data-ttu-id="3124d-103">Ta bort en virtuell nätverks utrustnings resurs.</span><span class="sxs-lookup"><span data-stu-id="3124d-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3124d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3124d-104">SYNTAX</span></span>

### <span data-ttu-id="3124d-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3124d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3124d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3124d-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3124d-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3124d-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3124d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3124d-108">DESCRIPTION</span></span>
<span data-ttu-id="3124d-109">Med kommandot Remove-AzNetworkVirtualAppliance tas en resurs för virtuella nätverk bort.</span><span class="sxs-lookup"><span data-stu-id="3124d-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3124d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3124d-110">EXAMPLES</span></span>

### <span data-ttu-id="3124d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3124d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="3124d-112">Ta bort en virtuell nätverks enhets resurs.</span><span class="sxs-lookup"><span data-stu-id="3124d-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3124d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3124d-113">PARAMETERS</span></span>

### <span data-ttu-id="3124d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3124d-114">-AsJob</span></span>
<span data-ttu-id="3124d-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3124d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3124d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3124d-116">-DefaultProfile</span></span>
<span data-ttu-id="3124d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3124d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3124d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3124d-118">-Force</span></span>
<span data-ttu-id="3124d-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3124d-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3124d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3124d-120">-Name</span></span>
<span data-ttu-id="3124d-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="3124d-121">The resource name.</span></span>

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

### <span data-ttu-id="3124d-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3124d-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="3124d-123">Resurs objekt.</span><span class="sxs-lookup"><span data-stu-id="3124d-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3124d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3124d-124">-PassThru</span></span>
<span data-ttu-id="3124d-125">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="3124d-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3124d-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3124d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3124d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3124d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3124d-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3124d-128">The resource group name.</span></span>

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

### <span data-ttu-id="3124d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3124d-129">-ResourceId</span></span>
<span data-ttu-id="3124d-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3124d-130">The Resource Id.</span></span>

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

### <span data-ttu-id="3124d-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3124d-131">-Confirm</span></span>
<span data-ttu-id="3124d-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3124d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3124d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3124d-133">-WhatIf</span></span>
<span data-ttu-id="3124d-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3124d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3124d-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3124d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3124d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3124d-136">CommonParameters</span></span>
<span data-ttu-id="3124d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3124d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3124d-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3124d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3124d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3124d-139">INPUTS</span></span>

### <span data-ttu-id="3124d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3124d-140">System.String</span></span>

### <span data-ttu-id="3124d-141">Microsoft. Azure. commands. Networks. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="3124d-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="3124d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3124d-142">OUTPUTS</span></span>

### <span data-ttu-id="3124d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3124d-143">System.Boolean</span></span>

## <span data-ttu-id="3124d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3124d-144">NOTES</span></span>

## <span data-ttu-id="3124d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3124d-145">RELATED LINKS</span></span>
