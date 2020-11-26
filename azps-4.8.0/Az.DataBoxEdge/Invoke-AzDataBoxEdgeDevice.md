---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 29bf8cf612d3569480c62784466879095ebcdb6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262320"
---
# <span data-ttu-id="32281-101">Invoke-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="32281-101">Invoke-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="32281-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32281-102">SYNOPSIS</span></span>
<span data-ttu-id="32281-103">Anropar specifika åtgärder på enheten.</span><span class="sxs-lookup"><span data-stu-id="32281-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="32281-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32281-104">SYNTAX</span></span>

### <span data-ttu-id="32281-105">InvokeScanForUpdateParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="32281-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32281-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32281-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeDevice -DeviceObject <PSDataBoxEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32281-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32281-114">DESCRIPTION</span></span>
<span data-ttu-id="32281-115">Cmdleten **Invoke-AzDataBoxEdgeDevice** anropar åtgärder för genomsökning, nedladdning och installation av uppdateringarna i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="32281-115">The **Invoke-AzDataBoxEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Data Box Edge device.</span></span> <span data-ttu-id="32281-116">En automatisk genomsökning körs på enheten dagligen, du kan aktivera genomsökningen genom att köra den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32281-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="32281-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32281-117">EXAMPLES</span></span>

### <span data-ttu-id="32281-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="32281-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="32281-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="32281-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="32281-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="32281-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="32281-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32281-121">PARAMETERS</span></span>

### <span data-ttu-id="32281-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32281-122">-AsJob</span></span>
<span data-ttu-id="32281-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="32281-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32281-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32281-124">-DefaultProfile</span></span>
<span data-ttu-id="32281-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32281-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32281-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="32281-126">-DeviceObject</span></span>
<span data-ttu-id="32281-127">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="32281-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="32281-128">-FetchUpdate</span></span>
<span data-ttu-id="32281-129">Hämtar uppdateringarna i en data Box Edge/gateway-enhet</span><span class="sxs-lookup"><span data-stu-id="32281-129">Downloads the updates on a data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="32281-130">-InstallUpdate</span></span>
<span data-ttu-id="32281-131">Installerar uppdateringarna på data Box Edge/gateway-enheten</span><span class="sxs-lookup"><span data-stu-id="32281-131">Installs the updates on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="32281-132">-Name</span></span>
<span data-ttu-id="32281-133">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="32281-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32281-134">-PassThru</span></span>
<span data-ttu-id="32281-135">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="32281-135">returns true if successful</span></span>

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

### <span data-ttu-id="32281-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32281-136">-ResourceGroupName</span></span>
<span data-ttu-id="32281-137">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="32281-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32281-138">-ResourceId</span></span>
<span data-ttu-id="32281-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="32281-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="32281-140">-ScanForUpdate</span></span>
<span data-ttu-id="32281-141">Söker efter uppdateringar i en data Box Edge/gateway-enhet.</span><span class="sxs-lookup"><span data-stu-id="32281-141">Scans for updates on a data box edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32281-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32281-142">-Confirm</span></span>
<span data-ttu-id="32281-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32281-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32281-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32281-144">-WhatIf</span></span>
<span data-ttu-id="32281-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32281-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32281-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32281-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32281-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32281-147">CommonParameters</span></span>
<span data-ttu-id="32281-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32281-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32281-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32281-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32281-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32281-150">INPUTS</span></span>

### <span data-ttu-id="32281-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="32281-151">None</span></span>

## <span data-ttu-id="32281-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32281-152">OUTPUTS</span></span>

### <span data-ttu-id="32281-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32281-153">System.Boolean</span></span>

## <span data-ttu-id="32281-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32281-154">NOTES</span></span>

## <span data-ttu-id="32281-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32281-155">RELATED LINKS</span></span>