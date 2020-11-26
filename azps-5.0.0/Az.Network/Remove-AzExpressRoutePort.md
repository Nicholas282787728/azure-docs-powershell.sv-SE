---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324575"
---
# <span data-ttu-id="7a193-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7a193-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="7a193-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a193-102">SYNOPSIS</span></span>
<span data-ttu-id="7a193-103">Tar bort en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7a193-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="7a193-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a193-104">SYNTAX</span></span>

### <span data-ttu-id="7a193-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7a193-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a193-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a193-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a193-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a193-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a193-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a193-108">DESCRIPTION</span></span>
<span data-ttu-id="7a193-109">Cmdleten **Remove-AzExpressRoutePort** tar bort en ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7a193-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="7a193-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a193-110">EXAMPLES</span></span>

### <span data-ttu-id="7a193-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7a193-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="7a193-112">Tar bort $PortName ExpressRoutePort-resursen i $rg resurs grupp i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7a193-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="7a193-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7a193-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="7a193-114">Tar bort ExpressRoutePort-resursen i InputObject.</span><span class="sxs-lookup"><span data-stu-id="7a193-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="7a193-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7a193-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="7a193-116">Tar bort ExpressRoutePort-resursen med ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="7a193-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="7a193-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a193-117">PARAMETERS</span></span>

### <span data-ttu-id="7a193-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a193-118">-AsJob</span></span>
<span data-ttu-id="7a193-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7a193-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a193-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a193-120">-DefaultProfile</span></span>
<span data-ttu-id="7a193-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a193-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a193-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7a193-122">-Force</span></span>
<span data-ttu-id="7a193-123">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="7a193-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="7a193-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a193-124">-InputObject</span></span>
<span data-ttu-id="7a193-125">ExpressRoute-portnumret</span><span class="sxs-lookup"><span data-stu-id="7a193-125">The express route port object</span></span>

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

### <span data-ttu-id="7a193-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a193-126">-Name</span></span>
<span data-ttu-id="7a193-127">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7a193-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="7a193-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a193-128">-PassThru</span></span>
<span data-ttu-id="7a193-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7a193-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7a193-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7a193-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a193-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a193-131">-ResourceGroupName</span></span>
<span data-ttu-id="7a193-132">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7a193-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="7a193-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a193-133">-ResourceId</span></span>
<span data-ttu-id="7a193-134">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="7a193-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="7a193-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a193-135">-Confirm</span></span>
<span data-ttu-id="7a193-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a193-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a193-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a193-137">-WhatIf</span></span>
<span data-ttu-id="7a193-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a193-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a193-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a193-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a193-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a193-140">CommonParameters</span></span>
<span data-ttu-id="7a193-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a193-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a193-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a193-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a193-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a193-143">INPUTS</span></span>

### <span data-ttu-id="7a193-144">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7a193-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="7a193-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7a193-145">System.String</span></span>

## <span data-ttu-id="7a193-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a193-146">OUTPUTS</span></span>

### <span data-ttu-id="7a193-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7a193-147">System.Boolean</span></span>

## <span data-ttu-id="7a193-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a193-148">NOTES</span></span>

## <span data-ttu-id="7a193-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a193-149">RELATED LINKS</span></span>

[<span data-ttu-id="7a193-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7a193-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="7a193-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7a193-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="7a193-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7a193-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)