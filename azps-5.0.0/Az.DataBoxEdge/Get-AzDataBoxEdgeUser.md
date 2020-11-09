---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321207"
---
# <span data-ttu-id="a7dc9-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a7dc9-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="a7dc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dc9-103">Hämtar de konfigurerade användarna för en enhet.</span><span class="sxs-lookup"><span data-stu-id="a7dc9-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="a7dc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7dc9-104">SYNTAX</span></span>

### <span data-ttu-id="a7dc9-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a7dc9-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dc9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7dc9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dc9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7dc9-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7dc9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7dc9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a7dc9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7dc9-109">DESCRIPTION</span></span>
<span data-ttu-id="a7dc9-110">Cmdleten **Get-AzDataBoxEdgeUser** visar de användare som har kon figurer ATS för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="a7dc9-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="a7dc9-111">Du kan nämna namnet i parametrar för att få information om en viss användare.</span><span class="sxs-lookup"><span data-stu-id="a7dc9-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="a7dc9-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7dc9-112">EXAMPLES</span></span>

### <span data-ttu-id="a7dc9-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a7dc9-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="a7dc9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7dc9-114">PARAMETERS</span></span>

### <span data-ttu-id="a7dc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dc9-115">-DefaultProfile</span></span>
<span data-ttu-id="a7dc9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7dc9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dc9-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="a7dc9-117">-DeviceName</span></span>
<span data-ttu-id="a7dc9-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="a7dc9-118">Device Name</span></span>

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

### <span data-ttu-id="a7dc9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a7dc9-119">-DeviceObject</span></span>
<span data-ttu-id="a7dc9-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="a7dc9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a7dc9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7dc9-121">-Name</span></span>
<span data-ttu-id="a7dc9-122">Namnen</span><span class="sxs-lookup"><span data-stu-id="a7dc9-122">Username</span></span>

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

### <span data-ttu-id="a7dc9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7dc9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7dc9-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a7dc9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a7dc9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7dc9-125">-ResourceId</span></span>
<span data-ttu-id="a7dc9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7dc9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a7dc9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dc9-127">CommonParameters</span></span>
<span data-ttu-id="a7dc9-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7dc9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dc9-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7dc9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dc9-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7dc9-130">INPUTS</span></span>

### <span data-ttu-id="a7dc9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a7dc9-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a7dc9-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7dc9-132">OUTPUTS</span></span>

### <span data-ttu-id="a7dc9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a7dc9-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="a7dc9-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7dc9-134">NOTES</span></span>

## <span data-ttu-id="a7dc9-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7dc9-135">RELATED LINKS</span></span>
