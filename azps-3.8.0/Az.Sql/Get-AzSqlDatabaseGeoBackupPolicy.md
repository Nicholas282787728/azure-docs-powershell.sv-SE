---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: d69d6c2976e71183fed07e2c18adc730d8ea6e61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089272"
---
# <span data-ttu-id="ff553-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ff553-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="ff553-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff553-102">SYNOPSIS</span></span>
<span data-ttu-id="ff553-103">Hämtar en databas princip för säkerhets kopiering av databasen.</span><span class="sxs-lookup"><span data-stu-id="ff553-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="ff553-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff553-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff553-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff553-105">DESCRIPTION</span></span>
<span data-ttu-id="ff553-106">Cmdleten **Get-AzSqlDatabaseGeoBackupPolicy** hämtar den geo säkerhets kopierings princip som registrerats för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="ff553-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="ff553-107">Det här är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="ff553-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="ff553-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff553-108">EXAMPLES</span></span>

## <span data-ttu-id="ff553-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff553-109">PARAMETERS</span></span>

### <span data-ttu-id="ff553-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff553-110">-DatabaseName</span></span>
<span data-ttu-id="ff553-111">Anger namnet på den databas som den här cmdleten ska ha princip för säkerhets kopiering för.</span><span class="sxs-lookup"><span data-stu-id="ff553-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff553-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff553-112">-DefaultProfile</span></span>
<span data-ttu-id="ff553-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff553-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff553-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff553-114">-ResourceGroupName</span></span>
<span data-ttu-id="ff553-115">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="ff553-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="ff553-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff553-116">-ServerName</span></span>
<span data-ttu-id="ff553-117">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="ff553-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff553-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff553-118">CommonParameters</span></span>
<span data-ttu-id="ff553-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff553-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff553-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff553-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff553-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff553-121">INPUTS</span></span>

### <span data-ttu-id="ff553-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ff553-122">System.String</span></span>

## <span data-ttu-id="ff553-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff553-123">OUTPUTS</span></span>

### <span data-ttu-id="ff553-124">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ff553-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="ff553-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff553-125">NOTES</span></span>

## <span data-ttu-id="ff553-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff553-126">RELATED LINKS</span></span>

[<span data-ttu-id="ff553-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ff553-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="ff553-128">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ff553-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
