---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746617"
---
# <span data-ttu-id="8d5e0-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d5e0-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="8d5e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5e0-103">Skapar en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="8d5e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d5e0-104">SYNTAX</span></span>

### <span data-ttu-id="8d5e0-105">NewByEditionAndComputeGenerationParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8d5e0-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d5e0-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="8d5e0-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d5e0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d5e0-107">DESCRIPTION</span></span>
<span data-ttu-id="8d5e0-108">Cmdleten **New-AzSqlInstance** skapar en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="8d5e0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d5e0-109">EXAMPLES</span></span>

### <span data-ttu-id="8d5e0-110">Exempel 1: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="8d5e0-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="8d5e0-111">Det här kommandot skapar en ny instans med hjälp av parametrarna för Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="8d5e0-112">Exempel 2: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="8d5e0-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="8d5e0-113">Det här kommandot skapar en ny instans genom att använda parametrarna Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="8d5e0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d5e0-114">PARAMETERS</span></span>

### <span data-ttu-id="8d5e0-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="8d5e0-115">-AdministratorCredential</span></span>
<span data-ttu-id="8d5e0-116">Instansens autentiseringsuppgifter för SQL-autentisering.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="8d5e0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d5e0-117">-AsJob</span></span>
<span data-ttu-id="8d5e0-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8d5e0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d5e0-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8d5e0-119">-AssignIdentity</span></span>
<span data-ttu-id="8d5e0-120">Skapa och tilldela en Azure Active Directory-identitet för den här hanterade instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8d5e0-121">-Sortering</span><span class="sxs-lookup"><span data-stu-id="8d5e0-121">-Collation</span></span>
<span data-ttu-id="8d5e0-122">Sortering av den SQL-hanterade instans som du kan använda.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="8d5e0-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8d5e0-123">-ComputeGeneration</span></span>
<span data-ttu-id="8d5e0-124">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="8d5e0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5e0-125">-DefaultProfile</span></span>
<span data-ttu-id="8d5e0-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5e0-127">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="8d5e0-127">-Edition</span></span>
<span data-ttu-id="8d5e0-128">Versionen för instansen.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="8d5e0-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8d5e0-129">-LicenseType</span></span>
<span data-ttu-id="8d5e0-130">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-130">Determines which License Type to use.</span></span> <span data-ttu-id="8d5e0-131">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="8d5e0-131">Possible values are:</span></span>
- <span data-ttu-id="8d5e0-132">BasePrice – Azure Hybrid förmån (AHB) rabatterat pris för befintliga SQL Server-licensserver-licenser tillämpas.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="8d5e0-133">Det bevarade instans tjänst priset för de befintliga licens ägarna för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="8d5e0-134">LicenseIncluded – Azure Hybrid förmån (AHB) rabatt på de befintliga licens ägarna för SQL Server används inte.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="8d5e0-135">Det bevarade instans tjänst priset inkluderar en ny licens kostnad för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e0-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="8d5e0-136">-Location</span></span>
<span data-ttu-id="8d5e0-137">Den plats där du vill skapa instansen</span><span class="sxs-lookup"><span data-stu-id="8d5e0-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e0-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d5e0-138">-Name</span></span>
<span data-ttu-id="8d5e0-139">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-139">Instance name.</span></span>

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

### <span data-ttu-id="8d5e0-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="8d5e0-140">-ProxyOverride</span></span>
<span data-ttu-id="8d5e0-141">Den Anslutnings typ som används för att ansluta till instansen.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="8d5e0-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="8d5e0-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="8d5e0-143">Om den offentliga data slut punkten är aktive rad för instansen.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="8d5e0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5e0-144">-ResourceGroupName</span></span>
<span data-ttu-id="8d5e0-145">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e0-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8d5e0-146">-SkuName</span></span>
<span data-ttu-id="8d5e0-147">SKU-namnet för instansen, t. ex. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="8d5e0-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="8d5e0-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8d5e0-148">-StorageSizeInGB</span></span>
<span data-ttu-id="8d5e0-149">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="8d5e0-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="8d5e0-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8d5e0-150">-SubnetId</span></span>
<span data-ttu-id="8d5e0-151">Det Subnet-ID som ska användas för att skapa en instans</span><span class="sxs-lookup"><span data-stu-id="8d5e0-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e0-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8d5e0-152">-Tag</span></span>
<span data-ttu-id="8d5e0-153">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="8d5e0-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="8d5e0-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="8d5e0-154">-TimezoneId</span></span>
<span data-ttu-id="8d5e0-155">ID för tids zonen för den instans som ska anges.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="8d5e0-156">En lista med tids zons-ID: n visas i vyn sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="8d5e0-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="8d5e0-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="8d5e0-157">-VCore</span></span>
<span data-ttu-id="8d5e0-158">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="8d5e0-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="8d5e0-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d5e0-159">-Confirm</span></span>
<span data-ttu-id="8d5e0-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5e0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5e0-161">-WhatIf</span></span>
<span data-ttu-id="8d5e0-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5e0-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5e0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5e0-164">CommonParameters</span></span>
<span data-ttu-id="8d5e0-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5e0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5e0-166">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d5e0-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5e0-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d5e0-167">INPUTS</span></span>

### <span data-ttu-id="8d5e0-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="8d5e0-168">None</span></span>

## <span data-ttu-id="8d5e0-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d5e0-169">OUTPUTS</span></span>

### <span data-ttu-id="8d5e0-170">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8d5e0-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="8d5e0-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d5e0-171">NOTES</span></span>

## <span data-ttu-id="8d5e0-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d5e0-172">RELATED LINKS</span></span>
