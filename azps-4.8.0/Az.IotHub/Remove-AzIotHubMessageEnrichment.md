---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259475"
---
# <span data-ttu-id="1bb10-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="1bb10-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="1bb10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bb10-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb10-103">Ta bort ett meddelande i IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="1bb10-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="1bb10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bb10-104">SYNTAX</span></span>

### <span data-ttu-id="1bb10-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1bb10-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb10-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1bb10-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb10-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1bb10-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb10-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bb10-108">DESCRIPTION</span></span>
<span data-ttu-id="1bb10-109">En detaljerad förklaring av hur meddelanden kan berikas i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="1bb10-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="1bb10-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bb10-110">EXAMPLES</span></span>

### <span data-ttu-id="1bb10-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1bb10-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="1bb10-112">Tar bort meddelandet "newKey".</span><span class="sxs-lookup"><span data-stu-id="1bb10-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="1bb10-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bb10-113">PARAMETERS</span></span>

### <span data-ttu-id="1bb10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb10-114">-DefaultProfile</span></span>
<span data-ttu-id="1bb10-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb10-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb10-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bb10-116">-InputObject</span></span>
<span data-ttu-id="1bb10-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="1bb10-117">IotHub object</span></span>

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

### <span data-ttu-id="1bb10-118">-Viktiga</span><span class="sxs-lookup"><span data-stu-id="1bb10-118">-Key</span></span>
<span data-ttu-id="1bb10-119">Beriknings tangenten.</span><span class="sxs-lookup"><span data-stu-id="1bb10-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="1bb10-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1bb10-120">-Name</span></span>
<span data-ttu-id="1bb10-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="1bb10-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1bb10-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bb10-122">-PassThru</span></span>
<span data-ttu-id="1bb10-123">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="1bb10-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="1bb10-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1bb10-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1bb10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb10-125">-ResourceGroupName</span></span>
<span data-ttu-id="1bb10-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1bb10-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1bb10-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb10-127">-ResourceId</span></span>
<span data-ttu-id="1bb10-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="1bb10-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1bb10-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1bb10-129">-Confirm</span></span>
<span data-ttu-id="1bb10-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1bb10-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb10-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb10-131">-WhatIf</span></span>
<span data-ttu-id="1bb10-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bb10-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb10-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1bb10-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb10-134">CommonParameters</span></span>
<span data-ttu-id="1bb10-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb10-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb10-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb10-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bb10-137">INPUTS</span></span>

### <span data-ttu-id="1bb10-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1bb10-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1bb10-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb10-139">System.String</span></span>

## <span data-ttu-id="1bb10-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bb10-140">OUTPUTS</span></span>

### <span data-ttu-id="1bb10-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bb10-141">System.Boolean</span></span>

## <span data-ttu-id="1bb10-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bb10-142">NOTES</span></span>

## <span data-ttu-id="1bb10-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bb10-143">RELATED LINKS</span></span>
