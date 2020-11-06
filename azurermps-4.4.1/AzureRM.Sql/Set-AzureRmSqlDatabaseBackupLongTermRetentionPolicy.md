---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577388"
---
# <span data-ttu-id="172e6-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="172e6-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="172e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="172e6-102">SYNOPSIS</span></span>
<span data-ttu-id="172e6-103">Ställer in en server för långsiktig bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="172e6-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="172e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="172e6-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="172e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="172e6-105">DESCRIPTION</span></span>
<span data-ttu-id="172e6-106">Cmdleten **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** anger den långsiktiga bevarande princip som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="172e6-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="172e6-107">Principen är en Azure Backup-resurs som används för att definiera säkerhets kopierings lagrings princip.</span><span class="sxs-lookup"><span data-stu-id="172e6-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="172e6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="172e6-108">EXAMPLES</span></span>

## <span data-ttu-id="172e6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="172e6-109">PARAMETERS</span></span>

### <span data-ttu-id="172e6-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="172e6-110">-DatabaseName</span></span>
<span data-ttu-id="172e6-111">Anger namnet på den SQL-databas som cmdleten ställer in en princip för.</span><span class="sxs-lookup"><span data-stu-id="172e6-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="172e6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="172e6-112">-ResourceGroupName</span></span>
<span data-ttu-id="172e6-113">Anger namnet på den resurs grupp som innehåller databasen.</span><span class="sxs-lookup"><span data-stu-id="172e6-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="172e6-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="172e6-114">-ResourceId</span></span>
<span data-ttu-id="172e6-115">Anger ID för en resurs.</span><span class="sxs-lookup"><span data-stu-id="172e6-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="172e6-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="172e6-116">-ServerName</span></span>
<span data-ttu-id="172e6-117">Anger den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="172e6-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="172e6-118">-State</span><span class="sxs-lookup"><span data-stu-id="172e6-118">-State</span></span>
<span data-ttu-id="172e6-119">Anger ett tillstånd.</span><span class="sxs-lookup"><span data-stu-id="172e6-119">Specifies a state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="172e6-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="172e6-120">-Confirm</span></span>
<span data-ttu-id="172e6-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="172e6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="172e6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="172e6-122">-WhatIf</span></span>
<span data-ttu-id="172e6-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="172e6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="172e6-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="172e6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="172e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172e6-125">-DefaultProfile</span></span>
<span data-ttu-id="172e6-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="172e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="172e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172e6-127">CommonParameters</span></span>
<span data-ttu-id="172e6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="172e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172e6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="172e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172e6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="172e6-130">INPUTS</span></span>

## <span data-ttu-id="172e6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="172e6-131">OUTPUTS</span></span>

## <span data-ttu-id="172e6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="172e6-132">NOTES</span></span>

## <span data-ttu-id="172e6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="172e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="172e6-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="172e6-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="172e6-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="172e6-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
