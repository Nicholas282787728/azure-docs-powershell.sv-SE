---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261617"
---
# <span data-ttu-id="66b3f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="66b3f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="66b3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b3f-103">Anger en säkerhets kopierings princip för kortvarigt bevarande.</span><span class="sxs-lookup"><span data-stu-id="66b3f-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="66b3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66b3f-104">SYNTAX</span></span>

### <span data-ttu-id="66b3f-105">PolicyByResourceServerDatabaseSet (standard)</span><span class="sxs-lookup"><span data-stu-id="66b3f-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b3f-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66b3f-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b3f-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="66b3f-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b3f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66b3f-108">DESCRIPTION</span></span>
<span data-ttu-id="66b3f-109">Cmdleten **set-AzSqlDatabaseBackupShortTermRetentionPolicy** hämtar den kortsiktiga bevarande principen som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="66b3f-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="66b3f-110">Policyn är den bevarande period, i dagar, för säkerhets kopior för återställning vid tillfället.</span><span class="sxs-lookup"><span data-stu-id="66b3f-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="66b3f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66b3f-111">EXAMPLES</span></span>

### <span data-ttu-id="66b3f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66b3f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="66b3f-113">Det här kommandot anger den kortsiktiga bevarande principen för database01 till 35 dagar.</span><span class="sxs-lookup"><span data-stu-id="66b3f-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="66b3f-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="66b3f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="66b3f-115">Det här kommandot anger den kortsiktiga bevarande principen för database01 till 35 dagar via överföring i ett databas objekt.</span><span class="sxs-lookup"><span data-stu-id="66b3f-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="66b3f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66b3f-116">PARAMETERS</span></span>

### <span data-ttu-id="66b3f-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="66b3f-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="66b3f-118">Databasobjektet för att hämta policyn för.</span><span class="sxs-lookup"><span data-stu-id="66b3f-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="66b3f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66b3f-119">-DatabaseName</span></span>
<span data-ttu-id="66b3f-120">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="66b3f-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="66b3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b3f-121">-DefaultProfile</span></span>
<span data-ttu-id="66b3f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66b3f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66b3f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b3f-123">-ResourceGroupName</span></span>
<span data-ttu-id="66b3f-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="66b3f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="66b3f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66b3f-125">-ResourceId</span></span>
<span data-ttu-id="66b3f-126">Den kortsiktiga resurs-ID för bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="66b3f-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="66b3f-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="66b3f-127">-RetentionDays</span></span>
<span data-ttu-id="66b3f-128">Inställningen för lagring av säkerhets kopior i dagar.</span><span class="sxs-lookup"><span data-stu-id="66b3f-128">The backup retention setting, in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b3f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66b3f-129">-ServerName</span></span>
<span data-ttu-id="66b3f-130">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="66b3f-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="66b3f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66b3f-131">-Confirm</span></span>
<span data-ttu-id="66b3f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66b3f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b3f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b3f-133">-WhatIf</span></span>
<span data-ttu-id="66b3f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66b3f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b3f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66b3f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b3f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b3f-136">CommonParameters</span></span>
<span data-ttu-id="66b3f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b3f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b3f-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66b3f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b3f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66b3f-139">INPUTS</span></span>

### <span data-ttu-id="66b3f-140">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="66b3f-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="66b3f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="66b3f-141">System.String</span></span>

## <span data-ttu-id="66b3f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66b3f-142">OUTPUTS</span></span>

### <span data-ttu-id="66b3f-143">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="66b3f-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="66b3f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66b3f-144">NOTES</span></span>

## <span data-ttu-id="66b3f-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66b3f-145">RELATED LINKS</span></span>