---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 97373d35cee4efb80ca2953c0085fe6b153ea138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920409"
---
# <span data-ttu-id="875b8-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="875b8-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="875b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="875b8-102">SYNOPSIS</span></span>
<span data-ttu-id="875b8-103">Hämtar en databas princip för säkerhets kopiering av databasen.</span><span class="sxs-lookup"><span data-stu-id="875b8-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="875b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="875b8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="875b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="875b8-105">DESCRIPTION</span></span>
<span data-ttu-id="875b8-106">Cmdleten **Get-AzSqlDatabaseGeoBackupPolicy** hämtar den geo säkerhets kopierings princip som registrerats för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="875b8-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="875b8-107">Det här är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="875b8-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="875b8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="875b8-108">EXAMPLES</span></span>

## <span data-ttu-id="875b8-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="875b8-109">PARAMETERS</span></span>

### <span data-ttu-id="875b8-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="875b8-110">-DatabaseName</span></span>
<span data-ttu-id="875b8-111">Anger namnet på den databas som den här cmdleten ska ha princip för säkerhets kopiering för.</span><span class="sxs-lookup"><span data-stu-id="875b8-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="875b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875b8-112">-DefaultProfile</span></span>
<span data-ttu-id="875b8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="875b8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="875b8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875b8-114">-ResourceGroupName</span></span>
<span data-ttu-id="875b8-115">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="875b8-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="875b8-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="875b8-116">-ServerName</span></span>
<span data-ttu-id="875b8-117">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="875b8-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="875b8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875b8-118">CommonParameters</span></span>
<span data-ttu-id="875b8-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875b8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875b8-120">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="875b8-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875b8-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="875b8-121">INPUTS</span></span>

### <span data-ttu-id="875b8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="875b8-122">System.String</span></span>

## <span data-ttu-id="875b8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="875b8-123">OUTPUTS</span></span>

### <span data-ttu-id="875b8-124">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="875b8-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="875b8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="875b8-125">NOTES</span></span>

## <span data-ttu-id="875b8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="875b8-126">RELATED LINKS</span></span>

[<span data-ttu-id="875b8-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="875b8-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="875b8-128">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="875b8-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
