---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 7b5c793bda8b05b78ce97e1f164126de62102fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576392"
---
# <span data-ttu-id="08d71-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d71-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="08d71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08d71-102">SYNOPSIS</span></span>
<span data-ttu-id="08d71-103">Tar bort en konfiguration för en SQL Database Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="08d71-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08d71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08d71-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08d71-105">DESCRIPTION</span></span>
<span data-ttu-id="08d71-106">Cmdleten **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** tar bort en konfiguration för SQL Database Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="08d71-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="08d71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08d71-107">EXAMPLES</span></span>

## <span data-ttu-id="08d71-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08d71-108">PARAMETERS</span></span>

### <span data-ttu-id="08d71-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d71-109">-DefaultProfile</span></span>
<span data-ttu-id="08d71-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="08d71-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08d71-111">-Force</span><span class="sxs-lookup"><span data-stu-id="08d71-111">-Force</span></span>
<span data-ttu-id="08d71-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="08d71-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08d71-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d71-113">-ResourceGroupName</span></span>
<span data-ttu-id="08d71-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="08d71-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="08d71-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08d71-115">-ServerName</span></span>
<span data-ttu-id="08d71-116">Anger namnet på en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="08d71-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="08d71-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="08d71-117">-VirtualEndpointName</span></span>
<span data-ttu-id="08d71-118">Anger namnet på en virtuell slut punkt.</span><span class="sxs-lookup"><span data-stu-id="08d71-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d71-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08d71-119">-Confirm</span></span>
<span data-ttu-id="08d71-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08d71-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08d71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d71-121">-WhatIf</span></span>
<span data-ttu-id="08d71-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08d71-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08d71-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08d71-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08d71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d71-124">CommonParameters</span></span>
<span data-ttu-id="08d71-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08d71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d71-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08d71-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d71-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08d71-127">INPUTS</span></span>

### <span data-ttu-id="08d71-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="08d71-128">None</span></span>
<span data-ttu-id="08d71-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="08d71-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08d71-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08d71-130">OUTPUTS</span></span>

## <span data-ttu-id="08d71-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08d71-131">NOTES</span></span>

## <span data-ttu-id="08d71-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08d71-132">RELATED LINKS</span></span>

[<span data-ttu-id="08d71-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d71-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="08d71-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d71-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="08d71-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d71-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="08d71-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="08d71-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
