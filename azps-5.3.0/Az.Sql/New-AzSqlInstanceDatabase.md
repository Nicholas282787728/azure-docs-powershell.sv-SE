---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522243"
---
# <span data-ttu-id="3c328-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3c328-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="3c328-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c328-102">SYNOPSIS</span></span>
<span data-ttu-id="3c328-103">Skapar en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="3c328-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="3c328-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c328-104">SYNTAX</span></span>

### <span data-ttu-id="3c328-105">CreateNewInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="3c328-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c328-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="3c328-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c328-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="3c328-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c328-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c328-108">DESCRIPTION</span></span>
<span data-ttu-id="3c328-109">Cmdleten **New-AzSqlInstanceDatabase** skapar en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="3c328-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="3c328-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c328-110">EXAMPLES</span></span>

### <span data-ttu-id="3c328-111">Exempel 1: skapa en databas på en angiven instans</span><span class="sxs-lookup"><span data-stu-id="3c328-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="3c328-112">Det här kommandot skapar en instans databas med namnet Database01 på instance managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="3c328-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="3c328-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c328-113">PARAMETERS</span></span>

### <span data-ttu-id="3c328-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c328-114">-AsJob</span></span>
<span data-ttu-id="3c328-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3c328-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c328-116">-Sortering</span><span class="sxs-lookup"><span data-stu-id="3c328-116">-Collation</span></span>
<span data-ttu-id="3c328-117">Sorteringen av databas sortering för Azure SQL-instans.</span><span class="sxs-lookup"><span data-stu-id="3c328-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="3c328-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c328-118">-DefaultProfile</span></span>
<span data-ttu-id="3c328-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c328-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c328-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3c328-120">-InstanceName</span></span>
<span data-ttu-id="3c328-121">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="3c328-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c328-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="3c328-122">-InstanceObject</span></span>
<span data-ttu-id="3c328-123">Instans objekt</span><span class="sxs-lookup"><span data-stu-id="3c328-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c328-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="3c328-124">-InstanceResourceId</span></span>
<span data-ttu-id="3c328-125">Instans resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3c328-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c328-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c328-126">-Name</span></span>
<span data-ttu-id="3c328-127">Namnet på den Azure SQL instance-databas som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3c328-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c328-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c328-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c328-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3c328-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c328-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3c328-130">-Tag</span></span>
<span data-ttu-id="3c328-131">De taggar som ska kopplas till Azure SQL instance-databasen</span><span class="sxs-lookup"><span data-stu-id="3c328-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="3c328-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c328-132">-Confirm</span></span>
<span data-ttu-id="3c328-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c328-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c328-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c328-134">-WhatIf</span></span>
<span data-ttu-id="3c328-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c328-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c328-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c328-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c328-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c328-137">CommonParameters</span></span>
<span data-ttu-id="3c328-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c328-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c328-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c328-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c328-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c328-140">INPUTS</span></span>

### <span data-ttu-id="3c328-141">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3c328-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="3c328-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3c328-142">System.String</span></span>

## <span data-ttu-id="3c328-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c328-143">OUTPUTS</span></span>

### <span data-ttu-id="3c328-144">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3c328-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3c328-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c328-145">NOTES</span></span>

## <span data-ttu-id="3c328-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c328-146">RELATED LINKS</span></span>
