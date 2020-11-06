---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a9389999bdbd93b332a3186ede1003c896552d1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574768"
---
# <span data-ttu-id="a8901-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a8901-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="a8901-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8901-102">SYNOPSIS</span></span>
<span data-ttu-id="a8901-103">Ställer in en server för långsiktig bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="a8901-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8901-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8901-104">SYNTAX</span></span>

### <span data-ttu-id="a8901-105">WeeklyRetentionRequired (standard)</span><span class="sxs-lookup"><span data-stu-id="a8901-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8901-106">Bakåtkompatibla</span><span class="sxs-lookup"><span data-stu-id="a8901-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8901-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="a8901-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8901-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="a8901-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8901-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="a8901-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8901-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8901-110">DESCRIPTION</span></span>
<span data-ttu-id="a8901-111">Cmdleten **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** anger den långsiktiga bevarande princip som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="a8901-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="a8901-112">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="a8901-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="a8901-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8901-113">EXAMPLES</span></span>

### <span data-ttu-id="a8901-114">Exempel 1: Ange vecko kvarhållande för den aktuella versionen av en policy för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="a8901-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


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

<span data-ttu-id="a8901-115">Detta anger den långsiktiga bevarande principen på database01 för att spara varje veckovis fullständig säkerhets kopiering i två veckor</span><span class="sxs-lookup"><span data-stu-id="a8901-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="a8901-116">Exempel 2: Ange månads kvarhållande för den aktuella versionen av en policy för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="a8901-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="a8901-117">Detta anger den långsiktiga bevarande principen på database01 för att spara den första fullständiga säkerhets kopian av varje månad i fem år</span><span class="sxs-lookup"><span data-stu-id="a8901-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="a8901-118">Exempel 3: Ange den årliga bevarande principen för den aktuella versionen av en långsiktig bevarande princip</span><span class="sxs-lookup"><span data-stu-id="a8901-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="a8901-119">Detta anger den långsiktiga bevarande principen för database01 att spara fullständig säkerhets kopiering som gjorts den 26th veckan på året i 10 år</span><span class="sxs-lookup"><span data-stu-id="a8901-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="a8901-120">Exempel 4: Ange varje bevarande för den aktuella versionen av en policy för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="a8901-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="a8901-121">Detta anger den långsiktiga bevarande principen på database01 för att spara varje fullständig säkerhets kopia i 14 dagar, den första fullständiga säkerhets kopian av varje månad i 24 veckor och den fullständiga säkerhets kopian som gjorts den 26th veckan på året i 10 år</span><span class="sxs-lookup"><span data-stu-id="a8901-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="a8901-122">Exempel 4: ta bort den långsiktiga bevarande principen</span><span class="sxs-lookup"><span data-stu-id="a8901-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="a8901-123">Tar bort policyn för database01 så att den inte längre sparar några långsiktiga säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="a8901-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="a8901-124">Detta påverkar inte säkerhets kopior som redan har gjorts</span><span class="sxs-lookup"><span data-stu-id="a8901-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="a8901-125">Exempel 4: ta bort den långsiktiga bevarande principen</span><span class="sxs-lookup"><span data-stu-id="a8901-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="a8901-126">Det här är ett annat sätt att ta bort policyn för database01 så att den inte längre sparar några långsiktiga säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="a8901-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="a8901-127">Detta påverkar inte säkerhets kopior som redan har gjorts</span><span class="sxs-lookup"><span data-stu-id="a8901-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="a8901-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8901-128">PARAMETERS</span></span>

### <span data-ttu-id="a8901-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8901-129">-DatabaseName</span></span>
<span data-ttu-id="a8901-130">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="a8901-130">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="a8901-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8901-131">-DefaultProfile</span></span>
<span data-ttu-id="a8901-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8901-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8901-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="a8901-133">-MonthlyRetention</span></span>
<span data-ttu-id="a8901-134">Månads kvarhållande.</span><span class="sxs-lookup"><span data-stu-id="a8901-134">The Monthly Retention.</span></span>
<span data-ttu-id="a8901-135">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="a8901-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="a8901-136">Det finns en minumum på 7 dagar och högst 10 år.</span><span class="sxs-lookup"><span data-stu-id="a8901-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="a8901-137">-RemovePolicy</span></span>
<span data-ttu-id="a8901-138">Om det anges tas princip för databasen bort.</span><span class="sxs-lookup"><span data-stu-id="a8901-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8901-139">-ResourceGroupName</span></span>
<span data-ttu-id="a8901-140">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a8901-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8901-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8901-141">-ResourceId</span></span>
<span data-ttu-id="a8901-142">Resurs-ID för säkerhets kopiering av princip för lång tids period.</span><span class="sxs-lookup"><span data-stu-id="a8901-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8901-143">-ServerName</span></span>
<span data-ttu-id="a8901-144">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="a8901-144">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="a8901-145">-State</span><span class="sxs-lookup"><span data-stu-id="a8901-145">-State</span></span>
<span data-ttu-id="a8901-146">Tillståndet för säkerhets kopierings principen för långsiktig lagring, "Enabled" eller "Disabled"</span><span class="sxs-lookup"><span data-stu-id="a8901-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="a8901-147">-WeeklyRetention</span></span>
<span data-ttu-id="a8901-148">Vecko kvarhållandet.</span><span class="sxs-lookup"><span data-stu-id="a8901-148">The Weekly Retention.</span></span>
<span data-ttu-id="a8901-149">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="a8901-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="a8901-150">Det finns en minumum på 7 dagar och högst 10 år.</span><span class="sxs-lookup"><span data-stu-id="a8901-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="a8901-151">-WeekOfYear</span></span>
<span data-ttu-id="a8901-152">Veckan på året, 1 till 52, för att spara årligt bevarande.</span><span class="sxs-lookup"><span data-stu-id="a8901-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="a8901-153">-YearlyRetention</span></span>
<span data-ttu-id="a8901-154">Årlig bevarande.</span><span class="sxs-lookup"><span data-stu-id="a8901-154">The Yearly Retention.</span></span>
<span data-ttu-id="a8901-155">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="a8901-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="a8901-156">Det finns en minumum på 7 dagar och högst 10 år.</span><span class="sxs-lookup"><span data-stu-id="a8901-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8901-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8901-157">-Confirm</span></span>
<span data-ttu-id="a8901-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8901-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8901-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8901-159">-WhatIf</span></span>
<span data-ttu-id="a8901-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8901-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8901-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8901-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8901-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8901-162">CommonParameters</span></span>
<span data-ttu-id="a8901-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8901-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8901-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8901-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8901-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8901-165">INPUTS</span></span>

### <span data-ttu-id="a8901-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a8901-166">System.String</span></span>

### <span data-ttu-id="a8901-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a8901-167">System.Int32</span></span>

## <span data-ttu-id="a8901-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8901-168">OUTPUTS</span></span>

### <span data-ttu-id="a8901-169">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a8901-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="a8901-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8901-170">NOTES</span></span>

## <span data-ttu-id="a8901-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8901-171">RELATED LINKS</span></span>

[<span data-ttu-id="a8901-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a8901-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="a8901-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a8901-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a8901-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a8901-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a8901-175">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a8901-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
