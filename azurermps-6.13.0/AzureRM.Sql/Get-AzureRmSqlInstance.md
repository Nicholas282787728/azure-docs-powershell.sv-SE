---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579940"
---
# <span data-ttu-id="7cd70-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7cd70-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="7cd70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cd70-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd70-103">Returnerar information om en Azure SQL-hanterad databas instans.</span><span class="sxs-lookup"><span data-stu-id="7cd70-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cd70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cd70-104">SYNTAX</span></span>

### <span data-ttu-id="7cd70-105">GetInstanceByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="7cd70-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cd70-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7cd70-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd70-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cd70-107">DESCRIPTION</span></span>
<span data-ttu-id="7cd70-108">Cmdleten **Get-AzureRmSqlInstance** returnerar information om ett eller flera Azure SQL-hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="7cd70-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="7cd70-109">Ange namnet på en instans om du endast vill visa information för den instansen.</span><span class="sxs-lookup"><span data-stu-id="7cd70-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="7cd70-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cd70-110">EXAMPLES</span></span>

### <span data-ttu-id="7cd70-111">Exempel 1: Hämta alla instanser kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="7cd70-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="7cd70-112">Med det här kommandot får du information om alla instanser tilldelade till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7cd70-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="7cd70-113">Exempel 2: Hämta information om en instans</span><span class="sxs-lookup"><span data-stu-id="7cd70-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="7cd70-114">Det här kommandot får information om förekomsten som heter managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7cd70-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="7cd70-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cd70-115">PARAMETERS</span></span>

### <span data-ttu-id="7cd70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd70-116">-DefaultProfile</span></span>
<span data-ttu-id="7cd70-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd70-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd70-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cd70-118">-Name</span></span>
<span data-ttu-id="7cd70-119">SQL-instansnamn.</span><span class="sxs-lookup"><span data-stu-id="7cd70-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd70-120">-ResourceGroupName</span></span>
<span data-ttu-id="7cd70-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7cd70-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd70-122">CommonParameters</span></span>
<span data-ttu-id="7cd70-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd70-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd70-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd70-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cd70-125">INPUTS</span></span>

### <span data-ttu-id="7cd70-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="7cd70-126">None</span></span>

## <span data-ttu-id="7cd70-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cd70-127">OUTPUTS</span></span>

### <span data-ttu-id="7cd70-128">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7cd70-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7cd70-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cd70-129">NOTES</span></span>

## <span data-ttu-id="7cd70-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cd70-130">RELATED LINKS</span></span>
