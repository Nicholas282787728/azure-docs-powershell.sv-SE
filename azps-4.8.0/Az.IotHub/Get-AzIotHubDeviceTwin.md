---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259694"
---
# <span data-ttu-id="1adac-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="1adac-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="1adac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1adac-102">SYNOPSIS</span></span>
<span data-ttu-id="1adac-103">Hämtar en enhet.</span><span class="sxs-lookup"><span data-stu-id="1adac-103">Gets a device twin.</span></span>

## <span data-ttu-id="1adac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1adac-104">SYNTAX</span></span>

### <span data-ttu-id="1adac-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1adac-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1adac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1adac-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1adac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1adac-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1adac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1adac-108">DESCRIPTION</span></span>
<span data-ttu-id="1adac-109">Hämtar en enhet.</span><span class="sxs-lookup"><span data-stu-id="1adac-109">Gets a device twin.</span></span> <span data-ttu-id="1adac-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins information finns i.</span><span class="sxs-lookup"><span data-stu-id="1adac-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="1adac-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1adac-111">EXAMPLES</span></span>

### <span data-ttu-id="1adac-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1adac-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="1adac-113">Returnerar enhetens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="1adac-113">Returns the device twin object.</span></span>

## <span data-ttu-id="1adac-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1adac-114">PARAMETERS</span></span>

### <span data-ttu-id="1adac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adac-115">-DefaultProfile</span></span>
<span data-ttu-id="1adac-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1adac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1adac-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1adac-117">-DeviceId</span></span>
<span data-ttu-id="1adac-118">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="1adac-118">Target Device Id.</span></span>

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

### <span data-ttu-id="1adac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1adac-119">-InputObject</span></span>
<span data-ttu-id="1adac-120">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="1adac-120">IotHub object</span></span>

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

### <span data-ttu-id="1adac-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1adac-121">-IotHubName</span></span>
<span data-ttu-id="1adac-122">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="1adac-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1adac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1adac-123">-ResourceGroupName</span></span>
<span data-ttu-id="1adac-124">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="1adac-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1adac-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1adac-125">-ResourceId</span></span>
<span data-ttu-id="1adac-126">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="1adac-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1adac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adac-127">CommonParameters</span></span>
<span data-ttu-id="1adac-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1adac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adac-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1adac-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adac-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1adac-130">INPUTS</span></span>

### <span data-ttu-id="1adac-131">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1adac-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1adac-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1adac-132">System.String</span></span>

## <span data-ttu-id="1adac-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1adac-133">OUTPUTS</span></span>

### <span data-ttu-id="1adac-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="1adac-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="1adac-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1adac-135">NOTES</span></span>

## <span data-ttu-id="1adac-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1adac-136">RELATED LINKS</span></span>
