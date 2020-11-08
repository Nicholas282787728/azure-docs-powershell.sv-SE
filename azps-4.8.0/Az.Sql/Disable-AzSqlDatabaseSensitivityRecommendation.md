---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261001"
---
# <span data-ttu-id="ad578-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="ad578-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="ad578-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad578-102">SYNOPSIS</span></span>
<span data-ttu-id="ad578-103">Inaktiverar (missar) känslighets rekommendationer för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="ad578-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="ad578-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad578-104">SYNTAX</span></span>

### <span data-ttu-id="ad578-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ad578-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad578-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad578-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad578-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad578-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad578-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad578-108">DESCRIPTION</span></span>
<span data-ttu-id="ad578-109">Disable-AzSqlDatabaseSensitivityRecommendation cmdlet inaktiverar (missar) känslighets rekommendationer för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="ad578-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="ad578-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad578-110">EXAMPLES</span></span>

### <span data-ttu-id="ad578-111">Exempel 1: inaktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ad578-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="ad578-112">Exempel 2: inaktivera känslighets rekommendationer för kolumner med känslighets rekommendationer i en Azure SQL-databas med dragning.</span><span class="sxs-lookup"><span data-stu-id="ad578-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="ad578-113">Exempel 3: inaktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-databas med hjälp av rör.</span><span class="sxs-lookup"><span data-stu-id="ad578-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="ad578-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad578-114">PARAMETERS</span></span>

### <span data-ttu-id="ad578-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad578-115">-AsJob</span></span>
<span data-ttu-id="ad578-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ad578-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad578-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ad578-117">-ColumnName</span></span>
<span data-ttu-id="ad578-118">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="ad578-118">Name of column.</span></span>

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

### <span data-ttu-id="ad578-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad578-119">-DatabaseName</span></span>
<span data-ttu-id="ad578-120">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ad578-120">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad578-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ad578-121">-DatabaseObject</span></span>
<span data-ttu-id="ad578-122">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ad578-122">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad578-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad578-123">-DefaultProfile</span></span>
<span data-ttu-id="ad578-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad578-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad578-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad578-125">-InputObject</span></span>
<span data-ttu-id="ad578-126">Ett objekt som representerar en känslighets klassificering i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="ad578-126">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad578-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad578-127">-PassThru</span></span>
<span data-ttu-id="ad578-128">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="ad578-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ad578-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad578-129">-ResourceGroupName</span></span>
<span data-ttu-id="ad578-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ad578-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad578-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ad578-131">-SchemaName</span></span>
<span data-ttu-id="ad578-132">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="ad578-132">Name of schema.</span></span>

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

### <span data-ttu-id="ad578-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ad578-133">-ServerName</span></span>
<span data-ttu-id="ad578-134">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="ad578-134">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad578-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="ad578-135">-TableName</span></span>
<span data-ttu-id="ad578-136">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="ad578-136">Name of table.</span></span>

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

### <span data-ttu-id="ad578-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad578-137">-Confirm</span></span>
<span data-ttu-id="ad578-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad578-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad578-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad578-139">-WhatIf</span></span>
<span data-ttu-id="ad578-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad578-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad578-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad578-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad578-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad578-142">CommonParameters</span></span>
<span data-ttu-id="ad578-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad578-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad578-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad578-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad578-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad578-145">INPUTS</span></span>

### <span data-ttu-id="ad578-146">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ad578-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ad578-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad578-147">OUTPUTS</span></span>

### <span data-ttu-id="ad578-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad578-148">System.Boolean</span></span>

## <span data-ttu-id="ad578-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad578-149">NOTES</span></span>

## <span data-ttu-id="ad578-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad578-150">RELATED LINKS</span></span>

[<span data-ttu-id="ad578-151">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="ad578-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)