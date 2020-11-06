---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0f43956dfa29dac2d7c6ca1869716400b8adad35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581952"
---
# <span data-ttu-id="46b4a-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46b4a-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="46b4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="46b4a-103">Hämtar en bevarande princip för en tids krävande databas.</span><span class="sxs-lookup"><span data-stu-id="46b4a-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46b4a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46b4a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="46b4a-106">Cmdleten **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** hämtar den långsiktiga bevarande principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="46b4a-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="46b4a-107">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="46b4a-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="46b4a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46b4a-108">EXAMPLES</span></span>

### <span data-ttu-id="46b4a-109">Exempel 1: hämta den senaste versionen av princip för bevarande</span><span class="sxs-lookup"><span data-stu-id="46b4a-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="46b4a-110">Med det här kommandot får du den senaste versionen av bevarande principen för lång sikt för database01</span><span class="sxs-lookup"><span data-stu-id="46b4a-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="46b4a-111">Exempel 2: hämta den bakåtkompatibla versionen av principen för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="46b4a-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="46b4a-112">Med det här kommandot får du den bakåtkompatibla versionen av den långsiktiga princip inställningen för database01</span><span class="sxs-lookup"><span data-stu-id="46b4a-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="46b4a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46b4a-113">PARAMETERS</span></span>

### <span data-ttu-id="46b4a-114">-Aktuell</span><span class="sxs-lookup"><span data-stu-id="46b4a-114">-Current</span></span>
<span data-ttu-id="46b4a-115">Om det inte anges returnerar kommandot den bakåtkompatibla princip informationen för behållnings perioden.</span><span class="sxs-lookup"><span data-stu-id="46b4a-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="46b4a-116">Annars returnerar kommandot den aktuella versionen av en bevarande princip för längre tid.</span><span class="sxs-lookup"><span data-stu-id="46b4a-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46b4a-117">-DatabaseName</span></span>
<span data-ttu-id="46b4a-118">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="46b4a-118">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b4a-119">-DefaultProfile</span></span>
<span data-ttu-id="46b4a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46b4a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b4a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b4a-121">-ResourceGroupName</span></span>
<span data-ttu-id="46b4a-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="46b4a-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46b4a-123">-ServerName</span></span>
<span data-ttu-id="46b4a-124">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="46b4a-124">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46b4a-125">-Confirm</span></span>
<span data-ttu-id="46b4a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46b4a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b4a-127">-WhatIf</span></span>
<span data-ttu-id="46b4a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46b4a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b4a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46b4a-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b4a-130">CommonParameters</span></span>
<span data-ttu-id="46b4a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="46b4a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b4a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b4a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46b4a-133">INPUTS</span></span>

### <span data-ttu-id="46b4a-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="46b4a-134">None</span></span>
<span data-ttu-id="46b4a-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="46b4a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46b4a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46b4a-136">OUTPUTS</span></span>

### <span data-ttu-id="46b4a-137">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="46b4a-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="46b4a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46b4a-138">NOTES</span></span>

## <span data-ttu-id="46b4a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46b4a-139">RELATED LINKS</span></span>

[<span data-ttu-id="46b4a-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="46b4a-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="46b4a-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="46b4a-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="46b4a-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46b4a-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="46b4a-143">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="46b4a-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
