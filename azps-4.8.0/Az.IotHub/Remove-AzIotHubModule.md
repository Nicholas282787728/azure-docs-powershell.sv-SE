---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262239"
---
# <span data-ttu-id="e3a77-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="e3a77-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="e3a77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3a77-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a77-103">Ta bort modul (er) på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="e3a77-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e3a77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3a77-104">SYNTAX</span></span>

### <span data-ttu-id="e3a77-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e3a77-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3a77-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3a77-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3a77-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e3a77-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a77-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3a77-108">DESCRIPTION</span></span>
<span data-ttu-id="e3a77-109">Ta bort modul (er) på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="e3a77-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e3a77-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3a77-110">EXAMPLES</span></span>

### <span data-ttu-id="e3a77-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3a77-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="e3a77-112">Ta bort en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="e3a77-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="e3a77-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e3a77-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="e3a77-114">Ta bort alla IoT-moduler.</span><span class="sxs-lookup"><span data-stu-id="e3a77-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="e3a77-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3a77-115">PARAMETERS</span></span>

### <span data-ttu-id="e3a77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a77-116">-DefaultProfile</span></span>
<span data-ttu-id="e3a77-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a77-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e3a77-118">-DeviceId</span></span>
<span data-ttu-id="e3a77-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="e3a77-119">Target Device Id.</span></span>

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

### <span data-ttu-id="e3a77-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3a77-120">-InputObject</span></span>
<span data-ttu-id="e3a77-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="e3a77-121">IotHub object</span></span>

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

### <span data-ttu-id="e3a77-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e3a77-122">-IotHubName</span></span>
<span data-ttu-id="e3a77-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="e3a77-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e3a77-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="e3a77-124">-ModuleId</span></span>
<span data-ttu-id="e3a77-125">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="e3a77-125">Target Module Id.</span></span>

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

### <span data-ttu-id="e3a77-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3a77-126">-PassThru</span></span>
<span data-ttu-id="e3a77-127">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="e3a77-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="e3a77-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e3a77-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3a77-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a77-129">-ResourceGroupName</span></span>
<span data-ttu-id="e3a77-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e3a77-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e3a77-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a77-131">-ResourceId</span></span>
<span data-ttu-id="e3a77-132">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="e3a77-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e3a77-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3a77-133">-Confirm</span></span>
<span data-ttu-id="e3a77-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3a77-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a77-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a77-135">-WhatIf</span></span>
<span data-ttu-id="e3a77-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3a77-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a77-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3a77-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a77-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a77-138">CommonParameters</span></span>
<span data-ttu-id="e3a77-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a77-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a77-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a77-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a77-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3a77-141">INPUTS</span></span>

### <span data-ttu-id="e3a77-142">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e3a77-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e3a77-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a77-143">System.String</span></span>

## <span data-ttu-id="e3a77-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3a77-144">OUTPUTS</span></span>

### <span data-ttu-id="e3a77-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3a77-145">System.Boolean</span></span>

## <span data-ttu-id="e3a77-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3a77-146">NOTES</span></span>

## <span data-ttu-id="e3a77-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3a77-147">RELATED LINKS</span></span>