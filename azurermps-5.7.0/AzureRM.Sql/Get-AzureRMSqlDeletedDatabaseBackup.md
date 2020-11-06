---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573228"
---
# <span data-ttu-id="0cbed-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0cbed-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="0cbed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cbed-102">SYNOPSIS</span></span>
<span data-ttu-id="0cbed-103">Hämtar en borttagen databas som du kan återställa.</span><span class="sxs-lookup"><span data-stu-id="0cbed-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cbed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cbed-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cbed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cbed-105">DESCRIPTION</span></span>
<span data-ttu-id="0cbed-106">Cmdleten **Get-AzureRMSqlDeletedDatabaseBackup** hämtar en angiven säkerhets kopia av BORTTAGen SQL-databas som du kan återställa eller alla borttagna säkerhets kopior som du kan återställa.</span><span class="sxs-lookup"><span data-stu-id="0cbed-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="0cbed-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="0cbed-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0cbed-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cbed-108">EXAMPLES</span></span>

### <span data-ttu-id="0cbed-109">Exempel 1: Hämta alla borttagna databas säkerhets kopior på en server</span><span class="sxs-lookup"><span data-stu-id="0cbed-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="0cbed-110">Det här kommandot får alla borttagna databas säkerhets kopior från en server.</span><span class="sxs-lookup"><span data-stu-id="0cbed-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="0cbed-111">Exempel 2: Hämta en angiven borttagen databas säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="0cbed-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="0cbed-112">Det här kommandot får den borttagna databas säkerhets kopian för ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="0cbed-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="0cbed-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cbed-113">PARAMETERS</span></span>

### <span data-ttu-id="0cbed-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0cbed-114">-DatabaseName</span></span>
<span data-ttu-id="0cbed-115">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="0cbed-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cbed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cbed-116">-DefaultProfile</span></span>
<span data-ttu-id="0cbed-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0cbed-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cbed-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="0cbed-118">-DeletionDate</span></span>
<span data-ttu-id="0cbed-119">Anger det datum, som ett **datetime** -objekt, som databasen togs bort.</span><span class="sxs-lookup"><span data-stu-id="0cbed-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="0cbed-120">Använd Get-Date cmdlet för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0cbed-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cbed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cbed-121">-ResourceGroupName</span></span>
<span data-ttu-id="0cbed-122">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="0cbed-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0cbed-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0cbed-123">-ServerName</span></span>
<span data-ttu-id="0cbed-124">Anger namnet på databas servern.</span><span class="sxs-lookup"><span data-stu-id="0cbed-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="0cbed-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0cbed-125">-Confirm</span></span>
<span data-ttu-id="0cbed-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0cbed-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cbed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cbed-127">-WhatIf</span></span>
<span data-ttu-id="0cbed-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0cbed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cbed-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0cbed-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cbed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cbed-130">CommonParameters</span></span>
<span data-ttu-id="0cbed-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cbed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cbed-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cbed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cbed-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cbed-133">INPUTS</span></span>

### <span data-ttu-id="0cbed-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="0cbed-134">None</span></span>
<span data-ttu-id="0cbed-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0cbed-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0cbed-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cbed-136">OUTPUTS</span></span>

## <span data-ttu-id="0cbed-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cbed-137">NOTES</span></span>

## <span data-ttu-id="0cbed-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cbed-138">RELATED LINKS</span></span>

[<span data-ttu-id="0cbed-139">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0cbed-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="0cbed-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0cbed-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
