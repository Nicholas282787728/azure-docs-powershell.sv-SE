---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525435"
---
# <span data-ttu-id="93221-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="93221-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="93221-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93221-102">SYNOPSIS</span></span>
<span data-ttu-id="93221-103">Hämta versions information för Service Fabric program typ.</span><span class="sxs-lookup"><span data-stu-id="93221-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="93221-104">Det går endast att använda program typer som distribueras av ARM.</span><span class="sxs-lookup"><span data-stu-id="93221-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="93221-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93221-105">SYNTAX</span></span>

### <span data-ttu-id="93221-106">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="93221-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93221-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="93221-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93221-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="93221-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93221-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93221-109">DESCRIPTION</span></span>
<span data-ttu-id="93221-110">Använd denna cmdlet för att hämta versions information för program typ i den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="93221-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="93221-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93221-111">EXAMPLES</span></span>

### <span data-ttu-id="93221-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93221-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="93221-113">I det här exemplet hämtas program typen "testAppType" med version "v1", om den inte hittar den resurs som det ger upphov till.</span><span class="sxs-lookup"><span data-stu-id="93221-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="93221-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="93221-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="93221-115">I det här exemplet visas en lista med de program typer som definierats för klustret och typen.</span><span class="sxs-lookup"><span data-stu-id="93221-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="93221-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93221-116">PARAMETERS</span></span>

### <span data-ttu-id="93221-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="93221-117">-ClusterName</span></span>
<span data-ttu-id="93221-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="93221-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93221-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93221-119">-DefaultProfile</span></span>
<span data-ttu-id="93221-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93221-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93221-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="93221-121">-Name</span></span>
<span data-ttu-id="93221-122">Ange namnet på program typen.</span><span class="sxs-lookup"><span data-stu-id="93221-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93221-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93221-123">-ResourceGroupName</span></span>
<span data-ttu-id="93221-124">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="93221-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93221-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93221-125">-ResourceId</span></span>
<span data-ttu-id="93221-126">Arm-ResourceId för program typ version.</span><span class="sxs-lookup"><span data-stu-id="93221-126">Arm ResourceId of the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93221-127">-Version</span><span class="sxs-lookup"><span data-stu-id="93221-127">-Version</span></span>
<span data-ttu-id="93221-128">Ange versionen för program typen.</span><span class="sxs-lookup"><span data-stu-id="93221-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93221-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93221-129">CommonParameters</span></span>
<span data-ttu-id="93221-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93221-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93221-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93221-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93221-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93221-132">INPUTS</span></span>

### <span data-ttu-id="93221-133">System. String</span><span class="sxs-lookup"><span data-stu-id="93221-133">System.String</span></span>

## <span data-ttu-id="93221-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93221-134">OUTPUTS</span></span>

### <span data-ttu-id="93221-135">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="93221-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="93221-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93221-136">NOTES</span></span>

## <span data-ttu-id="93221-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93221-137">RELATED LINKS</span></span>
