---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758272"
---
# <span data-ttu-id="2557d-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2557d-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="2557d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2557d-102">SYNOPSIS</span></span>
<span data-ttu-id="2557d-103">Tar bort en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="2557d-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2557d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2557d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2557d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2557d-105">DESCRIPTION</span></span>
<span data-ttu-id="2557d-106">Det här kommandot tar bort en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="2557d-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="2557d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2557d-107">EXAMPLES</span></span>

### <span data-ttu-id="2557d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2557d-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="2557d-109">Tar bort en befintlig Azure SQL Server-regel</span><span class="sxs-lookup"><span data-stu-id="2557d-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="2557d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2557d-110">PARAMETERS</span></span>

### <span data-ttu-id="2557d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2557d-111">-ResourceGroupName</span></span>
<span data-ttu-id="2557d-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2557d-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="2557d-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2557d-113">-ServerName</span></span>
<span data-ttu-id="2557d-114">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="2557d-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2557d-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="2557d-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="2557d-116">Namn på en Azure SQL Server-regel</span><span class="sxs-lookup"><span data-stu-id="2557d-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="2557d-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2557d-117">-Confirm</span></span>
<span data-ttu-id="2557d-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2557d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2557d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2557d-119">-WhatIf</span></span>
<span data-ttu-id="2557d-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2557d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2557d-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2557d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2557d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2557d-122">-DefaultProfile</span></span>
<span data-ttu-id="2557d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2557d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2557d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2557d-124">CommonParameters</span></span>
<span data-ttu-id="2557d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2557d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2557d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2557d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2557d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2557d-127">INPUTS</span></span>

### <span data-ttu-id="2557d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2557d-128">System.String</span></span>

## <span data-ttu-id="2557d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2557d-129">OUTPUTS</span></span>

### <span data-ttu-id="2557d-130">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="2557d-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="2557d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2557d-131">NOTES</span></span>

## <span data-ttu-id="2557d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2557d-132">RELATED LINKS</span></span>

