---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101870"
---
# <span data-ttu-id="d07c5-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07c5-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d07c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d07c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d07c5-103">Skapar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="d07c5-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="d07c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d07c5-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d07c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d07c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d07c5-106">Cmdleten **New-AzSqlServerDisasterRecoveryConfiguration** skapar en konfiguration för en system återställning för SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="d07c5-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d07c5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d07c5-107">EXAMPLES</span></span>

## <span data-ttu-id="d07c5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d07c5-108">PARAMETERS</span></span>

### <span data-ttu-id="d07c5-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d07c5-109">-AsJob</span></span>
<span data-ttu-id="d07c5-110">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d07c5-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d07c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07c5-111">-DefaultProfile</span></span>
<span data-ttu-id="d07c5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d07c5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d07c5-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d07c5-113">-FailoverPolicy</span></span>
<span data-ttu-id="d07c5-114">Anger principer för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="d07c5-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="d07c5-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07c5-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d07c5-116">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d07c5-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="d07c5-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d07c5-117">-PartnerServerName</span></span>
<span data-ttu-id="d07c5-118">Anger namnet på partner servern.</span><span class="sxs-lookup"><span data-stu-id="d07c5-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="d07c5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07c5-119">-ResourceGroupName</span></span>
<span data-ttu-id="d07c5-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d07c5-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d07c5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d07c5-121">-ServerName</span></span>
<span data-ttu-id="d07c5-122">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d07c5-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d07c5-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d07c5-123">-VirtualEndpointName</span></span>
<span data-ttu-id="d07c5-124">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d07c5-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="d07c5-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d07c5-125">-Confirm</span></span>
<span data-ttu-id="d07c5-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d07c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07c5-127">-WhatIf</span></span>
<span data-ttu-id="d07c5-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d07c5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07c5-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d07c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07c5-130">CommonParameters</span></span>
<span data-ttu-id="d07c5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07c5-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d07c5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07c5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d07c5-133">INPUTS</span></span>

### <span data-ttu-id="d07c5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d07c5-134">System.String</span></span>

## <span data-ttu-id="d07c5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d07c5-135">OUTPUTS</span></span>

### <span data-ttu-id="d07c5-136">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="d07c5-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="d07c5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d07c5-137">NOTES</span></span>

## <span data-ttu-id="d07c5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d07c5-138">RELATED LINKS</span></span>

[<span data-ttu-id="d07c5-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07c5-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d07c5-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07c5-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d07c5-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07c5-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d07c5-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d07c5-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
