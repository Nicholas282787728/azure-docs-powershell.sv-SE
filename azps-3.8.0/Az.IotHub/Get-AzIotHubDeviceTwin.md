---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090721"
---
# <span data-ttu-id="72767-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="72767-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="72767-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72767-102">SYNOPSIS</span></span>
<span data-ttu-id="72767-103">Hämtar en enhet.</span><span class="sxs-lookup"><span data-stu-id="72767-103">Gets a device twin.</span></span>

## <span data-ttu-id="72767-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72767-104">SYNTAX</span></span>

### <span data-ttu-id="72767-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="72767-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72767-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72767-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72767-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72767-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72767-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72767-108">DESCRIPTION</span></span>
<span data-ttu-id="72767-109">Hämtar en enhet.</span><span class="sxs-lookup"><span data-stu-id="72767-109">Gets a device twin.</span></span> <span data-ttu-id="72767-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins information finns i.</span><span class="sxs-lookup"><span data-stu-id="72767-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="72767-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72767-111">EXAMPLES</span></span>

### <span data-ttu-id="72767-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72767-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="72767-113">Returnerar enhetens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="72767-113">Returns the device twin object.</span></span>

## <span data-ttu-id="72767-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72767-114">PARAMETERS</span></span>

### <span data-ttu-id="72767-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72767-115">-DefaultProfile</span></span>
<span data-ttu-id="72767-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72767-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72767-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="72767-117">-DeviceId</span></span>
<span data-ttu-id="72767-118">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="72767-118">Target Device Id.</span></span>

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

### <span data-ttu-id="72767-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72767-119">-InputObject</span></span>
<span data-ttu-id="72767-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="72767-120">IotHub object</span></span>

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

### <span data-ttu-id="72767-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="72767-121">-IotHubName</span></span>
<span data-ttu-id="72767-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="72767-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="72767-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72767-123">-ResourceGroupName</span></span>
<span data-ttu-id="72767-124">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="72767-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="72767-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72767-125">-ResourceId</span></span>
<span data-ttu-id="72767-126">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="72767-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="72767-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72767-127">CommonParameters</span></span>
<span data-ttu-id="72767-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72767-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72767-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72767-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72767-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72767-130">INPUTS</span></span>

### <span data-ttu-id="72767-131">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="72767-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="72767-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72767-132">System.String</span></span>

## <span data-ttu-id="72767-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72767-133">OUTPUTS</span></span>

### <span data-ttu-id="72767-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="72767-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="72767-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72767-135">NOTES</span></span>

## <span data-ttu-id="72767-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72767-136">RELATED LINKS</span></span>
