---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263055"
---
# <span data-ttu-id="747c5-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="747c5-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="747c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="747c5-102">SYNOPSIS</span></span>
<span data-ttu-id="747c5-103">Ta bort en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="747c5-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="747c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="747c5-104">SYNTAX</span></span>

### <span data-ttu-id="747c5-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="747c5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="747c5-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="747c5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="747c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="747c5-108">DESCRIPTION</span></span>
<span data-ttu-id="747c5-109">Mer https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring information finns i.</span><span class="sxs-lookup"><span data-stu-id="747c5-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="747c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="747c5-110">EXAMPLES</span></span>

### <span data-ttu-id="747c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="747c5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="747c5-112">Ta bort en IoT Edge-distribution.</span><span class="sxs-lookup"><span data-stu-id="747c5-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="747c5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="747c5-113">PARAMETERS</span></span>

### <span data-ttu-id="747c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747c5-114">-DefaultProfile</span></span>
<span data-ttu-id="747c5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="747c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="747c5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="747c5-116">-InputObject</span></span>
<span data-ttu-id="747c5-117">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="747c5-117">IotHub object</span></span>

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

### <span data-ttu-id="747c5-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="747c5-118">-IotHubName</span></span>
<span data-ttu-id="747c5-119">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="747c5-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="747c5-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="747c5-120">-Name</span></span>
<span data-ttu-id="747c5-121">Identifierare för distributionen.</span><span class="sxs-lookup"><span data-stu-id="747c5-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="747c5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="747c5-122">-PassThru</span></span>
<span data-ttu-id="747c5-123">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="747c5-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="747c5-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="747c5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="747c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="747c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="747c5-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="747c5-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="747c5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="747c5-127">-ResourceId</span></span>
<span data-ttu-id="747c5-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="747c5-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="747c5-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="747c5-129">-Confirm</span></span>
<span data-ttu-id="747c5-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="747c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="747c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="747c5-131">-WhatIf</span></span>
<span data-ttu-id="747c5-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="747c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="747c5-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="747c5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="747c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747c5-134">CommonParameters</span></span>
<span data-ttu-id="747c5-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747c5-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747c5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747c5-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="747c5-137">INPUTS</span></span>

### <span data-ttu-id="747c5-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="747c5-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="747c5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="747c5-139">System.String</span></span>

## <span data-ttu-id="747c5-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="747c5-140">OUTPUTS</span></span>

### <span data-ttu-id="747c5-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="747c5-141">System.Boolean</span></span>

## <span data-ttu-id="747c5-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="747c5-142">NOTES</span></span>

## <span data-ttu-id="747c5-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="747c5-143">RELATED LINKS</span></span>