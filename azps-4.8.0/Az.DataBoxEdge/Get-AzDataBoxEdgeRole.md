---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9bda923d7a0e7e999ae8368fd648ee6745cbb226
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101590"
---
# <span data-ttu-id="699c8-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="699c8-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="699c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="699c8-102">SYNOPSIS</span></span>
<span data-ttu-id="699c8-103">Hämtar de tillgängliga rollerna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="699c8-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="699c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="699c8-104">SYNTAX</span></span>

### <span data-ttu-id="699c8-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="699c8-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="699c8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="699c8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="699c8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="699c8-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="699c8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="699c8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="699c8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="699c8-109">DESCRIPTION</span></span>
<span data-ttu-id="699c8-110">Cmdleten **Get-AzDataBoxEdgeRole** hämtar de tillgängliga IoT-rollerna för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="699c8-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="699c8-111">Du kan nämna parametern name för att få information om en specifik IoT-roll.</span><span class="sxs-lookup"><span data-stu-id="699c8-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="699c8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="699c8-112">EXAMPLES</span></span>

### <span data-ttu-id="699c8-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="699c8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="699c8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="699c8-114">PARAMETERS</span></span>

### <span data-ttu-id="699c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699c8-115">-DefaultProfile</span></span>
<span data-ttu-id="699c8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="699c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="699c8-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="699c8-117">-DeviceName</span></span>
<span data-ttu-id="699c8-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="699c8-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699c8-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="699c8-119">-DeviceObject</span></span>
<span data-ttu-id="699c8-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="699c8-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699c8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="699c8-121">-Name</span></span>
<span data-ttu-id="699c8-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="699c8-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="699c8-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="699c8-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="699c8-125">-ResourceId</span></span>
<span data-ttu-id="699c8-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="699c8-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699c8-127">CommonParameters</span></span>
<span data-ttu-id="699c8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699c8-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="699c8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699c8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="699c8-130">INPUTS</span></span>

### <span data-ttu-id="699c8-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="699c8-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="699c8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="699c8-132">OUTPUTS</span></span>

### <span data-ttu-id="699c8-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="699c8-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="699c8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="699c8-134">NOTES</span></span>

## <span data-ttu-id="699c8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="699c8-135">RELATED LINKS</span></span>
