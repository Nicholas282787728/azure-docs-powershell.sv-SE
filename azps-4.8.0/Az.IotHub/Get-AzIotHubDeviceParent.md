---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259696"
---
# <span data-ttu-id="2b8b0-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="2b8b0-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="2b8b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8b0-103">Hämta överordnad enhet för den angivna enheten.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="2b8b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b8b0-104">SYNTAX</span></span>

### <span data-ttu-id="2b8b0-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2b8b0-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b8b0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b8b0-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b8b0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b8b0-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8b0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b8b0-108">DESCRIPTION</span></span>
<span data-ttu-id="2b8b0-109">Hämta överordnad enhet för den angivna icke-gränsen.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="2b8b0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b8b0-110">EXAMPLES</span></span>

### <span data-ttu-id="2b8b0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2b8b0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
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
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="2b8b0-112">Hämta överordnad enhet för den angivna icke-gränsen.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="2b8b0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b8b0-113">PARAMETERS</span></span>

### <span data-ttu-id="2b8b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8b0-114">-DefaultProfile</span></span>
<span data-ttu-id="2b8b0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b8b0-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2b8b0-116">-DeviceId</span></span>
<span data-ttu-id="2b8b0-117">ID för icke-Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="2b8b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b8b0-118">-InputObject</span></span>
<span data-ttu-id="2b8b0-119">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="2b8b0-119">IotHub object</span></span>

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

### <span data-ttu-id="2b8b0-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2b8b0-120">-IotHubName</span></span>
<span data-ttu-id="2b8b0-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="2b8b0-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2b8b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b8b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b8b0-123">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="2b8b0-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2b8b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b8b0-124">-ResourceId</span></span>
<span data-ttu-id="2b8b0-125">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="2b8b0-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2b8b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8b0-126">CommonParameters</span></span>
<span data-ttu-id="2b8b0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b8b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8b0-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8b0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8b0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b8b0-129">INPUTS</span></span>

### <span data-ttu-id="2b8b0-130">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2b8b0-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2b8b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2b8b0-131">System.String</span></span>

## <span data-ttu-id="2b8b0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b8b0-132">OUTPUTS</span></span>

### <span data-ttu-id="2b8b0-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="2b8b0-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="2b8b0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b8b0-134">NOTES</span></span>

## <span data-ttu-id="2b8b0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b8b0-135">RELATED LINKS</span></span>