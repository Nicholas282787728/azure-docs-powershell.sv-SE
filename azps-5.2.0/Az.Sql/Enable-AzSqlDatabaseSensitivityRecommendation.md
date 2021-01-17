---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390141"
---
# <span data-ttu-id="d55b9-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="d55b9-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="d55b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d55b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d55b9-103">Aktiverar känslighets rekommendationer för kolumner (rekommendationer är aktiverade som standard i alla kolumner) i databasen.</span><span class="sxs-lookup"><span data-stu-id="d55b9-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="d55b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d55b9-104">SYNTAX</span></span>

### <span data-ttu-id="d55b9-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d55b9-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55b9-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d55b9-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d55b9-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d55b9-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d55b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d55b9-108">DESCRIPTION</span></span>
<span data-ttu-id="d55b9-109">Med cmdleten Enable-AzSqlDatabaseSensitivityRecommendation kan du aktivera känslighets rekommendationer för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="d55b9-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="d55b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d55b9-110">EXAMPLES</span></span>

### <span data-ttu-id="d55b9-111">Exempel 1: Aktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d55b9-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="d55b9-112">Exempel 2: Aktivera känslighets rekommendationer för en viss kolumn Azure SQL-databas med ledning.</span><span class="sxs-lookup"><span data-stu-id="d55b9-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="d55b9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d55b9-113">PARAMETERS</span></span>

### <span data-ttu-id="d55b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d55b9-114">-AsJob</span></span>
<span data-ttu-id="d55b9-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d55b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d55b9-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="d55b9-116">-ColumnName</span></span>
<span data-ttu-id="d55b9-117">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="d55b9-117">Name of column.</span></span>

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

### <span data-ttu-id="d55b9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d55b9-118">-DatabaseName</span></span>
<span data-ttu-id="d55b9-119">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d55b9-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="d55b9-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d55b9-120">-DatabaseObject</span></span>
<span data-ttu-id="d55b9-121">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="d55b9-121">The SQL database object.</span></span>

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

### <span data-ttu-id="d55b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55b9-122">-DefaultProfile</span></span>
<span data-ttu-id="d55b9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d55b9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d55b9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d55b9-124">-InputObject</span></span>
<span data-ttu-id="d55b9-125">Ett objekt som representerar en känslighets klassificering i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d55b9-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="d55b9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d55b9-126">-PassThru</span></span>
<span data-ttu-id="d55b9-127">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="d55b9-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="d55b9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d55b9-128">-ResourceGroupName</span></span>
<span data-ttu-id="d55b9-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d55b9-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="d55b9-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d55b9-130">-SchemaName</span></span>
<span data-ttu-id="d55b9-131">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="d55b9-131">Name of schema.</span></span>

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

### <span data-ttu-id="d55b9-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d55b9-132">-ServerName</span></span>
<span data-ttu-id="d55b9-133">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="d55b9-133">SQL server name.</span></span>

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

### <span data-ttu-id="d55b9-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="d55b9-134">-TableName</span></span>
<span data-ttu-id="d55b9-135">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="d55b9-135">Name of table.</span></span>

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

### <span data-ttu-id="d55b9-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d55b9-136">-Confirm</span></span>
<span data-ttu-id="d55b9-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d55b9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d55b9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55b9-138">-WhatIf</span></span>
<span data-ttu-id="d55b9-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d55b9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d55b9-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d55b9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d55b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55b9-141">CommonParameters</span></span>
<span data-ttu-id="d55b9-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55b9-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d55b9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55b9-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d55b9-144">INPUTS</span></span>

### <span data-ttu-id="d55b9-145">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="d55b9-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="d55b9-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d55b9-146">OUTPUTS</span></span>

### <span data-ttu-id="d55b9-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d55b9-147">System.Boolean</span></span>

## <span data-ttu-id="d55b9-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d55b9-148">NOTES</span></span>

## <span data-ttu-id="d55b9-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d55b9-149">RELATED LINKS</span></span>

[<span data-ttu-id="d55b9-150">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="d55b9-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)