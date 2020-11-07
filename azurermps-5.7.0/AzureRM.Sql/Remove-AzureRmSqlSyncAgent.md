---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: b357c44afd52dd398631b9b7edfcedb0360cf377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755574"
---
# <span data-ttu-id="6ca81-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="6ca81-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="6ca81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ca81-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca81-103">Tar bort en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="6ca81-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ca81-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ca81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ca81-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca81-106">Cmdleten **Remove-AzureRmSqlSyncAgent** tar bort en Azure SQL Sync-agent.</span><span class="sxs-lookup"><span data-stu-id="6ca81-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="6ca81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ca81-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca81-108">Exempel 1: ta bort en synkroniseringsresurs</span><span class="sxs-lookup"><span data-stu-id="6ca81-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="6ca81-109">Det här kommandot tar bort Azure SQL Sync-agenten med namnet syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="6ca81-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="6ca81-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ca81-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca81-111">-DefaultProfile</span></span>
<span data-ttu-id="6ca81-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6ca81-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ca81-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca81-113">-Force</span></span>
<span data-ttu-id="6ca81-114">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="6ca81-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6ca81-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ca81-115">-Name</span></span>
<span data-ttu-id="6ca81-116">Namnet på synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="6ca81-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca81-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ca81-117">-PassThru</span></span>
<span data-ttu-id="6ca81-118">Definierar om returnera den borttagna synkroniseringsresursen</span><span class="sxs-lookup"><span data-stu-id="6ca81-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="6ca81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca81-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ca81-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6ca81-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ca81-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ca81-121">-ServerName</span></span>
<span data-ttu-id="6ca81-122">Namnet på den Azure SQL-Server som synkroniseringsresursen finns i.</span><span class="sxs-lookup"><span data-stu-id="6ca81-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="6ca81-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ca81-123">-Confirm</span></span>
<span data-ttu-id="6ca81-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ca81-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca81-125">-WhatIf</span></span>
<span data-ttu-id="6ca81-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ca81-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca81-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ca81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca81-128">CommonParameters</span></span>
<span data-ttu-id="6ca81-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca81-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca81-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca81-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ca81-131">INPUTS</span></span>

### <span data-ttu-id="6ca81-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="6ca81-132">None</span></span>
<span data-ttu-id="6ca81-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6ca81-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ca81-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ca81-134">OUTPUTS</span></span>

### <span data-ttu-id="6ca81-135">Microsoft. Azure. commands. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="6ca81-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="6ca81-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ca81-136">NOTES</span></span>

## <span data-ttu-id="6ca81-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ca81-137">RELATED LINKS</span></span>

[<span data-ttu-id="6ca81-138">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="6ca81-138">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="6ca81-139">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="6ca81-139">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

