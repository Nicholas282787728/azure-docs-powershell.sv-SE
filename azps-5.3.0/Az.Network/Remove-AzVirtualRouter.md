---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425187"
---
# <span data-ttu-id="13158-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="13158-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="13158-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13158-102">SYNOPSIS</span></span>
<span data-ttu-id="13158-103">Tar bort en Azure-VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="13158-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="13158-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13158-104">SYNTAX</span></span>

### <span data-ttu-id="13158-105">VirtualRouterNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="13158-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13158-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13158-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13158-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13158-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13158-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13158-108">DESCRIPTION</span></span>
<span data-ttu-id="13158-109">Cmdleten **Remove-AzVirtualRouter** tar bort en Azure-VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="13158-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="13158-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13158-110">EXAMPLES</span></span>

### <span data-ttu-id="13158-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13158-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="13158-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13158-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="13158-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="13158-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="13158-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13158-114">PARAMETERS</span></span>

### <span data-ttu-id="13158-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13158-115">-AsJob</span></span>
<span data-ttu-id="13158-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="13158-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13158-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13158-117">-DefaultProfile</span></span>
<span data-ttu-id="13158-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13158-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13158-119">-Force</span><span class="sxs-lookup"><span data-stu-id="13158-119">-Force</span></span>
<span data-ttu-id="13158-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="13158-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="13158-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13158-121">-InputObject</span></span>
<span data-ttu-id="13158-122">Det virtuella router-indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="13158-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13158-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13158-123">-PassThru</span></span>
<span data-ttu-id="13158-124">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="13158-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="13158-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13158-125">-ResourceGroupName</span></span>
<span data-ttu-id="13158-126">Namnet på den virtuella routern i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="13158-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13158-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13158-127">-ResourceId</span></span>
<span data-ttu-id="13158-128">ID för virtuell router-resurs.</span><span class="sxs-lookup"><span data-stu-id="13158-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13158-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="13158-129">-RouterName</span></span>
<span data-ttu-id="13158-130">Namnet på den virtuella routern.</span><span class="sxs-lookup"><span data-stu-id="13158-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13158-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13158-131">-Confirm</span></span>
<span data-ttu-id="13158-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13158-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13158-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13158-133">-WhatIf</span></span>
<span data-ttu-id="13158-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13158-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13158-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13158-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13158-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13158-136">CommonParameters</span></span>
<span data-ttu-id="13158-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13158-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13158-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13158-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13158-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13158-139">INPUTS</span></span>

### <span data-ttu-id="13158-140">System. String</span><span class="sxs-lookup"><span data-stu-id="13158-140">System.String</span></span>

### <span data-ttu-id="13158-141">Microsoft. Azure. commands. Networks. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="13158-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="13158-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13158-142">OUTPUTS</span></span>

### <span data-ttu-id="13158-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13158-143">System.Boolean</span></span>

## <span data-ttu-id="13158-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13158-144">NOTES</span></span>

## <span data-ttu-id="13158-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13158-145">RELATED LINKS</span></span>
