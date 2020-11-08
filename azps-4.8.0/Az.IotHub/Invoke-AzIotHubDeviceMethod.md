---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103223"
---
# <span data-ttu-id="917cb-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="917cb-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="917cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="917cb-102">SYNOPSIS</span></span>
<span data-ttu-id="917cb-103">Starta en direkt metod på en enhet.</span><span class="sxs-lookup"><span data-stu-id="917cb-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="917cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="917cb-104">SYNTAX</span></span>

### <span data-ttu-id="917cb-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="917cb-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="917cb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="917cb-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="917cb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="917cb-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="917cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="917cb-108">DESCRIPTION</span></span>
<span data-ttu-id="917cb-109">Starta en direkt metod på en enhet.</span><span class="sxs-lookup"><span data-stu-id="917cb-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="917cb-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods information finns i.</span><span class="sxs-lookup"><span data-stu-id="917cb-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="917cb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="917cb-111">EXAMPLES</span></span>

### <span data-ttu-id="917cb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="917cb-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="917cb-113">Starta en enhets metod.</span><span class="sxs-lookup"><span data-stu-id="917cb-113">Invoke a device method.</span></span>

## <span data-ttu-id="917cb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="917cb-114">PARAMETERS</span></span>

### <span data-ttu-id="917cb-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="917cb-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="917cb-116">Antal sekunder att vänta tills en anslutning har genomförts.</span><span class="sxs-lookup"><span data-stu-id="917cb-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="917cb-117">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="917cb-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917cb-118">-DefaultProfile</span></span>
<span data-ttu-id="917cb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="917cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="917cb-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="917cb-120">-DeviceId</span></span>
<span data-ttu-id="917cb-121">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="917cb-121">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="917cb-122">-InputObject</span></span>
<span data-ttu-id="917cb-123">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="917cb-123">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="917cb-124">-IotHubName</span></span>
<span data-ttu-id="917cb-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="917cb-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="917cb-126">-Name</span></span>
<span data-ttu-id="917cb-127">Namnet på den metod som ska startas på den här enheten.</span><span class="sxs-lookup"><span data-stu-id="917cb-127">The name of the method to invoke on this device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-128">-Nyttolast</span><span class="sxs-lookup"><span data-stu-id="917cb-128">-Payload</span></span>
<span data-ttu-id="917cb-129">Nytto lasten för metoden att starta på den här enheten.</span><span class="sxs-lookup"><span data-stu-id="917cb-129">The payload for the method to invoke on this device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917cb-130">-ResourceGroupName</span></span>
<span data-ttu-id="917cb-131">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="917cb-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="917cb-132">-ResourceId</span></span>
<span data-ttu-id="917cb-133">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="917cb-133">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="917cb-134">-ResponseTimeOut</span></span>
<span data-ttu-id="917cb-135">Antal sekunder att vänta tills ett resultat erhålls från metoden Direct.</span><span class="sxs-lookup"><span data-stu-id="917cb-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="917cb-136">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="917cb-136">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="917cb-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="917cb-137">-Confirm</span></span>
<span data-ttu-id="917cb-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="917cb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917cb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="917cb-139">-WhatIf</span></span>
<span data-ttu-id="917cb-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="917cb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="917cb-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="917cb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="917cb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917cb-142">CommonParameters</span></span>
<span data-ttu-id="917cb-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917cb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917cb-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917cb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917cb-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="917cb-145">INPUTS</span></span>

### <span data-ttu-id="917cb-146">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="917cb-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="917cb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="917cb-147">System.String</span></span>

## <span data-ttu-id="917cb-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="917cb-148">OUTPUTS</span></span>

### <span data-ttu-id="917cb-149">Microsoft. Azure. commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="917cb-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="917cb-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="917cb-150">NOTES</span></span>

## <span data-ttu-id="917cb-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="917cb-151">RELATED LINKS</span></span>
