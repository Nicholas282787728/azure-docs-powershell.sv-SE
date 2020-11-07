---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: a78e22c66e5099ec3987fb98d1b354906c11a8d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757170"
---
# <span data-ttu-id="74a32-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="74a32-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="74a32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74a32-102">SYNOPSIS</span></span>
<span data-ttu-id="74a32-103">Uppdatera synkroniseringsschemat för en synkroniserad medlems databas eller en databas för Lösenordssynkronisering.</span><span class="sxs-lookup"><span data-stu-id="74a32-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="74a32-104">Den senaste databas schema från den riktiga databasen hämtas och sedan används den för att uppdatera schemat i databasen.</span><span class="sxs-lookup"><span data-stu-id="74a32-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="74a32-105">Om "SyncMemberName" anges uppdaterar det databasschemat för medlems databasen; Om du inte gör det kommer det att uppdatera Hub-databasschemat.</span><span class="sxs-lookup"><span data-stu-id="74a32-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a32-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74a32-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74a32-107">DESCRIPTION</span></span>
<span data-ttu-id="74a32-108">Cmdleten **Update-AzureRmSqlSyncSchema** uppdaterar synkroniseringsschemat för en synkroniserad medlems databas eller en synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="74a32-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="74a32-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74a32-109">EXAMPLES</span></span>

### <span data-ttu-id="74a32-110">Exempel 1: uppdatera synkroniseringsschemat för en nav-databas</span><span class="sxs-lookup"><span data-stu-id="74a32-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="74a32-111">Det här kommandot uppdaterar synkroniseringsschemat för NAV databasen i Sync-gruppsyncGroup01</span><span class="sxs-lookup"><span data-stu-id="74a32-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="74a32-112">Exempel 2: uppdatera synkroniseringsschemat för en medlems databas</span><span class="sxs-lookup"><span data-stu-id="74a32-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="74a32-113">Det här kommandot uppdaterar synkroniseringsschemat för medlems databasen i syncMember01</span><span class="sxs-lookup"><span data-stu-id="74a32-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="74a32-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74a32-114">PARAMETERS</span></span>

### <span data-ttu-id="74a32-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74a32-115">-DatabaseName</span></span>
<span data-ttu-id="74a32-116">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="74a32-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="74a32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a32-117">-DefaultProfile</span></span>
<span data-ttu-id="74a32-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="74a32-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74a32-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74a32-119">-PassThru</span></span>
<span data-ttu-id="74a32-120">Definierar om den synkroniserade gruppen ska returneras den här cmdleten fungerar</span><span class="sxs-lookup"><span data-stu-id="74a32-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a32-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a32-121">-ResourceGroupName</span></span>
<span data-ttu-id="74a32-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="74a32-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="74a32-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="74a32-123">-ServerName</span></span>
<span data-ttu-id="74a32-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="74a32-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="74a32-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="74a32-125">-SyncGroupName</span></span>
<span data-ttu-id="74a32-126">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="74a32-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a32-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="74a32-127">-SyncMemberName</span></span>
<span data-ttu-id="74a32-128">Synkroniserat medlems namn.</span><span class="sxs-lookup"><span data-stu-id="74a32-128">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a32-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74a32-129">-Confirm</span></span>
<span data-ttu-id="74a32-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74a32-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a32-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a32-131">-WhatIf</span></span>
<span data-ttu-id="74a32-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74a32-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a32-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74a32-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a32-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a32-134">CommonParameters</span></span>
<span data-ttu-id="74a32-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a32-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a32-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a32-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a32-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74a32-137">INPUTS</span></span>

### <span data-ttu-id="74a32-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="74a32-138">None</span></span>
<span data-ttu-id="74a32-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="74a32-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74a32-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74a32-140">OUTPUTS</span></span>

### <span data-ttu-id="74a32-141">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="74a32-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="74a32-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74a32-142">NOTES</span></span>

## <span data-ttu-id="74a32-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74a32-143">RELATED LINKS</span></span>
