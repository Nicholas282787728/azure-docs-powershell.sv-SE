---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574483"
---
# <span data-ttu-id="e18f2-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e18f2-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e18f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e18f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e18f2-103">Skapar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="e18f2-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e18f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e18f2-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e18f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e18f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e18f2-106">Cmdleten **New-AzureRmSqlServerDisasterRecoveryConfiguration** skapar en konfiguration för en system återställning för SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="e18f2-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e18f2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e18f2-107">EXAMPLES</span></span>

## <span data-ttu-id="e18f2-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e18f2-108">PARAMETERS</span></span>

### <span data-ttu-id="e18f2-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="e18f2-109">-FailoverPolicy</span></span>
<span data-ttu-id="e18f2-110">Anger principer för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="e18f2-110">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="e18f2-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18f2-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="e18f2-112">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e18f2-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="e18f2-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="e18f2-113">-PartnerServerName</span></span>
<span data-ttu-id="e18f2-114">Anger namnet på partner servern.</span><span class="sxs-lookup"><span data-stu-id="e18f2-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="e18f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="e18f2-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e18f2-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e18f2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e18f2-117">-ServerName</span></span>
<span data-ttu-id="e18f2-118">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="e18f2-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e18f2-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e18f2-119">-VirtualEndpointName</span></span>
<span data-ttu-id="e18f2-120">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e18f2-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="e18f2-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e18f2-121">-Confirm</span></span>
<span data-ttu-id="e18f2-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e18f2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e18f2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18f2-123">-WhatIf</span></span>
<span data-ttu-id="e18f2-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e18f2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e18f2-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e18f2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e18f2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18f2-126">-DefaultProfile</span></span>
<span data-ttu-id="e18f2-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e18f2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e18f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18f2-128">CommonParameters</span></span>
<span data-ttu-id="e18f2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e18f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18f2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18f2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e18f2-131">INPUTS</span></span>

## <span data-ttu-id="e18f2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e18f2-132">OUTPUTS</span></span>

## <span data-ttu-id="e18f2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e18f2-133">NOTES</span></span>

## <span data-ttu-id="e18f2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e18f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="e18f2-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e18f2-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e18f2-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e18f2-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e18f2-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e18f2-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e18f2-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e18f2-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
