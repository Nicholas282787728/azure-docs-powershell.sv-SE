---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271005"
---
# <span data-ttu-id="391f4-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="391f4-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="391f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="391f4-102">SYNOPSIS</span></span>
<span data-ttu-id="391f4-103">Skapa en modul på en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="391f4-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="391f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="391f4-104">SYNTAX</span></span>

### <span data-ttu-id="391f4-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="391f4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="391f4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="391f4-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="391f4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="391f4-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="391f4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="391f4-108">DESCRIPTION</span></span>
<span data-ttu-id="391f4-109">Skapa en modul på en mål-IoT-enhet med en annan autentiseringstyp i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="391f4-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="391f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="391f4-110">EXAMPLES</span></span>

### <span data-ttu-id="391f4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="391f4-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="391f4-112">Skapa en modul på en mål-IoT-enhet med standard verifiering (delad privat telefon).</span><span class="sxs-lookup"><span data-stu-id="391f4-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="391f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="391f4-113">PARAMETERS</span></span>

### <span data-ttu-id="391f4-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="391f4-114">-AuthMethod</span></span>
<span data-ttu-id="391f4-115">Den autentiseringstyp som en enhet ska skapas med.</span><span class="sxs-lookup"><span data-stu-id="391f4-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391f4-116">-DefaultProfile</span></span>
<span data-ttu-id="391f4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="391f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="391f4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="391f4-118">-DeviceId</span></span>
<span data-ttu-id="391f4-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="391f4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="391f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="391f4-120">-InputObject</span></span>
<span data-ttu-id="391f4-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="391f4-121">IotHub object</span></span>

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

### <span data-ttu-id="391f4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="391f4-122">-IotHubName</span></span>
<span data-ttu-id="391f4-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="391f4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="391f4-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="391f4-124">-ModuleId</span></span>
<span data-ttu-id="391f4-125">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="391f4-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391f4-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="391f4-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="391f4-127">Uttryckligt självsignerat certifikat-tumavtryck som ska användas för primär nycklar.</span><span class="sxs-lookup"><span data-stu-id="391f4-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="391f4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="391f4-128">-ResourceGroupName</span></span>
<span data-ttu-id="391f4-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="391f4-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="391f4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="391f4-130">-ResourceId</span></span>
<span data-ttu-id="391f4-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="391f4-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="391f4-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="391f4-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="391f4-133">Uttryckligt självsignerat certifikat-tumavtryck att använda för sekundär nycklar.</span><span class="sxs-lookup"><span data-stu-id="391f4-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391f4-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="391f4-134">-Confirm</span></span>
<span data-ttu-id="391f4-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="391f4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="391f4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="391f4-136">-WhatIf</span></span>
<span data-ttu-id="391f4-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="391f4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="391f4-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="391f4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="391f4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391f4-139">CommonParameters</span></span>
<span data-ttu-id="391f4-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="391f4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391f4-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="391f4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391f4-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="391f4-142">INPUTS</span></span>

### <span data-ttu-id="391f4-143">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="391f4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="391f4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="391f4-144">System.String</span></span>

## <span data-ttu-id="391f4-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="391f4-145">OUTPUTS</span></span>

### <span data-ttu-id="391f4-146">Microsoft. Azure. commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="391f4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="391f4-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="391f4-147">NOTES</span></span>

## <span data-ttu-id="391f4-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="391f4-148">RELATED LINKS</span></span>