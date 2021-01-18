---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: eca1227150741814178dbabe25caff79b3c3381e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524251"
---
# <span data-ttu-id="7b33e-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7b33e-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7b33e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b33e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b33e-103">Hämtar autentiseringsuppgifterna för lagrings kontot som motsvarar lagrings kontot på enheten.</span><span class="sxs-lookup"><span data-stu-id="7b33e-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="7b33e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b33e-104">SYNTAX</span></span>

### <span data-ttu-id="7b33e-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7b33e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b33e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b33e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b33e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b33e-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b33e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b33e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="7b33e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b33e-109">DESCRIPTION</span></span>
<span data-ttu-id="7b33e-110">Cmdleten **Get-AzDataBoxEdgeStorageAccountCredential** hämtar autentiseringsuppgifterna för lagrings kontot för motsvarande lagrings konto i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="7b33e-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="7b33e-111">Du kan ange parametrar för namn, resurs grupp namn och enhets namn för att få information om en viss autentiseringsuppgift för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7b33e-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="7b33e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b33e-112">EXAMPLES</span></span>

### <span data-ttu-id="7b33e-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b33e-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="7b33e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b33e-114">PARAMETERS</span></span>

### <span data-ttu-id="7b33e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b33e-115">-DefaultProfile</span></span>
<span data-ttu-id="7b33e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b33e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b33e-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="7b33e-117">-DeviceName</span></span>
<span data-ttu-id="7b33e-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="7b33e-118">Device Name</span></span>

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

### <span data-ttu-id="7b33e-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7b33e-119">-DeviceObject</span></span>
<span data-ttu-id="7b33e-120">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="7b33e-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="7b33e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b33e-121">-Name</span></span>
<span data-ttu-id="7b33e-122">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="7b33e-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="7b33e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b33e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b33e-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7b33e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7b33e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b33e-125">-ResourceId</span></span>
<span data-ttu-id="7b33e-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b33e-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="7b33e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b33e-127">CommonParameters</span></span>
<span data-ttu-id="7b33e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b33e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b33e-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b33e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b33e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b33e-130">INPUTS</span></span>

### <span data-ttu-id="7b33e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7b33e-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="7b33e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b33e-132">OUTPUTS</span></span>

### <span data-ttu-id="7b33e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7b33e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7b33e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b33e-134">NOTES</span></span>

## <span data-ttu-id="7b33e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b33e-135">RELATED LINKS</span></span>
