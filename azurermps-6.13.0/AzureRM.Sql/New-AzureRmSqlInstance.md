---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584867"
---
# <span data-ttu-id="99190-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="99190-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="99190-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99190-102">SYNOPSIS</span></span>
<span data-ttu-id="99190-103">Skapar en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="99190-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99190-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99190-104">SYNTAX</span></span>

### <span data-ttu-id="99190-105">NewByEditionAndComputeGenerationParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="99190-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99190-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="99190-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99190-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99190-107">DESCRIPTION</span></span>
<span data-ttu-id="99190-108">Cmdleten **New-AzureRmSqlInstance** skapar en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="99190-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="99190-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99190-109">EXAMPLES</span></span>

### <span data-ttu-id="99190-110">Exempel 1: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="99190-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="99190-111">Det här kommandot skapar en ny instans med hjälp av parametrarna för Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="99190-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="99190-112">Exempel 2: skapa en ny instans</span><span class="sxs-lookup"><span data-stu-id="99190-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="99190-113">Det här kommandot skapar en ny instans genom att använda parametrarna Edition och ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="99190-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="99190-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99190-114">PARAMETERS</span></span>

### <span data-ttu-id="99190-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="99190-115">-AdministratorCredential</span></span>
<span data-ttu-id="99190-116">Instansens autentiseringsuppgifter för SQL-autentisering.</span><span class="sxs-lookup"><span data-stu-id="99190-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99190-117">-AsJob</span></span>
<span data-ttu-id="99190-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="99190-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="99190-119">-AssignIdentity</span></span>
<span data-ttu-id="99190-120">Skapa och tilldela en Azure Active Directory-identitet för den här hanterade instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="99190-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="99190-121">-ComputeGeneration</span></span>
<span data-ttu-id="99190-122">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="99190-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99190-123">-DefaultProfile</span></span>
<span data-ttu-id="99190-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99190-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99190-125">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="99190-125">-Edition</span></span>
<span data-ttu-id="99190-126">Versionen för instansen.</span><span class="sxs-lookup"><span data-stu-id="99190-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="99190-127">-LicenseType</span></span>
<span data-ttu-id="99190-128">Avgör vilken licens typ av instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="99190-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="99190-129">-Location</span></span>
<span data-ttu-id="99190-130">Den plats där du vill skapa instansen</span><span class="sxs-lookup"><span data-stu-id="99190-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="99190-131">-Name</span></span>
<span data-ttu-id="99190-132">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="99190-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99190-133">-ResourceGroupName</span></span>
<span data-ttu-id="99190-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="99190-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="99190-135">-SkuName</span></span>
<span data-ttu-id="99190-136">SKU-namnet för instansen, t. ex. "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="99190-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="99190-137">-StorageSizeInGB</span></span>
<span data-ttu-id="99190-138">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="99190-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="99190-139">-SubnetId</span></span>
<span data-ttu-id="99190-140">Det Subnet-ID som ska användas för att skapa en instans</span><span class="sxs-lookup"><span data-stu-id="99190-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="99190-141">-Tag</span></span>
<span data-ttu-id="99190-142">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="99190-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="99190-143">-VCore</span></span>
<span data-ttu-id="99190-144">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="99190-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99190-145">-Confirm</span></span>
<span data-ttu-id="99190-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99190-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99190-147">-WhatIf</span></span>
<span data-ttu-id="99190-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99190-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99190-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99190-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99190-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99190-150">CommonParameters</span></span>
<span data-ttu-id="99190-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99190-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99190-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99190-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99190-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99190-153">INPUTS</span></span>

### <span data-ttu-id="99190-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="99190-154">None</span></span>

## <span data-ttu-id="99190-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99190-155">OUTPUTS</span></span>

### <span data-ttu-id="99190-156">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="99190-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="99190-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99190-157">NOTES</span></span>

## <span data-ttu-id="99190-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99190-158">RELATED LINKS</span></span>
