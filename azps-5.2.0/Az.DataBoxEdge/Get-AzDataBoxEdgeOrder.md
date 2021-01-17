---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391347"
---
# <span data-ttu-id="6097f-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6097f-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="6097f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6097f-102">SYNOPSIS</span></span>
<span data-ttu-id="6097f-103">Skaffa beställnings uppgifter för en enhet</span><span class="sxs-lookup"><span data-stu-id="6097f-103">Get the order details for a device</span></span>

## <span data-ttu-id="6097f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6097f-104">SYNTAX</span></span>

### <span data-ttu-id="6097f-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6097f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6097f-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6097f-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6097f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6097f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6097f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6097f-108">DESCRIPTION</span></span>
<span data-ttu-id="6097f-109">Cmdleten **Get-AzDataBoxEdgeOrder** hämtar beställnings informationen för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="6097f-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="6097f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6097f-110">EXAMPLES</span></span>

### <span data-ttu-id="6097f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6097f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="6097f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6097f-112">PARAMETERS</span></span>

### <span data-ttu-id="6097f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6097f-113">-DefaultProfile</span></span>
<span data-ttu-id="6097f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6097f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6097f-115">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="6097f-115">-DeviceName</span></span>
<span data-ttu-id="6097f-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6097f-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6097f-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6097f-117">-DeviceObject</span></span>
<span data-ttu-id="6097f-118">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="6097f-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6097f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6097f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6097f-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6097f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="6097f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6097f-121">-ResourceId</span></span>
<span data-ttu-id="6097f-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6097f-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="6097f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6097f-123">CommonParameters</span></span>
<span data-ttu-id="6097f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6097f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6097f-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6097f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6097f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6097f-126">INPUTS</span></span>

### <span data-ttu-id="6097f-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6097f-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="6097f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6097f-128">System.String</span></span>

## <span data-ttu-id="6097f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6097f-129">OUTPUTS</span></span>

### <span data-ttu-id="6097f-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6097f-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="6097f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6097f-131">NOTES</span></span>

## <span data-ttu-id="6097f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6097f-132">RELATED LINKS</span></span>
