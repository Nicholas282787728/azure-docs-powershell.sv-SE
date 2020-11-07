---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927153"
---
# <span data-ttu-id="4c33b-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4c33b-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="4c33b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c33b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c33b-103">Anger etiketterna för informations typer och känslighet för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="4c33b-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4c33b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c33b-104">SYNTAX</span></span>

### <span data-ttu-id="4c33b-105">ClassificationObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4c33b-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c33b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c33b-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c33b-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c33b-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c33b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c33b-108">DESCRIPTION</span></span>
<span data-ttu-id="4c33b-109">I Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet anges etiketterna för informations typer och känslighet för kolumner i den SQL-hanterade instans-databasen.</span><span class="sxs-lookup"><span data-stu-id="4c33b-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4c33b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c33b-110">EXAMPLES</span></span>

### <span data-ttu-id="4c33b-111">Exempel 1: Ange informations typ och känslighets etikett för en kolumn i en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="4c33b-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="4c33b-112">Exempel 2: Ange rekommenderade informations typer och känslighets etiketter för kolumner i en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="4c33b-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="4c33b-113">Exempel 3: Ange informations typ och känslighets etikett för en kolumn i en Azure SQL-hanterad instans databas med dragning.</span><span class="sxs-lookup"><span data-stu-id="4c33b-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="4c33b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c33b-114">PARAMETERS</span></span>

### <span data-ttu-id="4c33b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c33b-115">-AsJob</span></span>
<span data-ttu-id="4c33b-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4c33b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c33b-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="4c33b-117">-ClassificationObject</span></span>
<span data-ttu-id="4c33b-118">Ett objekt som representerar en känslighets klassificering för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="4c33b-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="4c33b-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4c33b-119">-ColumnName</span></span>
<span data-ttu-id="4c33b-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="4c33b-120">Name of column.</span></span>

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

### <span data-ttu-id="4c33b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4c33b-121">-DatabaseName</span></span>
<span data-ttu-id="4c33b-122">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="4c33b-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="4c33b-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4c33b-123">-DatabaseObject</span></span>
<span data-ttu-id="4c33b-124">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4c33b-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="4c33b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c33b-125">-DefaultProfile</span></span>
<span data-ttu-id="4c33b-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c33b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c33b-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="4c33b-127">-InformationType</span></span>
<span data-ttu-id="4c33b-128">Ett namn som beskriver informations typen för de data som lagras i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="4c33b-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="4c33b-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4c33b-129">-InstanceName</span></span>
<span data-ttu-id="4c33b-130">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="4c33b-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="4c33b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c33b-131">-PassThru</span></span>
<span data-ttu-id="4c33b-132">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="4c33b-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="4c33b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c33b-133">-ResourceGroupName</span></span>
<span data-ttu-id="4c33b-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4c33b-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c33b-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4c33b-135">-SchemaName</span></span>
<span data-ttu-id="4c33b-136">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="4c33b-136">Name of schema.</span></span>

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

### <span data-ttu-id="4c33b-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="4c33b-137">-SensitivityLabel</span></span>
<span data-ttu-id="4c33b-138">Ett namn som beskriver känsligheten för de data som lagras i kolumnen.</span><span class="sxs-lookup"><span data-stu-id="4c33b-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="4c33b-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="4c33b-139">-TableName</span></span>
<span data-ttu-id="4c33b-140">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="4c33b-140">Name of table.</span></span>

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

### <span data-ttu-id="4c33b-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c33b-141">-Confirm</span></span>
<span data-ttu-id="4c33b-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c33b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c33b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c33b-143">-WhatIf</span></span>
<span data-ttu-id="4c33b-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c33b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c33b-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c33b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c33b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c33b-146">CommonParameters</span></span>
<span data-ttu-id="4c33b-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c33b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c33b-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c33b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c33b-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c33b-149">INPUTS</span></span>

### <span data-ttu-id="4c33b-150">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4c33b-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="4c33b-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c33b-151">OUTPUTS</span></span>

### <span data-ttu-id="4c33b-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c33b-152">System.Boolean</span></span>

## <span data-ttu-id="4c33b-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c33b-153">NOTES</span></span>

## <span data-ttu-id="4c33b-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c33b-154">RELATED LINKS</span></span>

[<span data-ttu-id="4c33b-155">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="4c33b-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
