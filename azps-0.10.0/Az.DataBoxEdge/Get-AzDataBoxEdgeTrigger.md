---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 96c9b736398cb981dd055d072091aa24af4d3f6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924705"
---
# <span data-ttu-id="dc69f-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dc69f-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="dc69f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc69f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc69f-103">Få de utlösare som är konfigurerade på en enhet</span><span class="sxs-lookup"><span data-stu-id="dc69f-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="dc69f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc69f-104">SYNTAX</span></span>

### <span data-ttu-id="dc69f-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dc69f-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc69f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc69f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc69f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc69f-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc69f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc69f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="dc69f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc69f-109">DESCRIPTION</span></span>
<span data-ttu-id="dc69f-110">Cmdleten **Get-AzDataBoxEdgeTriger** hämtar utlösare för en enhet.</span><span class="sxs-lookup"><span data-stu-id="dc69f-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="dc69f-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om specifika utlösare</span><span class="sxs-lookup"><span data-stu-id="dc69f-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="dc69f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc69f-112">EXAMPLES</span></span>

### <span data-ttu-id="dc69f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc69f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="dc69f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc69f-114">PARAMETERS</span></span>

### <span data-ttu-id="dc69f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc69f-115">-DefaultProfile</span></span>
<span data-ttu-id="dc69f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc69f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc69f-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="dc69f-117">-DeviceName</span></span>
<span data-ttu-id="dc69f-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="dc69f-118">Device Name</span></span>

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

### <span data-ttu-id="dc69f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="dc69f-119">-DeviceObject</span></span>
<span data-ttu-id="dc69f-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="dc69f-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="dc69f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc69f-121">-Name</span></span>
<span data-ttu-id="dc69f-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="dc69f-122">Resource Name</span></span>

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

### <span data-ttu-id="dc69f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc69f-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc69f-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dc69f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dc69f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc69f-125">-ResourceId</span></span>
<span data-ttu-id="dc69f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc69f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="dc69f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc69f-127">CommonParameters</span></span>
<span data-ttu-id="dc69f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc69f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc69f-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc69f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc69f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc69f-130">INPUTS</span></span>

### <span data-ttu-id="dc69f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="dc69f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="dc69f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc69f-132">OUTPUTS</span></span>

### <span data-ttu-id="dc69f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="dc69f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="dc69f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc69f-134">NOTES</span></span>

## <span data-ttu-id="dc69f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc69f-135">RELATED LINKS</span></span>
