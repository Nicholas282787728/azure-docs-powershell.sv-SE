---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: dcc8d99cdf179ed3e069ef82fe758c4c699054a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756120"
---
# <span data-ttu-id="28cc3-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="28cc3-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="28cc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="28cc3-103">Hämtar en bevarande princip för en tids krävande databas.</span><span class="sxs-lookup"><span data-stu-id="28cc3-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28cc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28cc3-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28cc3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="28cc3-106">Cmdleten **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** hämtar den långsiktiga bevarande principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="28cc3-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="28cc3-107">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="28cc3-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="28cc3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28cc3-108">EXAMPLES</span></span>

### <span data-ttu-id="28cc3-109">Exempel 1: hämta den senaste versionen av princip för bevarande</span><span class="sxs-lookup"><span data-stu-id="28cc3-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="28cc3-110">Med det här kommandot får du den senaste versionen av bevarande principen för lång sikt för database01</span><span class="sxs-lookup"><span data-stu-id="28cc3-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="28cc3-111">Exempel 2: hämta den bakåtkompatibla versionen av principen för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="28cc3-111">Example 2: Get the legacy version of the long term retention policy</span></span>
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

<span data-ttu-id="28cc3-112">Med det här kommandot får du den bakåtkompatibla versionen av den långsiktiga princip inställningen för database01</span><span class="sxs-lookup"><span data-stu-id="28cc3-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="28cc3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28cc3-113">PARAMETERS</span></span>

### <span data-ttu-id="28cc3-114">-Aktuell</span><span class="sxs-lookup"><span data-stu-id="28cc3-114">-Current</span></span>
<span data-ttu-id="28cc3-115">Om det inte anges returnerar kommandot den bakåtkompatibla princip informationen för behållnings perioden.</span><span class="sxs-lookup"><span data-stu-id="28cc3-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="28cc3-116">Annars returnerar kommandot den aktuella versionen av en bevarande princip för längre tid.</span><span class="sxs-lookup"><span data-stu-id="28cc3-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28cc3-117">-DatabaseName</span></span>
<span data-ttu-id="28cc3-118">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="28cc3-118">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cc3-119">-DefaultProfile</span></span>
<span data-ttu-id="28cc3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28cc3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cc3-121">-ResourceGroupName</span></span>
<span data-ttu-id="28cc3-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="28cc3-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28cc3-123">-ServerName</span></span>
<span data-ttu-id="28cc3-124">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="28cc3-124">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28cc3-125">-Confirm</span></span>
<span data-ttu-id="28cc3-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28cc3-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cc3-127">-WhatIf</span></span>
<span data-ttu-id="28cc3-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28cc3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cc3-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28cc3-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cc3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cc3-130">CommonParameters</span></span>
<span data-ttu-id="28cc3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cc3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cc3-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cc3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cc3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28cc3-133">INPUTS</span></span>

### <span data-ttu-id="28cc3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="28cc3-134">System.String</span></span>

## <span data-ttu-id="28cc3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28cc3-135">OUTPUTS</span></span>

### <span data-ttu-id="28cc3-136">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="28cc3-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="28cc3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28cc3-137">NOTES</span></span>

## <span data-ttu-id="28cc3-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28cc3-138">RELATED LINKS</span></span>

[<span data-ttu-id="28cc3-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="28cc3-139">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="28cc3-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="28cc3-140">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="28cc3-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="28cc3-141">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="28cc3-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="28cc3-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
