---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 7b797b4088cab20ee1933ce88a2462288f04653e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260081"
---
# <span data-ttu-id="c49ed-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c49ed-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="c49ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c49ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c49ed-103">Tar lagrings konto planerna på enheten.</span><span class="sxs-lookup"><span data-stu-id="c49ed-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="c49ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c49ed-104">SYNTAX</span></span>

### <span data-ttu-id="c49ed-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c49ed-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c49ed-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c49ed-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c49ed-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c49ed-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c49ed-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c49ed-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="c49ed-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c49ed-109">DESCRIPTION</span></span>
<span data-ttu-id="c49ed-110">Cmdleten **Get-AzDataBoxEdgeStorageAccount** hämtar de lagrings konton som finns tillgängliga i en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="c49ed-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="c49ed-111">Du kan ange namnet som en parameter i cmdleten för att hämta information om ett specifikt lagrings konto för Edge.</span><span class="sxs-lookup"><span data-stu-id="c49ed-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="c49ed-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c49ed-112">EXAMPLES</span></span>

### <span data-ttu-id="c49ed-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c49ed-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="c49ed-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c49ed-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="c49ed-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c49ed-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="c49ed-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="c49ed-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="c49ed-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c49ed-117">PARAMETERS</span></span>

### <span data-ttu-id="c49ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49ed-118">-DefaultProfile</span></span>
<span data-ttu-id="c49ed-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c49ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c49ed-120">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="c49ed-120">-DeviceName</span></span>
<span data-ttu-id="c49ed-121">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="c49ed-121">Device Name</span></span>

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

### <span data-ttu-id="c49ed-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c49ed-122">-DeviceObject</span></span>
<span data-ttu-id="c49ed-123">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="c49ed-123">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="c49ed-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c49ed-124">-Name</span></span>
<span data-ttu-id="c49ed-125">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="c49ed-125">Resource Name</span></span>

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

### <span data-ttu-id="c49ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="c49ed-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c49ed-127">Resource Group Name</span></span>

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

### <span data-ttu-id="c49ed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c49ed-128">-ResourceId</span></span>
<span data-ttu-id="c49ed-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c49ed-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="c49ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49ed-130">CommonParameters</span></span>
<span data-ttu-id="c49ed-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49ed-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c49ed-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49ed-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c49ed-133">INPUTS</span></span>

### <span data-ttu-id="c49ed-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c49ed-134">System.String</span></span>

### <span data-ttu-id="c49ed-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c49ed-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="c49ed-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c49ed-136">OUTPUTS</span></span>

### <span data-ttu-id="c49ed-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c49ed-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="c49ed-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c49ed-138">NOTES</span></span>

## <span data-ttu-id="c49ed-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c49ed-139">RELATED LINKS</span></span>