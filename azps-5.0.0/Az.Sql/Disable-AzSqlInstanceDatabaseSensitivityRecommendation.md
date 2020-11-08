---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272634"
---
# <span data-ttu-id="b9952-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="b9952-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="b9952-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9952-102">SYNOPSIS</span></span>
<span data-ttu-id="b9952-103">Inaktiverar (missar) känslighets rekommendationer för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="b9952-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b9952-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9952-104">SYNTAX</span></span>

### <span data-ttu-id="b9952-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b9952-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9952-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9952-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9952-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9952-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9952-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9952-108">DESCRIPTION</span></span>
<span data-ttu-id="b9952-109">Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet inaktiverar (missar) känslighets rekommendationer för kolumner i den SQL-hanterade instans-databasen.</span><span class="sxs-lookup"><span data-stu-id="b9952-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b9952-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9952-110">EXAMPLES</span></span>

### <span data-ttu-id="b9952-111">Exempel 1: inaktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="b9952-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="b9952-112">Exempel 2: inaktivera känslighets rekommendationer för kolumner med känslighets rekommendationer i en Azure SQL-hanterad instans databas med rör.</span><span class="sxs-lookup"><span data-stu-id="b9952-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="b9952-113">Exempel 3: inaktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-hanterad instans med rör.</span><span class="sxs-lookup"><span data-stu-id="b9952-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="b9952-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9952-114">PARAMETERS</span></span>

### <span data-ttu-id="b9952-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9952-115">-AsJob</span></span>
<span data-ttu-id="b9952-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b9952-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9952-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="b9952-117">-ColumnName</span></span>
<span data-ttu-id="b9952-118">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="b9952-118">Name of column.</span></span>

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

### <span data-ttu-id="b9952-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b9952-119">-DatabaseName</span></span>
<span data-ttu-id="b9952-120">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="b9952-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="b9952-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b9952-121">-DatabaseObject</span></span>
<span data-ttu-id="b9952-122">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9952-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="b9952-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9952-123">-DefaultProfile</span></span>
<span data-ttu-id="b9952-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9952-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9952-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9952-125">-InputObject</span></span>
<span data-ttu-id="b9952-126">Ett objekt som representerar en känslighets klassificering för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b9952-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9952-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b9952-127">-InstanceName</span></span>
<span data-ttu-id="b9952-128">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b9952-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="b9952-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9952-129">-PassThru</span></span>
<span data-ttu-id="b9952-130">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="b9952-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="b9952-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9952-131">-ResourceGroupName</span></span>
<span data-ttu-id="b9952-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b9952-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9952-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="b9952-133">-SchemaName</span></span>
<span data-ttu-id="b9952-134">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="b9952-134">Name of schema.</span></span>

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

### <span data-ttu-id="b9952-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="b9952-135">-TableName</span></span>
<span data-ttu-id="b9952-136">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="b9952-136">Name of table.</span></span>

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

### <span data-ttu-id="b9952-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9952-137">-Confirm</span></span>
<span data-ttu-id="b9952-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9952-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9952-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9952-139">-WhatIf</span></span>
<span data-ttu-id="b9952-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9952-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9952-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9952-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9952-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9952-142">CommonParameters</span></span>
<span data-ttu-id="b9952-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9952-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9952-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9952-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9952-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9952-145">INPUTS</span></span>

### <span data-ttu-id="b9952-146">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b9952-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b9952-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9952-147">OUTPUTS</span></span>

### <span data-ttu-id="b9952-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9952-148">System.Boolean</span></span>

## <span data-ttu-id="b9952-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9952-149">NOTES</span></span>

## <span data-ttu-id="b9952-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9952-150">RELATED LINKS</span></span>

[<span data-ttu-id="b9952-151">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="b9952-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)