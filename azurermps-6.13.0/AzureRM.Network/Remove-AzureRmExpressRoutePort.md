---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576177"
---
# <span data-ttu-id="f51b7-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f51b7-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="f51b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f51b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f51b7-103">Tar bort en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f51b7-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f51b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f51b7-104">SYNTAX</span></span>

### <span data-ttu-id="f51b7-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f51b7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f51b7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f51b7-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f51b7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f51b7-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f51b7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f51b7-108">DESCRIPTION</span></span>
<span data-ttu-id="f51b7-109">Cmdleten **Remove-AzureRmExpressRoutePort** tar bort en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f51b7-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f51b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f51b7-110">EXAMPLES</span></span>

### <span data-ttu-id="f51b7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f51b7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f51b7-112">Tar bort $PortName ExpressRoutePort-resursen i $rg resurs grupp i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f51b7-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="f51b7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f51b7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="f51b7-114">Tar bort ExpressRoutePort-resursen i InputObject.</span><span class="sxs-lookup"><span data-stu-id="f51b7-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="f51b7-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f51b7-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="f51b7-116">Tar bort ExpressRoutePort-resursen med ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="f51b7-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="f51b7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f51b7-117">PARAMETERS</span></span>

### <span data-ttu-id="f51b7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f51b7-118">-AsJob</span></span>
<span data-ttu-id="f51b7-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f51b7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f51b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51b7-120">-DefaultProfile</span></span>
<span data-ttu-id="f51b7-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f51b7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51b7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f51b7-122">-Force</span></span>
<span data-ttu-id="f51b7-123">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="f51b7-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="f51b7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f51b7-124">-InputObject</span></span>
<span data-ttu-id="f51b7-125">ExpressRoute-portnumret</span><span class="sxs-lookup"><span data-stu-id="f51b7-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f51b7-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f51b7-126">-Name</span></span>
<span data-ttu-id="f51b7-127">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f51b7-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f51b7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f51b7-128">-PassThru</span></span>
<span data-ttu-id="f51b7-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f51b7-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f51b7-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f51b7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f51b7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f51b7-131">-ResourceGroupName</span></span>
<span data-ttu-id="f51b7-132">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f51b7-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f51b7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f51b7-133">-ResourceId</span></span>
<span data-ttu-id="f51b7-134">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="f51b7-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f51b7-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f51b7-135">-Confirm</span></span>
<span data-ttu-id="f51b7-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f51b7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f51b7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f51b7-137">-WhatIf</span></span>
<span data-ttu-id="f51b7-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f51b7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f51b7-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f51b7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f51b7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51b7-140">CommonParameters</span></span>
<span data-ttu-id="f51b7-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f51b7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51b7-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51b7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51b7-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f51b7-143">INPUTS</span></span>

### <span data-ttu-id="f51b7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f51b7-144">System.String</span></span>

### <span data-ttu-id="f51b7-145">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f51b7-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f51b7-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f51b7-146">OUTPUTS</span></span>

### <span data-ttu-id="f51b7-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="f51b7-147">System.Object</span></span>
## <span data-ttu-id="f51b7-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f51b7-148">NOTES</span></span>

## <span data-ttu-id="f51b7-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f51b7-149">RELATED LINKS</span></span>
