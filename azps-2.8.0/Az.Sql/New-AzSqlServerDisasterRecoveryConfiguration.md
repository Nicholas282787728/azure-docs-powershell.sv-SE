---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 8f1400ba07444a5fc14d2a3194edd9fe960aaccc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920299"
---
# <span data-ttu-id="ed23e-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed23e-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ed23e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed23e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed23e-103">Skapar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="ed23e-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="ed23e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed23e-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed23e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed23e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed23e-106">Cmdleten **New-AzSqlServerDisasterRecoveryConfiguration** skapar en konfiguration för en system återställning för SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="ed23e-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ed23e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed23e-107">EXAMPLES</span></span>

## <span data-ttu-id="ed23e-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed23e-108">PARAMETERS</span></span>

### <span data-ttu-id="ed23e-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed23e-109">-AsJob</span></span>
<span data-ttu-id="ed23e-110">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ed23e-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed23e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed23e-111">-DefaultProfile</span></span>
<span data-ttu-id="ed23e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ed23e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed23e-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ed23e-113">-FailoverPolicy</span></span>
<span data-ttu-id="ed23e-114">Anger principer för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="ed23e-114">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed23e-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed23e-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ed23e-116">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ed23e-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed23e-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ed23e-117">-PartnerServerName</span></span>
<span data-ttu-id="ed23e-118">Anger namnet på partner servern.</span><span class="sxs-lookup"><span data-stu-id="ed23e-118">Specifies the name of the partner server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed23e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed23e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed23e-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ed23e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ed23e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed23e-121">-ServerName</span></span>
<span data-ttu-id="ed23e-122">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="ed23e-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ed23e-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ed23e-123">-VirtualEndpointName</span></span>
<span data-ttu-id="ed23e-124">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="ed23e-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed23e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed23e-125">-Confirm</span></span>
<span data-ttu-id="ed23e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed23e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed23e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed23e-127">-WhatIf</span></span>
<span data-ttu-id="ed23e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed23e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed23e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed23e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed23e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed23e-130">CommonParameters</span></span>
<span data-ttu-id="ed23e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed23e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed23e-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed23e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed23e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed23e-133">INPUTS</span></span>

### <span data-ttu-id="ed23e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed23e-134">System.String</span></span>

## <span data-ttu-id="ed23e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed23e-135">OUTPUTS</span></span>

### <span data-ttu-id="ed23e-136">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="ed23e-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="ed23e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed23e-137">NOTES</span></span>

## <span data-ttu-id="ed23e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed23e-138">RELATED LINKS</span></span>

[<span data-ttu-id="ed23e-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed23e-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ed23e-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed23e-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ed23e-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed23e-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ed23e-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="ed23e-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
