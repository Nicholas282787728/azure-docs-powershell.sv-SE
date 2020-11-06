---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: 002b248195840cb7453757e92f9269e7a61d9fda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579708"
---
# <span data-ttu-id="d48dc-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="d48dc-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="d48dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d48dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d48dc-103">Hämtar de distinkta återställnings punkter från vilka ett SQL-datalager kan återställas.</span><span class="sxs-lookup"><span data-stu-id="d48dc-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d48dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d48dc-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d48dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d48dc-105">DESCRIPTION</span></span>
<span data-ttu-id="d48dc-106">Cmdleten **Get-AzureRmSqlDatabaseRestorePoints** hämtar de distinkta återställnings punkter som ett Azure SQL data-lager kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="d48dc-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="d48dc-107">För en Azure SQL-databas är återställnings fönstret kontinuerligt.</span><span class="sxs-lookup"><span data-stu-id="d48dc-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="d48dc-108">Det innebär att alla tidpunkter i databasens bevarande period kan användas som återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="d48dc-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="d48dc-109">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="d48dc-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d48dc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d48dc-110">EXAMPLES</span></span>

### <span data-ttu-id="d48dc-111">Exempel 1: Hämta alla återställnings punkter</span><span class="sxs-lookup"><span data-stu-id="d48dc-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
```

<span data-ttu-id="d48dc-112">Det här kommandot returnerar alla tillgängliga återställnings punkter för den Azure SQL-databas som heter Database01.</span><span class="sxs-lookup"><span data-stu-id="d48dc-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="d48dc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d48dc-113">PARAMETERS</span></span>

### <span data-ttu-id="d48dc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d48dc-114">-DatabaseName</span></span>
<span data-ttu-id="d48dc-115">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d48dc-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="d48dc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d48dc-116">-ResourceGroupName</span></span>
<span data-ttu-id="d48dc-117">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="d48dc-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="d48dc-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d48dc-118">-ServerName</span></span>
<span data-ttu-id="d48dc-119">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="d48dc-119">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="d48dc-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d48dc-120">-Confirm</span></span>
<span data-ttu-id="d48dc-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d48dc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d48dc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d48dc-122">-WhatIf</span></span>
<span data-ttu-id="d48dc-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d48dc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d48dc-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d48dc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d48dc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48dc-125">-DefaultProfile</span></span>
<span data-ttu-id="d48dc-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d48dc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d48dc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48dc-127">CommonParameters</span></span>
<span data-ttu-id="d48dc-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d48dc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48dc-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48dc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48dc-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d48dc-130">INPUTS</span></span>

## <span data-ttu-id="d48dc-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d48dc-131">OUTPUTS</span></span>

## <span data-ttu-id="d48dc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d48dc-132">NOTES</span></span>

## <span data-ttu-id="d48dc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d48dc-133">RELATED LINKS</span></span>

