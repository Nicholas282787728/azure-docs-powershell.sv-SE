---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fa187bad03027f1c0dd3e1c38e8b05dfb9257f05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746566"
---
# <span data-ttu-id="9a071-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9a071-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9a071-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a071-102">SYNOPSIS</span></span>
<span data-ttu-id="9a071-103">Tar bort data typerna och känslighets etiketterna för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="9a071-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9a071-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a071-104">SYNTAX</span></span>

### <span data-ttu-id="9a071-105">ClassificationObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9a071-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a071-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a071-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a071-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a071-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a071-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a071-108">DESCRIPTION</span></span>
<span data-ttu-id="9a071-109">Med Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet tas informations typerna och känslighets etiketterna för kolumner i Azure SQL-hanterade instans databasen bort.</span><span class="sxs-lookup"><span data-stu-id="9a071-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9a071-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a071-110">EXAMPLES</span></span>

### <span data-ttu-id="9a071-111">Exempel 1: ta bort informations typ och känslighets etikett för en kolumn i en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="9a071-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9a071-112">Exempel 2: ta bort aktuella informations typer och känslighets etiketter för kolumner i en Azure SQL-hanterad instans-databas med rör.</span><span class="sxs-lookup"><span data-stu-id="9a071-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="9a071-113">Exempel 3: ta bort informations typ och känslighets etikett för en kolumn i en Azure SQL-hanterad instans-databas med rör.</span><span class="sxs-lookup"><span data-stu-id="9a071-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9a071-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a071-114">PARAMETERS</span></span>

### <span data-ttu-id="9a071-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a071-115">-AsJob</span></span>
<span data-ttu-id="9a071-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9a071-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a071-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="9a071-117">-ClassificationObject</span></span>
<span data-ttu-id="9a071-118">Ett objekt som representerar en känslighets klassificering för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="9a071-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a071-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9a071-119">-ColumnName</span></span>
<span data-ttu-id="9a071-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="9a071-120">Name of column.</span></span>

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

### <span data-ttu-id="9a071-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a071-121">-DatabaseName</span></span>
<span data-ttu-id="9a071-122">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="9a071-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="9a071-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9a071-123">-DatabaseObject</span></span>
<span data-ttu-id="9a071-124">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a071-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a071-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a071-125">-DefaultProfile</span></span>
<span data-ttu-id="9a071-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a071-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a071-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9a071-127">-InstanceName</span></span>
<span data-ttu-id="9a071-128">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="9a071-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="9a071-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a071-129">-PassThru</span></span>
<span data-ttu-id="9a071-130">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="9a071-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9a071-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a071-131">-ResourceGroupName</span></span>
<span data-ttu-id="9a071-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9a071-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a071-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9a071-133">-SchemaName</span></span>
<span data-ttu-id="9a071-134">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="9a071-134">Name of schema.</span></span>

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

### <span data-ttu-id="9a071-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="9a071-135">-TableName</span></span>
<span data-ttu-id="9a071-136">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="9a071-136">Name of table.</span></span>

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

### <span data-ttu-id="9a071-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a071-137">-Confirm</span></span>
<span data-ttu-id="9a071-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a071-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a071-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a071-139">-WhatIf</span></span>
<span data-ttu-id="9a071-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a071-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a071-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a071-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a071-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a071-142">CommonParameters</span></span>
<span data-ttu-id="9a071-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a071-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a071-144">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a071-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a071-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a071-145">INPUTS</span></span>

### <span data-ttu-id="9a071-146">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9a071-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9a071-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a071-147">OUTPUTS</span></span>

### <span data-ttu-id="9a071-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a071-148">System.Boolean</span></span>

## <span data-ttu-id="9a071-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a071-149">NOTES</span></span>

## <span data-ttu-id="9a071-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a071-150">RELATED LINKS</span></span>

[<span data-ttu-id="9a071-151">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="9a071-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
