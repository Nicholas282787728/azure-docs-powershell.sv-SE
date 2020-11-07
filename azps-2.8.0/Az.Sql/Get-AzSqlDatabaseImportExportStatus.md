---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: b8a8100c55e10969eeee1723fe22deddfe5764ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920406"
---
# <span data-ttu-id="ce190-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="ce190-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="ce190-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce190-102">SYNOPSIS</span></span>
<span data-ttu-id="ce190-103">Hämtar information om en import eller export av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ce190-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="ce190-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce190-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce190-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce190-105">DESCRIPTION</span></span>
<span data-ttu-id="ce190-106">Cmdleten **Get-AzSqlDatabaseImportExportStatus** hämtar information om en BACPAC-fil import från ett lagrings konto till en Azure SQL-databas eller en export av en Azure SQL-databas som en BACPAC-fil till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ce190-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="ce190-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="ce190-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ce190-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce190-108">EXAMPLES</span></span>

### <span data-ttu-id="ce190-109">Exempel 1: Hämta import-och export status för en SQL-databas</span><span class="sxs-lookup"><span data-stu-id="ce190-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="ce190-110">Det här kommandot får statusen för en import-eller export förfrågan för en databas på den angivna URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="ce190-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="ce190-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce190-111">PARAMETERS</span></span>

### <span data-ttu-id="ce190-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce190-112">-DefaultProfile</span></span>
<span data-ttu-id="ce190-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ce190-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce190-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="ce190-114">-OperationStatusLink</span></span>
<span data-ttu-id="ce190-115">Anger den status länk som returneras från New-AzSqlDatabaseExport eller New-AzSqlDatabaseImport cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ce190-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce190-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce190-116">-Confirm</span></span>
<span data-ttu-id="ce190-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce190-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce190-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce190-118">-WhatIf</span></span>
<span data-ttu-id="ce190-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce190-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce190-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce190-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce190-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce190-121">CommonParameters</span></span>
<span data-ttu-id="ce190-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce190-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce190-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce190-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce190-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce190-124">INPUTS</span></span>

### <span data-ttu-id="ce190-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ce190-125">System.String</span></span>

## <span data-ttu-id="ce190-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce190-126">OUTPUTS</span></span>

### <span data-ttu-id="ce190-127">Microsoft. Azure. commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="ce190-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="ce190-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce190-128">NOTES</span></span>
* <span data-ttu-id="ce190-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="ce190-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="ce190-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce190-130">RELATED LINKS</span></span>

[<span data-ttu-id="ce190-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="ce190-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="ce190-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="ce190-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="ce190-133">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ce190-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
