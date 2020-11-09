---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322092"
---
# <span data-ttu-id="a5993-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a5993-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="a5993-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5993-102">SYNOPSIS</span></span>
<span data-ttu-id="a5993-103">Hämta resursinformation för hanterad nod.</span><span class="sxs-lookup"><span data-stu-id="a5993-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="a5993-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5993-104">SYNTAX</span></span>

### <span data-ttu-id="a5993-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a5993-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5993-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5993-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5993-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5993-107">DESCRIPTION</span></span>
<span data-ttu-id="a5993-108">Hämta resursinformation för hanterad nod.</span><span class="sxs-lookup"><span data-stu-id="a5993-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="a5993-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5993-109">EXAMPLES</span></span>

### <span data-ttu-id="a5993-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5993-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="a5993-111">Hämta information om nodtyp.</span><span class="sxs-lookup"><span data-stu-id="a5993-111">Get node type details.</span></span>

### <span data-ttu-id="a5993-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a5993-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="a5993-113">Hämta lista med nodtyper under det angivna klustret.</span><span class="sxs-lookup"><span data-stu-id="a5993-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="a5993-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5993-114">PARAMETERS</span></span>

### <span data-ttu-id="a5993-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a5993-115">-ClusterName</span></span>
<span data-ttu-id="a5993-116">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="a5993-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5993-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5993-117">-DefaultProfile</span></span>
<span data-ttu-id="a5993-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5993-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5993-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5993-119">-Name</span></span>
<span data-ttu-id="a5993-120">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="a5993-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5993-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5993-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5993-122">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5993-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5993-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5993-123">CommonParameters</span></span>
<span data-ttu-id="a5993-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5993-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5993-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5993-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5993-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5993-126">INPUTS</span></span>

### <span data-ttu-id="a5993-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a5993-127">System.String</span></span>

## <span data-ttu-id="a5993-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5993-128">OUTPUTS</span></span>

### <span data-ttu-id="a5993-129">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a5993-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="a5993-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5993-130">NOTES</span></span>

## <span data-ttu-id="a5993-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5993-131">RELATED LINKS</span></span>
