---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 314ebb4412b88e5476a63cf5a1025f26e2c41e69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091152"
---
# <span data-ttu-id="3bcff-101">Get-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3bcff-101">Get-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3bcff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bcff-102">SYNOPSIS</span></span>
<span data-ttu-id="3bcff-103">Hämtar informationen om tillgängliga data Box Edge-enheter.</span><span class="sxs-lookup"><span data-stu-id="3bcff-103">Gets the information on available Data Box Edge devices.</span></span>

## <span data-ttu-id="3bcff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bcff-104">SYNTAX</span></span>

### <span data-ttu-id="3bcff-105">ListByParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3bcff-105">ListByParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeDevice [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bcff-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bcff-107">GetExtendedInfoByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-107">GetExtendedInfoByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-ExtendedInfo] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bcff-108">GetNetworkSettingByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-108">GetNetworkSettingByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-NetworkSetting] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bcff-109">GetSummaryUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-109">GetSummaryUpdateByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-UpdateSummary] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bcff-110">GetAlertByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-110">GetAlertByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice -ResourceId <String> [-Alert] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bcff-111">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-111">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bcff-112">GetSummaryUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-112">GetSummaryUpdateParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-UpdateSummary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bcff-113">GetNetworkSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-113">GetNetworkSettingParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-NetworkSetting]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bcff-114">GetExtendedInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-114">GetExtendedInfoParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ExtendedInfo]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bcff-115">GetAlertParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bcff-115">GetAlertParameterSet</span></span>
```
Get-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-Alert]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bcff-116">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bcff-116">DESCRIPTION</span></span>
<span data-ttu-id="3bcff-117">Cmdleten **Get-AzDataBoxEdgeDevice** innehåller information om de tillgängliga Edge-enheterna för data.</span><span class="sxs-lookup"><span data-stu-id="3bcff-117">The **Get-AzDataBoxEdgeDevice** cmdlet gets the information about the available Data Box Edge Devices.</span></span> <span data-ttu-id="3bcff-118">Du kan ange namnet på enheten tillsammans med resurs grupp namnet för att få informationen på en specifik enhet.</span><span class="sxs-lookup"><span data-stu-id="3bcff-118">You can specify the Name of the device along with the Resource Group Name to get the information on a specific device.</span></span> 

## <span data-ttu-id="3bcff-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bcff-119">EXAMPLES</span></span>

### <span data-ttu-id="3bcff-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3bcff-120">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice
Name               ResourceGroupName  Model   Location
----               -----------------  -----   --------
deviceNameOne      resourceGroupName1 Edge    eastus
deviceNameTwo      resourceGroupName2 Edge    westus
deviceNameThree    resourceGroupName3 Gateway eastus
```

### <span data-ttu-id="3bcff-121">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3bcff-121">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceId /subscriptions/subscriptionId/resourcegroups/resourceGroupName/providers/Microsoft.DataBoxEdge/dataBoxEdgeDevices/deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

### <span data-ttu-id="3bcff-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3bcff-122">Example 3</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName deviceName
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="3bcff-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bcff-123">PARAMETERS</span></span>

### <span data-ttu-id="3bcff-124">-Avisera</span><span class="sxs-lookup"><span data-stu-id="3bcff-124">-Alert</span></span>
<span data-ttu-id="3bcff-125">Hämta varningarna på data Box Edge/gateway-enheten</span><span class="sxs-lookup"><span data-stu-id="3bcff-125">Fetch the alerts on the data box edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAlertByResourceIdParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bcff-126">-DefaultProfile</span></span>
<span data-ttu-id="3bcff-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bcff-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bcff-128">-ExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="3bcff-128">-ExtendedInfo</span></span>
<span data-ttu-id="3bcff-129">Hämtar ytterligare information om den angivna Edge/data Box gateway-enheten</span><span class="sxs-lookup"><span data-stu-id="3bcff-129">Gets additional information for the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetExtendedInfoByResourceIdParameterSet, GetExtendedInfoParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bcff-130">-Name</span></span>
<span data-ttu-id="3bcff-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3bcff-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-132">-NetworkSetting</span><span class="sxs-lookup"><span data-stu-id="3bcff-132">-NetworkSetting</span></span>
<span data-ttu-id="3bcff-133">Hämtar nätverks inställningar för den angivna data rutan Edge/data Box gateway-enhet</span><span class="sxs-lookup"><span data-stu-id="3bcff-133">Gets the network settings of the specified Data Box Edge/Data Box Gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNetworkSettingByResourceIdParameterSet, GetNetworkSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bcff-134">-ResourceGroupName</span></span>
<span data-ttu-id="3bcff-135">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3bcff-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListByParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetSummaryUpdateParameterSet, GetNetworkSettingParameterSet, GetExtendedInfoParameterSet, GetAlertParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bcff-136">-ResourceId</span></span>
<span data-ttu-id="3bcff-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bcff-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet, GetExtendedInfoByResourceIdParameterSet, GetNetworkSettingByResourceIdParameterSet, GetSummaryUpdateByResourceIdParameterSet, GetAlertByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-138">-UpdateSummary</span><span class="sxs-lookup"><span data-stu-id="3bcff-138">-UpdateSummary</span></span>
<span data-ttu-id="3bcff-139">Hämtar information om tillgängligheten för uppdateringar baserat på den senaste genomsökningen av enheten.</span><span class="sxs-lookup"><span data-stu-id="3bcff-139">Gets information about the availability of updates based on the last scan of the device.</span></span> <span data-ttu-id="3bcff-140">Den får också information om pågående nedladdning eller installation av enheten.</span><span class="sxs-lookup"><span data-stu-id="3bcff-140">It also gets information about any ongoing download or install jobs on the device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetSummaryUpdateByResourceIdParameterSet, GetSummaryUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcff-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bcff-141">CommonParameters</span></span>
<span data-ttu-id="3bcff-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bcff-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bcff-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bcff-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bcff-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bcff-144">INPUTS</span></span>

### <span data-ttu-id="3bcff-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="3bcff-145">None</span></span>

## <span data-ttu-id="3bcff-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bcff-146">OUTPUTS</span></span>

### <span data-ttu-id="3bcff-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3bcff-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="3bcff-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="3bcff-148">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeNetworkAdapter</span></span>

### <span data-ttu-id="3bcff-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span><span class="sxs-lookup"><span data-stu-id="3bcff-149">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDeviceExtendedInfo</span></span>

### <span data-ttu-id="3bcff-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span><span class="sxs-lookup"><span data-stu-id="3bcff-150">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUpdateSummary</span></span>

### <span data-ttu-id="3bcff-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span><span class="sxs-lookup"><span data-stu-id="3bcff-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeAlert</span></span>

## <span data-ttu-id="3bcff-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bcff-152">NOTES</span></span>

## <span data-ttu-id="3bcff-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bcff-153">RELATED LINKS</span></span>
