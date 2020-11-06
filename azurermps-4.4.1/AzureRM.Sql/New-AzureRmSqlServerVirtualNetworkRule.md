---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574480"
---
# <span data-ttu-id="9a63d-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9a63d-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="9a63d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a63d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a63d-103">Skapar en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="9a63d-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a63d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a63d-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a63d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a63d-105">DESCRIPTION</span></span>
<span data-ttu-id="9a63d-106">Skapar en regel för ett Azure SQL Server-nätverk.</span><span class="sxs-lookup"><span data-stu-id="9a63d-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="9a63d-107">Regler för virtuella nätverk används för att ansluta Azure SQL-servern till ett specifikt virtuellt nätverk för att begränsa åtkomsten på Azure SQL-servern så att den endast är tillgänglig i det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="9a63d-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="9a63d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a63d-108">EXAMPLES</span></span>

### <span data-ttu-id="9a63d-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a63d-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="9a63d-110">Skapar en regel för ett Azure SQL Server-nätverk</span><span class="sxs-lookup"><span data-stu-id="9a63d-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="9a63d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a63d-111">PARAMETERS</span></span>

### <span data-ttu-id="9a63d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a63d-112">-ResourceGroupName</span></span>
<span data-ttu-id="9a63d-113">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9a63d-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a63d-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9a63d-114">-ServerName</span></span>
<span data-ttu-id="9a63d-115">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="9a63d-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="9a63d-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="9a63d-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="9a63d-117">Namn på en Azure SQL Server-regel.</span><span class="sxs-lookup"><span data-stu-id="9a63d-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="9a63d-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="9a63d-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="9a63d-119">Det virtuella nätverkets nät-ID som anger Microsoft. Network-uppgifter</span><span class="sxs-lookup"><span data-stu-id="9a63d-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="9a63d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a63d-120">-Confirm</span></span>
<span data-ttu-id="9a63d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a63d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a63d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a63d-122">-WhatIf</span></span>
<span data-ttu-id="9a63d-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a63d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a63d-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a63d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a63d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a63d-125">-DefaultProfile</span></span>
<span data-ttu-id="9a63d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a63d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a63d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a63d-127">CommonParameters</span></span>
<span data-ttu-id="9a63d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a63d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a63d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a63d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a63d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a63d-130">INPUTS</span></span>

### <span data-ttu-id="9a63d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9a63d-131">System.String</span></span>

## <span data-ttu-id="9a63d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a63d-132">OUTPUTS</span></span>

### <span data-ttu-id="9a63d-133">Microsoft. Azure. commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="9a63d-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="9a63d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a63d-134">NOTES</span></span>

## <span data-ttu-id="9a63d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a63d-135">RELATED LINKS</span></span>

