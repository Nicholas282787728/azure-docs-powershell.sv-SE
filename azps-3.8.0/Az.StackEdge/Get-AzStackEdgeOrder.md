---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088796"
---
# <span data-ttu-id="8cae6-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8cae6-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="8cae6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cae6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cae6-103">Skaffa beställnings uppgifter för en enhet</span><span class="sxs-lookup"><span data-stu-id="8cae6-103">Get the order details for a device</span></span>

## <span data-ttu-id="8cae6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cae6-104">SYNTAX</span></span>

### <span data-ttu-id="8cae6-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8cae6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cae6-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cae6-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cae6-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cae6-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cae6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cae6-108">DESCRIPTION</span></span>
<span data-ttu-id="8cae6-109">Cmdleten **Get-AzStackEdgeOrder** hämtar beställnings informationen för en grupp Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="8cae6-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="8cae6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cae6-110">EXAMPLES</span></span>

### <span data-ttu-id="8cae6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8cae6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="8cae6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cae6-112">PARAMETERS</span></span>

### <span data-ttu-id="8cae6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cae6-113">-DefaultProfile</span></span>
<span data-ttu-id="8cae6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8cae6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cae6-115">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="8cae6-115">-DeviceName</span></span>
<span data-ttu-id="8cae6-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8cae6-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cae6-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8cae6-117">-DeviceObject</span></span>
<span data-ttu-id="8cae6-118">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="8cae6-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cae6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cae6-119">-ResourceGroupName</span></span>
<span data-ttu-id="8cae6-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8cae6-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cae6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cae6-121">-ResourceId</span></span>
<span data-ttu-id="8cae6-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cae6-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="8cae6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cae6-123">CommonParameters</span></span>
<span data-ttu-id="8cae6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cae6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cae6-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cae6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cae6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cae6-126">INPUTS</span></span>

### <span data-ttu-id="8cae6-127">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8cae6-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="8cae6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8cae6-128">System.String</span></span>

## <span data-ttu-id="8cae6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cae6-129">OUTPUTS</span></span>

### <span data-ttu-id="8cae6-130">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8cae6-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="8cae6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cae6-131">NOTES</span></span>

## <span data-ttu-id="8cae6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cae6-132">RELATED LINKS</span></span>