---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: c282ea9e902f26d010c2421339de68bc670e2f35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262975"
---
# <span data-ttu-id="29318-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="29318-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="29318-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29318-102">SYNOPSIS</span></span>
<span data-ttu-id="29318-103">Få information om tjänstens Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="29318-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="29318-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29318-104">SYNTAX</span></span>

### <span data-ttu-id="29318-105">ByResourceGroupAndCluster (standard)</span><span class="sxs-lookup"><span data-stu-id="29318-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29318-106">ByName</span><span class="sxs-lookup"><span data-stu-id="29318-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29318-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29318-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29318-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29318-108">DESCRIPTION</span></span>
<span data-ttu-id="29318-109">Denna cmdlet hämtar program informationen i angiven resurs grupp och kluster.</span><span class="sxs-lookup"><span data-stu-id="29318-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="29318-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29318-110">EXAMPLES</span></span>

### <span data-ttu-id="29318-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="29318-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="29318-112">I det här exemplet hämtas program resurs informationen för programmet "testApp".</span><span class="sxs-lookup"><span data-stu-id="29318-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="29318-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="29318-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="29318-114">I det här exemplet visas en lista med program under klustrets "testCluster".</span><span class="sxs-lookup"><span data-stu-id="29318-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="29318-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29318-115">PARAMETERS</span></span>

### <span data-ttu-id="29318-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="29318-116">-ClusterName</span></span>
<span data-ttu-id="29318-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="29318-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="29318-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29318-118">-DefaultProfile</span></span>
<span data-ttu-id="29318-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29318-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29318-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="29318-120">-Name</span></span>
<span data-ttu-id="29318-121">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="29318-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="29318-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29318-122">-ResourceGroupName</span></span>
<span data-ttu-id="29318-123">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29318-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="29318-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29318-124">-ResourceId</span></span>
<span data-ttu-id="29318-125">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="29318-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="29318-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29318-126">CommonParameters</span></span>
<span data-ttu-id="29318-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29318-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29318-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29318-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29318-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29318-129">INPUTS</span></span>

### <span data-ttu-id="29318-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29318-130">System.String</span></span>

## <span data-ttu-id="29318-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29318-131">OUTPUTS</span></span>

### <span data-ttu-id="29318-132">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="29318-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="29318-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29318-133">NOTES</span></span>

## <span data-ttu-id="29318-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29318-134">RELATED LINKS</span></span>
