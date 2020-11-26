---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273490"
---
# <span data-ttu-id="17be0-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="17be0-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="17be0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17be0-102">SYNOPSIS</span></span>
<span data-ttu-id="17be0-103">Anropa en metod för Edge-modul.</span><span class="sxs-lookup"><span data-stu-id="17be0-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="17be0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17be0-104">SYNTAX</span></span>

### <span data-ttu-id="17be0-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="17be0-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17be0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17be0-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17be0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="17be0-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17be0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17be0-108">DESCRIPTION</span></span>
<span data-ttu-id="17be0-109">Anropa en metod för Edge-modul.</span><span class="sxs-lookup"><span data-stu-id="17be0-109">Invoke an Edge module method.</span></span> <span data-ttu-id="17be0-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods information finns i.</span><span class="sxs-lookup"><span data-stu-id="17be0-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="17be0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17be0-111">EXAMPLES</span></span>

### <span data-ttu-id="17be0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17be0-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="17be0-113">Anropa en metod för Edge-modul.</span><span class="sxs-lookup"><span data-stu-id="17be0-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="17be0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17be0-114">PARAMETERS</span></span>

### <span data-ttu-id="17be0-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="17be0-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="17be0-116">Antal sekunder att vänta tills en anslutning har genomförts.</span><span class="sxs-lookup"><span data-stu-id="17be0-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="17be0-117">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="17be0-117">Default is 10.</span></span>

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

### <span data-ttu-id="17be0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17be0-118">-DefaultProfile</span></span>
<span data-ttu-id="17be0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17be0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17be0-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="17be0-120">-DeviceId</span></span>
<span data-ttu-id="17be0-121">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="17be0-121">Target Device Id.</span></span>

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

### <span data-ttu-id="17be0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17be0-122">-InputObject</span></span>
<span data-ttu-id="17be0-123">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="17be0-123">IotHub object</span></span>

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

### <span data-ttu-id="17be0-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="17be0-124">-IotHubName</span></span>
<span data-ttu-id="17be0-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="17be0-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="17be0-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="17be0-126">-ModuleId</span></span>
<span data-ttu-id="17be0-127">Mål enhetens modul-ID.</span><span class="sxs-lookup"><span data-stu-id="17be0-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17be0-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="17be0-128">-Name</span></span>
<span data-ttu-id="17be0-129">Namnet på den metod som ska anropas för den här modulen.</span><span class="sxs-lookup"><span data-stu-id="17be0-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="17be0-130">-Nyttolast</span><span class="sxs-lookup"><span data-stu-id="17be0-130">-Payload</span></span>
<span data-ttu-id="17be0-131">Nytto lasten för metoden att starta i den här modulen.</span><span class="sxs-lookup"><span data-stu-id="17be0-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="17be0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17be0-132">-ResourceGroupName</span></span>
<span data-ttu-id="17be0-133">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="17be0-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="17be0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17be0-134">-ResourceId</span></span>
<span data-ttu-id="17be0-135">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="17be0-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="17be0-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="17be0-136">-ResponseTimeOut</span></span>
<span data-ttu-id="17be0-137">Antal sekunder att vänta tills ett resultat erhålls från metoden Direct.</span><span class="sxs-lookup"><span data-stu-id="17be0-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="17be0-138">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="17be0-138">Default is 10.</span></span>

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

### <span data-ttu-id="17be0-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17be0-139">-Confirm</span></span>
<span data-ttu-id="17be0-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17be0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17be0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17be0-141">-WhatIf</span></span>
<span data-ttu-id="17be0-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17be0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17be0-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17be0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17be0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17be0-144">CommonParameters</span></span>
<span data-ttu-id="17be0-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17be0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17be0-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17be0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17be0-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17be0-147">INPUTS</span></span>

### <span data-ttu-id="17be0-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="17be0-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="17be0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="17be0-149">System.String</span></span>

## <span data-ttu-id="17be0-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17be0-150">OUTPUTS</span></span>

### <span data-ttu-id="17be0-151">Microsoft. Azure. commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="17be0-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="17be0-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17be0-152">NOTES</span></span>

## <span data-ttu-id="17be0-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17be0-153">RELATED LINKS</span></span>