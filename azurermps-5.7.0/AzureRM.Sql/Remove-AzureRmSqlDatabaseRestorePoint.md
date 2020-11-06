---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 235165b178a721bf5e450a2430a6454eb3b2c1be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581924"
---
# <span data-ttu-id="e5671-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e5671-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="e5671-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5671-102">SYNOPSIS</span></span>
<span data-ttu-id="e5671-103">Tar bort en given återställnings punkt från en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e5671-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5671-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5671-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5671-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5671-105">DESCRIPTION</span></span>
<span data-ttu-id="e5671-106">Cmdleten **Remove-AzureRmSqlDatabaseRestorePoint** tar bort en återställnings punkt från en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="e5671-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>

<span data-ttu-id="e5671-107">Denna cmdlet stöds för närvarande av SQL Server DataWarehouse-tjänsten i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e5671-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="e5671-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5671-108">EXAMPLES</span></span>

### <span data-ttu-id="e5671-109">Exempel 1: tar bort en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="e5671-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="e5671-110">Det här kommandot tar bort en återställnings punkt för en Azure SQL-databas skapad.</span><span class="sxs-lookup"><span data-stu-id="e5671-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="e5671-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5671-111">PARAMETERS</span></span>

### <span data-ttu-id="e5671-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e5671-112">-DatabaseName</span></span>
<span data-ttu-id="e5671-113">Anger namnet på SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="e5671-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="e5671-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5671-114">-DefaultProfile</span></span>
<span data-ttu-id="e5671-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e5671-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5671-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5671-116">-ResourceGroupName</span></span>
<span data-ttu-id="e5671-117">Anger namnet på den resurs grupp som SQL-databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="e5671-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="e5671-118">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="e5671-118">-RestorePointCreationDate</span></span>
<span data-ttu-id="e5671-119">Anger det datum då återställnings punkten skapades.</span><span class="sxs-lookup"><span data-stu-id="e5671-119">Specifies the restore point creation date.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5671-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e5671-120">-ServerName</span></span>
<span data-ttu-id="e5671-121">Anger namnet på den AzureSQL-server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="e5671-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e5671-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5671-122">-Confirm</span></span>
<span data-ttu-id="e5671-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5671-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5671-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5671-124">-WhatIf</span></span>
<span data-ttu-id="e5671-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5671-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5671-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5671-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5671-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5671-127">CommonParameters</span></span>
<span data-ttu-id="e5671-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5671-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5671-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5671-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5671-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5671-130">INPUTS</span></span>

## <span data-ttu-id="e5671-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5671-131">OUTPUTS</span></span>

## <span data-ttu-id="e5671-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5671-132">NOTES</span></span>

## <span data-ttu-id="e5671-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5671-133">RELATED LINKS</span></span>
