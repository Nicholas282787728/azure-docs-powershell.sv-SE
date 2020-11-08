---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270991"
---
# <span data-ttu-id="8b12c-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12c-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="8b12c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b12c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b12c-103">Visar en lista över alla eller en särskild IoT-konfiguration för automatisk enhets hantering.</span><span class="sxs-lookup"><span data-stu-id="8b12c-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="8b12c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b12c-104">SYNTAX</span></span>

### <span data-ttu-id="8b12c-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b12c-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b12c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8b12c-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b12c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8b12c-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b12c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b12c-108">DESCRIPTION</span></span>
<span data-ttu-id="8b12c-109">Få information om en automatisk enhets konfiguration eller en lista IoT automatisk enhets hantering i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8b12c-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="8b12c-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management information finns i.</span><span class="sxs-lookup"><span data-stu-id="8b12c-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="8b12c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b12c-111">EXAMPLES</span></span>

### <span data-ttu-id="8b12c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b12c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="8b12c-113">Få information om en IoT automatisk enhets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8b12c-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="8b12c-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8b12c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="8b12c-115">Lista IoT automatisk konfiguration av enhets hantering i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8b12c-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="8b12c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b12c-116">PARAMETERS</span></span>

### <span data-ttu-id="8b12c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b12c-117">-DefaultProfile</span></span>
<span data-ttu-id="8b12c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b12c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b12c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b12c-119">-InputObject</span></span>
<span data-ttu-id="8b12c-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="8b12c-120">IotHub object</span></span>

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

### <span data-ttu-id="8b12c-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8b12c-121">-IotHubName</span></span>
<span data-ttu-id="8b12c-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="8b12c-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8b12c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b12c-123">-Name</span></span>
<span data-ttu-id="8b12c-124">ID för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8b12c-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="8b12c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b12c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b12c-126">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8b12c-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8b12c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b12c-127">-ResourceId</span></span>
<span data-ttu-id="8b12c-128">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="8b12c-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8b12c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b12c-129">CommonParameters</span></span>
<span data-ttu-id="8b12c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b12c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b12c-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b12c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b12c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b12c-132">INPUTS</span></span>

### <span data-ttu-id="8b12c-133">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8b12c-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8b12c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8b12c-134">System.String</span></span>

## <span data-ttu-id="8b12c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b12c-135">OUTPUTS</span></span>

### <span data-ttu-id="8b12c-136">Microsoft. Azure. commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b12c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="8b12c-137">Microsoft. Azure. commands. Management. IotHub. Models. PSConfigurations []</span><span class="sxs-lookup"><span data-stu-id="8b12c-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="8b12c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b12c-138">NOTES</span></span>

## <span data-ttu-id="8b12c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b12c-139">RELATED LINKS</span></span>
