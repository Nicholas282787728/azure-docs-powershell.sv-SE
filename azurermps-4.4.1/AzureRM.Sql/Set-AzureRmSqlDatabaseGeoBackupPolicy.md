---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2cf85aac2d301653787bdf227db1cd187a887986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575772"
---
# <span data-ttu-id="e525f-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e525f-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="e525f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e525f-102">SYNOPSIS</span></span>
<span data-ttu-id="e525f-103">Ställer in en databas princip för säkerhets kopiering av databasen.</span><span class="sxs-lookup"><span data-stu-id="e525f-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e525f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e525f-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e525f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e525f-105">DESCRIPTION</span></span>
<span data-ttu-id="e525f-106">Cmdleten **set-AzureRmSqlDatabaseGeoBackupPolicy** anger den geo säkerhets kopierings princip som registrerats för en databas.</span><span class="sxs-lookup"><span data-stu-id="e525f-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="e525f-107">Det här är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="e525f-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="e525f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e525f-108">EXAMPLES</span></span>

## <span data-ttu-id="e525f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e525f-109">PARAMETERS</span></span>

### <span data-ttu-id="e525f-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e525f-110">-DatabaseName</span></span>
<span data-ttu-id="e525f-111">Anger namnet på den databas som den här cmdleten ställer in princip för geo-säkerhets kopiering för.</span><span class="sxs-lookup"><span data-stu-id="e525f-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="e525f-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e525f-112">-ResourceGroupName</span></span>
<span data-ttu-id="e525f-113">Anger namnet på resurs gruppen för den server som innehåller den här databasen.</span><span class="sxs-lookup"><span data-stu-id="e525f-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="e525f-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e525f-114">-ServerName</span></span>
<span data-ttu-id="e525f-115">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="e525f-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e525f-116">-State</span><span class="sxs-lookup"><span data-stu-id="e525f-116">-State</span></span>
<span data-ttu-id="e525f-117">Anger tillståndet för geo backup-principen.</span><span class="sxs-lookup"><span data-stu-id="e525f-117">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="e525f-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e525f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e525f-119">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="e525f-119">Enabled</span></span> 
- <span data-ttu-id="e525f-120">Aktiv</span><span class="sxs-lookup"><span data-stu-id="e525f-120">Disabled</span></span>

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

### <span data-ttu-id="e525f-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e525f-121">-Confirm</span></span>
<span data-ttu-id="e525f-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e525f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e525f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e525f-123">-WhatIf</span></span>
<span data-ttu-id="e525f-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e525f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e525f-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e525f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e525f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e525f-126">-DefaultProfile</span></span>
<span data-ttu-id="e525f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e525f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e525f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e525f-128">CommonParameters</span></span>
<span data-ttu-id="e525f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e525f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e525f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e525f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e525f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e525f-131">INPUTS</span></span>

## <span data-ttu-id="e525f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e525f-132">OUTPUTS</span></span>

## <span data-ttu-id="e525f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e525f-133">NOTES</span></span>

## <span data-ttu-id="e525f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e525f-134">RELATED LINKS</span></span>

[<span data-ttu-id="e525f-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e525f-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="e525f-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e525f-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
