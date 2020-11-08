---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259029"
---
# <span data-ttu-id="a2753-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a2753-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="a2753-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2753-102">SYNOPSIS</span></span>
<span data-ttu-id="a2753-103">Anger egenskaper för en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a2753-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a2753-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2753-104">SYNTAX</span></span>

### <span data-ttu-id="a2753-105">SetInstanceFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="a2753-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2753-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a2753-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2753-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a2753-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2753-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2753-108">DESCRIPTION</span></span>
<span data-ttu-id="a2753-109">Cmdleten **set-AzSqlInstance** ändrar egenskaper för en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a2753-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="a2753-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2753-110">EXAMPLES</span></span>

### <span data-ttu-id="a2753-111">Exempel 1: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore och-Edition</span><span class="sxs-lookup"><span data-stu-id="a2753-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="a2753-112">Exempel 2: ändra befintlig instans maskin varu generation med nytt värde för-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a2753-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="a2753-113">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore</span><span class="sxs-lookup"><span data-stu-id="a2753-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="a2753-114">Exempel 3: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore för en instans i en instans</span><span class="sxs-lookup"><span data-stu-id="a2753-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="a2753-115">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore för en instans i en instans</span><span class="sxs-lookup"><span data-stu-id="a2753-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="a2753-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2753-116">PARAMETERS</span></span>

### <span data-ttu-id="a2753-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="a2753-117">-AdministratorPassword</span></span>
<span data-ttu-id="a2753-118">Det nya administratörs lösen ordet för instansen.</span><span class="sxs-lookup"><span data-stu-id="a2753-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="a2753-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2753-119">-AsJob</span></span>
<span data-ttu-id="a2753-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a2753-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2753-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a2753-121">-AssignIdentity</span></span>
<span data-ttu-id="a2753-122">Skapa och tilldela en Azure Active Directory-identitet för den här instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="a2753-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a2753-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a2753-123">-ComputeGeneration</span></span>
<span data-ttu-id="a2753-124">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="a2753-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="a2753-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2753-125">-DefaultProfile</span></span>
<span data-ttu-id="a2753-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2753-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2753-127">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="a2753-127">-Edition</span></span>
<span data-ttu-id="a2753-128">Den version som ska kopplas till instansen.</span><span class="sxs-lookup"><span data-stu-id="a2753-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="a2753-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a2753-129">-Force</span></span>
<span data-ttu-id="a2753-130">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="a2753-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a2753-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2753-131">-InputObject</span></span>
<span data-ttu-id="a2753-132">AzureSqlManagedInstanceModel-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="a2753-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="a2753-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="a2753-133">-InstancePoolName</span></span>
<span data-ttu-id="a2753-134">Instansens Programpoolsnamn.</span><span class="sxs-lookup"><span data-stu-id="a2753-134">The instance pool name.</span></span>

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

### <span data-ttu-id="a2753-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a2753-135">-LicenseType</span></span>
<span data-ttu-id="a2753-136">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a2753-136">Determines which License Type to use.</span></span> <span data-ttu-id="a2753-137">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="a2753-137">Possible values are:</span></span>
- <span data-ttu-id="a2753-138">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="a2753-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="a2753-139">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2753-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="a2753-140">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="a2753-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="a2753-141">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2753-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="a2753-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a2753-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="a2753-143">Den minsta TLS-version som ska tillämpas för hanterade instanser</span><span class="sxs-lookup"><span data-stu-id="a2753-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="a2753-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2753-144">-Name</span></span>
<span data-ttu-id="a2753-145">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="a2753-145">Instance name.</span></span>

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

### <span data-ttu-id="a2753-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="a2753-146">-ProxyOverride</span></span>
<span data-ttu-id="a2753-147">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="a2753-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="a2753-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="a2753-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="a2753-149">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="a2753-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="a2753-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2753-150">-ResourceGroupName</span></span>
<span data-ttu-id="a2753-151">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a2753-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2753-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2753-152">-ResourceId</span></span>
<span data-ttu-id="a2753-153">ID för den instans som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="a2753-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="a2753-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a2753-154">-StorageSizeInGB</span></span>
<span data-ttu-id="a2753-155">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="a2753-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="a2753-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a2753-156">-Tag</span></span>
<span data-ttu-id="a2753-157">De taggar som ska kopplas till förekomsten.</span><span class="sxs-lookup"><span data-stu-id="a2753-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="a2753-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="a2753-158">-VCore</span></span>
<span data-ttu-id="a2753-159">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="a2753-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="a2753-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2753-160">-Confirm</span></span>
<span data-ttu-id="a2753-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2753-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2753-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2753-162">-WhatIf</span></span>
<span data-ttu-id="a2753-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2753-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2753-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2753-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2753-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2753-165">CommonParameters</span></span>
<span data-ttu-id="a2753-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2753-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2753-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2753-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2753-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2753-168">INPUTS</span></span>

### <span data-ttu-id="a2753-169">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a2753-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="a2753-170">System. String</span><span class="sxs-lookup"><span data-stu-id="a2753-170">System.String</span></span>

## <span data-ttu-id="a2753-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2753-171">OUTPUTS</span></span>

### <span data-ttu-id="a2753-172">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a2753-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a2753-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2753-173">NOTES</span></span>

## <span data-ttu-id="a2753-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2753-174">RELATED LINKS</span></span>
