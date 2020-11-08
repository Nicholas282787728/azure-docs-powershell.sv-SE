---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269863"
---
# <span data-ttu-id="cfe0d-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cfe0d-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="cfe0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfe0d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe0d-103">Hämtar de tillgängliga rollerna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="cfe0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfe0d-104">SYNTAX</span></span>

### <span data-ttu-id="cfe0d-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cfe0d-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe0d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe0d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe0d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe0d-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe0d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe0d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="cfe0d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfe0d-109">DESCRIPTION</span></span>
<span data-ttu-id="cfe0d-110">Cmdleten **Get-AzStackEdgeRole** hämtar de tillgängliga IoT-rollerna för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="cfe0d-111">Du kan nämna parametern name för att få information om en specifik IoT-roll.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="cfe0d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfe0d-112">EXAMPLES</span></span>

### <span data-ttu-id="cfe0d-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cfe0d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="cfe0d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfe0d-114">PARAMETERS</span></span>

### <span data-ttu-id="cfe0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe0d-115">-DefaultProfile</span></span>
<span data-ttu-id="cfe0d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe0d-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="cfe0d-117">-DeviceName</span></span>
<span data-ttu-id="cfe0d-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="cfe0d-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe0d-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cfe0d-119">-DeviceObject</span></span>
<span data-ttu-id="cfe0d-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="cfe0d-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe0d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfe0d-121">-Name</span></span>
<span data-ttu-id="cfe0d-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="cfe0d-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="cfe0d-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="cfe0d-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe0d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfe0d-125">-ResourceId</span></span>
<span data-ttu-id="cfe0d-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfe0d-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe0d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe0d-127">CommonParameters</span></span>
<span data-ttu-id="cfe0d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe0d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe0d-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfe0d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe0d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfe0d-130">INPUTS</span></span>

### <span data-ttu-id="cfe0d-131">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cfe0d-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="cfe0d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfe0d-132">OUTPUTS</span></span>

### <span data-ttu-id="cfe0d-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cfe0d-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="cfe0d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfe0d-134">NOTES</span></span>

## <span data-ttu-id="cfe0d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfe0d-135">RELATED LINKS</span></span>
