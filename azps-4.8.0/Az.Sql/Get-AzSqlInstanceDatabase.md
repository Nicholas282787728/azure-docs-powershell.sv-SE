---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260980"
---
# <span data-ttu-id="fe610-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe610-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="fe610-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe610-102">SYNOPSIS</span></span>
<span data-ttu-id="fe610-103">Returnerar information om Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="fe610-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="fe610-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe610-104">SYNTAX</span></span>

### <span data-ttu-id="fe610-105">GetInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="fe610-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe610-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="fe610-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe610-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="fe610-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe610-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe610-108">DESCRIPTION</span></span>
<span data-ttu-id="fe610-109">Cmdleten **Get-AzSqlInstanceDatabase** hämtar en eller flera Azure SQL-databaser från en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="fe610-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="fe610-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe610-110">EXAMPLES</span></span>

### <span data-ttu-id="fe610-111">Exempel 1: Hämta alla databaser på en instans</span><span class="sxs-lookup"><span data-stu-id="fe610-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
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

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="fe610-112">Det här kommandot får alla databaser från förekomsten managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="fe610-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="fe610-113">Exempel 2: Hämta en databas med namn på en hanterad instans</span><span class="sxs-lookup"><span data-stu-id="fe610-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
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

<span data-ttu-id="fe610-114">Det här kommandot får en databas som heter managedDatabase1 från en instans med namnet managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="fe610-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="fe610-115">Exempel 3: Hämta alla databaser på en instans med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="fe610-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
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

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="fe610-116">Det här kommandot får alla databaser från förekomsten managedInstance1 som börjar med "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="fe610-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="fe610-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe610-117">PARAMETERS</span></span>

### <span data-ttu-id="fe610-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe610-118">-DefaultProfile</span></span>
<span data-ttu-id="fe610-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe610-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe610-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fe610-120">-InstanceName</span></span>
<span data-ttu-id="fe610-121">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="fe610-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe610-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="fe610-122">-InstanceObject</span></span>
<span data-ttu-id="fe610-123">Instans objekt som ska användas för att hämta instans databasen</span><span class="sxs-lookup"><span data-stu-id="fe610-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe610-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="fe610-124">-InstanceResourceId</span></span>
<span data-ttu-id="fe610-125">Resurs-ID för instans objekt som ska visas</span><span class="sxs-lookup"><span data-stu-id="fe610-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe610-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe610-126">-Name</span></span>
<span data-ttu-id="fe610-127">Namnet på den Azure SQL instance-databas som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="fe610-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe610-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe610-128">-ResourceGroupName</span></span>
<span data-ttu-id="fe610-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fe610-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe610-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe610-130">CommonParameters</span></span>
<span data-ttu-id="fe610-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe610-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe610-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe610-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe610-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe610-133">INPUTS</span></span>

### <span data-ttu-id="fe610-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fe610-134">System.String</span></span>

### <span data-ttu-id="fe610-135">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="fe610-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="fe610-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe610-136">OUTPUTS</span></span>

### <span data-ttu-id="fe610-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fe610-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="fe610-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe610-138">NOTES</span></span>

## <span data-ttu-id="fe610-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe610-139">RELATED LINKS</span></span>