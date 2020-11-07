---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ac62ac0307422f0015fe578937a80a03e2a730d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746672"
---
# <span data-ttu-id="5447a-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5447a-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="5447a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5447a-102">SYNOPSIS</span></span>
<span data-ttu-id="5447a-103">Hämtar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="5447a-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="5447a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5447a-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5447a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5447a-105">DESCRIPTION</span></span>
<span data-ttu-id="5447a-106">Cmdleten **Get-AzSqlServerDisasterRecoveryConfiguration** har en konfiguration för SQL Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="5447a-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5447a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5447a-107">EXAMPLES</span></span>

## <span data-ttu-id="5447a-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5447a-108">PARAMETERS</span></span>

### <span data-ttu-id="5447a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5447a-109">-DefaultProfile</span></span>
<span data-ttu-id="5447a-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5447a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5447a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5447a-111">-ResourceGroupName</span></span>
<span data-ttu-id="5447a-112">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5447a-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5447a-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5447a-113">-ServerName</span></span>
<span data-ttu-id="5447a-114">Anger namnet på SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="5447a-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="5447a-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="5447a-115">-VirtualEndpointName</span></span>
<span data-ttu-id="5447a-116">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="5447a-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5447a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5447a-117">-Confirm</span></span>
<span data-ttu-id="5447a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5447a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5447a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5447a-119">-WhatIf</span></span>
<span data-ttu-id="5447a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5447a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5447a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5447a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5447a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5447a-122">CommonParameters</span></span>
<span data-ttu-id="5447a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5447a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5447a-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5447a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5447a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5447a-125">INPUTS</span></span>

### <span data-ttu-id="5447a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5447a-126">System.String</span></span>

## <span data-ttu-id="5447a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5447a-127">OUTPUTS</span></span>

### <span data-ttu-id="5447a-128">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="5447a-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="5447a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5447a-129">NOTES</span></span>

## <span data-ttu-id="5447a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5447a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5447a-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5447a-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5447a-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5447a-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5447a-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5447a-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5447a-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5447a-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

