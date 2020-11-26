---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102947"
---
# <span data-ttu-id="2f8c2-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="2f8c2-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="2f8c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8c2-103">Få de utlösare som är konfigurerade på en enhet</span><span class="sxs-lookup"><span data-stu-id="2f8c2-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="2f8c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f8c2-104">SYNTAX</span></span>

### <span data-ttu-id="2f8c2-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2f8c2-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f8c2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f8c2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f8c2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f8c2-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f8c2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f8c2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="2f8c2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f8c2-109">DESCRIPTION</span></span>
<span data-ttu-id="2f8c2-110">Cmdleten **Get-AzDataBoxEdgeTriger** hämtar utlösare för en enhet.</span><span class="sxs-lookup"><span data-stu-id="2f8c2-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="2f8c2-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om specifika utlösare</span><span class="sxs-lookup"><span data-stu-id="2f8c2-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="2f8c2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f8c2-112">EXAMPLES</span></span>

### <span data-ttu-id="2f8c2-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f8c2-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="2f8c2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f8c2-114">PARAMETERS</span></span>

### <span data-ttu-id="2f8c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8c2-115">-DefaultProfile</span></span>
<span data-ttu-id="2f8c2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f8c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8c2-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="2f8c2-117">-DeviceName</span></span>
<span data-ttu-id="2f8c2-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="2f8c2-118">Device Name</span></span>

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

### <span data-ttu-id="2f8c2-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="2f8c2-119">-DeviceObject</span></span>
<span data-ttu-id="2f8c2-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="2f8c2-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="2f8c2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f8c2-121">-Name</span></span>
<span data-ttu-id="2f8c2-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="2f8c2-122">Resource Name</span></span>

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

### <span data-ttu-id="2f8c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f8c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f8c2-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2f8c2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2f8c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f8c2-125">-ResourceId</span></span>
<span data-ttu-id="2f8c2-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f8c2-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="2f8c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8c2-127">CommonParameters</span></span>
<span data-ttu-id="2f8c2-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f8c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8c2-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f8c2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8c2-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f8c2-130">INPUTS</span></span>

### <span data-ttu-id="2f8c2-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2f8c2-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="2f8c2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f8c2-132">OUTPUTS</span></span>

### <span data-ttu-id="2f8c2-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="2f8c2-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="2f8c2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f8c2-134">NOTES</span></span>

## <span data-ttu-id="2f8c2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f8c2-135">RELATED LINKS</span></span>