---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090919"
---
# <span data-ttu-id="18a6b-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="18a6b-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="18a6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="18a6b-103">Tar bort data typerna och känslighets etiketterna för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="18a6b-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="18a6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18a6b-104">SYNTAX</span></span>

### <span data-ttu-id="18a6b-105">ClassificationObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="18a6b-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a6b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a6b-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a6b-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="18a6b-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18a6b-108">DESCRIPTION</span></span>
<span data-ttu-id="18a6b-109">Remove-AzSqlDatabaseSensitivityClassification cmdlet tar bort data typerna och känslighets etiketterna för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="18a6b-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="18a6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18a6b-110">EXAMPLES</span></span>

### <span data-ttu-id="18a6b-111">Exempel 1: ta bort informations typ och känslighets etikett för en kolumn i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="18a6b-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="18a6b-112">Exempel 2: ta bort aktuella informations typer och känslighets etiketter för kolumner i en Azure SQL-databas med hjälp av rör.</span><span class="sxs-lookup"><span data-stu-id="18a6b-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="18a6b-113">Exempel 3: ta bort informations typ och känslighets etikett för en kolumn i en Azure SQL-databas med dragning.</span><span class="sxs-lookup"><span data-stu-id="18a6b-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="18a6b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18a6b-114">PARAMETERS</span></span>

### <span data-ttu-id="18a6b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18a6b-115">-AsJob</span></span>
<span data-ttu-id="18a6b-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18a6b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18a6b-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="18a6b-117">-ClassificationObject</span></span>
<span data-ttu-id="18a6b-118">Ett objekt som representerar en känslighets klassificering i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="18a6b-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a6b-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="18a6b-119">-ColumnName</span></span>
<span data-ttu-id="18a6b-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="18a6b-120">Name of column.</span></span>

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

### <span data-ttu-id="18a6b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18a6b-121">-DatabaseName</span></span>
<span data-ttu-id="18a6b-122">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="18a6b-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="18a6b-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="18a6b-123">-DatabaseObject</span></span>
<span data-ttu-id="18a6b-124">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="18a6b-124">The SQL database object.</span></span>

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

### <span data-ttu-id="18a6b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a6b-125">-DefaultProfile</span></span>
<span data-ttu-id="18a6b-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18a6b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a6b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18a6b-127">-PassThru</span></span>
<span data-ttu-id="18a6b-128">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="18a6b-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="18a6b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a6b-129">-ResourceGroupName</span></span>
<span data-ttu-id="18a6b-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="18a6b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="18a6b-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="18a6b-131">-SchemaName</span></span>
<span data-ttu-id="18a6b-132">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="18a6b-132">Name of schema.</span></span>

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

### <span data-ttu-id="18a6b-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18a6b-133">-ServerName</span></span>
<span data-ttu-id="18a6b-134">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="18a6b-134">SQL server name.</span></span>

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

### <span data-ttu-id="18a6b-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="18a6b-135">-TableName</span></span>
<span data-ttu-id="18a6b-136">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="18a6b-136">Name of table.</span></span>

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

### <span data-ttu-id="18a6b-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18a6b-137">-Confirm</span></span>
<span data-ttu-id="18a6b-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18a6b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a6b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a6b-139">-WhatIf</span></span>
<span data-ttu-id="18a6b-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18a6b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18a6b-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18a6b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a6b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a6b-142">CommonParameters</span></span>
<span data-ttu-id="18a6b-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a6b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a6b-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18a6b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a6b-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18a6b-145">INPUTS</span></span>

### <span data-ttu-id="18a6b-146">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="18a6b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="18a6b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18a6b-147">OUTPUTS</span></span>

### <span data-ttu-id="18a6b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18a6b-148">System.Boolean</span></span>

## <span data-ttu-id="18a6b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18a6b-149">NOTES</span></span>

## <span data-ttu-id="18a6b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18a6b-150">RELATED LINKS</span></span>

[<span data-ttu-id="18a6b-151">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="18a6b-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)