---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425984"
---
# <span data-ttu-id="9246a-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="9246a-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="9246a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9246a-102">SYNOPSIS</span></span>
<span data-ttu-id="9246a-103">Skicka enhet-till-moln-meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9246a-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="9246a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9246a-104">SYNTAX</span></span>

### <span data-ttu-id="9246a-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9246a-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9246a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9246a-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9246a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9246a-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9246a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9246a-108">DESCRIPTION</span></span>
<span data-ttu-id="9246a-109">Kommandot stöder att skicka meddelanden med program-och system egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9246a-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="9246a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9246a-110">EXAMPLES</span></span>

### <span data-ttu-id="9246a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9246a-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="9246a-112">Skickar enhet till moln meddelandet med standard transport typen.</span><span class="sxs-lookup"><span data-stu-id="9246a-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="9246a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9246a-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="9246a-114">Skickar en MQTT-enhet till moln meddelandet.</span><span class="sxs-lookup"><span data-stu-id="9246a-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="9246a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9246a-115">PARAMETERS</span></span>

### <span data-ttu-id="9246a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9246a-116">-DefaultProfile</span></span>
<span data-ttu-id="9246a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9246a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9246a-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9246a-118">-DeviceId</span></span>
<span data-ttu-id="9246a-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="9246a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="9246a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9246a-120">-InputObject</span></span>
<span data-ttu-id="9246a-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="9246a-121">IotHub object</span></span>

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

### <span data-ttu-id="9246a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9246a-122">-IotHubName</span></span>
<span data-ttu-id="9246a-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="9246a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9246a-124">– Meddelande</span><span class="sxs-lookup"><span data-stu-id="9246a-124">-Message</span></span>
<span data-ttu-id="9246a-125">Meddelande text att skicka till IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9246a-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="9246a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9246a-126">-PassThru</span></span>
<span data-ttu-id="9246a-127">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="9246a-127">Allows to return the boolean object.</span></span> <span data-ttu-id="9246a-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9246a-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9246a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9246a-129">-ResourceGroupName</span></span>
<span data-ttu-id="9246a-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9246a-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9246a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9246a-131">-ResourceId</span></span>
<span data-ttu-id="9246a-132">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="9246a-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9246a-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="9246a-133">-TransportType</span></span>
<span data-ttu-id="9246a-134">Transport typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="9246a-134">Transport type to use.</span></span>
<span data-ttu-id="9246a-135">Standard är AMQP.</span><span class="sxs-lookup"><span data-stu-id="9246a-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9246a-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9246a-136">-Confirm</span></span>
<span data-ttu-id="9246a-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9246a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9246a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9246a-138">-WhatIf</span></span>
<span data-ttu-id="9246a-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9246a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9246a-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9246a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9246a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9246a-141">CommonParameters</span></span>
<span data-ttu-id="9246a-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9246a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9246a-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9246a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9246a-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9246a-144">INPUTS</span></span>

### <span data-ttu-id="9246a-145">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9246a-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9246a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9246a-146">System.String</span></span>

## <span data-ttu-id="9246a-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9246a-147">OUTPUTS</span></span>

### <span data-ttu-id="9246a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9246a-148">System.Boolean</span></span>

## <span data-ttu-id="9246a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9246a-149">NOTES</span></span>

## <span data-ttu-id="9246a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9246a-150">RELATED LINKS</span></span>
