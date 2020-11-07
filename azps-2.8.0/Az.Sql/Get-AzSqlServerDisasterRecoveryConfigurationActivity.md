---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 8fcd9b165722d1328bfbc87dd906f8b86e456579
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920612"
---
# <span data-ttu-id="a27f6-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="a27f6-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="a27f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a27f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a27f6-103">Hämtar aktivitet för en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="a27f6-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="a27f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a27f6-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a27f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a27f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a27f6-106">Cmdleten **Get-AzSqlServerDisasterRecoveryConfigurationActivity** hämtar aktivitet för en konfiguration för en SQL-databasserver för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="a27f6-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="a27f6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a27f6-107">EXAMPLES</span></span>

## <span data-ttu-id="a27f6-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a27f6-108">PARAMETERS</span></span>

### <span data-ttu-id="a27f6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27f6-109">-DefaultProfile</span></span>
<span data-ttu-id="a27f6-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a27f6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a27f6-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a27f6-111">-OperationId</span></span>
<span data-ttu-id="a27f6-112">Anger ID för operationen.</span><span class="sxs-lookup"><span data-stu-id="a27f6-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="a27f6-114">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a27f6-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a27f6-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a27f6-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="a27f6-116">Anger namnet på konfigurationen för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="a27f6-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27f6-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a27f6-117">-ServerName</span></span>
<span data-ttu-id="a27f6-118">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a27f6-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a27f6-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a27f6-119">-Confirm</span></span>
<span data-ttu-id="a27f6-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a27f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27f6-121">-WhatIf</span></span>
<span data-ttu-id="a27f6-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a27f6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a27f6-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a27f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27f6-124">CommonParameters</span></span>
<span data-ttu-id="a27f6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27f6-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a27f6-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27f6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a27f6-127">INPUTS</span></span>

### <span data-ttu-id="a27f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a27f6-128">System.String</span></span>

### <span data-ttu-id="a27f6-129">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a27f6-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a27f6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a27f6-130">OUTPUTS</span></span>

### <span data-ttu-id="a27f6-131">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="a27f6-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="a27f6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a27f6-132">NOTES</span></span>

## <span data-ttu-id="a27f6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a27f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="a27f6-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="a27f6-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
