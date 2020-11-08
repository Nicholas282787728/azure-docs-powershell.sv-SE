---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091141"
---
# <span data-ttu-id="b31f2-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b31f2-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b31f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b31f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b31f2-103">Tar lagrings konto planerna på enheten.</span><span class="sxs-lookup"><span data-stu-id="b31f2-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="b31f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b31f2-104">SYNTAX</span></span>

### <span data-ttu-id="b31f2-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b31f2-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31f2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b31f2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b31f2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b31f2-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b31f2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b31f2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="b31f2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b31f2-109">DESCRIPTION</span></span>
<span data-ttu-id="b31f2-110">Cmdleten **Get-AzDataBoxEdgeStorageAccount** hämtar de lagrings konton som finns tillgängliga i en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="b31f2-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="b31f2-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om ett specifikt lagrings konto för Edge.</span><span class="sxs-lookup"><span data-stu-id="b31f2-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="b31f2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b31f2-112">EXAMPLES</span></span>

### <span data-ttu-id="b31f2-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b31f2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="b31f2-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b31f2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="b31f2-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b31f2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="b31f2-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="b31f2-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="b31f2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b31f2-117">PARAMETERS</span></span>

### <span data-ttu-id="b31f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31f2-118">-DefaultProfile</span></span>
<span data-ttu-id="b31f2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b31f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b31f2-120">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="b31f2-120">-DeviceName</span></span>
<span data-ttu-id="b31f2-121">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="b31f2-121">Device Name</span></span>

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

### <span data-ttu-id="b31f2-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="b31f2-122">-DeviceObject</span></span>
<span data-ttu-id="b31f2-123">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="b31f2-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b31f2-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b31f2-124">-Name</span></span>
<span data-ttu-id="b31f2-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="b31f2-125">Resource Name</span></span>

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

### <span data-ttu-id="b31f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b31f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="b31f2-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b31f2-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b31f2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b31f2-128">-ResourceId</span></span>
<span data-ttu-id="b31f2-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b31f2-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b31f2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31f2-130">CommonParameters</span></span>
<span data-ttu-id="b31f2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31f2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31f2-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b31f2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31f2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b31f2-133">INPUTS</span></span>

### <span data-ttu-id="b31f2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b31f2-134">System.String</span></span>

### <span data-ttu-id="b31f2-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b31f2-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="b31f2-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b31f2-136">OUTPUTS</span></span>

### <span data-ttu-id="b31f2-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b31f2-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="b31f2-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b31f2-138">NOTES</span></span>

## <span data-ttu-id="b31f2-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b31f2-139">RELATED LINKS</span></span>
