---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: de7df0147cc28d413444282987f8d5b27f9607a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920530"
---
# <span data-ttu-id="d0936-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d0936-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="d0936-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0936-102">SYNOPSIS</span></span>
<span data-ttu-id="d0936-103">Tar bort en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="d0936-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="d0936-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0936-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0936-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0936-105">DESCRIPTION</span></span>
<span data-ttu-id="d0936-106">Det här kommandot tar bort en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="d0936-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="d0936-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0936-107">EXAMPLES</span></span>

### <span data-ttu-id="d0936-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0936-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="d0936-109">Tar bort en befintlig Azure SQL Server-regel</span><span class="sxs-lookup"><span data-stu-id="d0936-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="d0936-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0936-110">PARAMETERS</span></span>

### <span data-ttu-id="d0936-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0936-111">-AsJob</span></span>
<span data-ttu-id="d0936-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d0936-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0936-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0936-113">-DefaultProfile</span></span>
<span data-ttu-id="d0936-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0936-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0936-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0936-115">-ResourceGroupName</span></span>
<span data-ttu-id="d0936-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d0936-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0936-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0936-117">-ServerName</span></span>
<span data-ttu-id="d0936-118">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="d0936-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d0936-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="d0936-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="d0936-120">Namn på en Azure SQL Server-regel</span><span class="sxs-lookup"><span data-stu-id="d0936-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="d0936-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0936-121">-Confirm</span></span>
<span data-ttu-id="d0936-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0936-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0936-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0936-123">-WhatIf</span></span>
<span data-ttu-id="d0936-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0936-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0936-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0936-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0936-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0936-126">CommonParameters</span></span>
<span data-ttu-id="d0936-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0936-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0936-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0936-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0936-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0936-129">INPUTS</span></span>

### <span data-ttu-id="d0936-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d0936-130">System.String</span></span>

## <span data-ttu-id="d0936-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0936-131">OUTPUTS</span></span>

### <span data-ttu-id="d0936-132">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="d0936-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="d0936-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0936-133">NOTES</span></span>

## <span data-ttu-id="d0936-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0936-134">RELATED LINKS</span></span>
