---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520535"
---
# <span data-ttu-id="a5516-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5516-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="a5516-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5516-102">SYNOPSIS</span></span>
<span data-ttu-id="a5516-103">Tar bort en konfiguration för en SQL Database Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="a5516-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a5516-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5516-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5516-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5516-105">DESCRIPTION</span></span>
<span data-ttu-id="a5516-106">Cmdleten **Remove-AzSqlServerDisasterRecoveryConfiguration** tar bort en konfiguration för SQL Database Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="a5516-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a5516-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5516-107">EXAMPLES</span></span>

## <span data-ttu-id="a5516-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5516-108">PARAMETERS</span></span>

### <span data-ttu-id="a5516-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5516-109">-DefaultProfile</span></span>
<span data-ttu-id="a5516-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a5516-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5516-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a5516-111">-Force</span></span>
<span data-ttu-id="a5516-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a5516-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5516-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5516-113">-ResourceGroupName</span></span>
<span data-ttu-id="a5516-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a5516-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a5516-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5516-115">-ServerName</span></span>
<span data-ttu-id="a5516-116">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="a5516-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="a5516-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="a5516-117">-VirtualEndpointName</span></span>
<span data-ttu-id="a5516-118">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="a5516-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="a5516-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5516-119">-Confirm</span></span>
<span data-ttu-id="a5516-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5516-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5516-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5516-121">-WhatIf</span></span>
<span data-ttu-id="a5516-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5516-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5516-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5516-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5516-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5516-124">CommonParameters</span></span>
<span data-ttu-id="a5516-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5516-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5516-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5516-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5516-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5516-127">INPUTS</span></span>

### <span data-ttu-id="a5516-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5516-128">System.String</span></span>

## <span data-ttu-id="a5516-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5516-129">OUTPUTS</span></span>

### <span data-ttu-id="a5516-130">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="a5516-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="a5516-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5516-131">NOTES</span></span>

## <span data-ttu-id="a5516-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5516-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5516-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5516-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a5516-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5516-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a5516-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5516-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="a5516-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a5516-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
