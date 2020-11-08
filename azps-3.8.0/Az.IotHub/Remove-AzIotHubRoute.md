---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089236"
---
# <span data-ttu-id="d0f41-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d0f41-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="d0f41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0f41-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f41-103">Ta bort en väg i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="d0f41-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="d0f41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0f41-104">SYNTAX</span></span>

### <span data-ttu-id="d0f41-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d0f41-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f41-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0f41-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f41-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0f41-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f41-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0f41-108">DESCRIPTION</span></span>
<span data-ttu-id="d0f41-109">Ta bort en cirkulation till en slut punkt</span><span class="sxs-lookup"><span data-stu-id="d0f41-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="d0f41-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0f41-110">EXAMPLES</span></span>

### <span data-ttu-id="d0f41-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0f41-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="d0f41-112">Ta bort vägen "R1" från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="d0f41-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d0f41-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0f41-113">PARAMETERS</span></span>

### <span data-ttu-id="d0f41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f41-114">-DefaultProfile</span></span>
<span data-ttu-id="d0f41-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f41-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0f41-116">-InputObject</span></span>
<span data-ttu-id="d0f41-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="d0f41-117">IotHub Object</span></span>

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

### <span data-ttu-id="d0f41-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0f41-118">-Name</span></span>
<span data-ttu-id="d0f41-119">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="d0f41-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d0f41-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0f41-120">-PassThru</span></span>
<span data-ttu-id="d0f41-121">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="d0f41-121">Allows to return the boolean object.</span></span> <span data-ttu-id="d0f41-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d0f41-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0f41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f41-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0f41-124">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d0f41-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0f41-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f41-125">-ResourceId</span></span>
<span data-ttu-id="d0f41-126">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="d0f41-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d0f41-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="d0f41-127">-RouteName</span></span>
<span data-ttu-id="d0f41-128">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="d0f41-128">Name of the Route</span></span>

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

### <span data-ttu-id="d0f41-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0f41-129">-Confirm</span></span>
<span data-ttu-id="d0f41-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0f41-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f41-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f41-131">-WhatIf</span></span>
<span data-ttu-id="d0f41-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0f41-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f41-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0f41-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f41-134">CommonParameters</span></span>
<span data-ttu-id="d0f41-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f41-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f41-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f41-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0f41-137">INPUTS</span></span>

### <span data-ttu-id="d0f41-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d0f41-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d0f41-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f41-139">System.String</span></span>

## <span data-ttu-id="d0f41-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0f41-140">OUTPUTS</span></span>

### <span data-ttu-id="d0f41-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0f41-141">System.Boolean</span></span>

## <span data-ttu-id="d0f41-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0f41-142">NOTES</span></span>

## <span data-ttu-id="d0f41-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0f41-143">RELATED LINKS</span></span>
