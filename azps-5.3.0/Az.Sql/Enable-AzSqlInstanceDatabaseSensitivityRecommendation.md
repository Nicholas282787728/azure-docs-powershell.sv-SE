---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419480"
---
# <span data-ttu-id="a7546-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="a7546-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="a7546-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7546-102">SYNOPSIS</span></span>
<span data-ttu-id="a7546-103">Aktiverar känslighets rekommendationer för kolumner (rekommendationer är aktiverade som standard i alla kolumner) i den SQL-hanterade instans-databasen.</span><span class="sxs-lookup"><span data-stu-id="a7546-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a7546-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7546-104">SYNTAX</span></span>

### <span data-ttu-id="a7546-105">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a7546-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7546-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7546-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7546-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7546-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7546-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7546-108">DESCRIPTION</span></span>
<span data-ttu-id="a7546-109">Med Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet aktive ras känslighets rekommendationer för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="a7546-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a7546-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7546-110">EXAMPLES</span></span>

### <span data-ttu-id="a7546-111">Exempel 1: Aktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="a7546-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="a7546-112">Exempel 2: Aktivera känslighets rekommendationer för en viss kolumn i en Azure SQL-hanterad instans med rör.</span><span class="sxs-lookup"><span data-stu-id="a7546-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="a7546-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7546-113">PARAMETERS</span></span>

### <span data-ttu-id="a7546-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7546-114">-AsJob</span></span>
<span data-ttu-id="a7546-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a7546-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7546-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a7546-116">-ColumnName</span></span>
<span data-ttu-id="a7546-117">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="a7546-117">Name of column.</span></span>

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

### <span data-ttu-id="a7546-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7546-118">-DatabaseName</span></span>
<span data-ttu-id="a7546-119">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="a7546-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="a7546-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a7546-120">-DatabaseObject</span></span>
<span data-ttu-id="a7546-121">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a7546-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="a7546-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7546-122">-DefaultProfile</span></span>
<span data-ttu-id="a7546-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7546-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7546-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7546-124">-InputObject</span></span>
<span data-ttu-id="a7546-125">Ett objekt som representerar en känslighets klassificering för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="a7546-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="a7546-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a7546-126">-InstanceName</span></span>
<span data-ttu-id="a7546-127">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="a7546-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="a7546-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7546-128">-PassThru</span></span>
<span data-ttu-id="a7546-129">Anger om känslighets klassificerings modellen ska matas ut i slutet av cmdlet-körningen</span><span class="sxs-lookup"><span data-stu-id="a7546-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="a7546-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7546-130">-ResourceGroupName</span></span>
<span data-ttu-id="a7546-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a7546-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7546-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a7546-132">-SchemaName</span></span>
<span data-ttu-id="a7546-133">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="a7546-133">Name of schema.</span></span>

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

### <span data-ttu-id="a7546-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="a7546-134">-TableName</span></span>
<span data-ttu-id="a7546-135">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="a7546-135">Name of table.</span></span>

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

### <span data-ttu-id="a7546-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a7546-136">-Confirm</span></span>
<span data-ttu-id="a7546-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a7546-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7546-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7546-138">-WhatIf</span></span>
<span data-ttu-id="a7546-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a7546-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7546-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a7546-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7546-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7546-141">CommonParameters</span></span>
<span data-ttu-id="a7546-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7546-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7546-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7546-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7546-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7546-144">INPUTS</span></span>

### <span data-ttu-id="a7546-145">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a7546-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a7546-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7546-146">OUTPUTS</span></span>

### <span data-ttu-id="a7546-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7546-147">System.Boolean</span></span>

## <span data-ttu-id="a7546-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7546-148">NOTES</span></span>

## <span data-ttu-id="a7546-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7546-149">RELATED LINKS</span></span>

[<span data-ttu-id="a7546-150">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="a7546-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)