---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103454"
---
# <span data-ttu-id="7876e-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7876e-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7876e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7876e-102">SYNOPSIS</span></span>
<span data-ttu-id="7876e-103">Hämtar behållarna för ett Edge Storage-konto på en enhet.</span><span class="sxs-lookup"><span data-stu-id="7876e-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="7876e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7876e-104">SYNTAX</span></span>

### <span data-ttu-id="7876e-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7876e-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7876e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7876e-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7876e-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7876e-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7876e-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7876e-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="7876e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7876e-109">DESCRIPTION</span></span>
<span data-ttu-id="7876e-110">Cmdleten **Get-AzStackEdgeStorageContainer** hämtar lagrings behållaren för ett Edge Storage-konto på en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="7876e-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="7876e-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om en viss lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="7876e-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="7876e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7876e-112">EXAMPLES</span></span>

### <span data-ttu-id="7876e-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7876e-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="7876e-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7876e-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="7876e-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7876e-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="7876e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7876e-116">PARAMETERS</span></span>

### <span data-ttu-id="7876e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7876e-117">-DefaultProfile</span></span>
<span data-ttu-id="7876e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7876e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7876e-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="7876e-119">-DeviceName</span></span>
<span data-ttu-id="7876e-120">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="7876e-120">Device Name</span></span>

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

### <span data-ttu-id="7876e-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7876e-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7876e-122">Ange befintliga EdgeStorageAccount namn</span><span class="sxs-lookup"><span data-stu-id="7876e-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7876e-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="7876e-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="7876e-124">Ange befintligt EdgeStorageAccount-objekt</span><span class="sxs-lookup"><span data-stu-id="7876e-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7876e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7876e-125">-Name</span></span>
<span data-ttu-id="7876e-126">Namn på EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7876e-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7876e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7876e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7876e-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7876e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="7876e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7876e-129">-ResourceId</span></span>
<span data-ttu-id="7876e-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7876e-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7876e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7876e-131">CommonParameters</span></span>
<span data-ttu-id="7876e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7876e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7876e-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7876e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7876e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7876e-134">INPUTS</span></span>

### <span data-ttu-id="7876e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7876e-135">System.String</span></span>

### <span data-ttu-id="7876e-136">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7876e-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="7876e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7876e-137">OUTPUTS</span></span>

### <span data-ttu-id="7876e-138">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7876e-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7876e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7876e-139">NOTES</span></span>

## <span data-ttu-id="7876e-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7876e-140">RELATED LINKS</span></span>
