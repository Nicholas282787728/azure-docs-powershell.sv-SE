---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756767"
---
# <span data-ttu-id="82576-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="82576-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="82576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82576-102">SYNOPSIS</span></span>
<span data-ttu-id="82576-103">Skapar en ny återställnings punkt från vilken en SQL-databas kan återställas.</span><span class="sxs-lookup"><span data-stu-id="82576-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82576-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82576-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82576-105">DESCRIPTION</span></span>
<span data-ttu-id="82576-106">Cmdleten **New-AzureRmSqlDatabaseRestorePoint** skapar en ny återställnings punkt som en Azure SQL-databas kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="82576-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="82576-107">Denna cmdlet stöds för närvarande av SQL Server DataWarehouse-tjänsten i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="82576-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="82576-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82576-108">EXAMPLES</span></span>

### <span data-ttu-id="82576-109">Exempel 1: skapa en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="82576-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="82576-110">Det här kommandot skapar en återställnings punkt för Azure SQL-databasen och returnerar information om återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="82576-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="82576-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82576-111">PARAMETERS</span></span>

### <span data-ttu-id="82576-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82576-112">-DatabaseName</span></span>
<span data-ttu-id="82576-113">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="82576-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="82576-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82576-114">-DefaultProfile</span></span>
<span data-ttu-id="82576-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="82576-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82576-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82576-116">-ResourceGroupName</span></span>
<span data-ttu-id="82576-117">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="82576-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="82576-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="82576-118">-RestorePointLabel</span></span>
<span data-ttu-id="82576-119">Anger etiketten för återställnings punkten så att den blir lätt att identifiera.</span><span class="sxs-lookup"><span data-stu-id="82576-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82576-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82576-120">-ServerName</span></span>
<span data-ttu-id="82576-121">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="82576-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="82576-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82576-122">-Confirm</span></span>
<span data-ttu-id="82576-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82576-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82576-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82576-124">-WhatIf</span></span>
<span data-ttu-id="82576-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82576-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82576-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82576-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82576-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82576-127">CommonParameters</span></span>
<span data-ttu-id="82576-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82576-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82576-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82576-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82576-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82576-130">INPUTS</span></span>

## <span data-ttu-id="82576-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82576-131">OUTPUTS</span></span>

## <span data-ttu-id="82576-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82576-132">NOTES</span></span>

## <span data-ttu-id="82576-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82576-133">RELATED LINKS</span></span>
