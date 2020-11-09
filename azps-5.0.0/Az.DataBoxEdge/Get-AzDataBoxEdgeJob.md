---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321240"
---
# <span data-ttu-id="a2ba8-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="a2ba8-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="a2ba8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ba8-103">Hämtar schemalagda jobb på en enhet.</span><span class="sxs-lookup"><span data-stu-id="a2ba8-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="a2ba8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2ba8-104">SYNTAX</span></span>

### <span data-ttu-id="a2ba8-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a2ba8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2ba8-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="a2ba8-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2ba8-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2ba8-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a2ba8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="a2ba8-109">Cmdleten **Get-AzDataBoxEdgeJob** hämtar de aktiva jobben i en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="a2ba8-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="a2ba8-110">Du kan nämna parametern name för att få information om ett visst jobb.</span><span class="sxs-lookup"><span data-stu-id="a2ba8-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="a2ba8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2ba8-111">EXAMPLES</span></span>

### <span data-ttu-id="a2ba8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2ba8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="a2ba8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2ba8-113">PARAMETERS</span></span>

### <span data-ttu-id="a2ba8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ba8-114">-DefaultProfile</span></span>
<span data-ttu-id="a2ba8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ba8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ba8-116">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="a2ba8-116">-DeviceName</span></span>
<span data-ttu-id="a2ba8-117">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="a2ba8-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba8-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a2ba8-118">-DeviceObject</span></span>
<span data-ttu-id="a2ba8-119">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="a2ba8-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a2ba8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2ba8-120">-Name</span></span>
<span data-ttu-id="a2ba8-121">Namnet på jobbet, vanligt vis ett GUID</span><span class="sxs-lookup"><span data-stu-id="a2ba8-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ba8-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2ba8-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a2ba8-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ba8-124">-ResourceId</span></span>
<span data-ttu-id="a2ba8-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2ba8-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ba8-126">CommonParameters</span></span>
<span data-ttu-id="a2ba8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ba8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ba8-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2ba8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ba8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2ba8-129">INPUTS</span></span>

### <span data-ttu-id="a2ba8-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a2ba8-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a2ba8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2ba8-131">OUTPUTS</span></span>

### <span data-ttu-id="a2ba8-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="a2ba8-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="a2ba8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2ba8-133">NOTES</span></span>

## <span data-ttu-id="a2ba8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2ba8-134">RELATED LINKS</span></span>
