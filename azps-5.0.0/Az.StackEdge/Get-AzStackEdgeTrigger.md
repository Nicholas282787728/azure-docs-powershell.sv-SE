---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269861"
---
# <span data-ttu-id="0be32-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="0be32-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="0be32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0be32-102">SYNOPSIS</span></span>
<span data-ttu-id="0be32-103">Få de utlösare som är konfigurerade på en enhet</span><span class="sxs-lookup"><span data-stu-id="0be32-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="0be32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0be32-104">SYNTAX</span></span>

### <span data-ttu-id="0be32-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0be32-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0be32-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0be32-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0be32-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0be32-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0be32-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0be32-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0be32-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0be32-109">DESCRIPTION</span></span>
<span data-ttu-id="0be32-110">Cmdleten **Get-AzStackEdgeTriger** hämtar utlösare för en enhet.</span><span class="sxs-lookup"><span data-stu-id="0be32-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="0be32-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om specifika utlösare</span><span class="sxs-lookup"><span data-stu-id="0be32-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="0be32-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0be32-112">EXAMPLES</span></span>

### <span data-ttu-id="0be32-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0be32-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="0be32-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0be32-114">PARAMETERS</span></span>

### <span data-ttu-id="0be32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be32-115">-DefaultProfile</span></span>
<span data-ttu-id="0be32-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0be32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be32-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="0be32-117">-DeviceName</span></span>
<span data-ttu-id="0be32-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="0be32-118">Device Name</span></span>

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

### <span data-ttu-id="0be32-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0be32-119">-DeviceObject</span></span>
<span data-ttu-id="0be32-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="0be32-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="0be32-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0be32-121">-Name</span></span>
<span data-ttu-id="0be32-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="0be32-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0be32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be32-123">-ResourceGroupName</span></span>
<span data-ttu-id="0be32-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0be32-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0be32-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0be32-125">-ResourceId</span></span>
<span data-ttu-id="0be32-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0be32-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="0be32-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be32-127">CommonParameters</span></span>
<span data-ttu-id="0be32-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be32-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be32-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0be32-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be32-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0be32-130">INPUTS</span></span>

### <span data-ttu-id="0be32-131">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0be32-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="0be32-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0be32-132">OUTPUTS</span></span>

### <span data-ttu-id="0be32-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="0be32-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="0be32-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0be32-134">NOTES</span></span>

## <span data-ttu-id="0be32-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0be32-135">RELATED LINKS</span></span>
