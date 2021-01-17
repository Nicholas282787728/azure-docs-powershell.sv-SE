---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388119"
---
# <span data-ttu-id="0e1db-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0e1db-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="0e1db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e1db-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1db-103">Få information om tjänstens infrastruktur tjänst under angiven program och ett kluster.</span><span class="sxs-lookup"><span data-stu-id="0e1db-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="0e1db-104">Stöder endast funktioner som distribueras av ARM.</span><span class="sxs-lookup"><span data-stu-id="0e1db-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="0e1db-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e1db-105">SYNTAX</span></span>

### <span data-ttu-id="0e1db-106">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="0e1db-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e1db-107">ByName</span><span class="sxs-lookup"><span data-stu-id="0e1db-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e1db-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e1db-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e1db-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e1db-109">DESCRIPTION</span></span>
<span data-ttu-id="0e1db-110">Denna cmdlet hämtar tjänst informationen i angivet program och kluster.</span><span class="sxs-lookup"><span data-stu-id="0e1db-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="0e1db-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e1db-111">EXAMPLES</span></span>

### <span data-ttu-id="0e1db-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e1db-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="0e1db-113">Det här exemplet får tjänst resurs informationen för tjänsten "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="0e1db-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="0e1db-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0e1db-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="0e1db-115">I det här exemplet visas en lista med tjänsterna under programmet "testApp".</span><span class="sxs-lookup"><span data-stu-id="0e1db-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="0e1db-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e1db-116">PARAMETERS</span></span>

### <span data-ttu-id="0e1db-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0e1db-117">-ApplicationName</span></span>
<span data-ttu-id="0e1db-118">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="0e1db-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="0e1db-119">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="0e1db-119">-ClusterName</span></span>
<span data-ttu-id="0e1db-120">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="0e1db-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0e1db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1db-121">-DefaultProfile</span></span>
<span data-ttu-id="0e1db-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e1db-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e1db-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e1db-123">-Name</span></span>
<span data-ttu-id="0e1db-124">Ange namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0e1db-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="0e1db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e1db-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e1db-126">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0e1db-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0e1db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e1db-127">-ResourceId</span></span>
<span data-ttu-id="0e1db-128">Tjänstens ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0e1db-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="0e1db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1db-129">CommonParameters</span></span>
<span data-ttu-id="0e1db-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1db-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e1db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1db-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e1db-132">INPUTS</span></span>

### <span data-ttu-id="0e1db-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e1db-133">System.String</span></span>

## <span data-ttu-id="0e1db-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e1db-134">OUTPUTS</span></span>

### <span data-ttu-id="0e1db-135">Microsoft. Azure. commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="0e1db-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="0e1db-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e1db-136">NOTES</span></span>

## <span data-ttu-id="0e1db-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e1db-137">RELATED LINKS</span></span>
