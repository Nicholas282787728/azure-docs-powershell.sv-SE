---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 61cbe1ef1fc18ba9c2d6455c6cf56b4f951fdfd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743969"
---
# <span data-ttu-id="dc50b-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="dc50b-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="dc50b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc50b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc50b-103">Ta bort en väg i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="dc50b-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="dc50b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc50b-104">SYNTAX</span></span>

### <span data-ttu-id="dc50b-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dc50b-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc50b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc50b-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc50b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc50b-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc50b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc50b-108">DESCRIPTION</span></span>
<span data-ttu-id="dc50b-109">Ta bort en cirkulation till en slut punkt</span><span class="sxs-lookup"><span data-stu-id="dc50b-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="dc50b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc50b-110">EXAMPLES</span></span>

### <span data-ttu-id="dc50b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc50b-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="dc50b-112">Ta bort vägen "R1" från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="dc50b-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="dc50b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc50b-113">PARAMETERS</span></span>

### <span data-ttu-id="dc50b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc50b-114">-DefaultProfile</span></span>
<span data-ttu-id="dc50b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc50b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc50b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc50b-116">-InputObject</span></span>
<span data-ttu-id="dc50b-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="dc50b-117">IotHub Object</span></span>

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

### <span data-ttu-id="dc50b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc50b-118">-Name</span></span>
<span data-ttu-id="dc50b-119">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="dc50b-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dc50b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc50b-120">-PassThru</span></span>
<span data-ttu-id="dc50b-121">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="dc50b-121">Allows to return the boolean object.</span></span> <span data-ttu-id="dc50b-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="dc50b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc50b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc50b-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc50b-124">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="dc50b-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dc50b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc50b-125">-ResourceId</span></span>
<span data-ttu-id="dc50b-126">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="dc50b-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dc50b-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="dc50b-127">-RouteName</span></span>
<span data-ttu-id="dc50b-128">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="dc50b-128">Name of the Route</span></span>

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

### <span data-ttu-id="dc50b-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc50b-129">-Confirm</span></span>
<span data-ttu-id="dc50b-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc50b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc50b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc50b-131">-WhatIf</span></span>
<span data-ttu-id="dc50b-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc50b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc50b-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc50b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc50b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc50b-134">CommonParameters</span></span>
<span data-ttu-id="dc50b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc50b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc50b-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc50b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc50b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc50b-137">INPUTS</span></span>

### <span data-ttu-id="dc50b-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dc50b-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dc50b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc50b-139">System.String</span></span>

## <span data-ttu-id="dc50b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc50b-140">OUTPUTS</span></span>

### <span data-ttu-id="dc50b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc50b-141">System.Boolean</span></span>

## <span data-ttu-id="dc50b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc50b-142">NOTES</span></span>

## <span data-ttu-id="dc50b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc50b-143">RELATED LINKS</span></span>
