---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: ba8229bcddf27a2a14d50efc2cbd32e6e47015c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920389"
---
# <span data-ttu-id="866e4-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="866e4-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="866e4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="866e4-102">SYNOPSIS</span></span>
<span data-ttu-id="866e4-103">Hämtar de rekommenderade informations typerna och känslighets etiketterna för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="866e4-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="866e4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="866e4-104">SYNTAX</span></span>

### <span data-ttu-id="866e4-105">DatabaseObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="866e4-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="866e4-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="866e4-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866e4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="866e4-107">DESCRIPTION</span></span>
<span data-ttu-id="866e4-108">Get-AzSqlDatabaseSensitivityRecommendation cmdlet returnerar de rekommenderade informations typerna och känslighets etiketterna för kolumnerna i databasen.</span><span class="sxs-lookup"><span data-stu-id="866e4-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="866e4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="866e4-109">EXAMPLES</span></span>

### <span data-ttu-id="866e4-110">Exempel 1: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="866e4-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="866e4-111">Exempel 2: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-databas med rör.</span><span class="sxs-lookup"><span data-stu-id="866e4-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

## <span data-ttu-id="866e4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="866e4-112">PARAMETERS</span></span>

### <span data-ttu-id="866e4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="866e4-113">-AsJob</span></span>
<span data-ttu-id="866e4-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="866e4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="866e4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="866e4-115">-DatabaseName</span></span>
<span data-ttu-id="866e4-116">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="866e4-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="866e4-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="866e4-117">-DatabaseObject</span></span>
<span data-ttu-id="866e4-118">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="866e4-118">The SQL database object.</span></span>

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

### <span data-ttu-id="866e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866e4-119">-DefaultProfile</span></span>
<span data-ttu-id="866e4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="866e4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="866e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="866e4-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="866e4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="866e4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="866e4-123">-ServerName</span></span>
<span data-ttu-id="866e4-124">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="866e4-124">SQL server name.</span></span>

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

### <span data-ttu-id="866e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866e4-125">CommonParameters</span></span>
<span data-ttu-id="866e4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866e4-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="866e4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866e4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="866e4-128">INPUTS</span></span>

### <span data-ttu-id="866e4-129">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="866e4-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="866e4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="866e4-130">OUTPUTS</span></span>

### <span data-ttu-id="866e4-131">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="866e4-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="866e4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="866e4-132">NOTES</span></span>

## <span data-ttu-id="866e4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="866e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="866e4-134">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="866e4-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
