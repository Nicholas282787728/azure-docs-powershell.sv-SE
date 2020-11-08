---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259470"
---
# <span data-ttu-id="97fa3-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="97fa3-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="97fa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="97fa3-103">Ange den överordnade enheten för den angivna enheten.</span><span class="sxs-lookup"><span data-stu-id="97fa3-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="97fa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97fa3-104">SYNTAX</span></span>

### <span data-ttu-id="97fa3-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="97fa3-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97fa3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97fa3-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97fa3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="97fa3-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97fa3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97fa3-108">DESCRIPTION</span></span>
<span data-ttu-id="97fa3-109">Ange överordnad enhet för den angivna icke-gränsen.</span><span class="sxs-lookup"><span data-stu-id="97fa3-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="97fa3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97fa3-110">EXAMPLES</span></span>

### <span data-ttu-id="97fa3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97fa3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="97fa3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97fa3-112">PARAMETERS</span></span>

### <span data-ttu-id="97fa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fa3-113">-DefaultProfile</span></span>
<span data-ttu-id="97fa3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="97fa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97fa3-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="97fa3-115">-DeviceId</span></span>
<span data-ttu-id="97fa3-116">ID för icke-Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="97fa3-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="97fa3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="97fa3-117">-Force</span></span>
<span data-ttu-id="97fa3-118">Skriver över den överordnade enheten för den icke-fristående enheten.</span><span class="sxs-lookup"><span data-stu-id="97fa3-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="97fa3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97fa3-119">-InputObject</span></span>
<span data-ttu-id="97fa3-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="97fa3-120">IotHub object</span></span>

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

### <span data-ttu-id="97fa3-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="97fa3-121">-IotHubName</span></span>
<span data-ttu-id="97fa3-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="97fa3-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="97fa3-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="97fa3-123">-ParentDeviceId</span></span>
<span data-ttu-id="97fa3-124">ID för Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="97fa3-124">Id of edge device.</span></span>

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

### <span data-ttu-id="97fa3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97fa3-125">-ResourceGroupName</span></span>
<span data-ttu-id="97fa3-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="97fa3-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="97fa3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97fa3-127">-ResourceId</span></span>
<span data-ttu-id="97fa3-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="97fa3-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="97fa3-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97fa3-129">-Confirm</span></span>
<span data-ttu-id="97fa3-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97fa3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97fa3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97fa3-131">-WhatIf</span></span>
<span data-ttu-id="97fa3-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97fa3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97fa3-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97fa3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97fa3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fa3-134">CommonParameters</span></span>
<span data-ttu-id="97fa3-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97fa3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fa3-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97fa3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fa3-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97fa3-137">INPUTS</span></span>

### <span data-ttu-id="97fa3-138">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="97fa3-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="97fa3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97fa3-139">System.String</span></span>

## <span data-ttu-id="97fa3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97fa3-140">OUTPUTS</span></span>

### <span data-ttu-id="97fa3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="97fa3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="97fa3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97fa3-142">NOTES</span></span>

## <span data-ttu-id="97fa3-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97fa3-143">RELATED LINKS</span></span>
