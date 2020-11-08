---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088482"
---
# <span data-ttu-id="8dfdc-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="8dfdc-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="8dfdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8dfdc-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfdc-103">Returnerar information om det virtuella Azure SQL-klustret.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="8dfdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8dfdc-104">SYNTAX</span></span>

### <span data-ttu-id="8dfdc-105">GetVirtualClusterByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="8dfdc-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8dfdc-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8dfdc-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dfdc-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfdc-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dfdc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8dfdc-108">DESCRIPTION</span></span>
<span data-ttu-id="8dfdc-109">Cmdleten **Get-AzSqlVirtualCluster** returnerar information om ett eller flera virtuella kluster för Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="8dfdc-110">Ange namnet på ett virtuellt kluster för att visa information för bara det klustret.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="8dfdc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8dfdc-111">EXAMPLES</span></span>

### <span data-ttu-id="8dfdc-112">Exempel 1: Hämta alla virtuella kluster som är tilldelade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="8dfdc-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="8dfdc-113">Med det här kommandot får du information om alla virtuella kluster som tilldelats resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8dfdc-114">Exempel 2: få information om ett specifikt virtuellt kluster</span><span class="sxs-lookup"><span data-stu-id="8dfdc-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="8dfdc-115">Med det här kommandot får du information om det virtuella kluster VirtualCluster1 i resurs grupps ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8dfdc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8dfdc-116">PARAMETERS</span></span>

### <span data-ttu-id="8dfdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfdc-117">-DefaultProfile</span></span>
<span data-ttu-id="8dfdc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfdc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8dfdc-119">-Name</span></span>
<span data-ttu-id="8dfdc-120">Namnet på det virtuella klustret.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfdc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfdc-121">-ResourceGroupName</span></span>
<span data-ttu-id="8dfdc-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfdc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfdc-123">-ResourceId</span></span>
<span data-ttu-id="8dfdc-124">Resurs-ID för instans objekt som ska visas</span><span class="sxs-lookup"><span data-stu-id="8dfdc-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfdc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfdc-125">CommonParameters</span></span>
<span data-ttu-id="8dfdc-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfdc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfdc-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dfdc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfdc-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8dfdc-128">INPUTS</span></span>

### <span data-ttu-id="8dfdc-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="8dfdc-129">None</span></span>

## <span data-ttu-id="8dfdc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8dfdc-130">OUTPUTS</span></span>

### <span data-ttu-id="8dfdc-131">Microsoft. Azure. commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="8dfdc-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="8dfdc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8dfdc-132">NOTES</span></span>

## <span data-ttu-id="8dfdc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8dfdc-133">RELATED LINKS</span></span>
