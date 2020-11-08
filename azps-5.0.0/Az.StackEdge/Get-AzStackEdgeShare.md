---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270174"
---
# <span data-ttu-id="1cfcd-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1cfcd-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="1cfcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfcd-103">Hämtar de tillgängliga resurserna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="1cfcd-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="1cfcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cfcd-104">SYNTAX</span></span>

### <span data-ttu-id="1cfcd-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1cfcd-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cfcd-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfcd-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cfcd-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfcd-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cfcd-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfcd-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="1cfcd-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cfcd-109">DESCRIPTION</span></span>
<span data-ttu-id="1cfcd-110">Cmdleten **Get-AzStackEdgeShare** hämtar de tillgängliga resurserna för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="1cfcd-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="1cfcd-111">Om name anges kommer detta att få det här namnet.</span><span class="sxs-lookup"><span data-stu-id="1cfcd-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="1cfcd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cfcd-112">EXAMPLES</span></span>

### <span data-ttu-id="1cfcd-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1cfcd-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="1cfcd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cfcd-114">PARAMETERS</span></span>

### <span data-ttu-id="1cfcd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfcd-115">-DefaultProfile</span></span>
<span data-ttu-id="1cfcd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfcd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cfcd-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="1cfcd-117">-DeviceName</span></span>
<span data-ttu-id="1cfcd-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="1cfcd-118">Device Name</span></span>

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

### <span data-ttu-id="1cfcd-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="1cfcd-119">-DeviceObject</span></span>
<span data-ttu-id="1cfcd-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="1cfcd-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="1cfcd-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1cfcd-121">-Name</span></span>
<span data-ttu-id="1cfcd-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="1cfcd-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cfcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="1cfcd-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1cfcd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1cfcd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cfcd-125">-ResourceId</span></span>
<span data-ttu-id="1cfcd-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cfcd-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1cfcd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfcd-127">CommonParameters</span></span>
<span data-ttu-id="1cfcd-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfcd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfcd-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cfcd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfcd-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cfcd-130">INPUTS</span></span>

### <span data-ttu-id="1cfcd-131">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1cfcd-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="1cfcd-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cfcd-132">OUTPUTS</span></span>

### <span data-ttu-id="1cfcd-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1cfcd-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="1cfcd-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cfcd-134">NOTES</span></span>

## <span data-ttu-id="1cfcd-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cfcd-135">RELATED LINKS</span></span>
