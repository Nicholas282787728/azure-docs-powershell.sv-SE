---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092004"
---
# <span data-ttu-id="cb666-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb666-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="cb666-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb666-102">SYNOPSIS</span></span>
<span data-ttu-id="cb666-103">Hämtar en säkerhets kopierings princip för kort tids period.</span><span class="sxs-lookup"><span data-stu-id="cb666-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="cb666-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb666-104">SYNTAX</span></span>

### <span data-ttu-id="cb666-105">PolicyByResourceInstanceDatabaseSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cb666-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb666-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb666-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb666-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb666-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb666-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb666-108">DESCRIPTION</span></span>
<span data-ttu-id="cb666-109">Cmdleten **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** hämtar den korta term lagrings princip som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="cb666-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="cb666-110">Policyn är den bevarande period, i dagar, för säkerhets kopior för återställning vid tillfället.</span><span class="sxs-lookup"><span data-stu-id="cb666-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="cb666-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb666-111">EXAMPLES</span></span>

### <span data-ttu-id="cb666-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cb666-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="cb666-113">Det här kommandot hämtar den kortsiktiga bevarande principen för database01.</span><span class="sxs-lookup"><span data-stu-id="cb666-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="cb666-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cb666-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="cb666-115">Det här kommandot hämtar den kortsiktiga bevarande principen för database01 via överföringarna i ett databas objekt.</span><span class="sxs-lookup"><span data-stu-id="cb666-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="cb666-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="cb666-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="cb666-117">Det här kommandot hämtar den kortsiktiga bevarande principen för alla borttagna databaser med namnet database01 via överföring i ett borttaget databas objekt.</span><span class="sxs-lookup"><span data-stu-id="cb666-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="cb666-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb666-118">PARAMETERS</span></span>

### <span data-ttu-id="cb666-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb666-119">-DatabaseName</span></span>
<span data-ttu-id="cb666-120">Namnet på den Azure SQL instance-databas som du vill hämta säkerhets kopior för.</span><span class="sxs-lookup"><span data-stu-id="cb666-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb666-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb666-121">-DefaultProfile</span></span>
<span data-ttu-id="cb666-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb666-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb666-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="cb666-123">-DeletionDate</span></span>
<span data-ttu-id="cb666-124">Borttagnings datumet för Azure SQL instance-databasen att hämta säkerhets kopior för, med millisekunder precision (till exempel 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="cb666-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb666-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb666-125">-InputObject</span></span>
<span data-ttu-id="cb666-126">Det levande eller borttagna databasobjektet för att hämta eller ange principen.</span><span class="sxs-lookup"><span data-stu-id="cb666-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb666-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cb666-127">-InstanceName</span></span>
<span data-ttu-id="cb666-128">Namnet på den SQL-hanterade instans i Azure som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="cb666-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb666-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb666-129">-ResourceGroupName</span></span>
<span data-ttu-id="cb666-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cb666-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb666-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb666-131">-ResourceId</span></span>
<span data-ttu-id="cb666-132">Den kortsiktiga resurs-ID för bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="cb666-132">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb666-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb666-133">CommonParameters</span></span>
<span data-ttu-id="cb666-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb666-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb666-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb666-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb666-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb666-136">INPUTS</span></span>

### <span data-ttu-id="cb666-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="cb666-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="cb666-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cb666-138">System.String</span></span>

## <span data-ttu-id="cb666-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb666-139">OUTPUTS</span></span>

### <span data-ttu-id="cb666-140">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cb666-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="cb666-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb666-141">NOTES</span></span>

## <span data-ttu-id="cb666-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb666-142">RELATED LINKS</span></span>
