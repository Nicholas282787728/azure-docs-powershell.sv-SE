---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262241"
---
# <span data-ttu-id="de2b6-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="de2b6-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="de2b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="de2b6-103">Hämta inställningar för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="de2b6-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="de2b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de2b6-104">SYNTAX</span></span>

### <span data-ttu-id="de2b6-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="de2b6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de2b6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="de2b6-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de2b6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="de2b6-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de2b6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de2b6-108">DESCRIPTION</span></span>
<span data-ttu-id="de2b6-109">Hämta inställningar för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="de2b6-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="de2b6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de2b6-110">EXAMPLES</span></span>

### <span data-ttu-id="de2b6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de2b6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="de2b6-112">Hämta inställningar för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="de2b6-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="de2b6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de2b6-113">PARAMETERS</span></span>

### <span data-ttu-id="de2b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2b6-114">-DefaultProfile</span></span>
<span data-ttu-id="de2b6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de2b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de2b6-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="de2b6-116">-DeviceId</span></span>
<span data-ttu-id="de2b6-117">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="de2b6-117">Target Device Id.</span></span>

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

### <span data-ttu-id="de2b6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de2b6-118">-InputObject</span></span>
<span data-ttu-id="de2b6-119">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="de2b6-119">IotHub object</span></span>

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

### <span data-ttu-id="de2b6-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="de2b6-120">-IotHubName</span></span>
<span data-ttu-id="de2b6-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="de2b6-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="de2b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="de2b6-123">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="de2b6-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="de2b6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de2b6-124">-ResourceId</span></span>
<span data-ttu-id="de2b6-125">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="de2b6-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="de2b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2b6-126">CommonParameters</span></span>
<span data-ttu-id="de2b6-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2b6-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de2b6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2b6-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de2b6-129">INPUTS</span></span>

### <span data-ttu-id="de2b6-130">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="de2b6-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="de2b6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="de2b6-131">System.String</span></span>

## <span data-ttu-id="de2b6-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de2b6-132">OUTPUTS</span></span>

### <span data-ttu-id="de2b6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="de2b6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="de2b6-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de2b6-134">NOTES</span></span>

## <span data-ttu-id="de2b6-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de2b6-135">RELATED LINKS</span></span>
