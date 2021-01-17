---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404507"
---
# <span data-ttu-id="e25e7-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="e25e7-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="e25e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e25e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e25e7-103">Hämtar aktivitet för en konfiguration för återställning av databas server system.</span><span class="sxs-lookup"><span data-stu-id="e25e7-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="e25e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e25e7-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e25e7-105">DESCRIPTION</span></span>
<span data-ttu-id="e25e7-106">Cmdleten **Get-AzSqlServerDisasterRecoveryConfigurationActivity** hämtar aktivitet för en konfiguration för en SQL-databasserver för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="e25e7-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e25e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e25e7-107">EXAMPLES</span></span>

## <span data-ttu-id="e25e7-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e25e7-108">PARAMETERS</span></span>

### <span data-ttu-id="e25e7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25e7-109">-DefaultProfile</span></span>
<span data-ttu-id="e25e7-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e25e7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e25e7-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e25e7-111">-OperationId</span></span>
<span data-ttu-id="e25e7-112">Anger ID för operationen.</span><span class="sxs-lookup"><span data-stu-id="e25e7-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="e25e7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25e7-113">-ResourceGroupName</span></span>
<span data-ttu-id="e25e7-114">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e25e7-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e25e7-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e25e7-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="e25e7-116">Anger namnet på konfigurationen för återställning av server system.</span><span class="sxs-lookup"><span data-stu-id="e25e7-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="e25e7-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e25e7-117">-ServerName</span></span>
<span data-ttu-id="e25e7-118">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="e25e7-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e25e7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e25e7-119">-Confirm</span></span>
<span data-ttu-id="e25e7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e25e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25e7-121">-WhatIf</span></span>
<span data-ttu-id="e25e7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e25e7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25e7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e25e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25e7-124">CommonParameters</span></span>
<span data-ttu-id="e25e7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25e7-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e25e7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25e7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e25e7-127">INPUTS</span></span>

### <span data-ttu-id="e25e7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e25e7-128">System.String</span></span>

### <span data-ttu-id="e25e7-129">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e25e7-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e25e7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e25e7-130">OUTPUTS</span></span>

### <span data-ttu-id="e25e7-131">Microsoft. Azure. commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="e25e7-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="e25e7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e25e7-132">NOTES</span></span>

## <span data-ttu-id="e25e7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e25e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="e25e7-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e25e7-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
