---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088771"
---
# <span data-ttu-id="d105a-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d105a-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="d105a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d105a-102">SYNOPSIS</span></span>
<span data-ttu-id="d105a-103">Anropar specifika åtgärder på enheten.</span><span class="sxs-lookup"><span data-stu-id="d105a-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="d105a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d105a-104">SYNTAX</span></span>

### <span data-ttu-id="d105a-105">InvokeScanForUpdateParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d105a-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d105a-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d105a-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d105a-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d105a-114">DESCRIPTION</span></span>
<span data-ttu-id="d105a-115">Cmdleten **Invoke-AzStackEdgeDevice** anropar åtgärder för genomsökning, nedladdning och installation av uppdateringarna på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="d105a-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="d105a-116">En automatisk genomsökning körs på enheten dagligen, du kan aktivera genomsökningen genom att köra den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d105a-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="d105a-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d105a-117">EXAMPLES</span></span>

### <span data-ttu-id="d105a-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d105a-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="d105a-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d105a-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="d105a-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="d105a-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="d105a-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d105a-121">PARAMETERS</span></span>

### <span data-ttu-id="d105a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d105a-122">-AsJob</span></span>
<span data-ttu-id="d105a-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d105a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d105a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d105a-124">-DefaultProfile</span></span>
<span data-ttu-id="d105a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d105a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d105a-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d105a-126">-DeviceObject</span></span>
<span data-ttu-id="d105a-127">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="d105a-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d105a-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="d105a-128">-FetchUpdate</span></span>
<span data-ttu-id="d105a-129">Laddar ned uppdateringarna på en stapel Edge/gateway-enhet</span><span class="sxs-lookup"><span data-stu-id="d105a-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d105a-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="d105a-130">-InstallUpdate</span></span>
<span data-ttu-id="d105a-131">Installerar uppdateringarna på stack Edge/gateway-enheten</span><span class="sxs-lookup"><span data-stu-id="d105a-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d105a-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="d105a-132">-Name</span></span>
<span data-ttu-id="d105a-133">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="d105a-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d105a-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d105a-134">-PassThru</span></span>
<span data-ttu-id="d105a-135">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="d105a-135">returns true if successful</span></span>

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

### <span data-ttu-id="d105a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d105a-136">-ResourceGroupName</span></span>
<span data-ttu-id="d105a-137">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d105a-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d105a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d105a-138">-ResourceId</span></span>
<span data-ttu-id="d105a-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d105a-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d105a-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="d105a-140">-ScanForUpdate</span></span>
<span data-ttu-id="d105a-141">Söker efter uppdateringar på en stapel Edge/gateway-enhet.</span><span class="sxs-lookup"><span data-stu-id="d105a-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="d105a-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d105a-142">-Confirm</span></span>
<span data-ttu-id="d105a-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d105a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d105a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d105a-144">-WhatIf</span></span>
<span data-ttu-id="d105a-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d105a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d105a-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d105a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d105a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d105a-147">CommonParameters</span></span>
<span data-ttu-id="d105a-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d105a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d105a-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d105a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d105a-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d105a-150">INPUTS</span></span>

### <span data-ttu-id="d105a-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="d105a-151">None</span></span>

## <span data-ttu-id="d105a-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d105a-152">OUTPUTS</span></span>

### <span data-ttu-id="d105a-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d105a-153">System.Boolean</span></span>

## <span data-ttu-id="d105a-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d105a-154">NOTES</span></span>

## <span data-ttu-id="d105a-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d105a-155">RELATED LINKS</span></span>
