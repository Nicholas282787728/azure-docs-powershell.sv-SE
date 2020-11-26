---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263060"
---
# <span data-ttu-id="c8f87-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8f87-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="c8f87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8f87-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f87-103">Ta bort en IoT-enhets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8f87-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="c8f87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8f87-104">SYNTAX</span></span>

### <span data-ttu-id="c8f87-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c8f87-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8f87-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8f87-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8f87-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c8f87-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f87-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8f87-108">DESCRIPTION</span></span>
<span data-ttu-id="c8f87-109">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management information finns i.</span><span class="sxs-lookup"><span data-stu-id="c8f87-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="c8f87-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8f87-110">EXAMPLES</span></span>

### <span data-ttu-id="c8f87-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c8f87-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="c8f87-112">Ta bort en IoT-enhets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8f87-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="c8f87-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8f87-113">PARAMETERS</span></span>

### <span data-ttu-id="c8f87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f87-114">-DefaultProfile</span></span>
<span data-ttu-id="c8f87-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f87-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f87-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8f87-116">-InputObject</span></span>
<span data-ttu-id="c8f87-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="c8f87-117">IotHub object</span></span>

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

### <span data-ttu-id="c8f87-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c8f87-118">-IotHubName</span></span>
<span data-ttu-id="c8f87-119">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="c8f87-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c8f87-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8f87-120">-Name</span></span>
<span data-ttu-id="c8f87-121">ID för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c8f87-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="c8f87-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8f87-122">-PassThru</span></span>
<span data-ttu-id="c8f87-123">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="c8f87-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="c8f87-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c8f87-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8f87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f87-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8f87-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c8f87-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c8f87-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8f87-127">-ResourceId</span></span>
<span data-ttu-id="c8f87-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="c8f87-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c8f87-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8f87-129">-Confirm</span></span>
<span data-ttu-id="c8f87-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8f87-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f87-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f87-131">-WhatIf</span></span>
<span data-ttu-id="c8f87-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8f87-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8f87-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8f87-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f87-134">CommonParameters</span></span>
<span data-ttu-id="c8f87-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f87-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f87-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f87-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8f87-137">INPUTS</span></span>

### <span data-ttu-id="c8f87-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c8f87-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c8f87-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c8f87-139">System.String</span></span>

## <span data-ttu-id="c8f87-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8f87-140">OUTPUTS</span></span>

### <span data-ttu-id="c8f87-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8f87-141">System.Boolean</span></span>

## <span data-ttu-id="c8f87-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8f87-142">NOTES</span></span>

## <span data-ttu-id="c8f87-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8f87-143">RELATED LINKS</span></span>