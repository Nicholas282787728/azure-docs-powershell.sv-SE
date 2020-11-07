---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746705"
---
# <span data-ttu-id="e9845-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e9845-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="e9845-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9845-102">SYNOPSIS</span></span>
<span data-ttu-id="e9845-103">Returnerar information om en Azure SQL-hanterad databas instans.</span><span class="sxs-lookup"><span data-stu-id="e9845-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="e9845-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9845-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9845-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9845-105">DESCRIPTION</span></span>
<span data-ttu-id="e9845-106">Cmdleten **Get-AzSqlInstance** returnerar information om ett eller flera Azure SQL-hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="e9845-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="e9845-107">Ange namnet på en instans om du endast vill visa information för den instansen.</span><span class="sxs-lookup"><span data-stu-id="e9845-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="e9845-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9845-108">EXAMPLES</span></span>

### <span data-ttu-id="e9845-109">Exempel 1: Hämta alla instanser kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e9845-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="e9845-110">Med det här kommandot får du information om alla instanser tilldelade till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e9845-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e9845-111">Exempel 2: Hämta information om en instans</span><span class="sxs-lookup"><span data-stu-id="e9845-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="e9845-112">Det här kommandot får information om förekomsten som heter managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e9845-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="e9845-113">Exempel 3: Hämta alla instanser tilldelade till en resurs grupp med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="e9845-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="e9845-114">Med det här kommandot får du information om alla instanser tilldelade till resurs gruppen ResourceGroup01 som börjar med "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="e9845-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="e9845-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9845-115">PARAMETERS</span></span>

### <span data-ttu-id="e9845-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9845-116">-DefaultProfile</span></span>
<span data-ttu-id="e9845-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9845-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9845-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9845-118">-Name</span></span>
<span data-ttu-id="e9845-119">SQL-instansnamn.</span><span class="sxs-lookup"><span data-stu-id="e9845-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e9845-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9845-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9845-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e9845-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e9845-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9845-122">CommonParameters</span></span>
<span data-ttu-id="e9845-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9845-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9845-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9845-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9845-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9845-125">INPUTS</span></span>

### <span data-ttu-id="e9845-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9845-126">None</span></span>

## <span data-ttu-id="e9845-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9845-127">OUTPUTS</span></span>

### <span data-ttu-id="e9845-128">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e9845-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e9845-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9845-129">NOTES</span></span>

## <span data-ttu-id="e9845-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9845-130">RELATED LINKS</span></span>
