---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092017"
---
# <span data-ttu-id="9cd71-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9cd71-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="9cd71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cd71-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd71-103">Få information om tjänstens Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="9cd71-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="9cd71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cd71-104">SYNTAX</span></span>

### <span data-ttu-id="9cd71-105">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="9cd71-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd71-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9cd71-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd71-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cd71-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cd71-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cd71-108">DESCRIPTION</span></span>
<span data-ttu-id="9cd71-109">Denna cmdlet hämtar program informationen i angiven resurs grupp och kluster.</span><span class="sxs-lookup"><span data-stu-id="9cd71-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="9cd71-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cd71-110">EXAMPLES</span></span>

### <span data-ttu-id="9cd71-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9cd71-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="9cd71-112">I det här exemplet hämtas program resurs informationen för programmet "testApp".</span><span class="sxs-lookup"><span data-stu-id="9cd71-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="9cd71-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9cd71-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="9cd71-114">I det här exemplet visas en lista med program under klustrets "testCluster".</span><span class="sxs-lookup"><span data-stu-id="9cd71-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="9cd71-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cd71-115">PARAMETERS</span></span>

### <span data-ttu-id="9cd71-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9cd71-116">-ClusterName</span></span>
<span data-ttu-id="9cd71-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="9cd71-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9cd71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd71-118">-DefaultProfile</span></span>
<span data-ttu-id="9cd71-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd71-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cd71-120">-Name</span></span>
<span data-ttu-id="9cd71-121">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="9cd71-121">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd71-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd71-122">-ResourceGroupName</span></span>
<span data-ttu-id="9cd71-123">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9cd71-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9cd71-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cd71-124">-ResourceId</span></span>
<span data-ttu-id="9cd71-125">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9cd71-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="9cd71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd71-126">CommonParameters</span></span>
<span data-ttu-id="9cd71-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd71-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd71-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd71-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cd71-129">INPUTS</span></span>

### <span data-ttu-id="9cd71-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd71-130">System.String</span></span>

## <span data-ttu-id="9cd71-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cd71-131">OUTPUTS</span></span>

### <span data-ttu-id="9cd71-132">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="9cd71-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="9cd71-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cd71-133">NOTES</span></span>

## <span data-ttu-id="9cd71-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cd71-134">RELATED LINKS</span></span>
