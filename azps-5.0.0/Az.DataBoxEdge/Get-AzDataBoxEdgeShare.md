---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 6a20f81644827c84ee1ce215ad2e87268650caf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321232"
---
# <span data-ttu-id="0fb30-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0fb30-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="0fb30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fb30-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb30-103">Hämtar de tillgängliga resurserna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="0fb30-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="0fb30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fb30-104">SYNTAX</span></span>

### <span data-ttu-id="0fb30-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0fb30-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fb30-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb30-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fb30-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb30-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fb30-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb30-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="0fb30-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fb30-109">DESCRIPTION</span></span>
<span data-ttu-id="0fb30-110">Cmdleten **Get-AzDataBoxEdgeShare** hämtar de tillgängliga resurserna för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="0fb30-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="0fb30-111">Om name anges kommer detta att få det här namnet.</span><span class="sxs-lookup"><span data-stu-id="0fb30-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="0fb30-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fb30-112">EXAMPLES</span></span>

### <span data-ttu-id="0fb30-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fb30-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="0fb30-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fb30-114">PARAMETERS</span></span>

### <span data-ttu-id="0fb30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb30-115">-DefaultProfile</span></span>
<span data-ttu-id="0fb30-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fb30-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb30-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="0fb30-117">-DeviceName</span></span>
<span data-ttu-id="0fb30-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="0fb30-118">Device Name</span></span>

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

### <span data-ttu-id="0fb30-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="0fb30-119">-DeviceObject</span></span>
<span data-ttu-id="0fb30-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="0fb30-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="0fb30-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0fb30-121">-Name</span></span>
<span data-ttu-id="0fb30-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="0fb30-122">Resource Name</span></span>

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

### <span data-ttu-id="0fb30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb30-123">-ResourceGroupName</span></span>
<span data-ttu-id="0fb30-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0fb30-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0fb30-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fb30-125">-ResourceId</span></span>
<span data-ttu-id="0fb30-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fb30-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="0fb30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb30-127">CommonParameters</span></span>
<span data-ttu-id="0fb30-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fb30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb30-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fb30-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb30-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fb30-130">INPUTS</span></span>

### <span data-ttu-id="0fb30-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="0fb30-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="0fb30-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fb30-132">OUTPUTS</span></span>

### <span data-ttu-id="0fb30-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0fb30-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="0fb30-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fb30-134">NOTES</span></span>

## <span data-ttu-id="0fb30-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fb30-135">RELATED LINKS</span></span>