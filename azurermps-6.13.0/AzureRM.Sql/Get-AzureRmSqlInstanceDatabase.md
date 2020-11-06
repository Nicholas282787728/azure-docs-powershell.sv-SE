---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576745"
---
# <span data-ttu-id="60ef9-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="60ef9-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="60ef9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="60ef9-103">Returnerar information om Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="60ef9-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ef9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60ef9-104">SYNTAX</span></span>

### <span data-ttu-id="60ef9-105">GetInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="60ef9-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ef9-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="60ef9-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ef9-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="60ef9-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ef9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60ef9-108">DESCRIPTION</span></span>
<span data-ttu-id="60ef9-109">Cmdleten **Get-AzureRmSqlInstanceDatabase** hämtar en eller flera Azure SQL-databaser från en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="60ef9-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="60ef9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60ef9-110">EXAMPLES</span></span>

### <span data-ttu-id="60ef9-111">Exempel 1: Hämta alla databaser på en instans</span><span class="sxs-lookup"><span data-stu-id="60ef9-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="60ef9-112">Det här kommandot får alla databaser från förekomsten managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="60ef9-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="60ef9-113">Exempel 2: Hämta en databas med namn på en hanterad instans</span><span class="sxs-lookup"><span data-stu-id="60ef9-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="60ef9-114">Det här kommandot får en databas som heter managedDatabase1 från en instans med namnet managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="60ef9-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="60ef9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60ef9-115">PARAMETERS</span></span>

### <span data-ttu-id="60ef9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ef9-116">-DefaultProfile</span></span>
<span data-ttu-id="60ef9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60ef9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ef9-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="60ef9-118">-InstanceName</span></span>
<span data-ttu-id="60ef9-119">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="60ef9-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ef9-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="60ef9-120">-InstanceObject</span></span>
<span data-ttu-id="60ef9-121">Instans objekt som ska användas för att hämta instans databasen</span><span class="sxs-lookup"><span data-stu-id="60ef9-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ef9-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="60ef9-122">-InstanceResourceId</span></span>
<span data-ttu-id="60ef9-123">Resurs-ID för instans objekt som ska visas</span><span class="sxs-lookup"><span data-stu-id="60ef9-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60ef9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="60ef9-124">-Name</span></span>
<span data-ttu-id="60ef9-125">Namnet på den Azure SQL instance-databas som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="60ef9-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ef9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ef9-126">-ResourceGroupName</span></span>
<span data-ttu-id="60ef9-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="60ef9-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ef9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ef9-128">CommonParameters</span></span>
<span data-ttu-id="60ef9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ef9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ef9-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ef9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ef9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60ef9-131">INPUTS</span></span>

### <span data-ttu-id="60ef9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="60ef9-132">System.String</span></span>
<span data-ttu-id="60ef9-133">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="60ef9-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="60ef9-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60ef9-134">OUTPUTS</span></span>

### <span data-ttu-id="60ef9-135">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="60ef9-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="60ef9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60ef9-136">NOTES</span></span>

## <span data-ttu-id="60ef9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60ef9-137">RELATED LINKS</span></span>
