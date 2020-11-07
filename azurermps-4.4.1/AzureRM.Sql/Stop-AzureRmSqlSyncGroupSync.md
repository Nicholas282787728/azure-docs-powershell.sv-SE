---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 8a472307c475e093de6f8e6071c137afda5ec1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757435"
---
# <span data-ttu-id="921da-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="921da-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="921da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="921da-102">SYNOPSIS</span></span>
<span data-ttu-id="921da-103">Stoppar en synkronisering av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="921da-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="921da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="921da-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="921da-105">DESCRIPTION</span></span>
<span data-ttu-id="921da-106">Cmdleten **Stop-AzureRmSqlSyncGroupSync** stoppar synkroniseringen av en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="921da-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="921da-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="921da-107">EXAMPLES</span></span>

### <span data-ttu-id="921da-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="921da-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="921da-109">Det här kommandot stoppar den synkronisering som pågår för gruppen Sync-mysg.</span><span class="sxs-lookup"><span data-stu-id="921da-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="921da-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="921da-110">PARAMETERS</span></span>

### <span data-ttu-id="921da-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="921da-111">-Confirm</span></span>
<span data-ttu-id="921da-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="921da-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921da-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="921da-113">-DatabaseName</span></span>
<span data-ttu-id="921da-114">Namnet på Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="921da-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="921da-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="921da-115">-PassThru</span></span>
<span data-ttu-id="921da-116">Definierar om synkroniseringsresursen ska returneras</span><span class="sxs-lookup"><span data-stu-id="921da-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="921da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921da-117">-ResourceGroupName</span></span>
<span data-ttu-id="921da-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="921da-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="921da-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="921da-119">-ServerName</span></span>
<span data-ttu-id="921da-120">Namnet på Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="921da-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="921da-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="921da-121">-SyncGroupName</span></span>
<span data-ttu-id="921da-122">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="921da-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921da-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921da-123">-WhatIf</span></span>
<span data-ttu-id="921da-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="921da-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921da-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="921da-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921da-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921da-126">-DefaultProfile</span></span>
<span data-ttu-id="921da-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="921da-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="921da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921da-128">CommonParameters</span></span>
<span data-ttu-id="921da-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921da-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="921da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921da-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="921da-131">INPUTS</span></span>

## <span data-ttu-id="921da-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="921da-132">OUTPUTS</span></span>

### <span data-ttu-id="921da-133">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="921da-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="921da-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="921da-134">NOTES</span></span>

## <span data-ttu-id="921da-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="921da-135">RELATED LINKS</span></span>

[<span data-ttu-id="921da-136">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="921da-136">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

