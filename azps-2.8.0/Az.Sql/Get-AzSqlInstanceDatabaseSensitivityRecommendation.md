---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: d5923be20fd893aefee4e9a5789c2f6f57f20fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920629"
---
# <span data-ttu-id="64cef-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="64cef-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="64cef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64cef-102">SYNOPSIS</span></span>
<span data-ttu-id="64cef-103">Hämtar de rekommenderade informations typerna och känslighets etiketterna för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="64cef-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="64cef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64cef-104">SYNTAX</span></span>

### <span data-ttu-id="64cef-105">DatabaseObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="64cef-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64cef-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="64cef-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64cef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64cef-107">DESCRIPTION</span></span>
<span data-ttu-id="64cef-108">Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returnerar de rekommenderade informations typerna och känslighets etiketterna för kolumner i den SQL-hanterade instans-databasen.</span><span class="sxs-lookup"><span data-stu-id="64cef-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="64cef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64cef-109">EXAMPLES</span></span>

### <span data-ttu-id="64cef-110">Exempel 1: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="64cef-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="64cef-111">Exempel 2: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-hanterad instans med dragning.</span><span class="sxs-lookup"><span data-stu-id="64cef-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="64cef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64cef-112">PARAMETERS</span></span>

### <span data-ttu-id="64cef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64cef-113">-AsJob</span></span>
<span data-ttu-id="64cef-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="64cef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64cef-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64cef-115">-DatabaseName</span></span>
<span data-ttu-id="64cef-116">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="64cef-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="64cef-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="64cef-117">-DatabaseObject</span></span>
<span data-ttu-id="64cef-118">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="64cef-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64cef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64cef-119">-DefaultProfile</span></span>
<span data-ttu-id="64cef-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64cef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64cef-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="64cef-121">-InstanceName</span></span>
<span data-ttu-id="64cef-122">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="64cef-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="64cef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64cef-123">-ResourceGroupName</span></span>
<span data-ttu-id="64cef-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="64cef-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="64cef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64cef-125">CommonParameters</span></span>
<span data-ttu-id="64cef-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64cef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64cef-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64cef-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64cef-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64cef-128">INPUTS</span></span>

### <span data-ttu-id="64cef-129">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="64cef-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="64cef-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64cef-130">OUTPUTS</span></span>

### <span data-ttu-id="64cef-131">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="64cef-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="64cef-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64cef-132">NOTES</span></span>

## <span data-ttu-id="64cef-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64cef-133">RELATED LINKS</span></span>

[<span data-ttu-id="64cef-134">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="64cef-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)