---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520483"
---
# <span data-ttu-id="00ed6-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="00ed6-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="00ed6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="00ed6-103">Ställer in en databas princip för säkerhets kopiering av databasen.</span><span class="sxs-lookup"><span data-stu-id="00ed6-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="00ed6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00ed6-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00ed6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="00ed6-106">Cmdleten **set-AzSqlDatabaseGeoBackupPolicy** anger den geo säkerhets kopierings princip som registrerats för en databas.</span><span class="sxs-lookup"><span data-stu-id="00ed6-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="00ed6-107">Det här är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="00ed6-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="00ed6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00ed6-108">EXAMPLES</span></span>

## <span data-ttu-id="00ed6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00ed6-109">PARAMETERS</span></span>

### <span data-ttu-id="00ed6-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00ed6-110">-DatabaseName</span></span>
<span data-ttu-id="00ed6-111">Anger namnet på den databas som den här cmdleten ställer in princip för geo-säkerhets kopiering för.</span><span class="sxs-lookup"><span data-stu-id="00ed6-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="00ed6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ed6-112">-DefaultProfile</span></span>
<span data-ttu-id="00ed6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00ed6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00ed6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ed6-114">-ResourceGroupName</span></span>
<span data-ttu-id="00ed6-115">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="00ed6-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="00ed6-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="00ed6-116">-ServerName</span></span>
<span data-ttu-id="00ed6-117">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="00ed6-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="00ed6-118">-State</span><span class="sxs-lookup"><span data-stu-id="00ed6-118">-State</span></span>
<span data-ttu-id="00ed6-119">Anger tillståndet för geo backup-principen.</span><span class="sxs-lookup"><span data-stu-id="00ed6-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="00ed6-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="00ed6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00ed6-121">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="00ed6-121">Enabled</span></span> 
- <span data-ttu-id="00ed6-122">Aktiv</span><span class="sxs-lookup"><span data-stu-id="00ed6-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ed6-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00ed6-123">-Confirm</span></span>
<span data-ttu-id="00ed6-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00ed6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00ed6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ed6-125">-WhatIf</span></span>
<span data-ttu-id="00ed6-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00ed6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00ed6-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00ed6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00ed6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ed6-128">CommonParameters</span></span>
<span data-ttu-id="00ed6-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ed6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ed6-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00ed6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ed6-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00ed6-131">INPUTS</span></span>

### <span data-ttu-id="00ed6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00ed6-132">System.String</span></span>

## <span data-ttu-id="00ed6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00ed6-133">OUTPUTS</span></span>

### <span data-ttu-id="00ed6-134">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="00ed6-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="00ed6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00ed6-135">NOTES</span></span>

## <span data-ttu-id="00ed6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00ed6-136">RELATED LINKS</span></span>

[<span data-ttu-id="00ed6-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="00ed6-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="00ed6-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="00ed6-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

