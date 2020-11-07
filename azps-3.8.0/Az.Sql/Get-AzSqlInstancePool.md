---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: afbd74953f876ede2a03e94c4db46937470a92dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925770"
---
# <span data-ttu-id="581be-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="581be-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="581be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="581be-102">SYNOPSIS</span></span>
<span data-ttu-id="581be-103">Returnerar information om Azure SQL instance-poolen.</span><span class="sxs-lookup"><span data-stu-id="581be-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="581be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="581be-104">SYNTAX</span></span>

### <span data-ttu-id="581be-105">ListBySubOrResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="581be-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="581be-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="581be-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="581be-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="581be-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="581be-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="581be-108">DESCRIPTION</span></span>
<span data-ttu-id="581be-109">Cmdleten **Get-AzSqlInstancePool** returnerar information om en eller flera Azure SQL-instanser.</span><span class="sxs-lookup"><span data-stu-id="581be-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="581be-110">Ange namnet på en instans för att visa information för endast den instans.</span><span class="sxs-lookup"><span data-stu-id="581be-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="581be-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="581be-111">EXAMPLES</span></span>

### <span data-ttu-id="581be-112">Exempel 1: Hämta alla instanser av en kund prenumeration</span><span class="sxs-lookup"><span data-stu-id="581be-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="581be-113">Det här kommandot får information om alla instanser inom kund abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="581be-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="581be-114">Exempel 2: Hämta alla instanser i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="581be-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="581be-115">Med det här kommandot får du information om alla instanser i resurs gruppen resourcegroup01.</span><span class="sxs-lookup"><span data-stu-id="581be-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="581be-116">Exempel 3: Hämta information om en instans-pool</span><span class="sxs-lookup"><span data-stu-id="581be-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="581be-117">Med det här kommandot får du information om instancePool0.</span><span class="sxs-lookup"><span data-stu-id="581be-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="581be-118">Exempel 4: Hämta information om en instans med hjälp av resurs-ID för en pool</span><span class="sxs-lookup"><span data-stu-id="581be-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="581be-119">Med det här kommandot får du information om entitetsinstansen med dess resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="581be-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="581be-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="581be-120">PARAMETERS</span></span>

### <span data-ttu-id="581be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581be-121">-DefaultProfile</span></span>
<span data-ttu-id="581be-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="581be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="581be-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="581be-123">-Name</span></span>
<span data-ttu-id="581be-124">Instansens Programpoolsnamn.</span><span class="sxs-lookup"><span data-stu-id="581be-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="581be-125">-ResourceGroupName</span></span>
<span data-ttu-id="581be-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="581be-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="581be-127">-ResourceId</span></span>
<span data-ttu-id="581be-128">Resurs-ID för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="581be-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581be-129">CommonParameters</span></span>
<span data-ttu-id="581be-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="581be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581be-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="581be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581be-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="581be-132">INPUTS</span></span>

### <span data-ttu-id="581be-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="581be-133">None</span></span>

## <span data-ttu-id="581be-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="581be-134">OUTPUTS</span></span>

### <span data-ttu-id="581be-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="581be-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="581be-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="581be-136">NOTES</span></span>

## <span data-ttu-id="581be-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="581be-137">RELATED LINKS</span></span>
