---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 3c67c432f8f49927af4cbf357a4338f528c826b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582919"
---
# <span data-ttu-id="5dfdd-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="5dfdd-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="5dfdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5dfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfdd-103">Hämtar aktivitet för en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dfdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5dfdd-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dfdd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5dfdd-105">DESCRIPTION</span></span>
<span data-ttu-id="5dfdd-106">Cmdleten **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** hämtar aktivitet för en konfiguration för en SQL-databasserver för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="5dfdd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5dfdd-107">EXAMPLES</span></span>

## <span data-ttu-id="5dfdd-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5dfdd-108">PARAMETERS</span></span>

### <span data-ttu-id="5dfdd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfdd-109">-DefaultProfile</span></span>
<span data-ttu-id="5dfdd-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5dfdd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5dfdd-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5dfdd-111">-OperationId</span></span>
<span data-ttu-id="5dfdd-112">Anger ID för operationen.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-112">Specifies the operation ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfdd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfdd-113">-ResourceGroupName</span></span>
<span data-ttu-id="5dfdd-114">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5dfdd-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5dfdd-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="5dfdd-116">Anger namnet på konfigurationen för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfdd-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5dfdd-117">-ServerName</span></span>
<span data-ttu-id="5dfdd-118">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="5dfdd-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5dfdd-119">-Confirm</span></span>
<span data-ttu-id="5dfdd-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dfdd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dfdd-121">-WhatIf</span></span>
<span data-ttu-id="5dfdd-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfdd-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dfdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfdd-124">CommonParameters</span></span>
<span data-ttu-id="5dfdd-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfdd-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dfdd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfdd-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5dfdd-127">INPUTS</span></span>

### <span data-ttu-id="5dfdd-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="5dfdd-128">None</span></span>
<span data-ttu-id="5dfdd-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5dfdd-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5dfdd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5dfdd-130">OUTPUTS</span></span>

## <span data-ttu-id="5dfdd-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5dfdd-131">NOTES</span></span>

## <span data-ttu-id="5dfdd-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5dfdd-132">RELATED LINKS</span></span>

[<span data-ttu-id="5dfdd-133">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="5dfdd-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
