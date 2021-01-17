---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395720"
---
# <span data-ttu-id="323bf-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="323bf-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="323bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="323bf-102">SYNOPSIS</span></span>
<span data-ttu-id="323bf-103">Skapar en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="323bf-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="323bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="323bf-104">SYNTAX</span></span>

### <span data-ttu-id="323bf-105">NewByEditionAndComputeGenerationParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="323bf-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="323bf-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="323bf-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="323bf-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="323bf-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="323bf-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="323bf-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="323bf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="323bf-109">DESCRIPTION</span></span>
<span data-ttu-id="323bf-110">Cmdleten **New-AzSqlInstance** skapar en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="323bf-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="323bf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="323bf-111">EXAMPLES</span></span>

### <span data-ttu-id="323bf-112">Exempel 1: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="323bf-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="323bf-113">Det här kommandot skapar en ny instans med hjälp av parametern SkuName.</span><span class="sxs-lookup"><span data-stu-id="323bf-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="323bf-114">Exempel 2: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="323bf-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="323bf-115">Det här kommandot skapar en ny instans genom att använda parametrarna Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="323bf-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="323bf-116">Exempel 3: skapa en ny instans i en instans med hjälp av ett objekt i en instans</span><span class="sxs-lookup"><span data-stu-id="323bf-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="323bf-117">Det här kommandot skapar en ny instans i en instans med hjälp av ett objekt i en instans.</span><span class="sxs-lookup"><span data-stu-id="323bf-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="323bf-118">Exempel 4: skapa en ny instans i en instans med en instans-ID för en resurspool</span><span class="sxs-lookup"><span data-stu-id="323bf-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="323bf-119">Det här kommandot skapar en ny instans i en instans med hjälp av poolens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="323bf-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="323bf-120">Exempel 5: skapa en ny instans i en instans</span><span class="sxs-lookup"><span data-stu-id="323bf-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="323bf-121">Det här kommandot skapar en ny instans i en instans med namnet instancePool0</span><span class="sxs-lookup"><span data-stu-id="323bf-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="323bf-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="323bf-122">PARAMETERS</span></span>

### <span data-ttu-id="323bf-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="323bf-123">-AdministratorCredential</span></span>
<span data-ttu-id="323bf-124">Instansens autentiseringsuppgifter för SQL-autentisering.</span><span class="sxs-lookup"><span data-stu-id="323bf-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="323bf-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="323bf-125">-AsJob</span></span>
<span data-ttu-id="323bf-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="323bf-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="323bf-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="323bf-127">-AssignIdentity</span></span>
<span data-ttu-id="323bf-128">Skapa och tilldela en Azure Active Directory-identitet för den här hanterade instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="323bf-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="323bf-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="323bf-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="323bf-130">Redundans för säkerhets kopiering som används för att lagra säkerhets kopior för den SQL Azure-hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="323bf-131">Alternativen är: lokal, zon och geo</span><span class="sxs-lookup"><span data-stu-id="323bf-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="323bf-132">-Sortering</span><span class="sxs-lookup"><span data-stu-id="323bf-132">-Collation</span></span>
<span data-ttu-id="323bf-133">Sortering av den SQL-hanterade instans som du kan använda.</span><span class="sxs-lookup"><span data-stu-id="323bf-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="323bf-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="323bf-134">-ComputeGeneration</span></span>
<span data-ttu-id="323bf-135">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="323bf-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="323bf-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323bf-136">-DefaultProfile</span></span>
<span data-ttu-id="323bf-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="323bf-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="323bf-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="323bf-138">-DnsZonePartner</span></span>
<span data-ttu-id="323bf-139">Resurs-ID för partner-hanterad server för att ärva egenskapen DnsZone från för skapande av hanterad instans</span><span class="sxs-lookup"><span data-stu-id="323bf-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="323bf-140">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="323bf-140">-Edition</span></span>
<span data-ttu-id="323bf-141">Versionen för instansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="323bf-142">-Force</span><span class="sxs-lookup"><span data-stu-id="323bf-142">-Force</span></span>
<span data-ttu-id="323bf-143">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="323bf-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="323bf-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="323bf-144">-InstancePool</span></span>
<span data-ttu-id="323bf-145">Det överordnade objektet för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="323bf-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="323bf-146">-InstancePoolName</span></span>
<span data-ttu-id="323bf-147">Instans i vilken den här instansen placeras i.</span><span class="sxs-lookup"><span data-stu-id="323bf-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="323bf-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="323bf-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="323bf-149">Resurs-ID för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="323bf-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="323bf-150">-LicenseType</span></span>
<span data-ttu-id="323bf-151">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="323bf-151">Determines which License Type to use.</span></span> <span data-ttu-id="323bf-152">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="323bf-152">Possible values are:</span></span>
- <span data-ttu-id="323bf-153">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="323bf-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="323bf-154">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="323bf-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="323bf-155">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="323bf-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="323bf-156">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="323bf-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="323bf-157">-Plats</span><span class="sxs-lookup"><span data-stu-id="323bf-157">-Location</span></span>
<span data-ttu-id="323bf-158">Den plats där du vill skapa instansen</span><span class="sxs-lookup"><span data-stu-id="323bf-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="323bf-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="323bf-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="323bf-160">ID-konfigurationsfilen för den SQL Azure-hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="323bf-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="323bf-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="323bf-162">Den minsta TLS-version som ska tillämpas för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="323bf-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="323bf-163">-Namn</span><span class="sxs-lookup"><span data-stu-id="323bf-163">-Name</span></span>
<span data-ttu-id="323bf-164">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="323bf-164">Instance name.</span></span>

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

