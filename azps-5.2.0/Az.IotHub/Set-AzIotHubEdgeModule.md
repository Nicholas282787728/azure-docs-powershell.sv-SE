---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407755"
---
# <span data-ttu-id="a8bd8-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="a8bd8-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="a8bd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bd8-103">Ställ in Edge-moduler på en enda Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="a8bd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8bd8-104">SYNTAX</span></span>

### <span data-ttu-id="a8bd8-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a8bd8-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8bd8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a8bd8-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8bd8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a8bd8-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8bd8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="a8bd8-109">Tillämpar det tillhandahållna modulens konfigurations innehåll på den angivna Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="a8bd8-110">Obs! när kommandot körs skapas en samling av moduler som används för enheten.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="a8bd8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8bd8-111">EXAMPLES</span></span>

### <span data-ttu-id="a8bd8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8bd8-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="a8bd8-113">Testa moduler under utveckling genom att ange moduler på en målen het.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="a8bd8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8bd8-114">PARAMETERS</span></span>

### <span data-ttu-id="a8bd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bd8-115">-DefaultProfile</span></span>
<span data-ttu-id="a8bd8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8bd8-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a8bd8-117">-DeviceId</span></span>
<span data-ttu-id="a8bd8-118">Enhets-ID för Target Edge.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="a8bd8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8bd8-119">-InputObject</span></span>
<span data-ttu-id="a8bd8-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="a8bd8-120">IotHub object</span></span>

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

### <span data-ttu-id="a8bd8-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a8bd8-121">-IotHubName</span></span>
<span data-ttu-id="a8bd8-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="a8bd8-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a8bd8-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="a8bd8-123">-ModulesContent</span></span>
<span data-ttu-id="a8bd8-124">Konfigurations innehåll för moduler för IoT Edge-enheter.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8bd8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bd8-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8bd8-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="a8bd8-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a8bd8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8bd8-127">-ResourceId</span></span>
<span data-ttu-id="a8bd8-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="a8bd8-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a8bd8-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8bd8-129">-Confirm</span></span>
<span data-ttu-id="a8bd8-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8bd8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bd8-131">-WhatIf</span></span>
<span data-ttu-id="a8bd8-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8bd8-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8bd8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bd8-134">CommonParameters</span></span>
<span data-ttu-id="a8bd8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bd8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bd8-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bd8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bd8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8bd8-137">INPUTS</span></span>

### <span data-ttu-id="a8bd8-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a8bd8-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a8bd8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a8bd8-139">System.String</span></span>

## <span data-ttu-id="a8bd8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8bd8-140">OUTPUTS</span></span>

### <span data-ttu-id="a8bd8-141">Microsoft. Azure. commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="a8bd8-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="a8bd8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8bd8-142">NOTES</span></span>

## <span data-ttu-id="a8bd8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8bd8-143">RELATED LINKS</span></span>
