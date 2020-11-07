---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 94efd633a64bd1437206a00b83d86cf09fc56036
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746766"
---
# <span data-ttu-id="0fd1d-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0fd1d-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="0fd1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd1d-103">Hämtar en säkerhets kopierings princip för kort tids period.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="0fd1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fd1d-104">SYNTAX</span></span>

### <span data-ttu-id="0fd1d-105">PolicyByResourceServerDatabaseSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0fd1d-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fd1d-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0fd1d-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fd1d-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0fd1d-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fd1d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fd1d-108">DESCRIPTION</span></span>
<span data-ttu-id="0fd1d-109">Cmdleten **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** hämtar den korta term lagrings princip som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="0fd1d-110">Policyn är den bevarande period, i dagar, för säkerhets kopior för återställning vid tillfället.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="0fd1d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fd1d-111">EXAMPLES</span></span>

### <span data-ttu-id="0fd1d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fd1d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="0fd1d-113">Det här kommandot hämtar den kortsiktiga bevarande principen för database01.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="0fd1d-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0fd1d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="0fd1d-115">Det här kommandot hämtar den kortsiktiga bevarande principen för database01 via överföringarna i ett databas objekt.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="0fd1d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fd1d-116">PARAMETERS</span></span>

### <span data-ttu-id="0fd1d-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0fd1d-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="0fd1d-118">Databasobjektet för att hämta policyn för.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd1d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0fd1d-119">-DatabaseName</span></span>
<span data-ttu-id="0fd1d-120">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd1d-121">-DefaultProfile</span></span>
<span data-ttu-id="0fd1d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0fd1d-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd1d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fd1d-125">-ResourceId</span></span>
<span data-ttu-id="0fd1d-126">Den kortsiktiga resurs-ID för bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="0fd1d-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0fd1d-127">-ServerName</span></span>
<span data-ttu-id="0fd1d-128">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd1d-129">CommonParameters</span></span>
<span data-ttu-id="0fd1d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd1d-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fd1d-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd1d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fd1d-132">INPUTS</span></span>

### <span data-ttu-id="0fd1d-133">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0fd1d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="0fd1d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd1d-134">System.String</span></span>

## <span data-ttu-id="0fd1d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fd1d-135">OUTPUTS</span></span>

### <span data-ttu-id="0fd1d-136">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0fd1d-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="0fd1d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fd1d-137">NOTES</span></span>

## <span data-ttu-id="0fd1d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fd1d-138">RELATED LINKS</span></span>
