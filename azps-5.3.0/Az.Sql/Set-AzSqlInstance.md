---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522967"
---
# <span data-ttu-id="817e7-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="817e7-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="817e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="817e7-102">SYNOPSIS</span></span>
<span data-ttu-id="817e7-103">Anger egenskaper för en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="817e7-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="817e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="817e7-104">SYNTAX</span></span>

### <span data-ttu-id="817e7-105">SetInstanceFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="817e7-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="817e7-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="817e7-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="817e7-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="817e7-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817e7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="817e7-108">DESCRIPTION</span></span>
<span data-ttu-id="817e7-109">Cmdleten **set-AzSqlInstance** ändrar egenskaper för en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="817e7-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="817e7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="817e7-110">EXAMPLES</span></span>

### <span data-ttu-id="817e7-111">Exempel 1: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore och-Edition</span><span class="sxs-lookup"><span data-stu-id="817e7-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="817e7-112">Exempel 2: ändra befintlig instans maskin varu generation med nytt värde för-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="817e7-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="817e7-113">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore</span><span class="sxs-lookup"><span data-stu-id="817e7-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="817e7-114">Exempel 3: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore för en instans i en instans</span><span class="sxs-lookup"><span data-stu-id="817e7-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="817e7-115">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore för en instans i en instans</span><span class="sxs-lookup"><span data-stu-id="817e7-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="817e7-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="817e7-116">PARAMETERS</span></span>

### <span data-ttu-id="817e7-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="817e7-117">-AdministratorPassword</span></span>
<span data-ttu-id="817e7-118">Det nya administratörs lösen ordet för instansen.</span><span class="sxs-lookup"><span data-stu-id="817e7-118">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="817e7-119">-AsJob</span></span>
<span data-ttu-id="817e7-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="817e7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="817e7-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="817e7-121">-AssignIdentity</span></span>
<span data-ttu-id="817e7-122">Skapa och tilldela en Azure Active Directory-identitet för den här instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="817e7-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="817e7-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="817e7-123">-ComputeGeneration</span></span>
<span data-ttu-id="817e7-124">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="817e7-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="817e7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817e7-125">-DefaultProfile</span></span>
<span data-ttu-id="817e7-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="817e7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="817e7-127">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="817e7-127">-Edition</span></span>
<span data-ttu-id="817e7-128">Den version som ska kopplas till instansen.</span><span class="sxs-lookup"><span data-stu-id="817e7-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="817e7-129">-Force</span><span class="sxs-lookup"><span data-stu-id="817e7-129">-Force</span></span>
<span data-ttu-id="817e7-130">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="817e7-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="817e7-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="817e7-131">-InputObject</span></span>
<span data-ttu-id="817e7-132">AzureSqlManagedInstanceModel-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="817e7-132">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="817e7-133">-InstancePoolName</span></span>
<span data-ttu-id="817e7-134">Instansens Programpoolsnamn.</span><span class="sxs-lookup"><span data-stu-id="817e7-134">The instance pool name.</span></span>

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

### <span data-ttu-id="817e7-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="817e7-135">-LicenseType</span></span>
<span data-ttu-id="817e7-136">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="817e7-136">Determines which License Type to use.</span></span> <span data-ttu-id="817e7-137">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="817e7-137">Possible values are:</span></span>
- <span data-ttu-id="817e7-138">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="817e7-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="817e7-139">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="817e7-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="817e7-140">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="817e7-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="817e7-141">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="817e7-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="817e7-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="817e7-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="817e7-143">ID-konfigurationsfilen för den SQL Azure-hanterade instansen.</span><span class="sxs-lookup"><span data-stu-id="817e7-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="817e7-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="817e7-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="817e7-145">Den minsta TLS-version som ska tillämpas för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="817e7-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="817e7-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="817e7-146">-Name</span></span>
<span data-ttu-id="817e7-147">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="817e7-147">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="817e7-148">-ProxyOverride</span></span>
<span data-ttu-id="817e7-149">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="817e7-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="817e7-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="817e7-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="817e7-151">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="817e7-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817e7-152">-ResourceGroupName</span></span>
<span data-ttu-id="817e7-153">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="817e7-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="817e7-154">-ResourceId</span></span>
<span data-ttu-id="817e7-155">ID för den instans som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="817e7-155">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="817e7-156">-StorageSizeInGB</span></span>
<span data-ttu-id="817e7-157">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="817e7-157">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-158">-Tagg</span><span class="sxs-lookup"><span data-stu-id="817e7-158">-Tag</span></span>
<span data-ttu-id="817e7-159">De taggar som ska kopplas till förekomsten.</span><span class="sxs-lookup"><span data-stu-id="817e7-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="817e7-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="817e7-160">-VCore</span></span>
<span data-ttu-id="817e7-161">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="817e7-161">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817e7-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="817e7-162">-Confirm</span></span>
<span data-ttu-id="817e7-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="817e7-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="817e7-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817e7-164">-WhatIf</span></span>
<span data-ttu-id="817e7-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="817e7-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="817e7-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="817e7-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="817e7-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817e7-167">CommonParameters</span></span>
<span data-ttu-id="817e7-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="817e7-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817e7-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="817e7-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817e7-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="817e7-170">INPUTS</span></span>

### <span data-ttu-id="817e7-171">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="817e7-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="817e7-172">System. String</span><span class="sxs-lookup"><span data-stu-id="817e7-172">System.String</span></span>

## <span data-ttu-id="817e7-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="817e7-173">OUTPUTS</span></span>

### <span data-ttu-id="817e7-174">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="817e7-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="817e7-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="817e7-175">NOTES</span></span>

## <span data-ttu-id="817e7-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="817e7-176">RELATED LINKS</span></span>
