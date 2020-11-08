---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259466"
---
# <span data-ttu-id="db482-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="db482-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="db482-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db482-102">SYNOPSIS</span></span>
<span data-ttu-id="db482-103">Uppdatera ett meddelande som är berikat i IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="db482-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="db482-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db482-104">SYNTAX</span></span>

### <span data-ttu-id="db482-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db482-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db482-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="db482-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db482-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="db482-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db482-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db482-108">DESCRIPTION</span></span>
<span data-ttu-id="db482-109">En detaljerad förklaring av hur meddelanden kan berikas i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="db482-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="db482-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db482-110">EXAMPLES</span></span>

### <span data-ttu-id="db482-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db482-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="db482-112">Uppdaterar profilens värde till "updatedValue" för Key "newKey".</span><span class="sxs-lookup"><span data-stu-id="db482-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="db482-113">En detaljerad förklaring av hur meddelanden kan berikas i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="db482-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="db482-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="db482-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="db482-115">Uppdaterar profilens slut punkt till "endpoint1, endpoint2, endpoint3" för Key "newKey".</span><span class="sxs-lookup"><span data-stu-id="db482-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="db482-116">En detaljerad förklaring av hur meddelanden kan berikas i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="db482-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="db482-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db482-117">PARAMETERS</span></span>

### <span data-ttu-id="db482-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db482-118">-DefaultProfile</span></span>
<span data-ttu-id="db482-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db482-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db482-120">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="db482-120">-Endpoint</span></span>
<span data-ttu-id="db482-121">Slut punkter som du tillämpar på.</span><span class="sxs-lookup"><span data-stu-id="db482-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db482-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db482-122">-InputObject</span></span>
<span data-ttu-id="db482-123">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="db482-123">IotHub Object</span></span>

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

### <span data-ttu-id="db482-124">-Viktiga</span><span class="sxs-lookup"><span data-stu-id="db482-124">-Key</span></span>
<span data-ttu-id="db482-125">Beriknings tangenten.</span><span class="sxs-lookup"><span data-stu-id="db482-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="db482-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="db482-126">-Name</span></span>
<span data-ttu-id="db482-127">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="db482-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="db482-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db482-128">-ResourceGroupName</span></span>
<span data-ttu-id="db482-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="db482-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="db482-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db482-130">-ResourceId</span></span>
<span data-ttu-id="db482-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="db482-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="db482-132">-Värde</span><span class="sxs-lookup"><span data-stu-id="db482-132">-Value</span></span>
<span data-ttu-id="db482-133">Värdet för berikning.</span><span class="sxs-lookup"><span data-stu-id="db482-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="db482-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db482-134">-Confirm</span></span>
<span data-ttu-id="db482-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db482-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db482-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db482-136">-WhatIf</span></span>
<span data-ttu-id="db482-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db482-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db482-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db482-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db482-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db482-139">CommonParameters</span></span>
<span data-ttu-id="db482-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db482-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db482-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db482-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db482-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db482-142">INPUTS</span></span>

### <span data-ttu-id="db482-143">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="db482-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="db482-144">System. String</span><span class="sxs-lookup"><span data-stu-id="db482-144">System.String</span></span>

## <span data-ttu-id="db482-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db482-145">OUTPUTS</span></span>

### <span data-ttu-id="db482-146">Microsoft. Azure. commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="db482-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="db482-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db482-147">NOTES</span></span>

## <span data-ttu-id="db482-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db482-148">RELATED LINKS</span></span>
