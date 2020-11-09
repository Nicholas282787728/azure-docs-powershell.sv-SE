---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319803"
---
# <span data-ttu-id="cd386-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="cd386-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="cd386-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd386-102">SYNOPSIS</span></span>
<span data-ttu-id="cd386-103">Hämtar de aktuella informations typerna och känslighets etiketterna för kolumnerna i databasen.</span><span class="sxs-lookup"><span data-stu-id="cd386-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="cd386-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd386-104">SYNTAX</span></span>

### <span data-ttu-id="cd386-105">DatabaseObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cd386-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd386-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd386-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd386-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd386-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd386-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd386-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd386-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd386-109">DESCRIPTION</span></span>
<span data-ttu-id="cd386-110">Get-AzSqlDatabaseSensitivityClassification cmdlet returnerar de aktuella informations typerna och känslighets etiketterna för kolumnerna i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="cd386-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="cd386-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd386-111">EXAMPLES</span></span>

### <span data-ttu-id="cd386-112">Exempel 1: hämta aktuella informations typer och känslighets etiketter för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="cd386-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="cd386-113">Exempel 2: hämta aktuella informations typer och känslighets etiketter för en Azure SQL-databas med rör.</span><span class="sxs-lookup"><span data-stu-id="cd386-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="cd386-114">Exempel 3: Hämta aktuell informations typ och känslighets etikett för en viss kolumn i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="cd386-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="cd386-115">Exempel 4: Hämta aktuell informations typ och känslighets etikett för en viss kolumn i en Azure SQL-databas med hjälp av dragningen.</span><span class="sxs-lookup"><span data-stu-id="cd386-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="cd386-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd386-116">PARAMETERS</span></span>

### <span data-ttu-id="cd386-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd386-117">-AsJob</span></span>
<span data-ttu-id="cd386-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cd386-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="cd386-119">-ColumnName</span></span>
<span data-ttu-id="cd386-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="cd386-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd386-121">-DatabaseName</span></span>
<span data-ttu-id="cd386-122">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="cd386-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cd386-123">-DatabaseObject</span></span>
<span data-ttu-id="cd386-124">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="cd386-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd386-125">-DefaultProfile</span></span>
<span data-ttu-id="cd386-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd386-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd386-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd386-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd386-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd386-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cd386-129">-SchemaName</span></span>
<span data-ttu-id="cd386-130">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="cd386-130">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd386-131">-ServerName</span></span>
<span data-ttu-id="cd386-132">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="cd386-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="cd386-133">-TableName</span></span>
<span data-ttu-id="cd386-134">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="cd386-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd386-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd386-135">CommonParameters</span></span>
<span data-ttu-id="cd386-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd386-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd386-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd386-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd386-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd386-138">INPUTS</span></span>

### <span data-ttu-id="cd386-139">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cd386-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cd386-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd386-140">OUTPUTS</span></span>

### <span data-ttu-id="cd386-141">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="cd386-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="cd386-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd386-142">NOTES</span></span>

## <span data-ttu-id="cd386-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd386-143">RELATED LINKS</span></span>

[<span data-ttu-id="cd386-144">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="cd386-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
