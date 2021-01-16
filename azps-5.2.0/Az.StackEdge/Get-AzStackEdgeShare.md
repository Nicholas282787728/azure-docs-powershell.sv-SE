---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410272"
---
# <span data-ttu-id="28df8-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="28df8-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="28df8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28df8-102">SYNOPSIS</span></span>
<span data-ttu-id="28df8-103">Hämtar de tillgängliga resurserna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="28df8-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="28df8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28df8-104">SYNTAX</span></span>

### <span data-ttu-id="28df8-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="28df8-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28df8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28df8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28df8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28df8-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28df8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28df8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="28df8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28df8-109">DESCRIPTION</span></span>
<span data-ttu-id="28df8-110">Cmdleten **Get-AzStackEdgeShare** hämtar de tillgängliga resurserna för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="28df8-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="28df8-111">Om name anges kommer detta att få det här namnet.</span><span class="sxs-lookup"><span data-stu-id="28df8-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="28df8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28df8-112">EXAMPLES</span></span>

### <span data-ttu-id="28df8-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="28df8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="28df8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28df8-114">PARAMETERS</span></span>

### <span data-ttu-id="28df8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28df8-115">-DefaultProfile</span></span>
<span data-ttu-id="28df8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28df8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28df8-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="28df8-117">-DeviceName</span></span>
<span data-ttu-id="28df8-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="28df8-118">Device Name</span></span>

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

### <span data-ttu-id="28df8-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="28df8-119">-DeviceObject</span></span>
<span data-ttu-id="28df8-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="28df8-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="28df8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="28df8-121">-Name</span></span>
<span data-ttu-id="28df8-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="28df8-122">Resource Name</span></span>

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

### <span data-ttu-id="28df8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28df8-123">-ResourceGroupName</span></span>
<span data-ttu-id="28df8-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="28df8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="28df8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28df8-125">-ResourceId</span></span>
<span data-ttu-id="28df8-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="28df8-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="28df8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28df8-127">CommonParameters</span></span>
<span data-ttu-id="28df8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28df8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28df8-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28df8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28df8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28df8-130">INPUTS</span></span>

### <span data-ttu-id="28df8-131">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="28df8-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="28df8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28df8-132">OUTPUTS</span></span>

### <span data-ttu-id="28df8-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="28df8-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="28df8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28df8-134">NOTES</span></span>

## <span data-ttu-id="28df8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28df8-135">RELATED LINKS</span></span>
