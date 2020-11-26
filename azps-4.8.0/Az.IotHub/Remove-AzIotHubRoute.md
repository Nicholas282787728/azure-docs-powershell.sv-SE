---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102842"
---
# <span data-ttu-id="3a747-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3a747-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="3a747-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a747-102">SYNOPSIS</span></span>
<span data-ttu-id="3a747-103">Ta bort en väg i IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3a747-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="3a747-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a747-104">SYNTAX</span></span>

### <span data-ttu-id="3a747-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3a747-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a747-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a747-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a747-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3a747-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a747-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a747-108">DESCRIPTION</span></span>
<span data-ttu-id="3a747-109">Ta bort en cirkulation till en slut punkt</span><span class="sxs-lookup"><span data-stu-id="3a747-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="3a747-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a747-110">EXAMPLES</span></span>

### <span data-ttu-id="3a747-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3a747-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="3a747-112">Ta bort vägen "R1" från "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3a747-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="3a747-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a747-113">PARAMETERS</span></span>

### <span data-ttu-id="3a747-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a747-114">-DefaultProfile</span></span>
<span data-ttu-id="3a747-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a747-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a747-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a747-116">-InputObject</span></span>
<span data-ttu-id="3a747-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="3a747-117">IotHub Object</span></span>

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

### <span data-ttu-id="3a747-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3a747-118">-Name</span></span>
<span data-ttu-id="3a747-119">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="3a747-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3a747-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a747-120">-PassThru</span></span>
<span data-ttu-id="3a747-121">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="3a747-121">Allows to return the boolean object.</span></span> <span data-ttu-id="3a747-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3a747-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a747-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a747-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a747-124">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="3a747-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3a747-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a747-125">-ResourceId</span></span>
<span data-ttu-id="3a747-126">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="3a747-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3a747-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3a747-127">-RouteName</span></span>
<span data-ttu-id="3a747-128">Vägens namn</span><span class="sxs-lookup"><span data-stu-id="3a747-128">Name of the Route</span></span>

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

### <span data-ttu-id="3a747-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3a747-129">-Confirm</span></span>
<span data-ttu-id="3a747-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3a747-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a747-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a747-131">-WhatIf</span></span>
<span data-ttu-id="3a747-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3a747-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a747-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3a747-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a747-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a747-134">CommonParameters</span></span>
<span data-ttu-id="3a747-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a747-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a747-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a747-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a747-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a747-137">INPUTS</span></span>

### <span data-ttu-id="3a747-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3a747-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3a747-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3a747-139">System.String</span></span>

## <span data-ttu-id="3a747-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a747-140">OUTPUTS</span></span>

### <span data-ttu-id="3a747-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a747-141">System.Boolean</span></span>

## <span data-ttu-id="3a747-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a747-142">NOTES</span></span>

## <span data-ttu-id="3a747-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a747-143">RELATED LINKS</span></span>