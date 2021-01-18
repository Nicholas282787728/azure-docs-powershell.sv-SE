---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fe8cffb4ab9d79828795cc1148a3c109cfbfdddb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522991"
---
# <span data-ttu-id="ab0d8-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="ab0d8-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="ab0d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0d8-103">Hämtar de aktuella informations typerna och känslighets etiketterna för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ab0d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab0d8-104">SYNTAX</span></span>

### <span data-ttu-id="ab0d8-105">DatabaseObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ab0d8-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab0d8-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab0d8-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab0d8-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab0d8-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab0d8-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab0d8-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab0d8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab0d8-109">DESCRIPTION</span></span>
<span data-ttu-id="ab0d8-110">Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returnerar de aktuella informations typerna och känslighets etiketterna för kolumnerna i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="ab0d8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab0d8-111">EXAMPLES</span></span>

### <span data-ttu-id="ab0d8-112">Exempel 1: hämta aktuella informations typer och känslighets etiketter för en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="ab0d8-113">Exempel 2: hämta aktuella informations typer och känslighets etiketter för en Azure SQL-hanterad instans med rör.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="ab0d8-114">Exempel 3: Hämta aktuell informations typ och känslighets etikett för en viss kolumn i en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="ab0d8-115">Exempel 4: Hämta aktuell informations typ och känslighets etikett för en viss kolumn i en Azure SQL-hanterad instans-databas med dragning.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="ab0d8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab0d8-116">PARAMETERS</span></span>

### <span data-ttu-id="ab0d8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab0d8-117">-AsJob</span></span>
<span data-ttu-id="ab0d8-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ab0d8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab0d8-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ab0d8-119">-ColumnName</span></span>
<span data-ttu-id="ab0d8-120">Kolumn namn.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-120">Name of column.</span></span>

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

### <span data-ttu-id="ab0d8-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ab0d8-121">-DatabaseName</span></span>
<span data-ttu-id="ab0d8-122">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-122">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab0d8-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ab0d8-123">-DatabaseObject</span></span>
<span data-ttu-id="ab0d8-124">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab0d8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0d8-125">-DefaultProfile</span></span>
<span data-ttu-id="ab0d8-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab0d8-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ab0d8-127">-InstanceName</span></span>
<span data-ttu-id="ab0d8-128">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-128">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab0d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab0d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="ab0d8-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab0d8-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ab0d8-131">-SchemaName</span></span>
<span data-ttu-id="ab0d8-132">Namn på schema.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-132">Name of schema.</span></span>

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

### <span data-ttu-id="ab0d8-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="ab0d8-133">-TableName</span></span>
<span data-ttu-id="ab0d8-134">Namn på tabellen.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-134">Name of table.</span></span>

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

### <span data-ttu-id="ab0d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0d8-135">CommonParameters</span></span>
<span data-ttu-id="ab0d8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab0d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0d8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab0d8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0d8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab0d8-138">INPUTS</span></span>

### <span data-ttu-id="ab0d8-139">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ab0d8-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ab0d8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab0d8-140">OUTPUTS</span></span>

### <span data-ttu-id="ab0d8-141">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ab0d8-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ab0d8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab0d8-142">NOTES</span></span>

## <span data-ttu-id="ab0d8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab0d8-143">RELATED LINKS</span></span>

[<span data-ttu-id="ab0d8-144">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="ab0d8-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
