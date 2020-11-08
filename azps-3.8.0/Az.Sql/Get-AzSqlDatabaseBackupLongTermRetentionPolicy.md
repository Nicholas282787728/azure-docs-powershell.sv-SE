---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089287"
---
# <span data-ttu-id="fe868-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe868-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="fe868-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe868-102">SYNOPSIS</span></span>
<span data-ttu-id="fe868-103">Hämtar en bevarande princip för en tids krävande databas.</span><span class="sxs-lookup"><span data-stu-id="fe868-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="fe868-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe868-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe868-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe868-105">DESCRIPTION</span></span>
<span data-ttu-id="fe868-106">Cmdleten **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** hämtar den långsiktiga bevarande principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="fe868-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="fe868-107">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="fe868-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="fe868-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe868-108">EXAMPLES</span></span>

### <span data-ttu-id="fe868-109">Exempel 1: hämta den senaste versionen av princip för bevarande</span><span class="sxs-lookup"><span data-stu-id="fe868-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


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

<span data-ttu-id="fe868-110">Med det här kommandot får du den senaste versionen av bevarande principen för lång sikt för database01</span><span class="sxs-lookup"><span data-stu-id="fe868-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="fe868-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe868-111">PARAMETERS</span></span>

### <span data-ttu-id="fe868-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe868-112">-DatabaseName</span></span>
<span data-ttu-id="fe868-113">Namnet på den Azure SQL-databas du vill använda.</span><span class="sxs-lookup"><span data-stu-id="fe868-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="fe868-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe868-114">-DefaultProfile</span></span>
<span data-ttu-id="fe868-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe868-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe868-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe868-116">-ResourceGroupName</span></span>
<span data-ttu-id="fe868-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fe868-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe868-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fe868-118">-ServerName</span></span>
<span data-ttu-id="fe868-119">Namnet på den Azure SQL Server-databas som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="fe868-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="fe868-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe868-120">-Confirm</span></span>
<span data-ttu-id="fe868-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe868-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe868-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe868-122">-WhatIf</span></span>
<span data-ttu-id="fe868-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe868-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe868-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe868-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe868-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe868-125">CommonParameters</span></span>
<span data-ttu-id="fe868-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe868-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe868-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe868-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe868-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe868-128">INPUTS</span></span>

### <span data-ttu-id="fe868-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fe868-129">System.String</span></span>

## <span data-ttu-id="fe868-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe868-130">OUTPUTS</span></span>

### <span data-ttu-id="fe868-131">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fe868-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="fe868-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe868-132">NOTES</span></span>

## <span data-ttu-id="fe868-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe868-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe868-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe868-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fe868-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fe868-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fe868-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe868-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fe868-137">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fe868-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)