---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259024"
---
# <span data-ttu-id="e6692-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="e6692-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="e6692-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6692-102">SYNOPSIS</span></span>
<span data-ttu-id="e6692-103">Anger etiketterna för informations typer och känslighet för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="e6692-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="e6692-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6692-104">SYNTAX</span></span>

### <span data-ttu-id="e6692-105">ClassificationObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e6692-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6692-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6692-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6692-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6692-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6692-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6692-108">DESCRIPTION</span></span>
<span data-ttu-id="e6692-109">I Set-AzSqlDatabaseSensitivityClassification cmdlet anges etiketterna för informations typer och känslighet för kolumner i databasen.</span><span class="sxs-lookup"><span data-stu-id="e6692-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="e6692-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6692-110">EXAMPLES</span></span>

### <span data-ttu-id="e6692-111">Exempel 1: Ange informations typ och känslighets etikett för en kolumn i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e6692-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="e6692-112">Exempel 2: Ange rekommenderade informations typer och känslighets etiketter för kolumner i en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e6692-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="e6692-113">Exempel 3: Ange informations typ och känslighets etikett för en kolumn i en Azure SQL-databas, med dragning.</span><span class="sxs-lookup"><span data-stu-id="e6692-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="e6692-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6692-114">PARAMETERS</span></span>

### <span data-ttu-id="e6692-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6692-115">-AsJob</span></span>
<span data-ttu-id="e6692-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e6692-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6692-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="e6692-117">-ClassificationObject</span></span>
<span data-ttu-id="e6692-118">Ett objekt som representerar en känslighets klassificering i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e6692-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e6692-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e6692-119">-ColumnName</span></span>
<span data-ttu-id="e6692-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="e6692-120">Name of column.</span></span>

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

### <span data-ttu-id="e6692-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6692-121">-DatabaseName</span></span>
<span data-ttu-id="e6692-122">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e6692-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="e6692-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e6692-123">-DatabaseObject</span></span>
<span data-ttu-id="e6692-124">Objektet SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e6692-124">The SQL database object.</span></span>

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

### <span data-ttu-id="e6692-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6692-125">-DefaultProfile</span></span>
<span data-ttu-id="e6692-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6692-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6692-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="e6692-127">-InformationType</span></span>
<span data-ttu-id="e6692-128">Ett namn som beskriver informations typen för de data som lagras i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="e6692-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6692-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6692-129">-PassThru</span></span>
<span data-ttu-id="e6692-130">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="e6692-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e6692-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6692-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6692-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e6692-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6692-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e6692-133">-SchemaName</span></span>
<span data-ttu-id="e6692-134">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="e6692-134">Name of schema.</span></span>

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

### <span data-ttu-id="e6692-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="e6692-135">-SensitivityLabel</span></span>
<span data-ttu-id="e6692-136">Ett namn som beskriver känsligheten för de data som lagras i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="e6692-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6692-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6692-137">-ServerName</span></span>
<span data-ttu-id="e6692-138">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="e6692-138">SQL server name.</span></span>

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

### <span data-ttu-id="e6692-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="e6692-139">-TableName</span></span>
<span data-ttu-id="e6692-140">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="e6692-140">Name of table.</span></span>

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

### <span data-ttu-id="e6692-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6692-141">-Confirm</span></span>
<span data-ttu-id="e6692-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6692-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6692-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6692-143">-WhatIf</span></span>
<span data-ttu-id="e6692-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6692-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6692-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6692-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6692-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6692-146">CommonParameters</span></span>
<span data-ttu-id="e6692-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6692-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6692-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6692-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6692-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6692-149">INPUTS</span></span>

### <span data-ttu-id="e6692-150">Microsoft. Azure. commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e6692-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e6692-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6692-151">OUTPUTS</span></span>

### <span data-ttu-id="e6692-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6692-152">System.Boolean</span></span>

## <span data-ttu-id="e6692-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6692-153">NOTES</span></span>

## <span data-ttu-id="e6692-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6692-154">RELATED LINKS</span></span>

[<span data-ttu-id="e6692-155">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="e6692-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)