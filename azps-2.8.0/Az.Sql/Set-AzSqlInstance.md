---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920497"
---
# <span data-ttu-id="ec77c-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ec77c-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="ec77c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec77c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec77c-103">Anger egenskaper för en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ec77c-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ec77c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec77c-104">SYNTAX</span></span>

### <span data-ttu-id="ec77c-105">SetInstanceFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="ec77c-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec77c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ec77c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec77c-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ec77c-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec77c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec77c-108">DESCRIPTION</span></span>
<span data-ttu-id="ec77c-109">Cmdleten **set-AzSqlInstance** ändrar egenskaper för en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ec77c-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="ec77c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec77c-110">EXAMPLES</span></span>

### <span data-ttu-id="ec77c-111">Exempel 1: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore</span><span class="sxs-lookup"><span data-stu-id="ec77c-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="ec77c-112">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore</span><span class="sxs-lookup"><span data-stu-id="ec77c-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="ec77c-113">Exempel 2: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore för en instans i en instans</span><span class="sxs-lookup"><span data-stu-id="ec77c-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="ec77c-114">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore för en instans i en instans</span><span class="sxs-lookup"><span data-stu-id="ec77c-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="ec77c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec77c-115">PARAMETERS</span></span>

### <span data-ttu-id="ec77c-116">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="ec77c-116">-AdministratorPassword</span></span>
<span data-ttu-id="ec77c-117">Det nya administratörs lösen ordet för instansen.</span><span class="sxs-lookup"><span data-stu-id="ec77c-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="ec77c-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ec77c-118">-AssignIdentity</span></span>
<span data-ttu-id="ec77c-119">Skapa och tilldela en Azure Active Directory-identitet för den här instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="ec77c-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ec77c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec77c-120">-DefaultProfile</span></span>
<span data-ttu-id="ec77c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec77c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec77c-122">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="ec77c-122">-Edition</span></span>
<span data-ttu-id="ec77c-123">Den version som ska kopplas till instansen.</span><span class="sxs-lookup"><span data-stu-id="ec77c-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="ec77c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ec77c-124">-Force</span></span>
<span data-ttu-id="ec77c-125">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="ec77c-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ec77c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec77c-126">-InputObject</span></span>
<span data-ttu-id="ec77c-127">AzureSqlManagedInstanceModel-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="ec77c-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="ec77c-128">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="ec77c-128">-InstancePoolName</span></span>
<span data-ttu-id="ec77c-129">Instansens Programpoolsnamn.</span><span class="sxs-lookup"><span data-stu-id="ec77c-129">The instance pool name.</span></span>

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

### <span data-ttu-id="ec77c-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ec77c-130">-LicenseType</span></span>
<span data-ttu-id="ec77c-131">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ec77c-131">Determines which License Type to use.</span></span> <span data-ttu-id="ec77c-132">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="ec77c-132">Possible values are:</span></span>
- <span data-ttu-id="ec77c-133">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="ec77c-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ec77c-134">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec77c-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ec77c-135">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="ec77c-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ec77c-136">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec77c-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="ec77c-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec77c-137">-Name</span></span>
<span data-ttu-id="ec77c-138">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="ec77c-138">Instance name.</span></span>

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

### <span data-ttu-id="ec77c-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="ec77c-139">-ProxyOverride</span></span>
<span data-ttu-id="ec77c-140">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="ec77c-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="ec77c-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="ec77c-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="ec77c-142">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="ec77c-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="ec77c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec77c-143">-ResourceGroupName</span></span>
<span data-ttu-id="ec77c-144">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ec77c-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec77c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec77c-145">-ResourceId</span></span>
<span data-ttu-id="ec77c-146">ID för den instans som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="ec77c-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="ec77c-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ec77c-147">-StorageSizeInGB</span></span>
<span data-ttu-id="ec77c-148">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="ec77c-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="ec77c-149">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ec77c-149">-Tag</span></span>
<span data-ttu-id="ec77c-150">De taggar som ska kopplas till förekomsten.</span><span class="sxs-lookup"><span data-stu-id="ec77c-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="ec77c-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="ec77c-151">-VCore</span></span>
<span data-ttu-id="ec77c-152">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="ec77c-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="ec77c-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ec77c-153">-Confirm</span></span>
<span data-ttu-id="ec77c-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ec77c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec77c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec77c-155">-WhatIf</span></span>
<span data-ttu-id="ec77c-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ec77c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec77c-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ec77c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec77c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec77c-158">CommonParameters</span></span>
<span data-ttu-id="ec77c-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec77c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec77c-160">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec77c-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec77c-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec77c-161">INPUTS</span></span>

### <span data-ttu-id="ec77c-162">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ec77c-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="ec77c-163">System. String</span><span class="sxs-lookup"><span data-stu-id="ec77c-163">System.String</span></span>

## <span data-ttu-id="ec77c-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec77c-164">OUTPUTS</span></span>

### <span data-ttu-id="ec77c-165">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ec77c-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="ec77c-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec77c-166">NOTES</span></span>

## <span data-ttu-id="ec77c-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec77c-167">RELATED LINKS</span></span>
