---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 62f3c74f94ac0e775adc70f4eef9c4250e041145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584848"
---
# <span data-ttu-id="d5f8e-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5f8e-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="d5f8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f8e-103">Tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5f8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5f8e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5f8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5f8e-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f8e-106">Cmdleten **Remove-AzureRmSqlSyncGroup** tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d5f8e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5f8e-107">EXAMPLES</span></span>

### <span data-ttu-id="d5f8e-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="d5f8e-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="d5f8e-109">Det här kommandot tar bort synkroniseringsresursen för Azure SQL Database med namnet syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="d5f8e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5f8e-110">PARAMETERS</span></span>

### <span data-ttu-id="d5f8e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5f8e-111">-DatabaseName</span></span>
<span data-ttu-id="d5f8e-112">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d5f8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f8e-113">-DefaultProfile</span></span>
<span data-ttu-id="d5f8e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d5f8e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5f8e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5f8e-115">-Force</span></span>
<span data-ttu-id="d5f8e-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="d5f8e-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f8e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5f8e-117">-Name</span></span>
<span data-ttu-id="d5f8e-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f8e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5f8e-119">-PassThru</span></span>
<span data-ttu-id="d5f8e-120">Definierar om den borttagna synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="d5f8e-120">Defines Whether return the removed sync group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5f8e-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5f8e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5f8e-123">-ServerName</span></span>
<span data-ttu-id="d5f8e-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d5f8e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5f8e-125">-Confirm</span></span>
<span data-ttu-id="d5f8e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f8e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5f8e-127">-WhatIf</span></span>
<span data-ttu-id="d5f8e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5f8e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f8e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f8e-130">CommonParameters</span></span>
<span data-ttu-id="d5f8e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f8e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f8e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f8e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f8e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5f8e-133">INPUTS</span></span>

### <span data-ttu-id="d5f8e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5f8e-134">System.String</span></span>

## <span data-ttu-id="d5f8e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5f8e-135">OUTPUTS</span></span>

### <span data-ttu-id="d5f8e-136">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d5f8e-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d5f8e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5f8e-137">NOTES</span></span>

## <span data-ttu-id="d5f8e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5f8e-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5f8e-139">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5f8e-139">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="d5f8e-140">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5f8e-140">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="d5f8e-141">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d5f8e-141">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

