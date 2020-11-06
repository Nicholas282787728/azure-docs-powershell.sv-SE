---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 792d72c509df4c6b84f4ea86e597ddd8040a30d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583471"
---
# <span data-ttu-id="38383-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38383-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="38383-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="38383-102">SYNOPSIS</span></span>
<span data-ttu-id="38383-103">Hämtar en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="38383-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38383-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="38383-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38383-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="38383-105">DESCRIPTION</span></span>
<span data-ttu-id="38383-106">Cmdleten **Get-AzureRmSqlServerDisasterRecoveryConfiguration** har en konfiguration för SQL Server System återställning.</span><span class="sxs-lookup"><span data-stu-id="38383-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="38383-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="38383-107">EXAMPLES</span></span>

## <span data-ttu-id="38383-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="38383-108">PARAMETERS</span></span>

### <span data-ttu-id="38383-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38383-109">-DefaultProfile</span></span>
<span data-ttu-id="38383-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="38383-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38383-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38383-111">-ResourceGroupName</span></span>
<span data-ttu-id="38383-112">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="38383-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="38383-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38383-113">-ServerName</span></span>
<span data-ttu-id="38383-114">Anger namnet på SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="38383-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="38383-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="38383-115">-VirtualEndpointName</span></span>
<span data-ttu-id="38383-116">Anger namnet på den virtuella slut punkten.</span><span class="sxs-lookup"><span data-stu-id="38383-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="38383-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="38383-117">-Confirm</span></span>
<span data-ttu-id="38383-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="38383-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38383-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38383-119">-WhatIf</span></span>
<span data-ttu-id="38383-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="38383-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38383-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="38383-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38383-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38383-122">CommonParameters</span></span>
<span data-ttu-id="38383-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38383-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38383-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38383-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38383-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="38383-125">INPUTS</span></span>

### <span data-ttu-id="38383-126">System. String</span><span class="sxs-lookup"><span data-stu-id="38383-126">System.String</span></span>

## <span data-ttu-id="38383-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="38383-127">OUTPUTS</span></span>

### <span data-ttu-id="38383-128">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="38383-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="38383-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="38383-129">NOTES</span></span>

## <span data-ttu-id="38383-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="38383-130">RELATED LINKS</span></span>

[<span data-ttu-id="38383-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38383-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="38383-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38383-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="38383-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38383-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="38383-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="38383-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

