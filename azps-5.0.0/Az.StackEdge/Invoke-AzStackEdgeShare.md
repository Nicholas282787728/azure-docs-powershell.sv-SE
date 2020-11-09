---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324210"
---
# <span data-ttu-id="fa473-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fa473-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="fa473-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa473-102">SYNOPSIS</span></span>
<span data-ttu-id="fa473-103">Anropar specifika åtgärder på en resurs.</span><span class="sxs-lookup"><span data-stu-id="fa473-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="fa473-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa473-104">SYNTAX</span></span>

### <span data-ttu-id="fa473-105">InvokeByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fa473-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa473-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa473-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa473-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa473-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa473-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa473-108">DESCRIPTION</span></span>
<span data-ttu-id="fa473-109">Cmdleten **Invoke-AzStackEdgeShare** anropar åtgärden för att uppdatera data på en resurs på en grupp Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="fa473-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="fa473-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa473-110">EXAMPLES</span></span>

### <span data-ttu-id="fa473-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa473-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="fa473-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fa473-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="fa473-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa473-113">PARAMETERS</span></span>

### <span data-ttu-id="fa473-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa473-114">-AsJob</span></span>
<span data-ttu-id="fa473-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fa473-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa473-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa473-116">-DefaultProfile</span></span>
<span data-ttu-id="fa473-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa473-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa473-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="fa473-118">-DeviceName</span></span>
<span data-ttu-id="fa473-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="fa473-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa473-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa473-120">-InputObject</span></span>
<span data-ttu-id="fa473-121">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="fa473-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa473-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa473-122">-Name</span></span>
<span data-ttu-id="fa473-123">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="fa473-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa473-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa473-124">-PassThru</span></span>
<span data-ttu-id="fa473-125">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="fa473-125">returns true if successful</span></span>

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

### <span data-ttu-id="fa473-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="fa473-126">-RefreshData</span></span>
<span data-ttu-id="fa473-127">Uppdatera metadata för delar med data från molnet</span><span class="sxs-lookup"><span data-stu-id="fa473-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="fa473-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa473-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa473-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fa473-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa473-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa473-130">-ResourceId</span></span>
<span data-ttu-id="fa473-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa473-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa473-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa473-132">-Confirm</span></span>
<span data-ttu-id="fa473-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa473-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa473-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa473-134">-WhatIf</span></span>
<span data-ttu-id="fa473-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa473-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa473-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa473-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa473-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa473-137">CommonParameters</span></span>
<span data-ttu-id="fa473-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa473-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa473-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa473-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa473-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa473-140">INPUTS</span></span>

### <span data-ttu-id="fa473-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fa473-141">System.String</span></span>

### <span data-ttu-id="fa473-142">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fa473-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="fa473-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa473-143">OUTPUTS</span></span>

### <span data-ttu-id="fa473-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa473-144">System.Boolean</span></span>

## <span data-ttu-id="fa473-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa473-145">NOTES</span></span>

## <span data-ttu-id="fa473-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa473-146">RELATED LINKS</span></span>
