---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: bbb6841f615444175de93e59d4536a07461490de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756836"
---
# <span data-ttu-id="7ede2-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ede2-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="7ede2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ede2-102">SYNOPSIS</span></span>
<span data-ttu-id="7ede2-103">Hämtar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="7ede2-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ede2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ede2-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ede2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ede2-105">DESCRIPTION</span></span>
<span data-ttu-id="7ede2-106">Cmdleten **Get-AzureRmSqlServerDisasterRecoveryConfiguration** har en konfiguration för SQL Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="7ede2-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="7ede2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ede2-107">EXAMPLES</span></span>

## <span data-ttu-id="7ede2-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ede2-108">PARAMETERS</span></span>

### <span data-ttu-id="7ede2-109">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ede2-109">-ResourceGroupName</span></span>
<span data-ttu-id="7ede2-110">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7ede2-110">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7ede2-111">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ede2-111">-ServerName</span></span>
<span data-ttu-id="7ede2-112">Anger namnet på SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="7ede2-112">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="7ede2-113">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="7ede2-113">-VirtualEndpointName</span></span>
<span data-ttu-id="7ede2-114">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="7ede2-114">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="7ede2-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ede2-115">-Confirm</span></span>
<span data-ttu-id="7ede2-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ede2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ede2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ede2-117">-WhatIf</span></span>
<span data-ttu-id="7ede2-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ede2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ede2-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ede2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ede2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ede2-120">-DefaultProfile</span></span>
<span data-ttu-id="7ede2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ede2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ede2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ede2-122">CommonParameters</span></span>
<span data-ttu-id="7ede2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ede2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ede2-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ede2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ede2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ede2-125">INPUTS</span></span>

## <span data-ttu-id="7ede2-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ede2-126">OUTPUTS</span></span>

## <span data-ttu-id="7ede2-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ede2-127">NOTES</span></span>

## <span data-ttu-id="7ede2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ede2-128">RELATED LINKS</span></span>

[<span data-ttu-id="7ede2-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ede2-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7ede2-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ede2-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7ede2-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ede2-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7ede2-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="7ede2-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

