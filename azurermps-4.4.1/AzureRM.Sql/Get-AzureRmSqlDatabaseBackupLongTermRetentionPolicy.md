---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575790"
---
# <span data-ttu-id="856dd-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="856dd-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="856dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="856dd-102">SYNOPSIS</span></span>
<span data-ttu-id="856dd-103">Hämtar en bevarande princip för en tids krävande databas.</span><span class="sxs-lookup"><span data-stu-id="856dd-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="856dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="856dd-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="856dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="856dd-105">DESCRIPTION</span></span>
<span data-ttu-id="856dd-106">Cmdleten **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** hämtar den långsiktiga bevarande principen för databasen.</span><span class="sxs-lookup"><span data-stu-id="856dd-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="856dd-107">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="856dd-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="856dd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="856dd-108">EXAMPLES</span></span>

## <span data-ttu-id="856dd-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="856dd-109">PARAMETERS</span></span>

### <span data-ttu-id="856dd-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="856dd-110">-DatabaseName</span></span>
<span data-ttu-id="856dd-111">Anger namnet på den SQL-databas som denna cmdlet hämtar en princip för.</span><span class="sxs-lookup"><span data-stu-id="856dd-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="856dd-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856dd-112">-ResourceGroupName</span></span>
<span data-ttu-id="856dd-113">Anger namnet på den resurs grupp som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="856dd-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="856dd-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="856dd-114">-ServerName</span></span>
<span data-ttu-id="856dd-115">Anger den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="856dd-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="856dd-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="856dd-116">-Confirm</span></span>
<span data-ttu-id="856dd-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="856dd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856dd-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856dd-118">-WhatIf</span></span>
<span data-ttu-id="856dd-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="856dd-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="856dd-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="856dd-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856dd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856dd-121">-DefaultProfile</span></span>
<span data-ttu-id="856dd-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="856dd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="856dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856dd-123">CommonParameters</span></span>
<span data-ttu-id="856dd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856dd-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856dd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856dd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="856dd-126">INPUTS</span></span>

## <span data-ttu-id="856dd-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="856dd-127">OUTPUTS</span></span>

## <span data-ttu-id="856dd-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="856dd-128">NOTES</span></span>

## <span data-ttu-id="856dd-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="856dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="856dd-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="856dd-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="856dd-131">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="856dd-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
