---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271218"
---
# <span data-ttu-id="25518-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="25518-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="25518-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25518-102">SYNOPSIS</span></span>
<span data-ttu-id="25518-103">Hämtar schemalagda jobb på en enhet.</span><span class="sxs-lookup"><span data-stu-id="25518-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="25518-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25518-104">SYNTAX</span></span>

### <span data-ttu-id="25518-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25518-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25518-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="25518-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25518-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25518-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="25518-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25518-108">DESCRIPTION</span></span>
<span data-ttu-id="25518-109">Cmdleten **Get-AzStackEdgeJob** hämtar de aktiva jobben på en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="25518-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="25518-110">Du kan nämna parametern name för att få information om ett visst jobb.</span><span class="sxs-lookup"><span data-stu-id="25518-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="25518-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25518-111">EXAMPLES</span></span>

### <span data-ttu-id="25518-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25518-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="25518-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25518-113">PARAMETERS</span></span>

### <span data-ttu-id="25518-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25518-114">-DefaultProfile</span></span>
<span data-ttu-id="25518-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25518-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25518-116">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="25518-116">-DeviceName</span></span>
<span data-ttu-id="25518-117">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="25518-117">Name of the device</span></span>

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

### <span data-ttu-id="25518-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="25518-118">-DeviceObject</span></span>
<span data-ttu-id="25518-119">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="25518-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25518-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="25518-120">-Name</span></span>
<span data-ttu-id="25518-121">Namnet på jobbet, vanligt vis ett GUID</span><span class="sxs-lookup"><span data-stu-id="25518-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25518-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25518-122">-ResourceGroupName</span></span>
<span data-ttu-id="25518-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="25518-123">Resource Group Name</span></span>

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

### <span data-ttu-id="25518-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25518-124">-ResourceId</span></span>
<span data-ttu-id="25518-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="25518-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25518-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25518-126">CommonParameters</span></span>
<span data-ttu-id="25518-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25518-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25518-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25518-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25518-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25518-129">INPUTS</span></span>

### <span data-ttu-id="25518-130">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="25518-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="25518-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25518-131">OUTPUTS</span></span>

### <span data-ttu-id="25518-132">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="25518-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="25518-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25518-133">NOTES</span></span>

## <span data-ttu-id="25518-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25518-134">RELATED LINKS</span></span>