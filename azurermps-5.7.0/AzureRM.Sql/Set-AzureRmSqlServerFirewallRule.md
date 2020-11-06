---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574148"
---
# <span data-ttu-id="45e6a-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="45e6a-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="45e6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="45e6a-103">Ändrar en brand Väggs regel i Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="45e6a-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45e6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45e6a-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="45e6a-106">Cmdleten **set-AzureRmSqlServerFirewallRule** ändrar en brand Väggs regel i en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="45e6a-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="45e6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45e6a-107">EXAMPLES</span></span>

### <span data-ttu-id="45e6a-108">Exempel 1: ändra en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="45e6a-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="45e6a-109">Det här kommandot ändrar en brand Väggs regel som heter Rule01 på den server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="45e6a-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="45e6a-110">Kommandot ändrar Start-och slut-IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="45e6a-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="45e6a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45e6a-111">PARAMETERS</span></span>

### <span data-ttu-id="45e6a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e6a-112">-DefaultProfile</span></span>
<span data-ttu-id="45e6a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="45e6a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45e6a-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="45e6a-114">-EndIpAddress</span></span>
<span data-ttu-id="45e6a-115">Anger slutvärdet för IP-adressintervallet för den här regeln.</span><span class="sxs-lookup"><span data-stu-id="45e6a-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6a-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="45e6a-116">-FirewallRuleName</span></span>
<span data-ttu-id="45e6a-117">Anger namnet på brand Väggs regeln som ändras av den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45e6a-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e6a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e6a-118">-ResourceGroupName</span></span>
<span data-ttu-id="45e6a-119">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="45e6a-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="45e6a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45e6a-120">-ServerName</span></span>
<span data-ttu-id="45e6a-121">Anger namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="45e6a-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="45e6a-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="45e6a-122">-StartIpAddress</span></span>
<span data-ttu-id="45e6a-123">Anger startvärdet för IP-adressintervallet för brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="45e6a-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6a-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45e6a-124">-Confirm</span></span>
<span data-ttu-id="45e6a-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45e6a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e6a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e6a-126">-WhatIf</span></span>
<span data-ttu-id="45e6a-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45e6a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e6a-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45e6a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e6a-129">CommonParameters</span></span>
<span data-ttu-id="45e6a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e6a-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e6a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45e6a-132">INPUTS</span></span>

### <span data-ttu-id="45e6a-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="45e6a-133">None</span></span>
<span data-ttu-id="45e6a-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="45e6a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45e6a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45e6a-135">OUTPUTS</span></span>

### <span data-ttu-id="45e6a-136">Microsoft. Azure. commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="45e6a-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="45e6a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45e6a-137">NOTES</span></span>

## <span data-ttu-id="45e6a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45e6a-138">RELATED LINKS</span></span>

[<span data-ttu-id="45e6a-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="45e6a-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="45e6a-140">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="45e6a-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="45e6a-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="45e6a-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="45e6a-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="45e6a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


