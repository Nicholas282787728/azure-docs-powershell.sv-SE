---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 99892ee748de030a045bd9d0a022051206236198
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758271"
---
# <span data-ttu-id="a8c24-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a8c24-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="a8c24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8c24-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c24-103">Tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="a8c24-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8c24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8c24-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8c24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8c24-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c24-106">Cmdleten **Remove-AzureRmSqlSyncGroup** tar bort en Azure SQL Database Sync-grupp.</span><span class="sxs-lookup"><span data-stu-id="a8c24-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="a8c24-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8c24-107">EXAMPLES</span></span>

### <span data-ttu-id="a8c24-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="a8c24-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="a8c24-109">Det här kommandot tar bort synkroniseringsresursen för Azure SQL Database med namnet syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="a8c24-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="a8c24-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8c24-110">PARAMETERS</span></span>

### <span data-ttu-id="a8c24-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8c24-111">-Confirm</span></span>
<span data-ttu-id="a8c24-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8c24-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8c24-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8c24-113">-DatabaseName</span></span>
<span data-ttu-id="a8c24-114">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a8c24-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a8c24-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8c24-115">-Force</span></span>
<span data-ttu-id="a8c24-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="a8c24-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a8c24-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8c24-117">-Name</span></span>
<span data-ttu-id="a8c24-118">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="a8c24-118">The sync group name.</span></span>

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

### <span data-ttu-id="a8c24-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8c24-119">-PassThru</span></span>
<span data-ttu-id="a8c24-120">Definierar om den borttagna synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="a8c24-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="a8c24-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8c24-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8c24-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a8c24-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8c24-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8c24-123">-ServerName</span></span>
<span data-ttu-id="a8c24-124">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a8c24-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a8c24-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8c24-125">-WhatIf</span></span>
<span data-ttu-id="a8c24-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8c24-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8c24-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8c24-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8c24-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8c24-128">-DefaultProfile</span></span>
<span data-ttu-id="a8c24-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8c24-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8c24-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c24-130">CommonParameters</span></span>
<span data-ttu-id="a8c24-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c24-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c24-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c24-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c24-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8c24-133">INPUTS</span></span>

## <span data-ttu-id="a8c24-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8c24-134">OUTPUTS</span></span>

### <span data-ttu-id="a8c24-135">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a8c24-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a8c24-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8c24-136">NOTES</span></span>

## <span data-ttu-id="a8c24-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8c24-137">RELATED LINKS</span></span>

[<span data-ttu-id="a8c24-138">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a8c24-138">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a8c24-139">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a8c24-139">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a8c24-140">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a8c24-140">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

