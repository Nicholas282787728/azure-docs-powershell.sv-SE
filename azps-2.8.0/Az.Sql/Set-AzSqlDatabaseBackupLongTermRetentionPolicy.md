---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 965fb403789148967c2bbfbe431e350806e12144
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920517"
---
# <span data-ttu-id="20d5a-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="20d5a-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="20d5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="20d5a-103">Ställer in en server för långsiktig bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="20d5a-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="20d5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20d5a-104">SYNTAX</span></span>

### <span data-ttu-id="20d5a-105">WeeklyRetentionRequired (standard)</span><span class="sxs-lookup"><span data-stu-id="20d5a-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20d5a-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="20d5a-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20d5a-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="20d5a-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20d5a-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="20d5a-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20d5a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20d5a-109">DESCRIPTION</span></span>
<span data-ttu-id="20d5a-110">Cmdleten **set-AzSqlDatabaseBackupLongTermRetentionPolicy** anger den långsiktiga bevarande princip som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="20d5a-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="20d5a-111">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="20d5a-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="20d5a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20d5a-112">EXAMPLES</span></span>

### <span data-ttu-id="20d5a-113">Exempel 1: Ange vecko kvarhållande för den aktuella versionen av en policy för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="20d5a-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="20d5a-114">Detta anger den långsiktiga bevarande principen på database01 för att spara varje veckovis fullständig säkerhets kopiering i två veckor</span><span class="sxs-lookup"><span data-stu-id="20d5a-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="20d5a-115">Exempel 2: Ange månads kvarhållande för den aktuella versionen av en policy för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="20d5a-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="20d5a-116">Detta anger den långsiktiga bevarande principen på database01 för att spara den första fullständiga säkerhets kopian av varje månad i fem år</span><span class="sxs-lookup"><span data-stu-id="20d5a-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="20d5a-117">Exempel 3: Ange den årliga bevarande principen för den aktuella versionen av en långsiktig bevarande princip</span><span class="sxs-lookup"><span data-stu-id="20d5a-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="20d5a-118">Detta anger den långsiktiga bevarande principen för database01 att spara fullständig säkerhets kopiering som gjorts den 26th veckan på året i 10 år</span><span class="sxs-lookup"><span data-stu-id="20d5a-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="20d5a-119">Exempel 4: Ange varje bevarande för den aktuella versionen av en policy för långsiktigt bevarande</span><span class="sxs-lookup"><span data-stu-id="20d5a-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="20d5a-120">Detta anger den långsiktiga bevarande principen på database01 för att spara varje fullständig säkerhets kopia i 14 dagar, den första fullständiga säkerhets kopian av varje månad i 24 veckor och den fullständiga säkerhets kopian som gjorts den 26th veckan på året i 10 år</span><span class="sxs-lookup"><span data-stu-id="20d5a-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="20d5a-121">Exempel 4: ta bort den långsiktiga bevarande principen</span><span class="sxs-lookup"><span data-stu-id="20d5a-121">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="20d5a-122">Tar bort policyn för database01 så att den inte längre sparar några långsiktiga säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="20d5a-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="20d5a-123">Detta påverkar inte säkerhets kopior som redan har gjorts</span><span class="sxs-lookup"><span data-stu-id="20d5a-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="20d5a-124">Exempel 4: ta bort den långsiktiga bevarande principen</span><span class="sxs-lookup"><span data-stu-id="20d5a-124">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="20d5a-125">Det här är ett annat sätt att ta bort policyn för database01 så att den inte längre sparar några långsiktiga säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="20d5a-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="20d5a-126">Detta påverkar inte säkerhets kopior som redan har gjorts</span><span class="sxs-lookup"><span data-stu-id="20d5a-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="20d5a-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20d5a-127">PARAMETERS</span></span>

### <span data-ttu-id="20d5a-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="20d5a-128">-DatabaseName</span></span>
<span data-ttu-id="20d5a-129">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="20d5a-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="20d5a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d5a-130">-DefaultProfile</span></span>
<span data-ttu-id="20d5a-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20d5a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20d5a-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="20d5a-132">-MonthlyRetention</span></span>
<span data-ttu-id="20d5a-133">Månads kvarhållande.</span><span class="sxs-lookup"><span data-stu-id="20d5a-133">The Monthly Retention.</span></span>
<span data-ttu-id="20d5a-134">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="20d5a-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="20d5a-135">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="20d5a-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="20d5a-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="20d5a-136">-RemovePolicy</span></span>
<span data-ttu-id="20d5a-137">Om det anges tas princip för databasen bort.</span><span class="sxs-lookup"><span data-stu-id="20d5a-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="20d5a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d5a-138">-ResourceGroupName</span></span>
<span data-ttu-id="20d5a-139">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="20d5a-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="20d5a-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20d5a-140">-ServerName</span></span>
<span data-ttu-id="20d5a-141">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="20d5a-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="20d5a-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="20d5a-142">-WeeklyRetention</span></span>
<span data-ttu-id="20d5a-143">Vecko kvarhållandet.</span><span class="sxs-lookup"><span data-stu-id="20d5a-143">The Weekly Retention.</span></span>
<span data-ttu-id="20d5a-144">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="20d5a-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="20d5a-145">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="20d5a-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="20d5a-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="20d5a-146">-WeekOfYear</span></span>
<span data-ttu-id="20d5a-147">Veckan på året, 1 till 52, för att spara årligt bevarande.</span><span class="sxs-lookup"><span data-stu-id="20d5a-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="20d5a-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="20d5a-148">-YearlyRetention</span></span>
<span data-ttu-id="20d5a-149">Årlig bevarande.</span><span class="sxs-lookup"><span data-stu-id="20d5a-149">The Yearly Retention.</span></span>
<span data-ttu-id="20d5a-150">Om bara ett nummer skickas i stället för en ISO 8601-sträng, antas dagar vara enheter.</span><span class="sxs-lookup"><span data-stu-id="20d5a-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="20d5a-151">Det är minst 7 dagar och högst tio år.</span><span class="sxs-lookup"><span data-stu-id="20d5a-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="20d5a-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20d5a-152">-Confirm</span></span>
<span data-ttu-id="20d5a-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20d5a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d5a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d5a-154">-WhatIf</span></span>
<span data-ttu-id="20d5a-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20d5a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d5a-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20d5a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d5a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d5a-157">CommonParameters</span></span>
<span data-ttu-id="20d5a-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d5a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d5a-159">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20d5a-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d5a-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20d5a-160">INPUTS</span></span>

### <span data-ttu-id="20d5a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="20d5a-161">System.String</span></span>

### <span data-ttu-id="20d5a-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="20d5a-162">System.Int32</span></span>

## <span data-ttu-id="20d5a-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20d5a-163">OUTPUTS</span></span>

### <span data-ttu-id="20d5a-164">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="20d5a-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="20d5a-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20d5a-165">NOTES</span></span>

## <span data-ttu-id="20d5a-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20d5a-166">RELATED LINKS</span></span>

[<span data-ttu-id="20d5a-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="20d5a-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="20d5a-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="20d5a-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="20d5a-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="20d5a-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="20d5a-170">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="20d5a-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)