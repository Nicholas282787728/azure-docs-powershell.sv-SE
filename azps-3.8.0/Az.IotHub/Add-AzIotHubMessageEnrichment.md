---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925850"
---
# <span data-ttu-id="f85e3-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f85e3-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="f85e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f85e3-102">SYNOPSIS</span></span>
<span data-ttu-id="f85e3-103">Skapar en förstorad meddelande för valda slut punkter i IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f85e3-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="f85e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f85e3-104">SYNTAX</span></span>

### <span data-ttu-id="f85e3-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f85e3-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f85e3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f85e3-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f85e3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f85e3-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f85e3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f85e3-108">DESCRIPTION</span></span>
<span data-ttu-id="f85e3-109">Lägg till upp till 10 meddelande berikare per IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="f85e3-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="f85e3-110">Dessa läggs till som program egenskaper för meddelanden som skickas till valda slut punkter.</span><span class="sxs-lookup"><span data-stu-id="f85e3-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="f85e3-111">Mer information finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="f85e3-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="f85e3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f85e3-112">EXAMPLES</span></span>

### <span data-ttu-id="f85e3-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f85e3-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="f85e3-114">Lägg till en ny berikning med viktig "newKey" och värde "nytt värde".</span><span class="sxs-lookup"><span data-stu-id="f85e3-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="f85e3-115">Denna nya berikning tillämpas på slut punkter för "endpoint1" och "endpoint2".</span><span class="sxs-lookup"><span data-stu-id="f85e3-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="f85e3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f85e3-116">PARAMETERS</span></span>

### <span data-ttu-id="f85e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85e3-117">-DefaultProfile</span></span>
<span data-ttu-id="f85e3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f85e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f85e3-119">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="f85e3-119">-Endpoint</span></span>
<span data-ttu-id="f85e3-120">Slut punkter som du tillämpar på.</span><span class="sxs-lookup"><span data-stu-id="f85e3-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85e3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f85e3-121">-InputObject</span></span>
<span data-ttu-id="f85e3-122">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="f85e3-122">IotHub object</span></span>

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

### <span data-ttu-id="f85e3-123">-Viktiga</span><span class="sxs-lookup"><span data-stu-id="f85e3-123">-Key</span></span>
<span data-ttu-id="f85e3-124">Beriknings tangenten.</span><span class="sxs-lookup"><span data-stu-id="f85e3-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="f85e3-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f85e3-125">-Name</span></span>
<span data-ttu-id="f85e3-126">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="f85e3-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f85e3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85e3-127">-ResourceGroupName</span></span>
<span data-ttu-id="f85e3-128">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="f85e3-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f85e3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f85e3-129">-ResourceId</span></span>
<span data-ttu-id="f85e3-130">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="f85e3-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f85e3-131">-Värde</span><span class="sxs-lookup"><span data-stu-id="f85e3-131">-Value</span></span>
<span data-ttu-id="f85e3-132">Värdet för berikning.</span><span class="sxs-lookup"><span data-stu-id="f85e3-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="f85e3-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f85e3-133">-Confirm</span></span>
<span data-ttu-id="f85e3-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f85e3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f85e3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f85e3-135">-WhatIf</span></span>
<span data-ttu-id="f85e3-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f85e3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f85e3-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f85e3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f85e3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85e3-138">CommonParameters</span></span>
<span data-ttu-id="f85e3-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85e3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85e3-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f85e3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85e3-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f85e3-141">INPUTS</span></span>

### <span data-ttu-id="f85e3-142">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f85e3-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f85e3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f85e3-143">System.String</span></span>

## <span data-ttu-id="f85e3-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f85e3-144">OUTPUTS</span></span>

### <span data-ttu-id="f85e3-145">Microsoft. Azure. commands. Management. IotHub. Models. PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="f85e3-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="f85e3-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f85e3-146">NOTES</span></span>

## <span data-ttu-id="f85e3-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f85e3-147">RELATED LINKS</span></span>