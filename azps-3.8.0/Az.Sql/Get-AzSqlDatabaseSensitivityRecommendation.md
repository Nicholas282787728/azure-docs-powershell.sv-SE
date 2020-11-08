---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089347"
---
# <span data-ttu-id="ea5b5-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea5b5-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="ea5b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5b5-103">Hämtar de rekommenderade informations typerna och känslighets etiketterna för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="ea5b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea5b5-104">SYNTAX</span></span>

### <span data-ttu-id="ea5b5-105">DatabaseObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ea5b5-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea5b5-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5b5-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea5b5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea5b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ea5b5-108">Get-AzSqlDatabaseSensitivityRecommendation cmdlet returnerar de rekommenderade informations typerna och känslighets etiketterna för kolumnerna i databasen.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="ea5b5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea5b5-109">EXAMPLES</span></span>

### <span data-ttu-id="ea5b5-110">Exempel 1: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

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

### <span data-ttu-id="ea5b5-111">Exempel 2: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-databas med rör.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

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

## <span data-ttu-id="ea5b5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea5b5-112">PARAMETERS</span></span>

### <span data-ttu-id="ea5b5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea5b5-113">-AsJob</span></span>
<span data-ttu-id="ea5b5-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ea5b5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea5b5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea5b5-115">-DatabaseName</span></span>
<span data-ttu-id="ea5b5-116">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5b5-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ea5b5-117">-DatabaseObject</span></span>
<span data-ttu-id="ea5b5-118">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5b5-119">-DefaultProfile</span></span>
<span data-ttu-id="ea5b5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea5b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea5b5-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5b5-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea5b5-123">-ServerName</span></span>
<span data-ttu-id="ea5b5-124">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5b5-125">CommonParameters</span></span>
<span data-ttu-id="ea5b5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5b5-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea5b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5b5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea5b5-128">INPUTS</span></span>

### <span data-ttu-id="ea5b5-129">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ea5b5-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ea5b5-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea5b5-130">OUTPUTS</span></span>

### <span data-ttu-id="ea5b5-131">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ea5b5-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ea5b5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea5b5-132">NOTES</span></span>

## <span data-ttu-id="ea5b5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea5b5-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea5b5-134">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="ea5b5-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)