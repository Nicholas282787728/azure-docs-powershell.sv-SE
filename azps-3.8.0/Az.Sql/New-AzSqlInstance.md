---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 34b12387ef7c967349b6c5f8599d5be361ae43e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091416"
---
# <span data-ttu-id="62d86-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="62d86-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="62d86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62d86-102">SYNOPSIS</span></span>
<span data-ttu-id="62d86-103">Skapar en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="62d86-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="62d86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62d86-104">SYNTAX</span></span>

### <span data-ttu-id="62d86-105">NewByEditionAndComputeGenerationParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="62d86-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-MinimalTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d86-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62d86-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d86-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62d86-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62d86-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="62d86-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62d86-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62d86-109">DESCRIPTION</span></span>
<span data-ttu-id="62d86-110">Cmdleten **New-AzSqlInstance** skapar en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="62d86-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="62d86-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62d86-111">EXAMPLES</span></span>

### <span data-ttu-id="62d86-112">Exempel 1: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="62d86-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
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
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="62d86-113">Det här kommandot skapar en ny instans med hjälp av parametern SkuName.</span><span class="sxs-lookup"><span data-stu-id="62d86-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="62d86-114">Exempel 2: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="62d86-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="62d86-115">Det här kommandot skapar en ny instans genom att använda parametrarna Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="62d86-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="62d86-116">Exempel 3: skapa en ny instans i en instans med hjälp av ett objekt i en instans</span><span class="sxs-lookup"><span data-stu-id="62d86-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="62d86-117">Det här kommandot skapar en ny instans i en instans med hjälp av ett objekt i en instans.</span><span class="sxs-lookup"><span data-stu-id="62d86-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="62d86-118">Exempel 4: skapa en ny instans i en instans med en instans-ID för en resurspool</span><span class="sxs-lookup"><span data-stu-id="62d86-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="62d86-119">Det här kommandot skapar en ny instans i en instans med hjälp av poolens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="62d86-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="62d86-120">Exempel 5: skapa en ny instans i en instans</span><span class="sxs-lookup"><span data-stu-id="62d86-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
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
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="62d86-121">Det här kommandot skapar en ny instans i en instans med namnet instancePool0</span><span class="sxs-lookup"><span data-stu-id="62d86-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="62d86-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62d86-122">PARAMETERS</span></span>

