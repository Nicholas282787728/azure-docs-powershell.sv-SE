---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 8665119abafe928f140f79b2cec8ee2e8fcfeff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575456"
---
# <span data-ttu-id="0241a-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0241a-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="0241a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0241a-102">SYNOPSIS</span></span>
<span data-ttu-id="0241a-103">Tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="0241a-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0241a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0241a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0241a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0241a-105">DESCRIPTION</span></span>
<span data-ttu-id="0241a-106">Cmdleten **Remove-AzureRmSqlSyncGroup** tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="0241a-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0241a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0241a-107">EXAMPLES</span></span>

### <span data-ttu-id="0241a-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="0241a-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="0241a-109">Det här kommandot tar bort synkroniseringsresursen för Azure SQL Database med namnet syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="0241a-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="0241a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0241a-110">PARAMETERS</span></span>

### <span data-ttu-id="0241a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0241a-111">-DatabaseName</span></span>
<span data-ttu-id="0241a-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="0241a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0241a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0241a-113">-DefaultProfile</span></span>
<span data-ttu-id="0241a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0241a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0241a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0241a-115">-Force</span></span>
<span data-ttu-id="0241a-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="0241a-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0241a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0241a-117">-Name</span></span>
<span data-ttu-id="0241a-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="0241a-118">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0241a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0241a-119">-PassThru</span></span>
<span data-ttu-id="0241a-120">Definierar om den borttagna synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="0241a-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="0241a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0241a-121">-ResourceGroupName</span></span>
<span data-ttu-id="0241a-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0241a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="0241a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0241a-123">-ServerName</span></span>
<span data-ttu-id="0241a-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0241a-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0241a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0241a-125">-Confirm</span></span>
<span data-ttu-id="0241a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0241a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0241a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0241a-127">-WhatIf</span></span>
<span data-ttu-id="0241a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0241a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0241a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0241a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0241a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0241a-130">CommonParameters</span></span>
<span data-ttu-id="0241a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0241a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0241a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0241a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0241a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0241a-133">INPUTS</span></span>

### <span data-ttu-id="0241a-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="0241a-134">None</span></span>
<span data-ttu-id="0241a-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0241a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0241a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0241a-136">OUTPUTS</span></span>

### <span data-ttu-id="0241a-137">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="0241a-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0241a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0241a-138">NOTES</span></span>

## <span data-ttu-id="0241a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0241a-139">RELATED LINKS</span></span>

[<span data-ttu-id="0241a-140">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0241a-140">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="0241a-141">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0241a-141">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="0241a-142">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0241a-142">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

