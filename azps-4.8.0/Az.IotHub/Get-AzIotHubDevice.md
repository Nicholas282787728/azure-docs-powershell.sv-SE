---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261092"
---
# <span data-ttu-id="4a8eb-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="4a8eb-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="4a8eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8eb-103">Visar alla enheter eller en viss enhet i ett Azure IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="4a8eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a8eb-104">SYNTAX</span></span>

### <span data-ttu-id="4a8eb-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4a8eb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a8eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a8eb-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a8eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a8eb-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a8eb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a8eb-108">DESCRIPTION</span></span>
<span data-ttu-id="4a8eb-109">Få information om en IoT Hub-enhet eller en lista över alla enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="4a8eb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a8eb-110">EXAMPLES</span></span>

### <span data-ttu-id="4a8eb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a8eb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="4a8eb-112">Visa alla enheter i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="4a8eb-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4a8eb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="4a8eb-114">Få information om en IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="4a8eb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a8eb-115">PARAMETERS</span></span>

### <span data-ttu-id="4a8eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8eb-116">-DefaultProfile</span></span>
<span data-ttu-id="4a8eb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8eb-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4a8eb-118">-DeviceId</span></span>
<span data-ttu-id="4a8eb-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-119">Target Device Id.</span></span>

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

### <span data-ttu-id="4a8eb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a8eb-120">-InputObject</span></span>
<span data-ttu-id="4a8eb-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="4a8eb-121">IotHub object</span></span>

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

### <span data-ttu-id="4a8eb-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4a8eb-122">-IotHubName</span></span>
<span data-ttu-id="4a8eb-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="4a8eb-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4a8eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a8eb-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="4a8eb-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4a8eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a8eb-126">-ResourceId</span></span>
<span data-ttu-id="4a8eb-127">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="4a8eb-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4a8eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8eb-128">CommonParameters</span></span>
<span data-ttu-id="4a8eb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8eb-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a8eb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8eb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a8eb-131">INPUTS</span></span>

### <span data-ttu-id="4a8eb-132">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4a8eb-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4a8eb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a8eb-133">System.String</span></span>

## <span data-ttu-id="4a8eb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a8eb-134">OUTPUTS</span></span>

### <span data-ttu-id="4a8eb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="4a8eb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="4a8eb-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices []</span><span class="sxs-lookup"><span data-stu-id="4a8eb-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="4a8eb-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a8eb-137">NOTES</span></span>

## <span data-ttu-id="4a8eb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a8eb-138">RELATED LINKS</span></span>
