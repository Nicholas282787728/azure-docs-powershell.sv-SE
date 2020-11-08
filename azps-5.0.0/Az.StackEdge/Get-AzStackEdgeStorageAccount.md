---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262896"
---
# <span data-ttu-id="6f8a5-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f8a5-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6f8a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8a5-103">Tar lagrings konto planerna på enheten.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="6f8a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f8a5-104">SYNTAX</span></span>

### <span data-ttu-id="6f8a5-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6f8a5-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8a5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8a5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f8a5-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8a5-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f8a5-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f8a5-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="6f8a5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f8a5-109">DESCRIPTION</span></span>
<span data-ttu-id="6f8a5-110">Cmdleten **Get-AzStackEdgeStorageAccount** hämtar de lagrings konton som finns tillgängliga på en grupp Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="6f8a5-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om ett specifikt lagrings konto för Edge.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="6f8a5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f8a5-112">EXAMPLES</span></span>

### <span data-ttu-id="6f8a5-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6f8a5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="6f8a5-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6f8a5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="6f8a5-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6f8a5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="6f8a5-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="6f8a5-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="6f8a5-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f8a5-117">PARAMETERS</span></span>

### <span data-ttu-id="6f8a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8a5-118">-DefaultProfile</span></span>
<span data-ttu-id="6f8a5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f8a5-120">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="6f8a5-120">-DeviceName</span></span>
<span data-ttu-id="6f8a5-121">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="6f8a5-121">Device Name</span></span>

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

### <span data-ttu-id="6f8a5-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6f8a5-122">-DeviceObject</span></span>
<span data-ttu-id="6f8a5-123">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="6f8a5-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="6f8a5-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f8a5-124">-Name</span></span>
<span data-ttu-id="6f8a5-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="6f8a5-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f8a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f8a5-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6f8a5-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6f8a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8a5-128">-ResourceId</span></span>
<span data-ttu-id="6f8a5-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f8a5-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="6f8a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8a5-130">CommonParameters</span></span>
<span data-ttu-id="6f8a5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8a5-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f8a5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8a5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f8a5-133">INPUTS</span></span>

### <span data-ttu-id="6f8a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6f8a5-134">System.String</span></span>

### <span data-ttu-id="6f8a5-135">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6f8a5-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6f8a5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f8a5-136">OUTPUTS</span></span>

### <span data-ttu-id="6f8a5-137">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f8a5-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6f8a5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f8a5-138">NOTES</span></span>

## <span data-ttu-id="6f8a5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f8a5-139">RELATED LINKS</span></span>
