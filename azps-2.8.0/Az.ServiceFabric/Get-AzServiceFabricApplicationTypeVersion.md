---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 0af0b8ac4f632682ee60bd691c41fb4500c2c2a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919168"
---
# <span data-ttu-id="046a0-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="046a0-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="046a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="046a0-102">SYNOPSIS</span></span>
<span data-ttu-id="046a0-103">Hämta versions information för Service Fabric program typ.</span><span class="sxs-lookup"><span data-stu-id="046a0-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="046a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="046a0-104">SYNTAX</span></span>

### <span data-ttu-id="046a0-105">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="046a0-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="046a0-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="046a0-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="046a0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="046a0-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="046a0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="046a0-108">DESCRIPTION</span></span>
<span data-ttu-id="046a0-109">Använd denna cmdlet för att hämta versions information för program typ i den angivna resurs gruppen och klustret.</span><span class="sxs-lookup"><span data-stu-id="046a0-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="046a0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="046a0-110">EXAMPLES</span></span>

### <span data-ttu-id="046a0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="046a0-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="046a0-112">I det här exemplet hämtas program typen "testAppType" med version "v1", om den inte hittar den resurs som det ger upphov till.</span><span class="sxs-lookup"><span data-stu-id="046a0-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="046a0-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="046a0-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="046a0-114">I det här exemplet visas en lista med de program typer som definierats för klustret och typen.</span><span class="sxs-lookup"><span data-stu-id="046a0-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="046a0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="046a0-115">PARAMETERS</span></span>

### <span data-ttu-id="046a0-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="046a0-116">-ClusterName</span></span>
<span data-ttu-id="046a0-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="046a0-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="046a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046a0-118">-DefaultProfile</span></span>
<span data-ttu-id="046a0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="046a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="046a0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="046a0-120">-Name</span></span>
<span data-ttu-id="046a0-121">Ange namnet på program typen.</span><span class="sxs-lookup"><span data-stu-id="046a0-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="046a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="046a0-123">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="046a0-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="046a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="046a0-124">-ResourceId</span></span>
<span data-ttu-id="046a0-125">Arm-ResourceId för program typ version.</span><span class="sxs-lookup"><span data-stu-id="046a0-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="046a0-126">-Version</span><span class="sxs-lookup"><span data-stu-id="046a0-126">-Version</span></span>
<span data-ttu-id="046a0-127">Ange versionen för program typen.</span><span class="sxs-lookup"><span data-stu-id="046a0-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="046a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046a0-128">CommonParameters</span></span>
<span data-ttu-id="046a0-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046a0-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046a0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046a0-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="046a0-131">INPUTS</span></span>

### <span data-ttu-id="046a0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="046a0-132">System.String</span></span>

## <span data-ttu-id="046a0-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="046a0-133">OUTPUTS</span></span>

### <span data-ttu-id="046a0-134">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="046a0-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="046a0-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="046a0-135">NOTES</span></span>

## <span data-ttu-id="046a0-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="046a0-136">RELATED LINKS</span></span>
