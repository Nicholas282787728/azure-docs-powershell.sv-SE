---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403000"
---
# <span data-ttu-id="f2fba-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f2fba-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="f2fba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2fba-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fba-103">Få information om de hanterade kluster resurserna.</span><span class="sxs-lookup"><span data-stu-id="f2fba-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="f2fba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2fba-104">SYNTAX</span></span>

### <span data-ttu-id="f2fba-105">BySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="f2fba-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2fba-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2fba-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2fba-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f2fba-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2fba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2fba-108">DESCRIPTION</span></span>
<span data-ttu-id="f2fba-109">Få information om de hanterade kluster resurserna.</span><span class="sxs-lookup"><span data-stu-id="f2fba-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="f2fba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2fba-110">EXAMPLES</span></span>

### <span data-ttu-id="f2fba-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2fba-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="f2fba-112">Skaffa kluster information.</span><span class="sxs-lookup"><span data-stu-id="f2fba-112">Get cluster details.</span></span>

### <span data-ttu-id="f2fba-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f2fba-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="f2fba-114">Få en lista med kluster under den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2fba-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="f2fba-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f2fba-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="f2fba-116">Få en lista över kluster under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f2fba-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="f2fba-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2fba-117">PARAMETERS</span></span>

### <span data-ttu-id="f2fba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fba-118">-DefaultProfile</span></span>
<span data-ttu-id="f2fba-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2fba-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2fba-120">-Name</span></span>
<span data-ttu-id="f2fba-121">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="f2fba-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fba-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2fba-123">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2fba-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fba-124">CommonParameters</span></span>
<span data-ttu-id="f2fba-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2fba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fba-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2fba-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fba-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2fba-127">INPUTS</span></span>

### <span data-ttu-id="f2fba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f2fba-128">System.String</span></span>

## <span data-ttu-id="f2fba-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2fba-129">OUTPUTS</span></span>

### <span data-ttu-id="f2fba-130">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f2fba-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="f2fba-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2fba-131">NOTES</span></span>

## <span data-ttu-id="f2fba-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2fba-132">RELATED LINKS</span></span>
