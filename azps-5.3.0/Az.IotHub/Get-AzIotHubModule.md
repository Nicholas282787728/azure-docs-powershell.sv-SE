---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526015"
---
# <span data-ttu-id="588e7-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="588e7-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="588e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="588e7-102">SYNOPSIS</span></span>
<span data-ttu-id="588e7-103">Få information om en IoT-modul eller listmallar på en IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="588e7-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="588e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="588e7-104">SYNTAX</span></span>

### <span data-ttu-id="588e7-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="588e7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="588e7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="588e7-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="588e7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="588e7-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="588e7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="588e7-108">DESCRIPTION</span></span>
<span data-ttu-id="588e7-109">Få information om en IoT-modul eller listmallar på en IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="588e7-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="588e7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="588e7-110">EXAMPLES</span></span>

### <span data-ttu-id="588e7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="588e7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

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

<span data-ttu-id="588e7-112">Få information om en IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="588e7-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="588e7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="588e7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="588e7-114">Visa alla moduler på en IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="588e7-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="588e7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="588e7-115">PARAMETERS</span></span>

### <span data-ttu-id="588e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588e7-116">-DefaultProfile</span></span>
<span data-ttu-id="588e7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="588e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588e7-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="588e7-118">-DeviceId</span></span>
<span data-ttu-id="588e7-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="588e7-119">Target Device Id.</span></span>

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

### <span data-ttu-id="588e7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="588e7-120">-InputObject</span></span>
<span data-ttu-id="588e7-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="588e7-121">IotHub object</span></span>

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

### <span data-ttu-id="588e7-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="588e7-122">-IotHubName</span></span>
<span data-ttu-id="588e7-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="588e7-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="588e7-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="588e7-124">-ModuleId</span></span>
<span data-ttu-id="588e7-125">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="588e7-125">Target Module Id.</span></span>

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

### <span data-ttu-id="588e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="588e7-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="588e7-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="588e7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="588e7-128">-ResourceId</span></span>
<span data-ttu-id="588e7-129">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="588e7-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="588e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588e7-130">CommonParameters</span></span>
<span data-ttu-id="588e7-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588e7-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="588e7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588e7-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="588e7-133">INPUTS</span></span>

### <span data-ttu-id="588e7-134">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="588e7-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="588e7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="588e7-135">System.String</span></span>

## <span data-ttu-id="588e7-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="588e7-136">OUTPUTS</span></span>

### <span data-ttu-id="588e7-137">Microsoft. Azure. commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="588e7-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="588e7-138">Microsoft. Azure. commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="588e7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="588e7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="588e7-139">NOTES</span></span>

## <span data-ttu-id="588e7-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="588e7-140">RELATED LINKS</span></span>
