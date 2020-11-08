---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270984"
---
# <span data-ttu-id="4b603-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="4b603-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="4b603-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b603-102">SYNOPSIS</span></span>
<span data-ttu-id="4b603-103">Skriv ut kommaavgränsad lista över tilldelade underordnade enheter.</span><span class="sxs-lookup"><span data-stu-id="4b603-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="4b603-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b603-104">SYNTAX</span></span>

### <span data-ttu-id="4b603-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4b603-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b603-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4b603-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b603-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4b603-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b603-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b603-108">DESCRIPTION</span></span>
<span data-ttu-id="4b603-109">Visa alla tilldelade icke-arbetsenheter som kommaavgränsad lista över alla anslags enheter eller angiven enhet.</span><span class="sxs-lookup"><span data-stu-id="4b603-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="4b603-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b603-110">EXAMPLES</span></span>

### <span data-ttu-id="4b603-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4b603-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="4b603-112">Visa alla tilldelade icke-arbetsenheter som kommaavgränsad lista.</span><span class="sxs-lookup"><span data-stu-id="4b603-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="4b603-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4b603-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="4b603-114">Visa alla tilldelade icke-arbetsenheter som kommaavgränsad lista över alla kant enheter.</span><span class="sxs-lookup"><span data-stu-id="4b603-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="4b603-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b603-115">PARAMETERS</span></span>

### <span data-ttu-id="4b603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b603-116">-DefaultProfile</span></span>
<span data-ttu-id="4b603-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b603-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b603-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4b603-118">-DeviceId</span></span>
<span data-ttu-id="4b603-119">ID för Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="4b603-119">Id of edge device.</span></span>

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

### <span data-ttu-id="4b603-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b603-120">-InputObject</span></span>
<span data-ttu-id="4b603-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="4b603-121">IotHub object</span></span>

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

### <span data-ttu-id="4b603-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4b603-122">-IotHubName</span></span>
<span data-ttu-id="4b603-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="4b603-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4b603-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b603-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b603-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4b603-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4b603-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b603-126">-ResourceId</span></span>
<span data-ttu-id="4b603-127">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="4b603-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4b603-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b603-128">CommonParameters</span></span>
<span data-ttu-id="4b603-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b603-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b603-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b603-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b603-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b603-131">INPUTS</span></span>

### <span data-ttu-id="4b603-132">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4b603-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4b603-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4b603-133">System.String</span></span>

## <span data-ttu-id="4b603-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b603-134">OUTPUTS</span></span>

### <span data-ttu-id="4b603-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="4b603-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="4b603-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="4b603-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="4b603-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b603-137">NOTES</span></span>

## <span data-ttu-id="4b603-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b603-138">RELATED LINKS</span></span>
