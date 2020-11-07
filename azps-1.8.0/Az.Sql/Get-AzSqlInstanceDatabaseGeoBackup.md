---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: 3db29e4ab0f2ab4afc9a3c29ef8ea0335ed5d528
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746699"
---
# <span data-ttu-id="70e8c-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="70e8c-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="70e8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="70e8c-103">Returnerar information om redundant säkerhets kopiering av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="70e8c-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="70e8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70e8c-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70e8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="70e8c-106">Cmdleten **Get-AzSqlInstanceDatabaseGeoBackup** får en eller flera Azure SQL-databaser för redundanta säkerhets kopior från en hanterad Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="70e8c-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="70e8c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="70e8c-108">Exempel 1: Hämta alla överflödiga databas säkerhets kopior till en instans</span><span class="sxs-lookup"><span data-stu-id="70e8c-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="70e8c-109">Det här kommandot får alla överflödiga säkerhets kopior av databasen på instansen managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="70e8c-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="70e8c-110">Exempel 2: skaffa en redundant databas säkerhets kopia efter namn på en hanterad instans</span><span class="sxs-lookup"><span data-stu-id="70e8c-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="70e8c-111">Det här kommandot får en redundant säkerhets kopia av en databas med namnet managedDatabase1 från en instans med namnet managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="70e8c-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="70e8c-112">Exempel 3: Hämta alla överflödiga databas säkerhets kopior till en instans med filter</span><span class="sxs-lookup"><span data-stu-id="70e8c-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="70e8c-113">Det här kommandot får alla överflödiga säkerhets kopior av databasen på instansen managedInstance1 som börjar med "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="70e8c-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="70e8c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70e8c-114">PARAMETERS</span></span>

### <span data-ttu-id="70e8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e8c-115">-DefaultProfile</span></span>
<span data-ttu-id="70e8c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70e8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70e8c-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="70e8c-117">-InstanceName</span></span>
<span data-ttu-id="70e8c-118">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="70e8c-118">The name of the instance.</span></span>

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

### <span data-ttu-id="70e8c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="70e8c-119">-Name</span></span>
<span data-ttu-id="70e8c-120">Namnet på instans databasen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="70e8c-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="70e8c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e8c-121">-ResourceGroupName</span></span>
<span data-ttu-id="70e8c-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70e8c-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e8c-123">CommonParameters</span></span>
<span data-ttu-id="70e8c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e8c-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70e8c-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e8c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70e8c-126">INPUTS</span></span>

### <span data-ttu-id="70e8c-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="70e8c-127">None</span></span>

## <span data-ttu-id="70e8c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70e8c-128">OUTPUTS</span></span>

### <span data-ttu-id="70e8c-129">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="70e8c-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="70e8c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70e8c-130">NOTES</span></span>

## <span data-ttu-id="70e8c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70e8c-131">RELATED LINKS</span></span>