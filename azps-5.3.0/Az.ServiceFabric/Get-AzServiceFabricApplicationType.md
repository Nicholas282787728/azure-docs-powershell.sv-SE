---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525437"
---
# <span data-ttu-id="6556f-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6556f-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="6556f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6556f-102">SYNOPSIS</span></span>
<span data-ttu-id="6556f-103">Information om hur du skaffar Service Fabric-programmet.</span><span class="sxs-lookup"><span data-stu-id="6556f-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="6556f-104">Stöder bara program typer som distribueras av ARM.</span><span class="sxs-lookup"><span data-stu-id="6556f-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="6556f-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6556f-105">SYNTAX</span></span>

### <span data-ttu-id="6556f-106">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="6556f-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6556f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6556f-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6556f-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6556f-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6556f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6556f-109">DESCRIPTION</span></span>
<span data-ttu-id="6556f-110">Använd denna cmdlet för att få program typs informationen i angiven resurs grupp och kluster.</span><span class="sxs-lookup"><span data-stu-id="6556f-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="6556f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6556f-111">EXAMPLES</span></span>

### <span data-ttu-id="6556f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6556f-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="6556f-113">I det här exemplet hämtas program typs informationen med de angivna parametrarna, om den inte hittar den resurs som det ger upphov till.</span><span class="sxs-lookup"><span data-stu-id="6556f-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="6556f-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6556f-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="6556f-115">I det här exemplet visas en lista med de program typer som är definierade under det angivna klustret.</span><span class="sxs-lookup"><span data-stu-id="6556f-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="6556f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6556f-116">PARAMETERS</span></span>

### <span data-ttu-id="6556f-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="6556f-117">-ClusterName</span></span>
<span data-ttu-id="6556f-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="6556f-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6556f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6556f-119">-DefaultProfile</span></span>
<span data-ttu-id="6556f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6556f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6556f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6556f-121">-Name</span></span>
<span data-ttu-id="6556f-122">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="6556f-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6556f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6556f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6556f-124">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6556f-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6556f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6556f-125">-ResourceId</span></span>
<span data-ttu-id="6556f-126">Program typens arm ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6556f-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="6556f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6556f-127">CommonParameters</span></span>
<span data-ttu-id="6556f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6556f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6556f-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6556f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6556f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6556f-130">INPUTS</span></span>

### <span data-ttu-id="6556f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6556f-131">System.String</span></span>

## <span data-ttu-id="6556f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6556f-132">OUTPUTS</span></span>

### <span data-ttu-id="6556f-133">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="6556f-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="6556f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6556f-134">NOTES</span></span>

## <span data-ttu-id="6556f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6556f-135">RELATED LINKS</span></span>
