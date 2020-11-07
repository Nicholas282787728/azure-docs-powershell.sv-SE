---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757824"
---
# <span data-ttu-id="df748-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df748-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="df748-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df748-102">SYNOPSIS</span></span>
<span data-ttu-id="df748-103">Tar bort en konfiguration för en SQL Database Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="df748-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df748-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df748-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df748-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df748-105">DESCRIPTION</span></span>
<span data-ttu-id="df748-106">Cmdleten **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** tar bort en konfiguration för SQL Database Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="df748-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="df748-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df748-107">EXAMPLES</span></span>

## <span data-ttu-id="df748-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df748-108">PARAMETERS</span></span>

### <span data-ttu-id="df748-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df748-109">-DefaultProfile</span></span>
<span data-ttu-id="df748-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="df748-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df748-111">-Force</span><span class="sxs-lookup"><span data-stu-id="df748-111">-Force</span></span>
<span data-ttu-id="df748-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="df748-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df748-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df748-113">-ResourceGroupName</span></span>
<span data-ttu-id="df748-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="df748-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="df748-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df748-115">-ServerName</span></span>
<span data-ttu-id="df748-116">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="df748-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="df748-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="df748-117">-VirtualEndpointName</span></span>
<span data-ttu-id="df748-118">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="df748-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="df748-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df748-119">-Confirm</span></span>
<span data-ttu-id="df748-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df748-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df748-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df748-121">-WhatIf</span></span>
<span data-ttu-id="df748-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df748-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df748-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df748-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df748-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df748-124">CommonParameters</span></span>
<span data-ttu-id="df748-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df748-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df748-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df748-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df748-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df748-127">INPUTS</span></span>

### <span data-ttu-id="df748-128">System. String</span><span class="sxs-lookup"><span data-stu-id="df748-128">System.String</span></span>

## <span data-ttu-id="df748-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df748-129">OUTPUTS</span></span>

### <span data-ttu-id="df748-130">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="df748-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="df748-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df748-131">NOTES</span></span>

## <span data-ttu-id="df748-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df748-132">RELATED LINKS</span></span>

[<span data-ttu-id="df748-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df748-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="df748-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df748-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="df748-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="df748-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="df748-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="df748-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
