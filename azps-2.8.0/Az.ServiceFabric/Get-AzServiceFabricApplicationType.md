---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 78cec82383c257e325c35d0987de73f37aff253d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919170"
---
# <span data-ttu-id="79664-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="79664-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="79664-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79664-102">SYNOPSIS</span></span>
<span data-ttu-id="79664-103">Information om hur du skaffar Service Fabric-programmet.</span><span class="sxs-lookup"><span data-stu-id="79664-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="79664-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79664-104">SYNTAX</span></span>

### <span data-ttu-id="79664-105">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="79664-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79664-106">ByName</span><span class="sxs-lookup"><span data-stu-id="79664-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79664-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79664-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79664-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79664-108">DESCRIPTION</span></span>
<span data-ttu-id="79664-109">Använd denna cmdlet för att få program typs informationen i angiven resurs grupp och kluster.</span><span class="sxs-lookup"><span data-stu-id="79664-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="79664-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79664-110">EXAMPLES</span></span>

### <span data-ttu-id="79664-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="79664-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="79664-112">I det här exemplet hämtas program typs informationen med de angivna parametrarna, om den inte hittar den resurs som det ger upphov till.</span><span class="sxs-lookup"><span data-stu-id="79664-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="79664-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="79664-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="79664-114">I det här exemplet visas en lista med de program typer som är definierade under det angivna klustret.</span><span class="sxs-lookup"><span data-stu-id="79664-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="79664-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79664-115">PARAMETERS</span></span>

### <span data-ttu-id="79664-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="79664-116">-ClusterName</span></span>
<span data-ttu-id="79664-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="79664-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="79664-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79664-118">-DefaultProfile</span></span>
<span data-ttu-id="79664-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79664-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79664-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="79664-120">-Name</span></span>
<span data-ttu-id="79664-121">Ange namnet på program typen</span><span class="sxs-lookup"><span data-stu-id="79664-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="79664-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79664-122">-ResourceGroupName</span></span>
<span data-ttu-id="79664-123">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="79664-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="79664-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79664-124">-ResourceId</span></span>
<span data-ttu-id="79664-125">Program typens arm ResourceId.</span><span class="sxs-lookup"><span data-stu-id="79664-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="79664-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79664-126">CommonParameters</span></span>
<span data-ttu-id="79664-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79664-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79664-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79664-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79664-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79664-129">INPUTS</span></span>

### <span data-ttu-id="79664-130">System. String</span><span class="sxs-lookup"><span data-stu-id="79664-130">System.String</span></span>

## <span data-ttu-id="79664-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79664-131">OUTPUTS</span></span>

### <span data-ttu-id="79664-132">Microsoft. Azure. commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="79664-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="79664-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79664-133">NOTES</span></span>

## <span data-ttu-id="79664-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79664-134">RELATED LINKS</span></span>
