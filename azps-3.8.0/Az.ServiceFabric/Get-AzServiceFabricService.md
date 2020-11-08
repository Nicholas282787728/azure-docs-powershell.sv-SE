---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 62f1e4a9313ebcbd2ad6d815344dc18e5844ed13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089449"
---
# <span data-ttu-id="1c80a-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1c80a-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="1c80a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c80a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c80a-103">Få information om tjänstens infrastruktur tjänst under angiven program och ett kluster.</span><span class="sxs-lookup"><span data-stu-id="1c80a-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="1c80a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c80a-104">SYNTAX</span></span>

### <span data-ttu-id="1c80a-105">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="1c80a-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c80a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1c80a-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c80a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c80a-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c80a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c80a-108">DESCRIPTION</span></span>
<span data-ttu-id="1c80a-109">Denna cmdlet hämtar tjänst informationen i angivet program och kluster.</span><span class="sxs-lookup"><span data-stu-id="1c80a-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="1c80a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c80a-110">EXAMPLES</span></span>

### <span data-ttu-id="1c80a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1c80a-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="1c80a-112">Det här exemplet får tjänst resurs informationen för tjänsten "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="1c80a-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="1c80a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1c80a-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="1c80a-114">I det här exemplet visas en lista med tjänsterna under programmet "testApp".</span><span class="sxs-lookup"><span data-stu-id="1c80a-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="1c80a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c80a-115">PARAMETERS</span></span>

### <span data-ttu-id="1c80a-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1c80a-116">-ApplicationName</span></span>
<span data-ttu-id="1c80a-117">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="1c80a-117">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c80a-118">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="1c80a-118">-ClusterName</span></span>
<span data-ttu-id="1c80a-119">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="1c80a-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1c80a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c80a-120">-DefaultProfile</span></span>
<span data-ttu-id="1c80a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c80a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c80a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c80a-122">-Name</span></span>
<span data-ttu-id="1c80a-123">Ange namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1c80a-123">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c80a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c80a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c80a-125">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c80a-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1c80a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c80a-126">-ResourceId</span></span>
<span data-ttu-id="1c80a-127">Tjänstens ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1c80a-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="1c80a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c80a-128">CommonParameters</span></span>
<span data-ttu-id="1c80a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c80a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c80a-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c80a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c80a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c80a-131">INPUTS</span></span>

### <span data-ttu-id="1c80a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1c80a-132">System.String</span></span>

## <span data-ttu-id="1c80a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c80a-133">OUTPUTS</span></span>

### <span data-ttu-id="1c80a-134">Microsoft. Azure. commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="1c80a-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="1c80a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c80a-135">NOTES</span></span>

## <span data-ttu-id="1c80a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c80a-136">RELATED LINKS</span></span>
