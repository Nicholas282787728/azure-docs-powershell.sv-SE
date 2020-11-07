---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 558452481ed3feef979b78d7f134869d141caa20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743970"
---
# <span data-ttu-id="905a4-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="905a4-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="905a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="905a4-102">SYNOPSIS</span></span>
<span data-ttu-id="905a4-103">Ta bort ett meddelande i IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="905a4-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="905a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="905a4-104">SYNTAX</span></span>

### <span data-ttu-id="905a4-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="905a4-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="905a4-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="905a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="905a4-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="905a4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="905a4-108">DESCRIPTION</span></span>
<span data-ttu-id="905a4-109">En detaljerad förklaring av hur meddelanden kan berikas i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="905a4-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="905a4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="905a4-110">EXAMPLES</span></span>

### <span data-ttu-id="905a4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="905a4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="905a4-112">Tar bort meddelandet "newKey".</span><span class="sxs-lookup"><span data-stu-id="905a4-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="905a4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="905a4-113">PARAMETERS</span></span>

### <span data-ttu-id="905a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905a4-114">-DefaultProfile</span></span>
<span data-ttu-id="905a4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="905a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905a4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="905a4-116">-InputObject</span></span>
<span data-ttu-id="905a4-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="905a4-117">IotHub object</span></span>

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

### <span data-ttu-id="905a4-118">-Viktiga</span><span class="sxs-lookup"><span data-stu-id="905a4-118">-Key</span></span>
<span data-ttu-id="905a4-119">Beriknings tangenten.</span><span class="sxs-lookup"><span data-stu-id="905a4-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="905a4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="905a4-120">-Name</span></span>
<span data-ttu-id="905a4-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="905a4-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="905a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="905a4-122">-PassThru</span></span>
<span data-ttu-id="905a4-123">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="905a4-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="905a4-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="905a4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="905a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="905a4-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="905a4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="905a4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="905a4-127">-ResourceId</span></span>
<span data-ttu-id="905a4-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="905a4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="905a4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="905a4-129">-Confirm</span></span>
<span data-ttu-id="905a4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="905a4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="905a4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="905a4-131">-WhatIf</span></span>
<span data-ttu-id="905a4-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="905a4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="905a4-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="905a4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="905a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905a4-134">CommonParameters</span></span>
<span data-ttu-id="905a4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905a4-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905a4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905a4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="905a4-137">INPUTS</span></span>

### <span data-ttu-id="905a4-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="905a4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="905a4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="905a4-139">System.String</span></span>

## <span data-ttu-id="905a4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="905a4-140">OUTPUTS</span></span>

### <span data-ttu-id="905a4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="905a4-141">System.Boolean</span></span>

## <span data-ttu-id="905a4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="905a4-142">NOTES</span></span>

## <span data-ttu-id="905a4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="905a4-143">RELATED LINKS</span></span>
