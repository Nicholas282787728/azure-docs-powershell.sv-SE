---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserestorepoints
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: fac0e279bb52ecf17246926875daea4392e23e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579355"
---
# <span data-ttu-id="060dc-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="060dc-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="060dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="060dc-102">SYNOPSIS</span></span>
<span data-ttu-id="060dc-103">Hämtar de distinkta återställnings punkter från vilka ett SQL-datalager kan återställas.</span><span class="sxs-lookup"><span data-stu-id="060dc-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="060dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="060dc-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="060dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="060dc-105">DESCRIPTION</span></span>
<span data-ttu-id="060dc-106">Cmdleten **Get-AzureRmSqlDatabaseRestorePoints** hämtar de distinkta återställnings punkter som ett Azure SQL data-lager kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="060dc-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="060dc-107">För en Azure SQL-databas är återställnings fönstret kontinuerligt.</span><span class="sxs-lookup"><span data-stu-id="060dc-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="060dc-108">Det innebär att alla tidpunkter i databasens bevarande period kan användas som återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="060dc-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="060dc-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="060dc-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="060dc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="060dc-110">EXAMPLES</span></span>

### <span data-ttu-id="060dc-111">Exempel 1: Hämta alla återställnings punkter</span><span class="sxs-lookup"><span data-stu-id="060dc-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="060dc-112">Det här kommandot returnerar alla tillgängliga återställnings punkter för den Azure SQL-databas som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="060dc-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="060dc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="060dc-113">PARAMETERS</span></span>

### <span data-ttu-id="060dc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="060dc-114">-DatabaseName</span></span>
<span data-ttu-id="060dc-115">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="060dc-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="060dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060dc-116">-DefaultProfile</span></span>
<span data-ttu-id="060dc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="060dc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="060dc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060dc-118">-ResourceGroupName</span></span>
<span data-ttu-id="060dc-119">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="060dc-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="060dc-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="060dc-120">-ServerName</span></span>
<span data-ttu-id="060dc-121">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="060dc-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="060dc-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="060dc-122">-Confirm</span></span>
<span data-ttu-id="060dc-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="060dc-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060dc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060dc-124">-WhatIf</span></span>
<span data-ttu-id="060dc-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="060dc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="060dc-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="060dc-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060dc-127">CommonParameters</span></span>
<span data-ttu-id="060dc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="060dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060dc-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060dc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="060dc-130">INPUTS</span></span>

### <span data-ttu-id="060dc-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="060dc-131">None</span></span>
<span data-ttu-id="060dc-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="060dc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="060dc-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="060dc-133">OUTPUTS</span></span>

## <span data-ttu-id="060dc-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="060dc-134">NOTES</span></span>

## <span data-ttu-id="060dc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="060dc-135">RELATED LINKS</span></span>
