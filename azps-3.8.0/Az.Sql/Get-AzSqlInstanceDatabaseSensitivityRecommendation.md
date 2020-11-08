---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092000"
---
# <span data-ttu-id="14d11-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="14d11-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="14d11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14d11-102">SYNOPSIS</span></span>
<span data-ttu-id="14d11-103">Hämtar de rekommenderade informations typerna och känslighets etiketterna för kolumner i Azure SQL-hanterade instans databasen.</span><span class="sxs-lookup"><span data-stu-id="14d11-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="14d11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14d11-104">SYNTAX</span></span>

### <span data-ttu-id="14d11-105">DatabaseObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="14d11-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14d11-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d11-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d11-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14d11-107">DESCRIPTION</span></span>
<span data-ttu-id="14d11-108">Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returnerar de rekommenderade informations typerna och känslighets etiketterna för kolumner i den SQL-hanterade instans-databasen.</span><span class="sxs-lookup"><span data-stu-id="14d11-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="14d11-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14d11-109">EXAMPLES</span></span>

### <span data-ttu-id="14d11-110">Exempel 1: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-hanterad instans-databas.</span><span class="sxs-lookup"><span data-stu-id="14d11-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

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

### <span data-ttu-id="14d11-111">Exempel 2: Hämta rekommenderade informations typer och känslighets etiketter för en Azure SQL-hanterad instans med dragning.</span><span class="sxs-lookup"><span data-stu-id="14d11-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

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

## <span data-ttu-id="14d11-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14d11-112">PARAMETERS</span></span>

### <span data-ttu-id="14d11-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14d11-113">-AsJob</span></span>
<span data-ttu-id="14d11-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="14d11-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14d11-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="14d11-115">-DatabaseName</span></span>
<span data-ttu-id="14d11-116">Namnet på den SQL-hanterade instans-databas som hanteras av Azure.</span><span class="sxs-lookup"><span data-stu-id="14d11-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="14d11-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="14d11-117">-DatabaseObject</span></span>
<span data-ttu-id="14d11-118">Databas objekt för hanterade instanser av Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="14d11-118">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="14d11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d11-119">-DefaultProfile</span></span>
<span data-ttu-id="14d11-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14d11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d11-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="14d11-121">-InstanceName</span></span>
<span data-ttu-id="14d11-122">Namn på Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="14d11-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="14d11-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d11-123">-ResourceGroupName</span></span>
<span data-ttu-id="14d11-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="14d11-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="14d11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d11-125">CommonParameters</span></span>
<span data-ttu-id="14d11-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d11-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14d11-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d11-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14d11-128">INPUTS</span></span>

### <span data-ttu-id="14d11-129">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="14d11-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="14d11-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14d11-130">OUTPUTS</span></span>

### <span data-ttu-id="14d11-131">Microsoft. Azure. commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="14d11-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="14d11-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14d11-132">NOTES</span></span>

## <span data-ttu-id="14d11-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14d11-133">RELATED LINKS</span></span>

[<span data-ttu-id="14d11-134">Läs mer om identifiering och klassificering av data i Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="14d11-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)