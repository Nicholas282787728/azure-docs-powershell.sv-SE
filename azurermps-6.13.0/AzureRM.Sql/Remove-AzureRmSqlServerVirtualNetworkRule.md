---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c6011b1b8b23c5fd6a21075199f6a6d89c72e0cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757331"
---
# <span data-ttu-id="29116-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29116-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="29116-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29116-102">SYNOPSIS</span></span>
<span data-ttu-id="29116-103">Tar bort en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="29116-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29116-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29116-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29116-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29116-105">DESCRIPTION</span></span>
<span data-ttu-id="29116-106">Det här kommandot tar bort en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="29116-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="29116-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29116-107">EXAMPLES</span></span>

### <span data-ttu-id="29116-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="29116-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="29116-109">Tar bort en befintlig Azure SQL Server-regel</span><span class="sxs-lookup"><span data-stu-id="29116-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="29116-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29116-110">PARAMETERS</span></span>

### <span data-ttu-id="29116-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29116-111">-AsJob</span></span>
<span data-ttu-id="29116-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="29116-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29116-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29116-113">-DefaultProfile</span></span>
<span data-ttu-id="29116-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29116-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29116-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29116-115">-ResourceGroupName</span></span>
<span data-ttu-id="29116-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29116-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="29116-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29116-117">-ServerName</span></span>
<span data-ttu-id="29116-118">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="29116-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="29116-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="29116-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="29116-120">Namn på en Azure SQL Server-regel</span><span class="sxs-lookup"><span data-stu-id="29116-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="29116-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29116-121">-Confirm</span></span>
<span data-ttu-id="29116-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29116-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29116-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29116-123">-WhatIf</span></span>
<span data-ttu-id="29116-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29116-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29116-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29116-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29116-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29116-126">CommonParameters</span></span>
<span data-ttu-id="29116-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29116-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29116-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29116-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29116-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29116-129">INPUTS</span></span>

### <span data-ttu-id="29116-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29116-130">System.String</span></span>

## <span data-ttu-id="29116-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29116-131">OUTPUTS</span></span>

### <span data-ttu-id="29116-132">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="29116-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="29116-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29116-133">NOTES</span></span>

## <span data-ttu-id="29116-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29116-134">RELATED LINKS</span></span>