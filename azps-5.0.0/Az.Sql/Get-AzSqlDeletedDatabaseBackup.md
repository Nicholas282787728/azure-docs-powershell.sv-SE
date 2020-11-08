---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263392"
---
# <span data-ttu-id="d9193-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d9193-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="d9193-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9193-102">SYNOPSIS</span></span>
<span data-ttu-id="d9193-103">Hämtar en borttagen databas som du kan återställa.</span><span class="sxs-lookup"><span data-stu-id="d9193-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="d9193-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9193-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9193-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9193-105">DESCRIPTION</span></span>
<span data-ttu-id="d9193-106">Cmdleten **Get-AzSqlDeletedDatabaseBackup** hämtar en angiven säkerhets kopia av BORTTAGen SQL-databas som du kan återställa eller alla borttagna säkerhets kopior som du kan återställa.</span><span class="sxs-lookup"><span data-stu-id="d9193-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="d9193-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="d9193-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d9193-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9193-108">EXAMPLES</span></span>

### <span data-ttu-id="d9193-109">Exempel 1: Hämta alla borttagna databas säkerhets kopior på en server</span><span class="sxs-lookup"><span data-stu-id="d9193-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="d9193-110">Det här kommandot får alla borttagna databas säkerhets kopior från en server.</span><span class="sxs-lookup"><span data-stu-id="d9193-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="d9193-111">Exempel 2: Hämta en angiven borttagen databas säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="d9193-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="d9193-112">Det här kommandot får den borttagna databas säkerhets kopian för ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="d9193-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="d9193-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9193-113">PARAMETERS</span></span>

### <span data-ttu-id="d9193-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9193-114">-DatabaseName</span></span>
<span data-ttu-id="d9193-115">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d9193-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9193-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9193-116">-DefaultProfile</span></span>
<span data-ttu-id="d9193-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d9193-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9193-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="d9193-118">-DeletionDate</span></span>
<span data-ttu-id="d9193-119">Anger det datum, som ett **datetime** -objekt, som databasen togs bort.</span><span class="sxs-lookup"><span data-stu-id="d9193-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="d9193-120">Använd Get-Date cmdlet för att få ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d9193-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9193-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9193-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9193-122">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="d9193-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d9193-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9193-123">-ServerName</span></span>
<span data-ttu-id="d9193-124">Anger namnet på databas servern.</span><span class="sxs-lookup"><span data-stu-id="d9193-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="d9193-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9193-125">-Confirm</span></span>
<span data-ttu-id="d9193-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9193-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9193-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9193-127">-WhatIf</span></span>
<span data-ttu-id="d9193-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9193-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9193-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9193-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9193-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9193-130">CommonParameters</span></span>
<span data-ttu-id="d9193-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9193-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9193-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9193-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9193-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9193-133">INPUTS</span></span>

### <span data-ttu-id="d9193-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d9193-134">System.String</span></span>

### <span data-ttu-id="d9193-135">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9193-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d9193-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9193-136">OUTPUTS</span></span>

### <span data-ttu-id="d9193-137">Microsoft. Azure. commands. SQL. backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="d9193-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="d9193-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9193-138">NOTES</span></span>

## <span data-ttu-id="d9193-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9193-139">RELATED LINKS</span></span>

[<span data-ttu-id="d9193-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d9193-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="d9193-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d9193-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