### <span data-ttu-id="323bf-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="323bf-165">-ProxyOverride</span></span>
<span data-ttu-id="323bf-166">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="323bf-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="323bf-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="323bf-168">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="323bf-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="323bf-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="323bf-169">-ResourceGroupName</span></span>
<span data-ttu-id="323bf-170">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="323bf-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="323bf-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="323bf-171">-SkuName</span></span>
<span data-ttu-id="323bf-172">SKU-namnet för instansen, t. ex. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="323bf-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="323bf-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="323bf-173">-StorageSizeInGB</span></span>
<span data-ttu-id="323bf-174">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="323bf-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="323bf-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="323bf-175">-SubnetId</span></span>
<span data-ttu-id="323bf-176">Det Subnet-ID som ska användas för att skapa en instans</span><span class="sxs-lookup"><span data-stu-id="323bf-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="323bf-177">-Tagg</span><span class="sxs-lookup"><span data-stu-id="323bf-177">-Tag</span></span>
<span data-ttu-id="323bf-178">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="323bf-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="323bf-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="323bf-179">-TimezoneId</span></span>
<span data-ttu-id="323bf-180">ID för tids zonen för den instans som ska anges.</span><span class="sxs-lookup"><span data-stu-id="323bf-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="323bf-181">En lista med tids zons-ID: n visas i vyn sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="323bf-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="323bf-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="323bf-182">-VCore</span></span>
<span data-ttu-id="323bf-183">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="323bf-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="323bf-184">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="323bf-184">-Confirm</span></span>
<span data-ttu-id="323bf-185">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="323bf-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="323bf-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="323bf-186">-WhatIf</span></span>
<span data-ttu-id="323bf-187">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="323bf-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="323bf-188">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="323bf-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="323bf-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323bf-189">CommonParameters</span></span>
<span data-ttu-id="323bf-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="323bf-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323bf-191">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="323bf-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323bf-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="323bf-192">INPUTS</span></span>

### <span data-ttu-id="323bf-193">Ingen</span><span class="sxs-lookup"><span data-stu-id="323bf-193">None</span></span>

## <span data-ttu-id="323bf-194">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="323bf-194">OUTPUTS</span></span>

### <span data-ttu-id="323bf-195">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="323bf-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="323bf-196">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="323bf-196">NOTES</span></span>

## <span data-ttu-id="323bf-197">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="323bf-197">RELATED LINKS</span></span>
