---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 1fb3f802971f6724545c7006ed67ff01da4d7842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579312"
---
# <span data-ttu-id="72a19-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="72a19-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="72a19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72a19-102">SYNOPSIS</span></span>
<span data-ttu-id="72a19-103">Skapar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="72a19-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72a19-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72a19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72a19-105">DESCRIPTION</span></span>
<span data-ttu-id="72a19-106">Cmdleten **New-AzureRmSqlServerDisasterRecoveryConfiguration** skapar en konfiguration för en system återställning för SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="72a19-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="72a19-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72a19-107">EXAMPLES</span></span>

## <span data-ttu-id="72a19-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72a19-108">PARAMETERS</span></span>

### <span data-ttu-id="72a19-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72a19-109">-AsJob</span></span>
<span data-ttu-id="72a19-110">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="72a19-110">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="72a19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a19-111">-DefaultProfile</span></span>
<span data-ttu-id="72a19-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72a19-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72a19-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="72a19-113">-FailoverPolicy</span></span>
<span data-ttu-id="72a19-114">Anger principer för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="72a19-114">Specifies the failover policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a19-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a19-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="72a19-116">Anger namnet på partner resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72a19-116">Specifies the name of the partner resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a19-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="72a19-117">-PartnerServerName</span></span>
<span data-ttu-id="72a19-118">Anger namnet på partner servern.</span><span class="sxs-lookup"><span data-stu-id="72a19-118">Specifies the name of the partner server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a19-119">-ResourceGroupName</span></span>
<span data-ttu-id="72a19-120">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72a19-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="72a19-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72a19-121">-ServerName</span></span>
<span data-ttu-id="72a19-122">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="72a19-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="72a19-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="72a19-123">-VirtualEndpointName</span></span>
<span data-ttu-id="72a19-124">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="72a19-124">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a19-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72a19-125">-Confirm</span></span>
<span data-ttu-id="72a19-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72a19-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a19-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a19-127">-WhatIf</span></span>
<span data-ttu-id="72a19-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72a19-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72a19-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72a19-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a19-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a19-130">CommonParameters</span></span>
<span data-ttu-id="72a19-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a19-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a19-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a19-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a19-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72a19-133">INPUTS</span></span>

### <span data-ttu-id="72a19-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="72a19-134">None</span></span>
<span data-ttu-id="72a19-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="72a19-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72a19-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72a19-136">OUTPUTS</span></span>

## <span data-ttu-id="72a19-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72a19-137">NOTES</span></span>

## <span data-ttu-id="72a19-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72a19-138">RELATED LINKS</span></span>

[<span data-ttu-id="72a19-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="72a19-139">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="72a19-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="72a19-140">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="72a19-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="72a19-141">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="72a19-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="72a19-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
