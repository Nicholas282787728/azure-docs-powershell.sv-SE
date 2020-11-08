---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bb9ae3ba225c67a98b6c3588e1dc0c63f02170ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269900"
---
# <span data-ttu-id="a5ef4-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a5ef4-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="a5ef4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ef4-103">Skapar en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a5ef4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5ef4-104">SYNTAX</span></span>

### <span data-ttu-id="a5ef4-105">NewByEditionAndComputeGenerationParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a5ef4-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ef4-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5ef4-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ef4-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5ef4-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ef4-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="a5ef4-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ef4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5ef4-109">DESCRIPTION</span></span>
<span data-ttu-id="a5ef4-110">Cmdleten **New-AzSqlInstance** skapar en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="a5ef4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5ef4-111">EXAMPLES</span></span>

### <span data-ttu-id="a5ef4-112">Exempel 1: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="a5ef4-113">Det här kommandot skapar en ny instans med hjälp av parametern SkuName.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="a5ef4-114">Exempel 2: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="a5ef4-115">Det här kommandot skapar en ny instans genom att använda parametrarna Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="a5ef4-116">Exempel 3: skapa en ny instans i en instans med hjälp av ett objekt i en instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="a5ef4-117">Det här kommandot skapar en ny instans i en instans med hjälp av ett objekt i en instans.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="a5ef4-118">Exempel 4: skapa en ny instans i en instans med en instans-ID för en resurspool</span><span class="sxs-lookup"><span data-stu-id="a5ef4-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="a5ef4-119">Det här kommandot skapar en ny instans i en instans med hjälp av poolens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="a5ef4-120">Exempel 5: skapa en ny instans i en instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="a5ef4-121">Det här kommandot skapar en ny instans i en instans med namnet instancePool0</span><span class="sxs-lookup"><span data-stu-id="a5ef4-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="a5ef4-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5ef4-122">PARAMETERS</span></span>

### <span data-ttu-id="a5ef4-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="a5ef4-123">-AdministratorCredential</span></span>
<span data-ttu-id="a5ef4-124">Instansens autentiseringsuppgifter för SQL-autentisering.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="a5ef4-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5ef4-125">-AsJob</span></span>
<span data-ttu-id="a5ef4-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a5ef4-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5ef4-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a5ef4-127">-AssignIdentity</span></span>
<span data-ttu-id="a5ef4-128">Skapa och tilldela en Azure Active Directory-identitet för den här hanterade instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a5ef4-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a5ef4-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a5ef4-130">Redundans för säkerhets kopiering som används för att lagra säkerhets kopior för den SQL Azure-hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="a5ef4-131">Alternativen är: lokal, zon och geo</span><span class="sxs-lookup"><span data-stu-id="a5ef4-131">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ef4-132">-Sortering</span><span class="sxs-lookup"><span data-stu-id="a5ef4-132">-Collation</span></span>
<span data-ttu-id="a5ef4-133">Sortering av den SQL-hanterade instans som du kan använda.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="a5ef4-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a5ef4-134">-ComputeGeneration</span></span>
<span data-ttu-id="a5ef4-135">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="a5ef4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ef4-136">-DefaultProfile</span></span>
<span data-ttu-id="a5ef4-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ef4-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="a5ef4-138">-DnsZonePartner</span></span>
<span data-ttu-id="a5ef4-139">Resurs-ID för partner-hanterad server för att ärva egenskapen DnsZone från för skapande av hanterad instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="a5ef4-140">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="a5ef4-140">-Edition</span></span>
<span data-ttu-id="a5ef4-141">Versionen för instansen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="a5ef4-142">-Force</span><span class="sxs-lookup"><span data-stu-id="a5ef4-142">-Force</span></span>
<span data-ttu-id="a5ef4-143">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="a5ef4-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a5ef4-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="a5ef4-144">-InstancePool</span></span>
<span data-ttu-id="a5ef4-145">Det överordnade objektet för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="a5ef4-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="a5ef4-146">-InstancePoolName</span></span>
<span data-ttu-id="a5ef4-147">Instans i vilken den här instansen placeras i.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="a5ef4-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ef4-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="a5ef4-149">Resurs-ID för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="a5ef4-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a5ef4-150">-LicenseType</span></span>
<span data-ttu-id="a5ef4-151">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-151">Determines which License Type to use.</span></span> <span data-ttu-id="a5ef4-152">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="a5ef4-152">Possible values are:</span></span>
- <span data-ttu-id="a5ef4-153">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="a5ef4-154">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="a5ef4-155">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="a5ef4-156">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="a5ef4-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="a5ef4-157">-Location</span></span>
<span data-ttu-id="a5ef4-158">Den plats där du vill skapa instansen</span><span class="sxs-lookup"><span data-stu-id="a5ef4-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="a5ef4-159">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a5ef4-159">-MinimalTlsVersion</span></span>
<span data-ttu-id="a5ef4-160">Den minsta TLS-version som ska tillämpas för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="a5ef4-160">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ef4-161">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5ef4-161">-Name</span></span>
<span data-ttu-id="a5ef4-162">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-162">Instance name.</span></span>

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

### <span data-ttu-id="a5ef4-163">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="a5ef4-163">-ProxyOverride</span></span>
<span data-ttu-id="a5ef4-164">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-164">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="a5ef4-165">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="a5ef4-165">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="a5ef4-166">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-166">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="a5ef4-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ef4-167">-ResourceGroupName</span></span>
<span data-ttu-id="a5ef4-168">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-168">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5ef4-169">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a5ef4-169">-SkuName</span></span>
<span data-ttu-id="a5ef4-170">SKU-namnet för instansen, t. ex. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="a5ef4-170">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="a5ef4-171">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a5ef4-171">-StorageSizeInGB</span></span>
<span data-ttu-id="a5ef4-172">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-172">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="a5ef4-173">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a5ef4-173">-SubnetId</span></span>
<span data-ttu-id="a5ef4-174">Det Subnet-ID som ska användas för att skapa en instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-174">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="a5ef4-175">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a5ef4-175">-Tag</span></span>
<span data-ttu-id="a5ef4-176">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="a5ef4-176">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="a5ef4-177">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="a5ef4-177">-TimezoneId</span></span>
<span data-ttu-id="a5ef4-178">ID för tids zonen för den instans som ska anges.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-178">The time zone id for the instance to set.</span></span> <span data-ttu-id="a5ef4-179">En lista med tids zons-ID: n visas i vyn sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="a5ef4-179">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="a5ef4-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="a5ef4-180">-VCore</span></span>
<span data-ttu-id="a5ef4-181">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="a5ef4-181">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="a5ef4-182">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5ef4-182">-Confirm</span></span>
<span data-ttu-id="a5ef4-183">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ef4-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ef4-184">-WhatIf</span></span>
<span data-ttu-id="a5ef4-185">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ef4-186">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ef4-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ef4-187">CommonParameters</span></span>
<span data-ttu-id="a5ef4-188">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ef4-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ef4-189">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5ef4-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ef4-190">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5ef4-190">INPUTS</span></span>

### <span data-ttu-id="a5ef4-191">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5ef4-191">None</span></span>

## <span data-ttu-id="a5ef4-192">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5ef4-192">OUTPUTS</span></span>

### <span data-ttu-id="a5ef4-193">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a5ef4-193">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a5ef4-194">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5ef4-194">NOTES</span></span>

## <span data-ttu-id="a5ef4-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5ef4-195">RELATED LINKS</span></span>
