---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260083"
---
# <span data-ttu-id="9fde1-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9fde1-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9fde1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fde1-102">SYNOPSIS</span></span>
<span data-ttu-id="9fde1-103">Hämtar information om bandbredds scheman</span><span class="sxs-lookup"><span data-stu-id="9fde1-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="9fde1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fde1-104">SYNTAX</span></span>

### <span data-ttu-id="9fde1-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9fde1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fde1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fde1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fde1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fde1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fde1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fde1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9fde1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fde1-109">DESCRIPTION</span></span>
<span data-ttu-id="9fde1-110">Cmdleten **Get-AzDataBoxEdgeBandwidthSchedule** hämtar information om bandbredds scheman.</span><span class="sxs-lookup"><span data-stu-id="9fde1-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="9fde1-111">Du kan ange namnet på ett schema tillsammans med resurs gruppens namn och enhets namn för att få information om ett visst bandbredds schema</span><span class="sxs-lookup"><span data-stu-id="9fde1-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="9fde1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fde1-112">EXAMPLES</span></span>

### <span data-ttu-id="9fde1-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9fde1-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="9fde1-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9fde1-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="9fde1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fde1-115">PARAMETERS</span></span>

### <span data-ttu-id="9fde1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fde1-116">-DefaultProfile</span></span>
<span data-ttu-id="9fde1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9fde1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fde1-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="9fde1-118">-DeviceName</span></span>
<span data-ttu-id="9fde1-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="9fde1-119">Device Name</span></span>

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

### <span data-ttu-id="9fde1-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9fde1-120">-DeviceObject</span></span>
<span data-ttu-id="9fde1-121">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="9fde1-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="9fde1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9fde1-122">-Name</span></span>
<span data-ttu-id="9fde1-123">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="9fde1-123">Resource Name</span></span>

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

### <span data-ttu-id="9fde1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fde1-124">-ResourceGroupName</span></span>
<span data-ttu-id="9fde1-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9fde1-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9fde1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fde1-126">-ResourceId</span></span>
<span data-ttu-id="9fde1-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fde1-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="9fde1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fde1-128">CommonParameters</span></span>
<span data-ttu-id="9fde1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fde1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fde1-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fde1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fde1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fde1-131">INPUTS</span></span>

### <span data-ttu-id="9fde1-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9fde1-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9fde1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fde1-133">OUTPUTS</span></span>

### <span data-ttu-id="9fde1-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9fde1-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9fde1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fde1-135">NOTES</span></span>

## <span data-ttu-id="9fde1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fde1-136">RELATED LINKS</span></span>