### <span data-ttu-id="62d86-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="62d86-123">-AdministratorCredential</span></span>
<span data-ttu-id="62d86-124">Instansens autentiseringsuppgifter för SQL-autentisering.</span><span class="sxs-lookup"><span data-stu-id="62d86-124">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62d86-125">-AsJob</span></span>
<span data-ttu-id="62d86-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="62d86-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="62d86-127">-AssignIdentity</span></span>
<span data-ttu-id="62d86-128">Skapa och tilldela en Azure Active Directory-identitet för den här hanterade instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="62d86-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-129">-Sortering</span><span class="sxs-lookup"><span data-stu-id="62d86-129">-Collation</span></span>
<span data-ttu-id="62d86-130">Sortering av den SQL-hanterade instans som du kan använda.</span><span class="sxs-lookup"><span data-stu-id="62d86-130">The collation of the Azure SQL Managed Instance to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="62d86-131">-ComputeGeneration</span></span>
<span data-ttu-id="62d86-132">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="62d86-132">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d86-133">-DefaultProfile</span></span>
<span data-ttu-id="62d86-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62d86-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d86-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="62d86-135">-DnsZonePartner</span></span>
<span data-ttu-id="62d86-136">Resurs-ID för partner-hanterad server för att ärva egenskapen DnsZone från för skapande av hanterad instans</span><span class="sxs-lookup"><span data-stu-id="62d86-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-137">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="62d86-137">-Edition</span></span>
<span data-ttu-id="62d86-138">Versionen för instansen.</span><span class="sxs-lookup"><span data-stu-id="62d86-138">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="62d86-139">-InstancePool</span></span>
<span data-ttu-id="62d86-140">Det överordnade objektet för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="62d86-140">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-141">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="62d86-141">-MinimalTlsVersion</span></span>
<span data-ttu-id="62d86-142">Den minsta TLS-version som ska tillämpas för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="62d86-142">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-143">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="62d86-143">-InstancePoolName</span></span>
<span data-ttu-id="62d86-144">Instans i vilken den här instansen placeras i.</span><span class="sxs-lookup"><span data-stu-id="62d86-144">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-145">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="62d86-145">-InstancePoolResourceId</span></span>
<span data-ttu-id="62d86-146">Resurs-ID för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="62d86-146">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-147">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="62d86-147">-LicenseType</span></span>
<span data-ttu-id="62d86-148">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="62d86-148">Determines which License Type to use.</span></span> <span data-ttu-id="62d86-149">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="62d86-149">Possible values are:</span></span>
- <span data-ttu-id="62d86-150">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="62d86-150">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="62d86-151">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62d86-151">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="62d86-152">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="62d86-152">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="62d86-153">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62d86-153">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-154">-Plats</span><span class="sxs-lookup"><span data-stu-id="62d86-154">-Location</span></span>
<span data-ttu-id="62d86-155">Den plats där du vill skapa instansen</span><span class="sxs-lookup"><span data-stu-id="62d86-155">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-156">-Namn</span><span class="sxs-lookup"><span data-stu-id="62d86-156">-Name</span></span>
<span data-ttu-id="62d86-157">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="62d86-157">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-158">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="62d86-158">-ProxyOverride</span></span>
<span data-ttu-id="62d86-159">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="62d86-159">The connection type used for connecting to the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-160">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="62d86-160">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="62d86-161">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="62d86-161">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d86-162">-ResourceGroupName</span></span>
<span data-ttu-id="62d86-163">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="62d86-163">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="62d86-164">-SkuName</span></span>
<span data-ttu-id="62d86-165">SKU-namnet för instansen, t. ex. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="62d86-165">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-166">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="62d86-166">-StorageSizeInGB</span></span>
<span data-ttu-id="62d86-167">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="62d86-167">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-168">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="62d86-168">-SubnetId</span></span>
<span data-ttu-id="62d86-169">Det Subnet-ID som ska användas för att skapa en instans</span><span class="sxs-lookup"><span data-stu-id="62d86-169">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-170">-Tagg</span><span class="sxs-lookup"><span data-stu-id="62d86-170">-Tag</span></span>
<span data-ttu-id="62d86-171">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="62d86-171">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-172">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="62d86-172">-TimezoneId</span></span>
<span data-ttu-id="62d86-173">ID för tids zonen för den instans som ska anges.</span><span class="sxs-lookup"><span data-stu-id="62d86-173">The time zone id for the instance to set.</span></span> <span data-ttu-id="62d86-174">En lista med tids zons-ID: n visas i vyn sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="62d86-174">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-175">-VCore</span><span class="sxs-lookup"><span data-stu-id="62d86-175">-VCore</span></span>
<span data-ttu-id="62d86-176">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="62d86-176">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-177">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62d86-177">-Confirm</span></span>
<span data-ttu-id="62d86-178">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62d86-178">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d86-179">-WhatIf</span></span>
<span data-ttu-id="62d86-180">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62d86-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d86-181">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62d86-181">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d86-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d86-182">CommonParameters</span></span>
<span data-ttu-id="62d86-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d86-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d86-184">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62d86-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d86-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62d86-185">INPUTS</span></span>

### <span data-ttu-id="62d86-186">Ingen</span><span class="sxs-lookup"><span data-stu-id="62d86-186">None</span></span>

## <span data-ttu-id="62d86-187">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62d86-187">OUTPUTS</span></span>

### <span data-ttu-id="62d86-188">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="62d86-188">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="62d86-189">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62d86-189">NOTES</span></span>

## <span data-ttu-id="62d86-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62d86-190">RELATED LINKS</span></span>
