---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388122"
---
# <span data-ttu-id="5a936-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5a936-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="5a936-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a936-102">SYNOPSIS</span></span>
<span data-ttu-id="5a936-103">Få information om tjänstens Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="5a936-103">Get Service Fabric application details.</span></span> <span data-ttu-id="5a936-104">Stöder endast program som distribueras av armar.</span><span class="sxs-lookup"><span data-stu-id="5a936-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="5a936-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a936-105">SYNTAX</span></span>

### <span data-ttu-id="5a936-106">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="5a936-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a936-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5a936-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a936-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a936-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a936-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a936-109">DESCRIPTION</span></span>
<span data-ttu-id="5a936-110">Denna cmdlet hämtar program informationen i angiven resurs grupp och kluster.</span><span class="sxs-lookup"><span data-stu-id="5a936-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="5a936-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a936-111">EXAMPLES</span></span>

### <span data-ttu-id="5a936-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a936-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="5a936-113">I det här exemplet hämtas program resurs informationen för programmet "testApp".</span><span class="sxs-lookup"><span data-stu-id="5a936-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="5a936-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5a936-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="5a936-115">I det här exemplet visas en lista med program under klustrets "testCluster".</span><span class="sxs-lookup"><span data-stu-id="5a936-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="5a936-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a936-116">PARAMETERS</span></span>

### <span data-ttu-id="5a936-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5a936-117">-ClusterName</span></span>
<span data-ttu-id="5a936-118">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="5a936-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5a936-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a936-119">-DefaultProfile</span></span>
<span data-ttu-id="5a936-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a936-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a936-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a936-121">-Name</span></span>
<span data-ttu-id="5a936-122">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="5a936-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="5a936-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a936-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a936-124">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a936-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5a936-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a936-125">-ResourceId</span></span>
<span data-ttu-id="5a936-126">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5a936-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="5a936-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a936-127">CommonParameters</span></span>
<span data-ttu-id="5a936-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a936-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a936-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a936-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a936-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a936-130">INPUTS</span></span>

### <span data-ttu-id="5a936-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5a936-131">System.String</span></span>

## <span data-ttu-id="5a936-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a936-132">OUTPUTS</span></span>

### <span data-ttu-id="5a936-133">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="5a936-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="5a936-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a936-134">NOTES</span></span>

## <span data-ttu-id="5a936-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a936-135">RELATED LINKS</span></span>
