---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2e5e313fe35770e6841909e1f0718cfe3d9c8664
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756440"
---
# <span data-ttu-id="b07ad-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b07ad-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="b07ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b07ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b07ad-103">Hämtar en databas princip för säkerhets kopiering av databasen.</span><span class="sxs-lookup"><span data-stu-id="b07ad-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b07ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b07ad-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b07ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b07ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b07ad-106">Cmdleten **Get-AzureRmSqlDatabaseGeoBackupPolicy** hämtar den geo säkerhets kopierings princip som registrerats för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="b07ad-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="b07ad-107">Det här är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="b07ad-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="b07ad-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b07ad-108">EXAMPLES</span></span>

## <span data-ttu-id="b07ad-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b07ad-109">PARAMETERS</span></span>

### <span data-ttu-id="b07ad-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b07ad-110">-DatabaseName</span></span>
<span data-ttu-id="b07ad-111">Anger namnet på den databas som den här cmdleten ska ha princip för säkerhets kopiering för.</span><span class="sxs-lookup"><span data-stu-id="b07ad-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07ad-112">-DefaultProfile</span></span>
<span data-ttu-id="b07ad-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b07ad-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b07ad-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07ad-114">-ResourceGroupName</span></span>
<span data-ttu-id="b07ad-115">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="b07ad-115">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07ad-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b07ad-116">-ServerName</span></span>
<span data-ttu-id="b07ad-117">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="b07ad-117">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07ad-118">CommonParameters</span></span>
<span data-ttu-id="b07ad-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07ad-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07ad-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07ad-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b07ad-121">INPUTS</span></span>

### <span data-ttu-id="b07ad-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="b07ad-122">None</span></span>
<span data-ttu-id="b07ad-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b07ad-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b07ad-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b07ad-124">OUTPUTS</span></span>

## <span data-ttu-id="b07ad-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b07ad-125">NOTES</span></span>

## <span data-ttu-id="b07ad-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b07ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="b07ad-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b07ad-127">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="b07ad-128">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b07ad-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
