---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526028"
---
# <span data-ttu-id="8e487-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="8e487-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="8e487-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e487-102">SYNOPSIS</span></span>
<span data-ttu-id="8e487-103">Skaffa anslutnings strängen för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8e487-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="8e487-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e487-104">SYNTAX</span></span>

### <span data-ttu-id="8e487-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8e487-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e487-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e487-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e487-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8e487-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e487-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e487-108">DESCRIPTION</span></span>
<span data-ttu-id="8e487-109">Lista anslutnings sträng för alla enheter eller en mål-IoT-enhet i ett Azure IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8e487-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="8e487-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e487-110">EXAMPLES</span></span>

### <span data-ttu-id="8e487-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e487-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="8e487-112">Visa alla enheter anslutnings sträng i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="8e487-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="8e487-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8e487-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="8e487-114">Hämta sekundär anslutnings strängen för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="8e487-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="8e487-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e487-115">PARAMETERS</span></span>

### <span data-ttu-id="8e487-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e487-116">-DefaultProfile</span></span>
<span data-ttu-id="8e487-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e487-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e487-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8e487-118">-DeviceId</span></span>
<span data-ttu-id="8e487-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="8e487-119">Target Device Id.</span></span>

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

### <span data-ttu-id="8e487-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e487-120">-InputObject</span></span>
<span data-ttu-id="8e487-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="8e487-121">IotHub object</span></span>

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

### <span data-ttu-id="8e487-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8e487-122">-IotHubName</span></span>
<span data-ttu-id="8e487-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="8e487-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8e487-124">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="8e487-124">-KeyType</span></span>
<span data-ttu-id="8e487-125">Typ av policy för delad åtkomst för autentisering.</span><span class="sxs-lookup"><span data-stu-id="8e487-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e487-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e487-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e487-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8e487-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8e487-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e487-128">-ResourceId</span></span>
<span data-ttu-id="8e487-129">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="8e487-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8e487-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e487-130">CommonParameters</span></span>
<span data-ttu-id="8e487-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e487-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e487-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e487-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e487-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e487-133">INPUTS</span></span>

### <span data-ttu-id="8e487-134">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8e487-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8e487-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8e487-135">System.String</span></span>

## <span data-ttu-id="8e487-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e487-136">OUTPUTS</span></span>

### <span data-ttu-id="8e487-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="8e487-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="8e487-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e487-138">NOTES</span></span>

## <span data-ttu-id="8e487-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e487-139">RELATED LINKS</span></span>
