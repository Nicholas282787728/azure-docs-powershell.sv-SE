---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582531"
---
# <span data-ttu-id="78a84-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="78a84-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="78a84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78a84-102">SYNOPSIS</span></span>
<span data-ttu-id="78a84-103">Anger egenskaper för en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="78a84-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78a84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78a84-104">SYNTAX</span></span>

### <span data-ttu-id="78a84-105">SetInstanceFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="78a84-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78a84-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="78a84-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78a84-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="78a84-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a84-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78a84-108">DESCRIPTION</span></span>
<span data-ttu-id="78a84-109">Cmdleten **set-AzureRmSqlInstance** ändrar egenskaper för en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="78a84-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="78a84-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78a84-110">EXAMPLES</span></span>

### <span data-ttu-id="78a84-111">Exempel 1: Ange befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore</span><span class="sxs-lookup"><span data-stu-id="78a84-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="78a84-112">Det här kommandot anger en befintlig instans med nya värden för-AdministratorPassword,-LicenseType,-StorageSizeInGB och-VCore</span><span class="sxs-lookup"><span data-stu-id="78a84-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="78a84-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78a84-113">PARAMETERS</span></span>

### <span data-ttu-id="78a84-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="78a84-114">-AdministratorPassword</span></span>
<span data-ttu-id="78a84-115">Det nya administratörs lösen ordet för instansen.</span><span class="sxs-lookup"><span data-stu-id="78a84-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="78a84-116">-AssignIdentity</span></span>
<span data-ttu-id="78a84-117">Skapa och tilldela en Azure Active Directory-identitet för den här instansen för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="78a84-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="78a84-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a84-118">-DefaultProfile</span></span>
<span data-ttu-id="78a84-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78a84-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a84-120">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="78a84-120">-Edition</span></span>
<span data-ttu-id="78a84-121">Den version som ska kopplas till instansen.</span><span class="sxs-lookup"><span data-stu-id="78a84-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-122">-Force</span><span class="sxs-lookup"><span data-stu-id="78a84-122">-Force</span></span>
<span data-ttu-id="78a84-123">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="78a84-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="78a84-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78a84-124">-InputObject</span></span>
<span data-ttu-id="78a84-125">AzureSqlManagedInstanceModel-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="78a84-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="78a84-126">-LicenseType</span></span>
<span data-ttu-id="78a84-127">Avgör vilken licens typ av instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="78a84-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="78a84-128">-Name</span></span>
<span data-ttu-id="78a84-129">Instans namn.</span><span class="sxs-lookup"><span data-stu-id="78a84-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a84-130">-ResourceGroupName</span></span>
<span data-ttu-id="78a84-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="78a84-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78a84-132">-ResourceId</span></span>
<span data-ttu-id="78a84-133">ID för den instans som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="78a84-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="78a84-134">-StorageSizeInGB</span></span>
<span data-ttu-id="78a84-135">Bestämmer hur stor lagrings storlek som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="78a84-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="78a84-136">-Tag</span></span>
<span data-ttu-id="78a84-137">De taggar som ska kopplas till förekomsten.</span><span class="sxs-lookup"><span data-stu-id="78a84-137">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="78a84-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="78a84-138">-VCore</span></span>
<span data-ttu-id="78a84-139">Bestämmer hur många VCore som ska kopplas till en instans</span><span class="sxs-lookup"><span data-stu-id="78a84-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a84-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78a84-140">-Confirm</span></span>
<span data-ttu-id="78a84-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78a84-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a84-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a84-142">-WhatIf</span></span>
<span data-ttu-id="78a84-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78a84-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78a84-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78a84-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a84-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a84-145">CommonParameters</span></span>
<span data-ttu-id="78a84-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a84-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a84-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a84-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a84-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78a84-148">INPUTS</span></span>

### <span data-ttu-id="78a84-149">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="78a84-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="78a84-150">System. String</span><span class="sxs-lookup"><span data-stu-id="78a84-150">System.String</span></span>

## <span data-ttu-id="78a84-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78a84-151">OUTPUTS</span></span>

### <span data-ttu-id="78a84-152">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="78a84-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="78a84-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78a84-153">NOTES</span></span>

## <span data-ttu-id="78a84-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78a84-154">RELATED LINKS</span></span>
